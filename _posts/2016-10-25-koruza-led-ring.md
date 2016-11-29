---
layout: post
title: "Koruza LED Ring Display and Event Demonstration"
description: ""
category: KORUZA
tags: [KORUZA, KORUZA Pro, Koruza LED ring, demo, event demonstration]
---
{% include JB/setup %}

The challenge of demonstrating wireless optical communication with an invisible optical beam as with our [KORUZA](http://koruza.net/){:target="_blank"} system is in showing the transmission of data with light, since it is difficult to have a direct interaction between people and data. To be able to demonstrate at least in part what is going on, we have resorted to using LED diodes and mimicking what is going on. For KORUZA units we have built magnetically attachable LED rings (Adafruit NeoPixel 24) that color code the optical power received at either unit. One can then, by blocking the optical beam, partially or completely see to what degree the power has been lost and play with the system. To show the data being sent between the units, we have employed an addressable LED strip propagating pulses of light between the two units, stopping when the actual optical beam is blocked.

The technical implementation of this demonstration is rather straightforward. A Raspberry Pi is interfaced with NeoPixel LED rings through USB driver Fadecandy and directly via SPI to the LED strip. It fetches the information about the KORUZA optical link directly from KORUZA units via ubus protocol. A simple script processes the information and drives the LEDs - you can find it on [GitHub](https://github.com/IRNAS/koruza-led-demo){:target="_blank"}

We have premiered this demonstration at [ARS Electronica 2016](http://www.aec.at/radicalatoms/en/artist-lab-institute-irnas/){:target="_blank"} and demonstrated it at [Maker Faire Rome 2016](http://www.makerfairerome.eu/en/){:target="_blank"}. The LED ring feature has proven to be such a good idea, we have implemented support for it directly into the KORUZA control system, so that we can now directly attach the LED ring to the unit, which is very practical during experimentation and fog experiments. Details about this implementation can be found on [GitHub](https://github.com/IRNAS/koruza_driver_firmware/pull/9
){:target="_blank"}.

[![koruza-led-ring]({{ site.url }}/post_files/koruza-pro-dev/koruza-led-ring.jpg){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/koruza-led-ring.jpg){: .img-open}
[![koruza-led-ring]({{ site.url }}/post_files/koruza-pro-dev/demo-maker-faire.jpg){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/demo-maker-faire.jpg){: .img-open}