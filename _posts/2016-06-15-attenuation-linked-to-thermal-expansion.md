---
layout: post
title: "Attenuation linked to thermal expansion"
description: "We analysed data obtained in past months from our wireless optical test network KORUZA, to determine relationship between temperature and link attenuation."
category: KORUZA
tags: [KORUZA, Testing, Experiment, Attenuation]
---
{% include JB/setup %}

In the last few months our [wireless optical test network KORUZA](http://koruza.net/deployments/){:target="_blank"} has been contentiously expanding and thus providing us with suitable environment for testing the performance and reliability of KORUZA system. 

As evidenced by link analysis in the [past](http://irnas.eu/koruza/2016/03/01/link-attenuation-due-to-temperature-variation){:target="_blank"}, significant misalignment and signal attenuation can be attributed to the thermal expansion. Cyclical change in signal power was observed in units, deployed in geographical regions associated with high daily temperature fluctuations. Newly collected data from past months confirms such assumption. 
Displayed below is monthly data collected from deployment in Point Arena, California, illustrating daily correlation between the temperature measured inside the unit (due to great similarity temperature data for just one unit is plotted), and received optical power on both units. 

[![point-arena.png]({{ site.url }}/post_files/temp/point-arena.png){: .img-full}]({{ site.url }}/post_files/temp/point-arena.png){: .img-open}

While attenuation is clearly linked to the temperature variation, it is hard to determine to what extend. A link in Slovenia, connecting center Tkalka with educational center Academia, deployed as a part of wlan slovenia network in Maribor, Slovenia, did provide some insight on the matter due to its particular mounting location; while one unit is mounted on the rooftop with direct exposure to all environmental factors, direct sunlight in particular, other one is shield by a roof shelter and thus experiencing much lover daily temperature fluctuations. 

[![tkalka-unit.jpg]({{ site.url }}/post_files/temp/tkalka-unit.jpg){: .img-half}]({{ site.url }}/post_files/temp/tkalka-unit.jpg){: .img-open}
[![academia-unit.JPG]({{ site.url }}/post_files/temp/academia-unit.JPG){: .img-half}]({{ site.url }}/post_files/temp/academia-unit.JPG){: .img-open}

Figure below illustrates correlation between received power and internal temperature of  units. Unit 2, mounted under the roof, has experienced more consistent temperature with only few degrees between night and daily average. Consequently data indicates more steady reception of optical power on Unit 1. The opposite trend can be observed on Unit 2, receiving power from Unit 1, which was subject to more prominent temperature variation.  

[![tkalka.png]({{ site.url }}/post_files/temp/tkalka.png){: .img-full}]({{ site.url }}/post_files/temp/tkalka.png){: .img-open}

Data suggests internal misalignment of the transmitter/receiver (same module in KORUZA) probably subject to thermal extension. As expected, effect of misalignment is more prominent on receiving unit due to change in optical beam angle, amplified by the distance between units, while reception on transmitting unit, undergoing misalignment, remains mostly unaffected. We are actively testing and developing auto-tracking algorithms currently to adjust for these problems and compensate over a longer period of time.