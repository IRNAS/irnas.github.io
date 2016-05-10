---
layout: post
title: "KORUZA v2 motor system"
description: "We've started with a development of mechanical modules for Koruza v2, which is aimed to be produced on a larger scale for end users. Because of that, new mechanical design needs to be production friendly and must enable low cost production."
category: KORUZA
tags: [KORUZA, KORUZA v2, motor system, development]
---
{% include JB/setup %}


We've started with a development of mechanical modules for Koruza v2, which is aimed to be produced on a larger scale for end users. Because of that, new mechanical design needs to be production friendly and must enable low cost production. Material chosen for backbone structure of Koruza v2 is aluminum because of its low mass and price, it is also easy to shape using various tools (CNC laser cutter, Waterjet, CNC milling and turning).
Our first priority, speaking about mechanical module, was to reinvent motor system used for laser beam alignment. Since new Koruza will have much smaller outer dimensions it has to be more compact without compromising accuracy and reliability.

**Spherical bearings:**

Because of the movement of the lens tube, we have to ensure movement of the end of the lens tube in all directions simultaneously. In the first iteration of the prototype we used the design with spherical bearings, which enables simultaneous movement in all three axes. We used the M5 metric thread, which was responsible for movement of the lens cylinder in x and y axes. In this design a motor and a nut are freely suspended with the use of spherical bearings. To eliminate movement of the motor and the nut in the axis of rotation (backlash) we would need to use a series of springs, which makes the system unreliable and complicated, that is why we abandoned this design.

[![motor-system-1]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-1.JPG){: .img-full}]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-1.JPG){: .img-open}

**Spring couplers:**

In attempt to resolve the issue from the first design we replaced the spherical bearings with a flexible spring coupler at the motor side and with a plain radial bearing at the nut side. This design in theory allows movement only in x or y axes, while allowing the spherical travel of the lens cylinder. In the experiment we found out that this design is extremely sensitive to the concentricity of the motor axis with M5 rod and parallelism holes in the nut and coupler, resulting in unlinear movement of the IR beam.

[![motor-system-2]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-2.JPG){: .img-full}]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-2.JPG){: .img-open}

**Sliding linear nut system:**

The design, which accommodates all our requirements, is a nut with a sliding surface that enables movement in linear direction and at the same time free spherical movements on the other nut. Plastic used for surface sliding nut has excellent self-lubricating properties, allowing smooth linear movement without sticking or shaking. The retraction force is reached with one diagonally positioned spring. Such system of movement is compact in size and enables easy installation. Moreover, indirect burden on the engine axis and lower operating torques will result in a longer engine life.

[![motor-system-1]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-3.JPG){: .img-full}]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-3.JPG){: .img-open}