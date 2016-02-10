---
layout: post
title: "Fog experiment - first results"
description: "In the past month we conducted several fog experiments, testing performance of the KORUZA Free Space Optical system under low visibility conditions in our open source test facility."
category: KORUZA
tags: [KORUZA, Testing Tunnel, Testing, Experiment]
---
{% include JB/setup %}


In the past month we conducted several fog experiments, testing performance of the KORUZA Free Space Optical system under low visibility conditions in our open source [test facility](http://irnas.eu/test-facility.html){:target="_blank"}. The main setup remained the [same](http://irnas.eu/koruza/2015/12/21/koruza-testing-tunnel){:target="_blank"}, thus fog was produced using glycol-based theatre fog machines and dispersed down the 50m tunnel using two fans. Due to insufficient measurement range the measuring system, consisting of TSL2561 Light-to-Digital Ambient light sensor with an I2C interface and green laser at 532nm wavelength, was upgraded using lens to focus the green laser beam on receiver active area and hence increase measurement range. Three such measuring systems were used; one along the whole length of the tunnel and two additional, covering half of the range to ensure homogeneous distribution of fog. 

Data from four optical links was simultaneously collected and then analysed, calculating attenuation coefficient, measured in dB/km, for given visibility in km, obtained from sensor data. To validate credibility of experimental setup, especially fog production method, we compared data to some known attenuation models, predicting level of attenuation for given visibility and wavelength. While measured data followed the general trend of predicted models (see comparison to Kruse and Ijaz models and read more about them [here](https://www.researchgate.net/publication/236161987_Modeling_of_Fog_and_Smoke_Attenuation_in_Free_Space_Optical_Communications_Link_Under_Controlled_Laboratory_Conditions){:target="_blank"}, we did not find a close match. In particular, measured attenuation difference between wavelengths was much larger than suggested by models. 


[![fit-kruse.png]({{ site.url }}/post_files/fog/fit-kruse.png){: .img-full}]({{ site.url }}/post_files/fog/fit-kruse.png){: .img-open}
[![fit-ijaz-fog]({{ site.url }}/post_files/fog/fit-ijaz-fog.png){: .img-full}]({{ site.url }}/post_files/fog/fit-ijaz-fog.png){: .img-open}

However we found similarity to the attenuation model in case of smoke (see comparison between measurements and Ijaz model for smoke attenuation below), suggesting produced glycol fog posses similar properties than smoke. 

[![fit-ijaz-smoke]({{ site.url }}/post_files/fog/fit-ijaz-smoke.png){: .img-full}]({{ site.url }}/post_files/fog/fit-ijaz-smoke.png){: .img-open}

The assumption was confirmed, as data collected in experiment using signal flares to create smoke, matched data obtained in the fog-machine experiment. Data was fitted to predicted model; best custom fit was achieved when region of dens fog with visibility less than 150m and region of moderate fog with visibility between 0.15 and 0.75km were treated separately. 

[![fit-model-combined]({{ site.url }}/post_files/fog/fit-model-combined.png){: .img-full}]({{ site.url }}/post_files/fog/fit-model-combined.png){: .img-open}
[![fit-model-combined-2]({{ site.url }}/post_files/fog/fit-model-combined-2.png){: .img-full}]({{ site.url }}/post_files/fog/fit-model-combined-2.png){: .img-open}

Although we found that glycol-based fog used in experiment does not have same optical properties as natural fog, obtained results so far suggest KORUZA system is not very sensitive to lower visibility conditions as in the case of very low visibility around 25m a 50m link was still operational with around 300 dB/km attenuation. Also, predicted difference between wavelengths was evident, with higher wavelengths (1550nm and 1490nm) performing significantly better. To evaluate KORUZA performance in the case of fog an alternative method for creating artificial fog is needed; we plan to repeat the experiment using dry ice to generate fog in the near future. 
