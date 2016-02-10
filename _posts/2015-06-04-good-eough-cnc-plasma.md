---
layout: post
title: "Good-enough useful-open-hardware CNC/Plasma cutter - Plasma cutter selection"
description: "Introducing good-enough machine design and overview of CNC/plasma design in the works"
category: GoodEnoughCNC
tags: [CNC, Plasma, GoodEnoughCNC, Development]
---
{% include JB/setup %}

In preparation to equip the 3 axis machine design introduced in the previous weeks  [blog]({{ site.url }}/goodenoughcnc/2015/05/27/good-eough-cnc-Zaxis), we have set to find and test suitable plasma cutting torch machines and pick the cheapest device that produces reasonably good results. To fall within the lowest cost range, the selection was limited to plasma torches designed for hand-held operation.

A Slovenian welding supply company [Varesi](http://www.varesi.si/) has kindly invited us to visit their shop with our CNC machine and test a number of plasma cutters on the spot. By driving across the country to their location, we could not leave behind our CNC machine. Although the machine is 140x125cm in outer dimensions, by removing the tighteners and turning it into a parallelogram, we could fit the whole machine in the back of a Ford Mondeo Estate without any disassembly. This is was very exciting and well demonstrates design simplicity and versatility. The CNC was up and running at Varesi in only a few minutes, having to only align the right angles and connect the cables.

From a selection of several vendors, we have set our eyes on two machines, the mid-end [Cebora Power Plasma 3035/M](http://www.cebora.it/art_279_presentazione_prod_uk.html) and low-end range Chinese BMF CUT 50M [as on Amazon](http://www.amazon.de/NTF-Druckluft-Plasmaschneider-Inverter-Schneiden/dp/B00VE6PCMK) or [Varesi website](http://www.varesi.si/trgovina/varilni-aparati/bmp/inverterske-plazme-bmp/bmp-cut-50m), sold in numerous varieties under a number of different brand names and about the tenth of the cost of the high-end machine.

[![good-enough-plasma]({{ site.url }}/downloads/plasma/14.jpg){: .img-half} ]({{ site.url }}/downloads/plasma/14.jpg){: .img-open}

[![good-enough-plasma-2]({{ site.url }}/downloads/plasma/15.jpg){: .img-half} ]({{ site.url }}/downloads/plasma/15.jpg){: .img-open}

Unfortunately, we did not manage to try out the plasma on the machine on site, due to that days tight schedule and the requirement to introduce some modifications. We did however try out the plasma cutters the old fashion way - by hand. After switching from BMF to Cebora, we experienced a clear difference in the simplicity of establishing the arc (Cebora HF start is of great help) and the smoothness of the cut. However lacking previous experience with such tools, we made cuts of reasonable quality with either machine. When the low-end machine was handled by experienced professionals, the cuts made were of similar quality to the mid-end one.

BMF Cut 50M proved to be ideal for our application due to a number of reasons:

 * 50A rated machine for up to 16mm cut thickness, however realistically behaving as a 30A high-end machine.
 * Removable electrode and torch allow for simple installation of the Torch Height Control circuit, not the case with mid-end machine.
 * Standalone trigger connector, allowing for simple control from the CNC without internal modifications, not the case with mid-end machine.
 * Low-cost of nozzles, electrodes and other consumables as well as replacement torches.
 
However there are a number of features that would be welcome, such as:

 * Voltage measurement port, ideally with 1:50 voltage divider.
 * HF start/pilot arc.
 * Built-in air compressor.
 
With the current machine, an air compressor is required, capable of supplying 30-100 l/min at pressure 0.2-0.4 (2-4 bar) MPa, when connected to the plasma cutter. Tests have shown that a low cost suitcase style compressor <del>has insufficient flow and thus we are in search for a good cost-effective option</del> may have sufficient flow for operation. Additionally plasma cutters are sensitive to moisture in compressed air, resulting in premature torch failures and shorter consumables life. Professional solutions are expensive and thus we will be evaluating other options.

The disassembly of the CUT50M device has shown that voltage measurement probes can easily be attached to screw terminals just behind the front panel, as well as the circuit board version CUT400UB 70UM with date 20140426. Further information on the design would be welcome, like schematic diagram or other cutting machines using the same internal electronics.

Currently, we are finalizing the connections to the control electronics and designing a mounting element to attach the torch to the Z axis. We should be cutting metal in a few days.

[![good enough plasma]({{ site.url }}/downloads/plasma/16.jpg){: .img-full}]({{ site.url }}/downloads/plasma/16.jpg){: .img-open}
