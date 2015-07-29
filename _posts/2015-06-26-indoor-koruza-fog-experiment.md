---
layout: post
title: "Indoor KORUZA fog experiment "
description: "A small experiment to learn how to generate fog and evaluate impact on wireless optical systems"
category: 
tags: []
---
{% include JB/setup %}

Wireless optical also called Free-Space Optical (FSO) systems use visible or near IR wavelengths to wirelessly transmit data and are thus susceptible to ambient influences. Temporal decrease in performance can appear due to adverse weather conditions, such as fog, smoke, turbulence and heavy snow, limiting the visibility exactly as we see it with our eyes. For FSO terrestrial systems, primarily located in urban areas offering mid-range connections, the leading cause of attenuation is the presence of aerosols such as fog, smoke or dust in the atmosphere, due to scattering and absorption of the optical beam.
 
Due to unpredictable nature of weather conditions, it is hard to conduct a reliable outdoor experiment, that would allow to study relation between concentration, type of aerosols and FSO link availability. Time dependency and irregular appearance of fog, together with possible inhomogeneous distribution along the link, make it difficult to execute accurate and repeatable measurements.
 
To conduct reliable tests of the systems such as [KORUZA](http://koruza.net), we designed an indoor experiment, closely mimicking ambient conditions in the case of fog, smoke or both.
Outdoor conditions will be simulated in a 50m corridor, constructed using tables and soft clear PVC foil. A fog-like conditions will be created inside the corridor with the help of the fog machine, dry ice and also a signal flare to simulate particle smoke. Wireless optical KORUZA link should be established down the test corridor along with an independent visibility measurement system, consisting of a green laser and receiver. 

![good enough plasma]({{ site.url }}/post_files/fog-indoor/img1.jpg)

To evaluate the experiment design and consider possible issues a small scale experiment was conducted beforehand. We improvised a 14m corridor using clear PVC foil and plastic support. At both ends the corridor was left open and a pair of KORUZA units was set up together with a visibility measurement system. Fog was generated using dry ice with intention to asses its suitability and predict its behaviour in the large scale experiment.
 
The most challenging aspect of the experiment showed to be inhomogeneous production of the fog along the length of the corridor. Produced fog dissolved relatively quickly, due to summer temperatures in the building and minor drafts. Another persistent problem was maintaining the desired fog density as most of the time fog was either much denser then in worse case outdoor conditions or non-existent.

Data from the experiment was collected and analysed, where visibility and attenuation coefficients were calculated. We have been capable of generating visibility conditions in the range of 200-1000m for brief moments, however insufficient for reliable experimentation. 

For more efficient fog generation using dry ice we have developer an optimized approach compared to the common mixture of hot water and dry ice. The latter has been put into a conventional kettle modified to constantly boil the water, such that the evaporation rate was maximized. Not only the amount of fog has been increased, but the rate of dry ice evaporation has been reduced. For future experiments we have resolved to use a number of such heaters to generate fog at constant intervals along the corridor length.

![good enough plasma]({{ site.url }}/post_files/fog-indoor/img2.jpg)

![good enough plasma]({{ site.url }}/post_files/fog-indoor/img3.jpg)



