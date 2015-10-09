---
layout: post
title: "Data analysis for KORUZA system."
description: "Data analysis of collected measurements of KORUZA units at various locations."
category: 
tags: []
---
{% include JB/setup %}


The key component of the successful design process is evaluation of performance and determination of critical factors that may contribute to less-then optimal functionality or even system failure. To pin-point such factors, relevant for operation of KORUZA system, performance data was collected for longer time-periods on various location over the world. 
Every unit is extended with test equipment and sensors to evaluate the performance, link properties as well as observing environmental parameters. Measurements are collected at the rate of 1Hz, except the optical received power at the rate of 10Hz and can be observed in real time through [nodewatcher](https://dev.wlan-si.net/wiki/Nodewatcher) platform or examined in raw form suitable for further analysis.  

While performing analysis, we were interested in detection of events in two different time-scales; namely observation of gradual changes during longer period of time and correlation between various variables, such as link performance vs. temperature variation, and also evaluation of short term changes such as scintillation. 

As vector with sensor data is collected every 100 milliseconds, moving average filter was applied first to remove noise. Invalid data was removed in the process as well. Afterwords correlation between two units and different variables was calculated and analysed. 

Noise and other short therm effects were studied separately. We evaluated level of noise and tried to determine possible reasons for it. 

![plot]({{ site.url }}/post_files/data-analysis/fig1.jpg)
![plot]({{ site.url }}/post_files/data-analysis/noise1.jpg)

In the above plots we can see data reduction using moving average filter of power vs. time and close-up with average noise estimation. 

In the future we plan to implement real-time analysis directly on the processor in each KORUZA unit. That would allow us easier observation of the changes and possible diagnostics of system performance. 