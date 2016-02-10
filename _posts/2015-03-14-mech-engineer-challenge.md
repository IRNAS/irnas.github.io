---
layout: post
title: "Design challenge for mechanical engineer open position"
description: "A basic design task for evaluating candidates for the job."
category: IRNAS
tags: [Vacancy, IRNAS]
---
{% include JB/setup %}

We have received a number of applications for the advertised [open position]({{ site.url }}/irnas/2015/02/25/open-position-mech-engineer) of a mechanical engineer. A selection of the applicants will be invited for interviews when they have completed the following design task:

Dual motorized HEX (Allen) key drive system for automatic calibration of the [KORUZA](http://koruza.net) system using low-cost 3D printing and minimal amount of additional parts. Wireless optical system KORUZA consists of an invisible IR optical beam and a green optical beam for alignment purpose. When the unit is assembled, the green laser must be aligned experimentally by rotating two M3 DIN912 screws embedded in the structure. The green laser is flexibly mounted so it pivots and the two screws are used to adjust the position of two wedges (wedge has a nut embedded), which cause the pan/tilt of green optical beam. Between the head of the screw and the wedge there are two stacked springs (5mm diameter, 12mm length - 7mm compressed, 1mm spring steel). 

Estimate the torque delivered by the drive to be at least 5 times the one required to fully compress the spring stack. Design a drive system using off-the-shelf hex keys. Note that the screw head is sunk approximately 20mm in the structure and the hole leading to it has the same diameter as the head itself.

The drive system must fit within the bounds of the KORUZA system and must not obstruct the lens. Positions of the screws, lens and outer bounds must be derived from [STL]({{ site.url }}/downloads/TaskMechEng/koruza-v5-front_mockup.stl) and/or [DXF]({{ site.url }}/downloads/TaskMechEng/koruza-v5-front_mockup.dxf) files.

Requirements for key drive system:

* Drive two M3 DIN912 screws
* Use [24BYJ58]({{ site.url }}/downloads/TaskMechEng/24BYJ48-03-4.pdf)stepper motors
* Design is 3D printable with low-cost FDM (make sure parts are printable)
* Use bearings only if really needed
 
Requirements for submission of the task:

* Design in any 3D CAD you are comfortable with (OpenSCAD is preferred)
* Publish the finished design on [GitHub](http://github.com) and document it accordingly to [http://www.ohwr.org/projects/cernohl/wiki](CERN OHL)
* Honestly report the time required to complete the task
 
 
[![KORUZA front view]({{ site.url }}/downloads/TaskMechEng/koruza-front.jpg){: .img-full}]({{ site.url }}/downloads/TaskMechEng/koruza-front.jpg){: .img-open}


