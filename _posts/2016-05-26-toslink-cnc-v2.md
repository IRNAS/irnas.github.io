---
layout: post
title: "ToslinkCNC v2 - release"
description: "We released an improved version of ToslinkCNC v2."
category: GoodEnoughCNC
tags: [CNC, GoodEnoughCNC, Toslink, Open Source Hardware, ToslinkCNC]
---
{% include JB/setup %}


Optical control of CNC machines is the future, enabling low-cost and resilient wiring for affordable manufacturing. We have now launched the version 2 of the system with a number of new features. You can check out the blog on previous version [here](http://irnas.eu/goodenoughcnc/2016/03/10/toslink-cnc){:target="_blank"}.

Using the previous version for about 5 machines we've learnt a lot, a number of changes now make it much better. Hardware footprint has been reduced and unified, such that the CPLD based optical board can now be a transmitter or receiver, only with a firmware change. The optical control system can now be seamlessly integrated with Raspberry Pi, Arduino, Planet-CNC controller or any other CNC control system operating with step and direction signals. This makes it perfectly suitable for new machines being built as well as a retrofit of older systems.

[![toslinkcnc-4]({{ site.url }}/post_files/toslink/toslink-arduino-3.jpg){: .img-half}]({{ site.url }}/post_files/toslink/toslink-arduino-3.jpg){: .img-open}
[![toslinkcnc-5]({{ site.url }}/post_files/toslink/toslink-raspberry-pi-2.jpg){: .img-half}]({{ site.url }}/post_files/toslink/toslink-raspberry-pi-2.jpg){: .img-open}

[![toslinkcnc-6]({{ site.url }}/post_files/toslink/toslink-planetcnc-1.jpg){: .img-full}]({{ site.url }}/post_files/toslink/toslink-planetcnc-1.jpg){: .img-open}

ToslinkCNC main board is designed as a single axis device, featuring one receiver and two transmitter optical interfaces and a number of electrical connections through two versions of interfaces. RaspberryPi connector contains signals for 3 separate axis and enable signals, such that the board can be a transmitter for the complete system or extended with a shield to connect to other controllers. On board there are connections for 5V power input, one input and one output as well as a screw terminal or IDC port for step, direction and enable signals to connect to a stepper driver. The RaspberryPi connector also contains pins for JTAG programming of the main board. Currently there is only one shield available that doubles as the interface for the transmitter connected to Arduino or [PlanetCNC controller](http://planet-cnc.com/){:target="_blank"}. When the main board is in function of the receiver, stepper drivers can be connected to it, our default choice being PoStep25-32.

[![toslinkcnc-1]({{ site.url }}/post_files/toslink/toslink-transceiver-diagram.png){: .img-half}]({{ site.url }}/post_files/toslink/toslink-transceiver-diagram.png){: .img-open}
[![toslinkcnc-2]({{ site.url }}/post_files/toslink/toslink-receiver-2-diagram.png){: .img-half}]({{ site.url }}/post_files/toslink/toslink-receiver-2-diagram.png){: .img-open}

[![toslinkcnc-3]({{ site.url }}/post_files/toslink/toslink-transmitter-diagram.png){: .img-full}]({{ site.url }}/post_files/toslink/toslink-transmitter-diagram.png){: .img-open}

The version 2 is not yet perfect, however we are successfully using it with [GoodEnoughCNC Hybrid](http://goodenoughcnc.eu/){:target="_blank"} machines also in challenging conditions, for example with plasma cutters. Future work is required to add proper support for end-switches by significantly optimizing the CPLD code and adding a few more features. Project is open source open hardware, [documented on Github](https://github.com/IRNAS/ToslinkCNC){:target="_blank"}, and you are welcome to have a go at helping out with the development.





