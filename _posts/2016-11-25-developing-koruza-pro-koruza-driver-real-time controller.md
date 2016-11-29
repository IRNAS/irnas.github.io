---
layout: post
title: "Developing KORUZA Pro: Koruza Driver - Real-Time Controller"
description: "The Koruza driver is an additional board to Koruza router. Its main task is to handle the real-time parts of Koruza system, like stepper motors for the laser beam positioning, infrared communication between two Koruza units, encoders for stepper motors, etc."
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Koruza Driver, Real-Time Controller]
---
{% include JB/setup %}

The Koruza driver is an additional board to [Koruza router](https://github.com/IRNAS/KORUZA-router){:target="_blank"}. Its main task is to handle the real-time parts of [Koruza system](http://koruza.net/){:target="_blank"}, like stepper motors for the laser beam positioning, infrared communication between two Koruza units, encoders for stepper motors, etc. 

The Koruza driver consists of the two separate PCB boards. First is the [driver board](https://github.com/IRNAS/Universal-Stepper-Driver-Rpi){:target="_blank"}. It is the main controller board that contains the power supply block, MCU, unipolar stepper drivers, and all the necessary connectors Koruza unit needs. The second is [Koruza expander board](https://github.com/IRNAS/Koruza_Expander_Board){:target="_blank"}. This board adjusts the signals of the driver board for the Kouza router connector, regulates power supply from PoE to +12 V so the Koruza router can work properly, and adds the special connectors like four wire connector for the USB camera.

Because both boards, the driver, and the router have processors, there must be some kind of communication between the Koruza router CPU and the Koruza driver MCU. A majority of the systems which have this kind of architecture are using UART communication between two processors. This way they can exchange data and commands. It is necessary to establish a good protocol between the two processors. A chosen protocol is based on TLVs, which makes it extensible in a backwards-compatible way. Each protocol message looks like this:

```
[TLV#1] [TLV#2] ...
```
And each TLV looks like this:

```
[type: 1 byte] [length: 2 bytes] [value: length bytes]
```

All protocol values are in network byte order (big endian). The use of TLVs enables older protocol implementations to skip newer TLVs. 

Of course, you could ask, why two boards, couldn't all this be done on the single PCB? The answer is [YES](http://replygif.net/i/551.gif){:target="_blank"}, it could, but when you want something fast and reliable you have to compromise. And this is the case with rapid prototyping in electronics. Certainly these two boards will be merged into one in the final version of [Koruza Pro](http://new.koruza.net/){:target="_blank"}, but it the adjustment will be much easier, to do this now when that we know are aware of all the possible problems and have the working version of the Koruza driver. 

[![mounting-system]({{ site.url }}/post_files/koruza-pro-dev/koruza-driver.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/koruza-driver.JPG){: .img-open}







