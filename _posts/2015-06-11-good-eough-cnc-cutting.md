---
layout: post
title: "Good-enough useful-open-hardware CNC/Plasma cutter - Cutting"
description: "Introducing good-enough machine design and overview of CNC/plasma design in the works"
category: GoodEnoughCNC
tags: [CNC, Plasma, GoodEnoughCNC]
---
{% include JB/setup %}


Our Good-enough CNC plasma cutter is finally operational! After making some finishing touches [as outlined previously]({{ site.url }}/goodenoughcnc/2015/06/04/good-eough-cnc-plasma) on the CNC platform, we paired it with our BMF CUT 50M plasma cutter and air compressor.

A 3D printed torch holder mounted on Z axis mechanism behaves perfectly. As shown on the photos of the first test, we are currently using only a half the holder and some zip-ties for greater flexibility, however by adding the other half of the holder later on, the torch will be reliably locked in place with 4 screws. The torch holder was designed for mounting the original handle, as leaving the plasma cutter untouched has numerous advantages:

 * Warranty is retained.
 * Easily dis-mountable for further hand-held use.
 * Low-cost design as torches designed for CNCs are expensive.

The plasma cutter was positioned on bed of concrete tiles to protect the workshop floor and raised to allow space for the 3 mm thick steel plate to be put on blocks of wood and cut. For now, the cables were simply hung from the ceiling. 

We were pleased to see the first cut piece fall to the concrete. The Torch Height Controller does its job perfectly and keeps the cut voltage consistent around the shape. The kerf was uniform in width and the cut surface was clean. Top spatter was minimal, but the dross build-up at the bottom was significant. After adjusting the parameters, primarily increasing the cutting speed and current, the cuts became significantly cleaner. The photo below demonstrates the reduction in dross as the speed and current went up. We started with 10 A, just grazing the surface and went up to 25 A and later 35 A. The speed went from 500 mm/min to 750mm/min and later 1000mm/min.

There is still much to learn and try out, so we will be testing and using the machine in the next couple of days to get a hang of it. At the same time we will be finalizing the design, optimizing components and preparing the open-source release documentation for release in a week.

[![good enough plasma]({{ site.url }}/downloads/plasma/17.jpg){: .img-half}]({{ site.url }}/downloads/plasma/17.jpg){: .img-open}
[![good enough plasma]({{ site.url }}/downloads/plasma/18.jpg){: .img-half}]({{ site.url }}/downloads/plasma/18.jpg){: .img-open}

<iframe width="560" height="315" src="https://www.youtube.com/embed/IsliOHDgIus" frameborder="0" allowfullscreen></iframe>