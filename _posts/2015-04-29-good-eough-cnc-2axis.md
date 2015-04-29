---
layout: post
title: "Good-enough useful-open-hardware CNC/Plasma cutter - 2 axis prototype"
description: "Introducing good-enough machine design and overview of CNC/plasma design in the works"
category: 
tags: []
---
{% include JB/setup %}

Continuing the development work described in our [ previous blog]({{ site.url }}/2015/04/16/good-eough-cnc-intro/) of a single axis prototype, we have now constructed a 2-axis prototype. First test have proven to be very successful, with smooth motion and mechanical strength to sustain repeated motion undet approximately 70kg vertical load. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/436FoAMxD0M" frameborder="0" allowfullscreen></iframe>

Following the same guidelines, the XY gantry was constructed using exclusively a drill press and an angle grinder.  A few components for mounting and tightning the belt and endswitches were made using 3D printing and laser cutting, however they could be made by hand rather simply. We strive to create the design that can be extremely versatile and made with any combination of low or high tech manufacturing methods available to the end user. Our design of parts bases on functionality, regardless of the way they are made. Someone might find drilling holes in a piece of wood the simplest method, while for us it was 3D printing and laser cutting, once the plasma cutter will be operational this may be the preferred way.

The 2 axis gantry now occupies quite some space however for such a machine we have managed to keep the count of different parts to the minimum. The entire gantry including trolleys uses one type of bearings for motion and another for the belt, three different screw variants and a number of nuts and washers. All the three trolleys are of the identical design to enable simples construction and minimize possible errors.

The gantry is designed to be built with loose tolerances, accommodating for imperfections in the design that arise from:

 * standard square tubing profile is not perfectly rectangular not straight
 * tubing surfaces may not be flat
 * cutting tubing to exact lengths with an angle grinder is almost impossible
 * manual hole drilling is not an exact process, we have managed to drill them with 0.2mm tolerance
 * accurate marking of hole positions is not always possible

Our design assumes parts are not perfect and implements adjustment mechanisms where required. The X axis that carries the plasma cutter or spindle is runs on a single rail that sits on top of two Y axis trolleys. It is fixed to one with a single screw allowing for pivot and fixed to the other with sufficient movement along the rail axis, accounting for non-parallel Y axes. 

Trolleys are designed and documented such that holes are dimensioned relative to each other and aligned only to one edge of the profile, to ensure tolerance stack-up is kept to a minimum.	

We are currently working on testing the XY gantry and sorting out all the details, such as belt mounting, endswitches, adjustment of right angle between axes and smooth motion. Once this is completed we will release the full documentation.

The approximate cost of such XY gantry excluding stepper motors is $100, including all square tubing, nuts and bolts, belts and bearings. Basic control electronics and stepper motors should be available for another $200.

![good enoguh plasma]({{ site.url }}/downloads/plasma/9.jpg)

![good enoguh plasma]({{ site.url }}/downloads/plasma/10.jpg)
 
