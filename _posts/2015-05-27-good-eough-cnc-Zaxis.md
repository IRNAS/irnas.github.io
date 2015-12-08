---
layout: post
title: "Good-enough useful-open-hardware CNC/Plasma cutter - Z axis prototype"
description: "Introducing good-enough machine design and overview of CNC/plasma design in the works"
category: GoodEnoughCNC
tags: [CNC, Plasma, GoodEnoughCNC, Development]
---
{% include JB/setup %}

Continuing the development work described in our [ previous blog]({{ site.url }}/2015/04/29/good-eough-cnc-Zaxis/) of a XY gantry prototype, we have now added a number of improvements and constructed the Z axis. We have evaluated a number of common practices in Z axis design on small CNC machines and have found that the majority of designs consists of precise milled parts or expensive linear mechanical parts. The requirements for our Z stage have been set to:

* limit the torsion of the X axis trolley
* minimize the assembly weight
* use widely available assembly parts and limit any custom parts to be made out of sheet material or 3D printed
* allow for an arbitrary length of the Z axis

[![good enoguh plasma]({{ site.url }}/downloads/plasma/13.jpg){: .img-full}]({{ site.url }}/downloads/plasma/13.jpg){: .img-open}

The above list is realized in the design with the following rationale. Torsion of the trolley is minimized by reducing the offset of the tool to the center of X axis. Conventional designs of CNC machines use two rails for X axis and are less prone to this problem. 

The most significant advantage of making the two guide rods a part of the movable Z axis is their variable length, allowing one to easily configure the machine in any setup without modifying parts. Linear motion is implemented with a M6 threaded rod and a NEMA17 stepper motor, supporting axis length variation. Bearings and rails have been reused from [Troublemaker 3D printer](http://www.thingiverse.com/thing:263814), since they are widely available and low cost.

[![good enoguh plasma]({{ site.url }}/downloads/plasma/12.jpg){: .img-full}]({{ site.url }}/downloads/plasma/12.jpg){: .img-open}

Good enough CNC design aims to concentrate all essential parts on the trolleys themselves, reducing the complexity of remaining parts as well as enabling the square tubing for the axes to be easily swapped with longer/shorter pieces to accommodate a number of user requirements. Mounts for end-switches are designed such that no extra holes are required and can be easily installed as an add on, since they are not crucial for bare-minimum operation. All 3D printed parts are designed to be symmetrical and thus only a single version is used multiple times on a machine.

Paralleling of the construction while retaining the portability has been a significant issue, however we have managed to achieve good robustness and simple construction by using a set of 
turnbuckles. When both are tightened to create tension between tubes, the whole gantry becomes very rigid, while it is simple to undo them and fold the construction, should it be transported.

[![good enoguh plasma]({{ site.url }}/downloads/plasma/11.jpg){: .img-full}]({{ site.url }}/downloads/plasma/11.jpg){: .img-open}

As usually, video or it did not happen. Enjoy watching our logo being drawn on paper and the load test of the machine, which can easily move under about 60kg load.

<iframe width="560" height="315" src="https://www.youtube.com/embed/4pPv4le0X7k" frameborder="0" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/ORQ5XDI6lFc" frameborder="0" allowfullscreen></iframe>
