---
layout: post
title: "Motor performance test"
description: "Procedure for testing motor performance, using camera and video analysis."
category: 
tags: []
---
{% include JB/setup %}

With the design of the new [generation 1.0]({{ site.url }}/2015/08/05/koruza-1-0/) KORUZA being finalised, we have started with testing of various system components to objectively evaluate design changes and performance. As we are planning to implement the new [alignment algorithm]({{ site.url }}/2015/09/03/alignment-algorithm-testing/) on units in near future, testing of the motor performance, responsible for subtle changes in the pointing direction, needs to be performed. 

In particular, we want to evaluate motor responsiveness and accuracy of movements over time. Moreover, effect of divers external conditions such as temperature fluctuation and humidity, needs to be analysed. 
Since IR beam is invisible to the human eye and even hard to detect in daylight using phosphor coating NIR detection card, the green laser, serving as an visual alignment add, can be observed instead. Both laser beams are made parallel during the initial calibration procedure, thus tracking the green laser instead of IR beam offers equivalent results.  

Laser is pointed to the flat, monochrome surface, where the green dot is monitored by camera. Each captured frame is filtered to remove noise and merge areas with similar luminosity. Image is then segmented based on the set tolerance, which varies with lightning conditions. Dot couture is identified by analysing the contrast in brightness. Assuming uniform, circular shape of the pointing laser dot, centre is identified as a midpoint of the circular approximation to the contour. 
Procedure is repeated for each frame to enable tracking of the centre coordinates over time. 

So far tests suggest promising behaviour. Recurrent motion of the laser in small squares was observed over period of time at various distances. Analysis showed that movement path remains unchanged over the time period  at all distances and even more importantly, laser always returns to the same starting position, a very important aspect in the alignment procedure, where the beam needs to return to the optimal position after each iteration. 

![dot]({{ site.url }}/post_files/video/img1.jpg)

In the above plot we can see square movement over 15 min period at 1 m distance. We are planing to repeat tracking tests at various distances in more controlled environment. More changeling movements will be analysed as well (greater speed, diagonal movement, etc.). 