---
layout: post
title: "Optical communication for CNC control - design overview"
description: "Introducing optical communication to low-cost CNC machines"
category: 
tags: []
---
{% include JB/setup %}

CNC machines merge large metal and thus conductive mechanics with high power tools, ranging from several kW spindles to plasma cutters and their control systems in particular suffer from noise problems and ground loops, resulting in sporadic failures or even damage to the control electronics. An unlimited number of papers, articles and forums suggest solutions, however in lower-cost and DIY machines they are often poorly implemented. For use with our Good-enough CNC plasma cutter, we have set to rethink the overall electrical system design and introduce the following key changes:

 * Motion unit is a standalone/universal device, consisting of a stepper motor, stepper driver, encoder or any other feedback mechanism and end-switches and other protection mechanisms.
 * End-switches and other machine protection mechanisms are control-system independent, as control systems under development or without significant quality control can misbehave.
 * Connection to every motion unit consists of a power cable (12-48V DC) and fibre-optic connection with control signals. Reverse communication may be implemented if need be.
 
The communication system is designed to be independent of the actual motion controller and compatible with either [proprietary PlanetCNC](http://planet-cnc.com) or [open-source Smoothie-board](http://smoothieware.org/smoothieboard) and scalable to any number of axis.

For fibre optical communication [Toslink](http://en.wikipedia.org/wiki/TOSLINK) standard is chosen as pre-made cables are generally available as well as transceiver modules sold at low-cost. Normally supported raw bitrate of 16Mbps is sufficiently fast and range of 15m appropriate for use in CNC machines. We have opted to implement prototypes with DLR1111 receiver and DLT1111 transmitter modules.

A number of open source projects implement such functionality, however none exactly optimized for out use-case. [Toslink UART](http://opencores.org/project,uart_fiber), [Toslink serializer](http://opencores.org/project,parallel_io_through_fiber) and [TosNet](http://robolabwiki.sdu.dk/mediawiki/index.php/TosNet) are most notable implementations to serve as a guideline. The main limitations of Toslink modules used are 16Mbps bitrate limit and 0.1Mbps minimal bitrate limit with the need for the communication to be DC balanced and thus UART protocol can not be directly used. Furthermore limitations imposed by control signals to stepper motors are 150kHz or 250kHz maximal step rate with the control signal consisting of step, direction, enable logical lines and in reverse direction one or two end-switch logical lines. Additionally we may wish to have a few logical lines either direction for probes etc.
 
Several modulation options are possible with different complexity of implementation and efficiency, mentioning a few:

 * 8b/10b encoding - max 5same bytes in row, thus min rate 3.2Mbps and effective bitrate 12.8Mbps - easiest if supported in hardware
 * hack NRZ to RTZ UART - send a byte and its inverse thus min rate 1.78Mbps when data sent at 16Mbps - easy to support at up to 250000baud 8N1 (2.5Mbps) on microcontrollers
 * Manchester encoded UART 8N1 - min rate 8Mbps and effective bitrate 8Mbps - not straightforward to implement in low-cost devices at that speed
 
Implementation in hardware:

 * Microcontrollers - a low cost and easily programmable option however can not simply implement such throughput in low-cost versions
 * FPGAa - simple to implement the functionality, however devices are not that low-cost, Xilinx Spartan-3 20EUR
 * CPLDs - similar to FPGAs but much simpler and can be low-cost, such as Xilin XC9572XL - 3.8EUR





Many devices connect to the computer trough serial interface. Being able to easily establish connection trough serial port communication and then also analyse, process and visually represent received or send data, can therefore be useful in many cases. [GNU Octave](http://www.gnu.org/software/octave/) is an open software that recently, with release of instrument-control package, allows for all of that, the only downside being very limited documentation and lack of provided examples to help with debugging.

We present straightforward instructions on how to establish serial communication, manage connection settings, send and receive data.  A sample code, illustrating described procedures is also enclosed. In particular, we established connection with Stellaris LaunchPad running [Energia](http://energia.nu) code which is [Arduino](http://arduino.cc) compatible.

First, an instrument-control package must be installed. It can be found on [Sourceforge] (http://octave.sourceforge.net/instrument-control/).  Open the folder containing downloaded files in Octave and in prompt execute command:

```pkg install instrument-control-0.2.1.tar.gz```

If installed correctly, you will not receive any message, otherwise error message will appear. By default, package is not available from prompt and must be loaded each time with the command:

```pkg load instrument-control``

You can easily check if package is loaded correctly using the flowing:

```if (exist("serial") == 3)
    disp("Serial: Supported")
else
    disp("Serial: Unsupported")
endif```

Once the package is loaded, all functions for serial communication can be accessed. All of them, together with a brief description, can be found on the [website](http://octave.sourceforge.net/instrument-control/overview.html).

In order to establish the connection, the serial port object needs to be created first:

```s = serial_setup('COM5')```

where 'COM5' is replaced with an appropriate interface path (which can be found in the Device Manager on Windows). Default connection settings can be changed. To view the initial state use

```get(s)```

which will return the current settings structure. Any feature can be changed with the set function

```set (s, 'property',value)```

Pay special attention to ’timeout’, as the default value -1, means blocking the call. More about other options can be found [online](http://octave.sourceforge.net/instrument-control/function/@octave_serial/set.html)

To send or receive data, functions 'srl_read' and 'srl_write' are used:

```[data, count] = srl_read(s,n)```

reads n bytes from port and write them as uint8 array in the data variable. Count represents the number of bytes successfully read.  Currently this is the only form in which Octave reads from and writes to the serial port, therefore uint8 array must be converted to desired form. 'typecast' [This](https://www.gnu.org/software/octave/doc/interpreter/Built_002din-Data-Types.html)  function can be used. For example, reading a single float:

```data = srl_read(s,4);
data_float=typecast(uint8(data), 'single');```

To just convert an uint8 array to a string use char(data). Similar, when writing back to the serial port, any structure needs to be converted to either string or uint8 array. For example, if we want to write variable data_float back:

```data = typecast( single(data_float), 'uint8');
srl_write(s, data);```

or to write a string:

```srl_write(s, 'Hello world!')```

To flush the pending input use:

```srl_flush(s)```

Once you are done communicating with serial port, be careful to properly close it, as otherwise it cannot be used by any other device, or reopened in Octave:

```fclose(s);
clear s;```

Note that communication may hang in certain cases, thus 'pause' is used between calls where this may happen.

You can find a sample code for Energia/Arduino device and Octave, containing main and three sub-functions,in our [GitHub repository](https://github.com/IRNAS/MathFunctions/tree/master/SerialCommunicationOctaveArduino). Function serial_setup() establishes connection and settings, serial_red1() reads array of different type of variables, then serial_write1() writes back changed values.  Note that this is an early release of an unoptimized code which at least on the micro-controller side can be significantly optimized. 
 
 



