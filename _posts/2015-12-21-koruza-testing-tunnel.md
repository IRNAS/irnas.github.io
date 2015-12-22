---
layout: post
title: "KORUZA test facility and fog experiment"
description: "Recently, we started the construction and development of KORUZA test facility, the first open-source testing facility, primarily applicable for conducting experimental work on free space optical (FSO) communication systems."
category: KORUZA
tags: [KORUZA, Testing Tunnel, Testing]
---
{% include JB/setup %}


Recently, we started the construction and development of [KORUZA](http://koruza.net/){:target="_blank"} test facility, the first open-source testing facility, primarily applicable for conducting experimental work on free space optical (FSO) communication systems, but also relevant for extensive analysis of any other free space systems utilising laser or other wireless, light propagating
technology.

[![tunnel]({{ site.url }}/post_files/tunnel/tunel6.JPG){: .img-half}]({{ site.url }}/post_files/tunnel/tunel6.JPG){: .img-open}
[![tunnel]({{ site.url }}/post_files/tunnel/tunel8.JPG){: .img-half}]({{ site.url }}/post_files/tunnel/tunel8.JPG){: .img-open}

The leading objective is to provide comprehensive, well rounded set of experiments and tests, sufficient to assess the performance of the FSO system in various, naturally occurring conditions. We aim to introduce alternative test methods and procedures, providing good-enough results for development purposes at affordable price and made them freely available to the research community. 

Experiments will focus on two aspects; first is the assessment and analysis of system and its components, such as signal impairment due to temperature variation, suitability of lenses with various focal lengths and prototyping of the 10Gb connection. The second one is performance evaluation under exposure to various stress factors, fog and artificially induced vibrations being one of them.

Experiments are performed in a 50m corridor, 2m high and 1m wide, constructed using clear PVC foil draped over rigid, wooden frame inside a dark hall. Up to three FSO links can be set up parallel, each of them mounted on a railing fixed in the concrete block, eliminating misalignment due to unstable mounting. The ventilation system, consisting of a fan with airflow rate of 3000 cubic meters per hour, placed at one end of the tunnel, allows for all air in the tunnel to change in under 2 minutes.

[![tunnel]({{ site.url }}/post_files/tunnel/shema.png){: .img-full}]({{ site.url }}/post_files/tunnel/shema.png){: .img-open}

So far we focused on the fog experiment where the link availability is monitored under changing atmospheric visibility. As in the previous [experiment]({{ site.url }}/koruza/2015/07/15/outdoor-koruza-fog-experiment/), fog is produce using the fog machine and then uniformly distributed down the corridor with ventilation system. Fog is monitored using  TSL2560 Light-to-Digital Ambient light sensor with SMBus interface, paired with the green laser at 532nm wavelength, measuring transmittance and consequentially visibility. Data, both from the KORUZA units and measurement sensor, is collected and monitored in real time using websocket protocol.

Conducted experiments were partially successful, some improvements are still needed. Realistic fog conditions were successfully produced, as the ventilation system allowed for uniform distribution of produced fog in relatively short time. Fog was then slowly blown away by the constant air flow. Received optical power on both units and luminous flux on the light sensor were logged the whole time. Later analysis showed expected difference in attenuation between two wavelengths, where 1550 nm unit performed significantly better than the 1310 nm one. However the light sensor in conduction with green laser did not have large enough measurement range to accurately determine visibility in heavy fog conditions. We plan to install an additional lens on the light receiver to increase active area and possibly use higher-power laser to increase initial intensity.  

[![tunnel]({{ site.url }}/post_files/tunnel/fig1.jpg){: .img-full}]({{ site.url }}/post_files/tunnel/fig1.jpg){: .img-open}

