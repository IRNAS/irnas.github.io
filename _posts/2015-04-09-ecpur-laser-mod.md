---
layout: post
title: "Modification of a low-cost 40W laser cutter"
description: "Details about modifying a laser cutter with different control electronics and other details."
category: Other Projects
tags: [Other Projects, Laser cutter]
---
{% include JB/setup %}

For fast prototyping and development purposes we have purchased an [ECPUR NEW3020 low-cost 40W CO2 laser cutter/engraver](http://www.ecpur.com/itm/2220.html) but without Moshi control electronics, saving on the cost. We have installed a custom control electronics and introduced a number of small fixes to improve the performance, usefulness and safety of operation.

The following parts were installed/supplies with the laser cutter on our order:

 * Fully assembled laser cutter without control electronics, but including MYJG40W power supply.
 * Water pump
 * Extractor fan
 
We have chosen to install [Planet CNC](http://planet-cnc.com) control electronics due to extremely good support and reasonable pricing. While it is no open-source it does significantly speed up the development process and operates more reliably. However the same modification process applies to installing some other controller, for example open source [LAOS controller](http://redmine.laoslaser.org/projects/laos/wiki).

 * [Controller MK3/4](http://www.planet-cnc.com/index.php?page=hardware)
 * 2pcs [MotorDriver 2.5A - 32](http://www.planet-cnc.com/index.php?page=shop)
 
Additionally the following parts were used:

 * 20L canister with distilled water for cooling
 * Airbrush compressor 2.8bar (40PSI) - 13 l/min
 
The lack of proper documentation and some corner-cutting in assembly and design of the laser cutter required the following modifications:

 * Design of a new front plate
 * Controller installation
 * Cutting bed replacement with HEX grid and hight adjusted
 * Installation of interlock safety switched
 * Modification of air suction intake
 
 We will detail all the modifications and create instructions for performing them shortly.

  [![Laser-cutter1]({{ site.url }}/downloads/laser/image1.jpg){: .img-half}]({{ site.url }}/downloads/laser/image1.jpg){: .img-open}
 [![Laser-cutter2]({{ site.url }}/downloads/laser/image1.jpg){: .img-half}]({{ site.url }}/downloads/laser/image2.jpg){: .img-open}
 
