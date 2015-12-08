---
layout: post
title: "Good-enough useful-open-hardware CNC/Plasma cutter - Design overview"
description: "Introducing good-enough machine design and overview of CNC/plasma design in the works"
category: GoodEnoughCNC
tags: [GoodEnoughCNC, CNC, Plasma, Design, Prototype]
---
{% include JB/setup %}

Constructing machines and physical systems is always challenging. Industry in vast majority aims to use highest precision and reliability machines, to be capable of producing even the most complicated parts designers come up with. We are flipping such approach on its head, trading precision of manufacturing tools for simplicity and low cost of their construction, to reduce the entry barrier for using them in any environment. We put brain power into figuring out how to make things work even if all assembly parts are imprecise.

To support the development of wireless optical system [KORUZA](http://koruza.net) and construction of its enclosures, we have set to construct a simple and effective good-enough CNC machine that can be used with a mill or plasma cutter. Our main guidelines are simplicity and minimal entry barrier to construction which is well aligned in philosophy with [Open source ecology](http://opensourceecology.org/).

General guidelines for good-enough machine design:

 * maximal impact versus complexity - how many useful thing you can make with the machine without increasing its complexity
 * low entry barrier - should use only standard widely available assembly parts and material and be constructed with basic tools
 * bootstrap / self-replicating design - use the bare minimal version of the machine to build better quality parts and upgrades
 * open-source open-hardware documented using [useful source]({{ site.url }}/2015/03/08/useful-source) documentation
 
Outer enclosure of KORUZA system is constructed out of standard sheet metal and square tubing elements cut into shape, currently performed by high specialized companies. [Open Source ecology Compressed Earth Brick press](http://opensourceecology.org/portfolio/ceb-press/) can leverage the same machine for building it.

<iframe width="420" height="315" src="https://www.youtube.com/embed/J9esTNeq7_s" frameborder="0" allowfullscreen></iframe>

Design guidelines for good-enough CNC/plasma machine are:

 * use only standard square steel tubing and screws/bearings
 * make the design independent of machining area size - build any size that is needed
 * construct the basic gantry mechanics only with a drill press and angle grinder

Use-cases:

 * cut large sheets of metal. Place the machine to be free-standing on the material you cut. Thus only lighter cut pieces and the machine itself need to be moved.
 * make the machine adaptable to size and user requirements
 * upgrade it with Z axis and 4/5th axis, cut square/round profiles on all sides
 
Firstly, we have designed a simple one axis gantry system to evaluate design options. Using standard 40x40x3mm and 100x100x3mm steel tubing, 608ZZ standard bearings and screws we have made three iterations of bearing placements and optimized the assembly to use 6 bearings for a single trolley, stably confining the trolley to linear only movement. With the designs shown in photos below, we have achieved reliable operation with speeds in excess of 35000mm/min on a single axis using only GT2 6mm bearings. Design documentation of this prototype [is available]({{ site.url }}/downloads/plasma/GoodEnoughCNCplasma.pdf).

The control system currently uses good quality [Planet-CNC](http://www.planet-cnc.com/) controllers and  [PoLabs stepper drivers](http://www.poscope.com/index.php?route=product/category&path=68) with NEMA23 motors, all of which can be readily replaced with open source systems.
 

[![good enoguh plasma]({{ site.url }}/downloads/plasma/1.jpg){: .img-half}]({{ site.url }}/downloads/plasma/1.jpg){: .img-open}
[![good enoguh plasma]({{ site.url }}/downloads/plasma/2.jpg){: .img-half}]({{ site.url }}/downloads/plasma/2.jpg){: .img-open}

[![good enoguh plasma]({{ site.url }}/downloads/plasma/3.jpg){: .img-half}]({{ site.url }}/downloads/plasma/3.jpg){: .img-open}
[![good enoguh plasma]({{ site.url }}/downloads/plasma/4.jpg){: .img-half}]({{ site.url }}/downloads/plasma/4.jpg){: .img-open}

[![good enoguh plasma]({{ site.url }}/downloads/plasma/6.jpg){: .img-half}]({{ site.url }}/downloads/plasma/6.jpg){: .img-open}
[![good enoguh plasma]({{ site.url }}/downloads/plasma/7.jpg){: .img-half}]({{ site.url }}/downloads/plasma/7.jpg){: .img-open}

[![good enoguh plasma]({{ site.url }}/downloads/plasma/8.jpg){: .img-full}]({{ site.url }}/downloads/plasma/8.jpg){: .img-open}
 
