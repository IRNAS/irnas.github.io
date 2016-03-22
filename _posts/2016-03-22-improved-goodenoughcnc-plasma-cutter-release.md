---
layout: post
title: "Improved GoodEnoughCNC Plasma cutter release"
description: "The latest version of our GoodEnoughCNC Plasma, with the improved design of Z-axis construction, has been released."
category: GoodEnoughCNC
tags: [CNC, GoodEnoughCNC, Plasma, Plasma cutter, Open Source Hardware]
---
{% include JB/setup %}


The latest version of our [GoodEnoughCNC Plasma](http://goodenoughcnc.eu/machines/#plasma){:target="_blank"}, with the improved design of Z-axis construction, has been released. The mechanism of the previous Z-axis consisted of drawer guides, which was causing quiet some problems. The drawer guides have been jamming during the CNC operation because the heat from plasma caused problems with the plastic retainers in the guides. Consequently there were loss in steps.

The new Z axis movement mechanism consists of two round metal rods that are rigidly inserted in X shape aluminium profiles. These round rods are sliding on bearings that are positioned on four M8 bolts. The positions of those carrier bolts can be slightly moved. The height is regulated with M8 rod which is connected to the motor shaft. The M8 rod runs trough standard M8 hex nut which is inserted in the housing that is connected to the main metal plate. The whole Z-axis construction is now a lot simpler, easier to build, more robust and cheaper. With the new Z-axis we can simply change plasma cutter with the mill, with which we can cut smaller wooden panels.

[![goodenoughcnc-plasma-cutter-1]({{ site.url }}/post_files/plasma/plasma.jpg){: .img-half}]({{ site.url }}/post_files/plasma/plasma.jpg){: .img-open}
[![goodenoughcnc-plasma-cutter-2]({{ site.url }}/post_files/plasma/z-axis.jpg){: .img-half}]({{ site.url }}/post_files/plasma/z-axis.jpg){: .img-open}

We have also successfully used our new [ToslinkCNC](http://irnas.eu/goodenoughcnc/2016/03/10/toslink-cnc){:target="_blank"} control system for operating [GoodEnoughCNC Plasma](http://goodenoughcnc.eu/machines/#plasma){:target="_blank"}. The optical signal travels from the transmitter to the receiver on the Y1 axis. From there it goes to the Y2 axis and the X axis. The signal chain continues from the X axis to the Z axis and return link goes from the Z axis back directly to the transmitter. All the necessary cables are now situated in power chain which has been added along X axis.

Check the video of our [GoodEnoughCNC Plasma](http://goodenoughcnc.eu/machines/#plasma){:target="_blank"} in action, where we used it to make the trolley parts for our [Large Mill](http://goodenoughcnc.eu/machines/#large-mill){:target="_blank"}.

<iframe width="95%" height="400px" style="margin-bottom:10px" src="https://www.youtube.com/embed/D9Y70XkeLIY" frameborder="0" allowfullscreen></iframe>

You can check source documentation for this project on [Github](https://github.com/IRNAS/GoodEnoughCNC-PlasmaCutter){:target="_blank"}. We'll also have the updated assembly instructions ready in the next couple of weeks. Stay tuned!




