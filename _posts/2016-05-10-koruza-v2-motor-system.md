---
layout: post
title: "KORUZA v2 motor system"
description: "We've started with a development of mechanical modules for Koruza v2, which is aimed to be produced on a larger scale for end users. Because of that, new mechanical design needs to be production friendly and must enable low cost production."
category: KORUZA
tags: [KORUZA, KORUZA v2, motor system, development]
---
{% include JB/setup %}


We've started with a development of mechanical modules for Koruza v2, which is aimed to be produced on a larger scale for end users. Because of that, new mechanical design needs to be production friendly and must enable low cost production. Material chosen for backbone structure of Koruza v2 is aluminum because of its low mass and price, it is also easy to shape using various tools (CNC laser cutter, Waterjet, CNC milling and turning).
Our first priority in mechanical module was to reinvent motor system used for laser beam alignment. Since new Koruza will have much smaller outer dimensions it has to be more compact without compromising accuracy and reliability.

**Spherical bearings:**

Due to the movement of the lens tube, we have to ensure movement of the end of the lens tube in all directions simultaneously. In the first iteration of the prototype we used design with spherical bearings, which provide simultaneous movement in all three axes. We used the M5 metric thread, which was responsible for movement of the lens cylinder in x and y axes. In this design the motor and nut is freely suspended with the use of spherical bearings. To eliminate movement of motor and nut in the axis of rotation (backlash) we would need to use a series of springs, which would make the system unreliable and complicated and therefore we abandoned this design.

[![motor-system-1]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-1.JPG){: .img-full}]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-1.JPG){: .img-open}

**Spring couplers:**

In attempt to resolve issue from the first design we replaced spherical bearings with flexible spring coupler at motor side and plain radial bearing at nut side. This design will in theory allow movement only in x or y axes, while allowing the spherical travel of lens cylinder. We found out in the experiment that this design is extremely sensitive to the concentricity of the motor axis with M5 rod and parallelism holes in the nut and coupler, resulting in an unlinear movement of IR beam.

[![motor-system-2]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-2.JPG){: .img-full}]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-2.JPG){: .img-open}

**Sliding linear nut system:**

The design, which accommodate all our requirements is a nut with a sliding surface, which enables movement of a nut in linear direction and at the same time (free spherical movements on the other nut). Plastic used for surface sliding nut has excellent self-lubricating properties, allowing smooth linear movement without sticking or shaking. The retraction force is reached with one diagonally positioned spring. Such a system of movement has compact size and enables easy installation. Indirect burden on the engine axis and lower operating torques will result in a longer engine life.

[![motor-system-1]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-3.JPG){: .img-full}]({{ site.url }}/post_files/koruzav2-motor-system/motor-system-3.JPG){: .img-open}