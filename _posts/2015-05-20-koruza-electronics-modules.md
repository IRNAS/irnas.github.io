---
layout: post
title: "KORUZA optical system - electronics modular design"
description: "Control electronics split into standalone modules."
category: KORUZA
tags: [KORUZA, Electronics]
---
{% include JB/setup %}

KORUZA wireless optical systems electronics design currently implements the the bare minimum functions required on a prototype assembly with a number of bugs and missing features. We have chosen to implement all the required functions in a number of standalone modules, to maximize their reuse in other projects as well as to enable versatility in experimentation with the system and simplest evolution of modules on their own. Once an optimal solution is determined we will create a standalone integrated electronics control board, optimizing for low cost a larger volumes.

The following is a brief design overview which will later be followed with detailed information for ever module.

Electronics of the system is divided into five standalone open hardware projects, each implementing a standalone set of functions, interconnecting via standard serial interfaces UART, I2C or SPI via a common connector. The core is a control board interfacing all modules and running the project specific code which can be reprogrammed remotely, all modules are project non-specific and can be reused otherwise, all will be released open source once sufficiently stable.

The modules are introduced in the following image and descriptions below. Should you like to contribute to the development of any of these, please get in touch:

[![koruza electronics modules]({{ site.url }}/images/koruza/ElectronicsDiagram.png){: .img-full}]({{ site.url }}/images/koruza/ElectronicsDiagram.png){: .img-open}

 1. **KORUZA control board** - implements connectivity to all other modules and runs KORUZA unit control and auto-alignment algorithms.
 * floating point capable processor, ARM based
 * USB interface for communication and reprogramming
 * support for 1-wire and other sensors
 * connections to all other modules
 * STATUS: working prototype with functions of some modules

 1. **Unipolar stepper controller with feedback**
 * driving 3 unipolar stepper motors 28BYJ48 or 24BYJ48 with suitable JST connectors
 * support for 6 end-switches, two which can be directly attached to the PCB without cables
 * support for per-axis encoder or movement indicator
 * integrated processor for movement control with feedback and end-switch control
 * UART, I2C and SPI interfaces for receiving G-code style commands
 * STATUS: prototype being designed
 
 1. **SFP module extension electronics**
 * interfaces a standard SFP module and socket as an extension board
 * allows external I2C communication to the SFP module
 * STATUS: stable prototype 

 1. **Laser pointer data link**
 * low-speed data communication with modulated Green DPSS laser and multiple tv IR detectors
 * based on MicroModem project
 * UART link or custom packet protocol
 * forward error correction
 * STATUS: pending development
  
 1. **Power supply module**
 * 12-24V passive PoE input
 * dual regulated output 5V and 9-12V adjustable
 * power consumption monitoring
 * STATUS: operational prototype
  
 1. **KORUZA calibration tool**
 * 9 pixel IR detector for 1100nm-1650nm range
 * measurement of KORUZA optical beam diameter and divergence
 * calibration of the green laser pointer to be parallel with IR beam
 * RGB led optical power feedback
 * WiFi connectivity with ESP8266
 * STATUS: operational prototype, 2nd prototype in development
 
 Additionally to the open hardware modules, the following off-the shelf moduels are present in the system:
 
 1. **WiFi router**
 * running OpenWRT firmware
 * powered from 5V source
 * small form-factor
 * ethernet and USB ports
 * CHOICE: GL-iNet 6416A
 
 1. **Media converter**
 * 1Gbps ethernet port
 * SFP module port
 * powered from 5V or 9V source
 * ethernet and USB ports
 * CHOICE: TP-Link MC220L

