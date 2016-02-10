---
layout: post
title: "ToslinkCNC - Optical communication for CNC control - design overview"
description: "Introducing ToslinkCNC optical communication to low-cost CNC machines"
category: GoodEnoughCNC
tags: [CNC, GoodEnoughCNC, Toslink, Open Source Hardware]
---
{% include JB/setup %}

CNC machines merge large metal and thus conductive mechanics with high power tools, ranging from several kW spindles to plasma cutters and their control systems in particular suffer from noise problems and ground loops, resulting in sporadic failures or even damage to the control electronics. An significant number of papers, articles and forums suggest solutions, however in lower-cost and DIY machines they are often poorly implemented. For use with our [Good-enough CNC plasma cutter]({{ site.url }}/goodenoughcnc/2015/06/04/good-eough-cnc-plasma), we have set to rethink the overall electrical system design and introduce the following key changes:

 * Motion unit is a standalone/universal device, consisting of a stepper motor, stepper driver, encoder or any other feedback mechanism and end-switches and other protection mechanisms. Generally mounted next to the stepper motor in an enclosed box.
 * End-switches and other machine protection mechanisms are control-system independent, as control systems under development or without significant quality control can misbehave.
 * Connection to every motion unit consists of a power cable (12-48V DC) and fibre-optic connection with control signals. Reverse communication may be implemented if need be.
 
The communication system is designed to be independent of the actual motion controller and compatible with either proprietary [PlanetCNC](http://planet-cnc.com) or open-source [Smoothie-board](http://smoothieware.org/smoothieboard) and scalable to any number of axis.

For fibre optical communication [Toslink](http://en.wikipedia.org/wiki/TOSLINK) standard is chosen as pre-made cables are generally available as well as transceiver modules sold at low-cost. Normally supported raw bitrate of 16Mbps is sufficiently fast and range of 15m appropriate for use in CNC machines. We have opted to implement prototypes with DLR1111 receiver and DLT1111 transmitter modules. Bending radius of the cable is in the 20mm range and cost of cables is often lower then equivalent distance of 4 wire cable used for motors.

A number of open source projects implement such functionality, however none is exactly optimized for out use-case. [Toslink UART](http://opencores.org/project,uart_fiber), [Toslink serializer](http://opencores.org/project,parallel_io_through_fiber) and [TosNet](http://robolabwiki.sdu.dk/mediawiki/index.php/TosNet) are most notable implementations to serve as a guideline. The main limitations of Toslink modules used are 16Mbps bitrate limit and 0.1Mbps minimal bitrate limit with the need for the communication to be DC balanced and thus UART protocol can not be directly used. Further limitations imposed by control signals to stepper motors are 150kHz or 250kHz maximal step rate with the control signal consisting of step, direction, enable logical lines and in reverse direction one or two end-switch logical lines. Additionally we may wish to have a few logical lines either direction for probes etc.
 
Several modulation options are possible with different complexity of implementation and efficiency, mentioning a few:

 * 8b/10b encoding - max 5 same bytes in row, thus min rate 3.2Mbps and effective bitrate 12.8Mbps - easiest if supported in hardware
 * hack NRZ to RTZ UART - send a byte and its inverse thus min rate 1.78Mbps when data sent at 16Mbps - easy to support at up to 250000baud 8N1 (2.5Mbps but data throughput in encodign case 1.25Mbps) on microcontrollers
 * Manchester encoded UART 8N1 - min rate 8Mbps and effective bitrate 8Mbps - not straightforward to implement in low-cost devices at that speed
 * FSK modulation - different duration for 1 and 0 pulses - assume 16MHz for 1 and 8MHz for 0, average throughput for equal number of values 12Mbps
 
Implementation in hardware:

 * Microcontrollers - a low cost and easily programmable option however can not simply implement such throughput in low-cost versions, MSP430 from 1EUR onwards
 * FPGAa - simple to implement the functionality, however devices are not that low-cost, Xilinx Spartan-3 20EUR
 * CPLDs - similar to FPGAs but much simpler and can be low-cost, such as Xilin XC9572XL (50MHz) - 3.8EUR
 
Throughput requirements are governed by a number of Motion units per fibre and link overhead (framing and CRC, lets assume 10% for now). Every motion unit requires 3+1(optional output) single logical signals updated with 150kHz-250kHz rate and thus bitrate per Motion unit without overhead is 750kbps (3@150kHz) or 1000kbps (4@250kHz), depending on the setup.

[![toslinkcnc]({{ site.url }}/downloads/ToslinkCNC/ToslinkCNCElectronicsDiagram.png){: .img-full}]({{ site.url }}/downloads/ToslinkCNC/ToslinkCNCElectronicsDiagram.png){: .img-open}

System design is broken down into previously described Motion units designed by user and not directly a part of this project. We imagine two key scenarios to validate ToslinkCNC approach.

**Motion unit advanced**: Machine consist of a fully featured control system and has daisy-chaining between axes. The motion unit implements ToslinkCNC transceiver communication and optionally a separate motion control unit interfacing end-switches or encoders for closed loop control. Axis signal can either be removed from the communication stream and replaced with logical outputs or continues further, a user can select which of the channels is available and if it gets replaced with a jumper.

**Motion unit simple**: Machine in the simplest form using ToslinkCNC Slave which select a single channel out of the communication and a logic output and exposes them to the motor driver. User selects which channel and logical output is used with a jumper.

**Plasma control unit**: Connects with a Plasma cutter machine and measures the voltage as well as controls the trigger. Internally uses a low-speed communication ToslinkCNC UART link and custom Arduino code can be run on the device.

Initially we aim to implement the following ToslinkCNC devices:

 * **ToslinkCNC Master**: Receives inputs for 4 motion axis and 4 logical signals from CNC controller and outputs them to single optical channel, multiple optical outputs may be present. Return optical signal from a daisy-chained link of multiple Motion units is returned and logical signals can be coupled back into the controller. The unit is powered from 5-25V DC and implemented on a CPLD, supporting the maximal 250kHz refresh rate.
 * **ToslinkCNC Slave**: Receives the optical communication and outputs a single motion axis signals long with selected logical signal. Axis is user selected, implemented on a CPLD.
 * **ToslinkCNC Transceiver**: Receives the optical communication and outputs a single motion axis signals long with selected logical signals, motion signals can be replaced with logical signals. Optical output send the data after replacing. Implemented on a CPLD.
 * **ToslinkCNC UART link**: Bi-directionally communicates via UART. Units run Arduino and can thus handle custom code. Implemented with AtMega328 or similar low cost MCU. Can include a shield for specific application, such as plasma torch height control.

We are posting this as the initial design for discussion and it will be evolved in the following weeks through a series of prototypes. Please do get in touch if you would like to contribute to the development or have helpful information. The design will be fully open source.

 
 



