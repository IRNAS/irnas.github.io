---
layout: post
title: "CNC milling machine - update"
description: "Update on development of the GoodEnoughCNC milling machine."
category: 
tags: []
---
{% include JB/setup %}

[Last week]({{ site.url }}/2015/08/11/cnc-mill/) we finished designing the frame and X, Y axis for CNC milling machine, so we started with assembly of the main frame. The biggest challenge in constructing was to ensure the accuracy of the composition, which is a key element to achieve the required tolerances in CNC milling. As the use of advanced machine tools for many people around the world are still difficult to reach, we have to find an effective way for assembly that would allow us sufficient accuracy using only basic tools.

![cnc-mill]({{ site.url }}/post_files/cnc-mill2/mill1.JPG)

With this in mind, we have developed a plan for the assembly, which simultaneously eliminates errors and deviations in the construction (cutting profiles to the final dimensions, positioning of the holes, their squareness upon each other, ..). We have found out that the best accuracy is achieved if the holes for the screws are drilled simultaneously between two profiles, during the assembly of individual components.  In this way, we can adapt to the differences between holes in the two components. Also, it is much easier to ensure squareness between the individual components, which is crucial for the stability of the structure.

![cnc-mill]({{ site.url }}/post_files/cnc-mill2/mill2.JPG)
![cnc-mill]({{ site.url }}/post_files/cnc-mill2/mill4.JPG)

With this method of manufacturing, we achieved very good results in terms of squareness and parallelism of construction:
- Deviations after a diagonal measurement: less then + - 0.5 mm to 3500 mm,
- Parallel beams: less then + - 0.4 mm to 3000mm,
- Parallel feet of the table less then + - 1mm,
- Deviation of 3000mm beam (in the middle, with 80kg load): 0,5mm.

![cnc-mill]({{ site.url }}/post_files/cnc-mill2/mill3.JPG)
![cnc-mill]({{ site.url }}/post_files/cnc-mill2/mill5.JPG)

At the same time we have finished constructing the Z axis. We opted for the version with double guides, on linear bearings. Such design ensures a 200 mm movement in Z axis. Drive is provided via stepper motor with gear reducer, which is already used to drive the X and Y axes. We believe that the said structure will be rigid enough for CNC milling of wood and aluminium. So far, we have chosen 12 mm lead with the possibility of change to the 14 mm version. For spindle we used water cooled 2.2 kW motor, which provides 40,000 rev / min.








