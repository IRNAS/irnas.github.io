---
layout: post
title: "Sorting out a backlash problem on our CNC mill router"
description: "This week we were sorting out problems with backlash on our CNC mill router."
category: GoodEnoughCNC
tags: [GoodEnoughCNC, CNC mill router, Backlash]
---
{% include JB/setup %}


This week we were sorting out problems with backlash on our [GoodEnoughCNC](http://goodenoughcnc.eu/){:target="_blank"} mill router. 

We were using Nema 23 stepper motors with 1:15 planetary gear reductor, which has backlash of 0,8 mm and we were unable to eliminate it with program compensation. 

We decided to replace planetary gear reductor with timing belts and series of pulleys. To successfully achieve 1:15 transmission we had to use two timing belts each having 1:4 gear ratio (combined 1:16). We've made prototype out of plywood to make sure that pulleys and belt tensioners are positioned correctly.

[![storage-room-1]({{ site.url }}/post_files/CNC-mill-router-problem/prototype.jpg){: .img-half}]({{ site.url }}/post_files/CNC-mill-router-problem/prototype.jpg){: .img-open}
[![storage-room-2]({{ site.url }}/post_files/CNC-mill-router-problem/pulley.jpg){: .img-half}]({{ site.url }}/post_files/CNC-mill-router-problem/pulley.jpg){: .img-open}

Currently we are searching for an alternative for standard aluminum pulleys. They are expensive and pulleys with 25+ teeth are hard to get locally. That's why we've made two prototypes of 45 teeth pulley: a 3D printed one and another one lasercut out of plywood. Both are awaiting further testing for durability. 


