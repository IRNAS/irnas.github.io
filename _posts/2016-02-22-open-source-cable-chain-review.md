---
layout: post
title: "Open source cable chain review"
description: "Cable/energy chains are a very convenient and durable way of organizing cables on CNC machines moving along cartesian axes. While they can be obtained at low cost in some cases, this may not be the case in all places around the world and in all dimensions. Hereby we are reviewing open source cable chain designs available for manufacturing."
category: GoodEnoughCNC
tags: [GoodEnoughCNC, cable chain, review]
---
{% include JB/setup %}


Cable/energy chains are a very convenient and durable way of organizing cables on CNC machines moving along cartesian axes. While they can be obtained at low cost in some cases, this may not be the case in all places around the world and in all dimensions. Hereby we are reviewing open source cable chain designs available for manufacturing, categorizing them per manufacturing process and plans available. Some alternative methods to cable chains are mentioned as well. A nice tutorial on choosing cable-chains on [Instructables](http://www.instructables.com/id/Selecting-cabledragenergy-chains-for-CNC/){:target="_blank"} is a good read to start with.

[![cable-chain]({{ site.url }}/post_files/cable-chains/cable-chain.JPG){: .img-full}]({{ site.url }}/post_files/cable-chains/cable-chain.JPG){: .img-open}

Cable chains are generally assembled from snap-together plastic pieces and are characterized by their inner dimensions, bending radius and of open/closed type, meaning that cables can be inserted from the side in the chain or they need to be threaded through. A typical application considered in this review is [GoodEnoughCNC](http://goodenoughcnc.eu/){:target="_blank"} machine with dimensions of 1x1 m or 2x3 m and top moving speeds of 10 m/min. Typical cabling applications inside the chain are fiber and 2.5 mm<sup>2</sup> wires for power or mains and 8 mm compressed air line.

Commercial grade cable chains are available from a number of suppliers, from no-name brands to igus, Kabelschlepp and others. For inner dimensions roughly 10x20 mm pricing generally ranges between 25-50 EUR/m and for some no-name brands the price is about 6 EUR/m.

The open source DIY cable chains can be made most commonly from 3D printed chain links or CNC/laser cut sheet material pieces.

[John Nicol's](http://makerplane.org/?p=1753){:target="_blank"} design is suitable for heavier duty cables, build out of glued plywood pieces linked with fabric and staples. A very straightforward method of manufacturing requires only hand tools, however quite a bit of effort. Assuming you are building a CNC, you can as well run the machine you are building without this and use it to build a more complicated design. [Grunblau Cable Carrier](http://www.grunblau.com/downloadsBMO.htm){:target="_blank"} as shown on [images](http://www.cnczone.com/forums/diy-cnc-router-table-machines/84792-free-parts.html){:target="_blank"} uses milled MDF cable chain links that are cut from sheet material and snapped together, by applying some glue the links they can be fixed together. The downside of the design is the closed design if cables need to be changed and the wear on wooden joints of the chain. [Rogerquin](http://www.cnczone.com/forums/videos/172959-cnc.html){:target="_blank"} MDF cable chain is a more optimal design requiring no glue, and is potentially more resilient to wear, however the remaining problem is inserting the cables as the chain does not open, depending on the application. Another notable mention cut from polyproilene is [8020cnc](http://www.8020cnc.com/cable%20carrier){:target="_blank"} version.

3D printable designs offer more versatility in design and printing the chain link in one piece at the expense of longer production time. [eiPionezero design](http://www.thingiverse.com/thing:666118){:target="_blank"} is one of the most advanced printable options, however it requires slow and precise printing for good results. [This design](http://www.thingiverse.com/thing:34661){:target="_blank"} is a more printable design but with less detail, but most optimal design found on thingiverse appears to be by [Claghorn](http://www.thingiverse.com/thing:611593){:target="_blank"}.


The economics of DIY cable chains depends on the application and durability required, while they are suitable for home machines, a professional chain might be a better choice and have less associated problems for more demanding applications. Using average fablab/hackspace prices for manufacturing, we can evaluate the cost DIY builds on an example of 1m energy chain. 3 mm MDF cut chain mentioned above has 33 links per meter roughly translating to 30 min of laser-cutting time and approximately 15EUR machining cost. 3D printable version mentioned above will take about 6h of 3D printing time on Troublemaker printer with 0.6 mm nozzle, which translates to about 18 EUR machining cost.

Evaluating the cost of DIY construction beyond the point of hobby use where machine amortization is not used shows that no significant savings can be made using these open-designs and low-cost options from no-name brands are an optimal choice.
