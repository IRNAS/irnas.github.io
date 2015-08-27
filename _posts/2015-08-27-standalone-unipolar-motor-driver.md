---
layout: post
title: "Universal unipolar motor driver for KORUZA"
description: "Control electronics split into standalone modules."
category: 
tags: []
---
{% include JB/setup %}

Nearing the release of [KORUZA 1.0](http://koruza.net) wireless optical system the standalone system modules are nearing completion. Automated alignment uses low-cost 24BYJ48-03 stepper motors, similar to more popular 28BYJ48 ones. The control system following our [modular electronics approach]({{site.url }}/2015/05/20/koruza-electronics-modules/) has been developed to implement standalone functions for maximal reuse in many different projects.

![stepper controller]({{ site.url }}/post_files/uumd/board.jpg)

The lack of a low-cost stepper controller designed for use with the low-cost motors has motivated us to implement an universal solution with minor optimizations for use in KORUZA. Standalone unipolar motor driver has a number of welcome features:

 * driving 3 unipolar stepper motors 28BYJ48 or 24BYJ48 with suitable JST connectors
 * support for 6 end-switches, two which can be directly attached to the PCB without cables, such that control board can be positioned in a corner of the moving object.
 * support for 3 encoders for closed-loop control in high-precision systems
 * based on Texas Instruments MSP430G2955 in [Energia](http://energia.nu) environment
 * UART, I2C and SPI interfaces for receiving the control commands
 * unified serial connector for all interfaces
 * STATUS: operational prototype
 
Micro-controller has been chosen based on cost and pin number as well as availability in a sufficiently friendly package, however increasing the software development effort. Current revision has been tested wit custom Energia code, however we aim to port to it [GRBL](https://github.com/grbl/grbl) firmware and thus make it directly interfacable from computer.

Alternative applications discovered thus-far for the controller board are listed below. We are always looking for ideas and people who would like to use it in their system, do ge tin touch:

 * 3D printer auto bed-levelling system
 * open-source microscope automation system
 * optics lab micrometer drive motorization
 * mini 3D printers and robots
 
 Sources are in the process of release to [IRNAS Universal Unipolar Stepper Controller Github](https://github.com/IRNAS/UniversalUnipolarStepperController)
 




