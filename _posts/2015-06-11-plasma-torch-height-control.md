---
layout: post
title: "Plasma torch voltage measurement and height control"
description: "Developing a reliable and low-cost plasma torch height controller"
category: GoodEnoughCNC
tags: [Plasma, CNC, GoodEnoughCNC, Development]
---
{% include JB/setup %}

[Our good-enough CNC plasma]({{ site.url }}/2015/06/04/good-eough-cnc-plasma/) is being put through the paces and we are improving all design aspects. We have experienced some problems with measuring the plasma cutting voltage (arc voltage is monitored to maintain the cut on bent material). Although using the professional Promo Plasma THC 150 controller, optocouplers connecting it to the CNC controller were burned along with a pin. Thus we took a step back to rethink the overall design and evaluate possible improvements.

[![good enough plasma]({{ site.url }}/downloads/plasma/19.jpg){: .img-full}]({{ site.url }}/downloads/plasma/19.jpg){: .img-open}

[In ToslinkCNC]({{ site.url }}/2015/06/05/optical-cnc-control-toslink/) design we are planning to implement fully optical control for the CNC and have taken the first chance to start developing the idea. For that purpose we have built a simple system using Arduino Pro Mini and Toslink transmitters and receivers to establish a digital 19200baud communication between them using Manchester encoding after evaluating the use of hardware UART interfaces and SPI interfaces. The Toslink receiver limitation of 0.1Mbps bitrate effectively prohibits its use with low cost devices. However after detailed experimentation we have discovered this limit is primarily imposed by the automatic gain and thus pushing the receiver into saturation. By introducing a controlled attenuation on the Toslink communication, the minimal bitrate has been reduced to 0.04Mbps while retaining error free communication. Attenuation has been introduced simply by slipping a piece of paper between the fiber end and the receiver. This finding is very significant as it unlocks the potential for Toslink use in many open hardware projects at minimal cost. We have implemented a test link between the Promo THC and our controller, carrying the logical signals over the fiber link, however the prototype controller with the nest of wires carrying out the optical communication has been too susceptible to RF noise from plasma cutter for any real use. We have now designed PCBs and will shortly continue its development and release the system.

[![good enough plasma]({{ site.url }}/downloads/plasma/21.jpg){: .img-full}]({{ site.url }}/downloads/plasma/21.jpg){: .img-open}

Digital transmission over fiber is not yet applicable to our problem, thus we have devised an even better strategy for measuring the plasma cutter voltage and controlling its trigger via analog optical communication. A standard 5mm LED diode has been coupled to the plasma cutter output via a potential divider, such that the light intensity varies with the plasma arc voltage. As the LED diode intensity corresponds non-linearly with respect to the applied current and the photoresistor on the other end of the link behaves likewise, a calibration procedure has been developed with curve fitting for response linearisation and applied to an Arduino board with simple control code generating commands for the CNC controller to reduce or increase the cutting voltage. Currently we are testing the design on our machine and improving it prior to open source release.

The approach has been extended in the reverse direction between cnc control electronics and plasma cutter to activate its trigger. A relay is triggered with a photoresistor via a MOSFET with the light supplied over a fibre from the controller. A very low cost solution effective in isolating the control system and exposing only low-cost and generally robust components to critical high voltage environments.

[![good enough plasma]({{ site.url }}/downloads/plasma/20.jpg){: .img-half}]({{ site.url }}/downloads/plasma/20.jpg){: .img-open}
[![good enough plasma]({{ site.url }}/downloads/plasma/22.jpg){: .img-half}]({{ site.url }}/downloads/plasma/22.jpg){: .img-open}

After a few intensive days of experimenting with fibres and Toslink in particular, we have devised a number of low-cost and good performance solutions for use not only with plasma cutters but with CNC machines in general, replacing the need for optocouplers and heavy cable shielding. Future improvements on the design will make it more reliable and suitable for implementation in a number of other applications.