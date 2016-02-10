---
layout: post
title: "Outdoor KORUZA fog experiment "
description: "A larger experiment to learn how to generate fog and evaluate impact on wireless optical systems at 50m length"
category: KORUZA
tags: [KORUZA, Fog, Experiment]
---
{% include JB/setup %}

We have [proposed and prototyped]({{ site.url }}/koruza/2015/06/26/indoor-koruza-fog-experiment){target="_blank"} an artificial fog experiment to evaluate its impact on wireless optical system [KORUZA](http://koruza.net){target="_blank"}, more specifically the correlation between the presence of aerosol particles in the atmosphere on wireless optical link performance. Unfortunately, no relevant data could be collected due to numerous obstacles faced during the experiment, nevertheless we gained very valuable experience about the system performance under challenging conditions and rethought the experiment design. 

As planned we set up a 50m long outdoor tunnel, using tables and clear PVC foil as shown below. Corridor proved to be easy to assemble, while still creating satisfactory conditions for the experiment.

The first problem appeared when we attempted to establish two wireless optical KORUZA links down the corridor. Alignment process proved to be very difficult, even though we performed 
collimation and calibration processes previous day on both unit pairs. Strong summer sunlight prevented us from seeing the alignment green laser and performing the initial system calibration. The green dot became almost invisible after approximately 25m, making the initial alignment challenging. Reflective property of the PVC foil, used to build the corridor, proved to be problematic as well, since few times the wireless optical link was established through an reflection. As such this is an interesting fact and may be explored for some applications.

High temperatures, of more than 35 degrees Celsius outside and up to 55 degrees in the corridor, also took a toll on the system performance. Even when we managed to establish the link,
it fluctuated significantly, either due to thermal expansion of the units or significant turbulences established in the tunnel, performing much like a chimney.

Another significant problem was the design of the optical visibility measurement system. Initial design predicted the use of four green lasers and photo-detectors, that would determine 
visibility at 5m, 20m, 35m and 50m, in order to control fog homogeneity and general visibility conditions in the corridor. However, as green lasers used were exposed to the high temperatures, they could not be detected or even aligned with the sensors more than 5m away. After few hours, most of them stopped working altogether. Photo-detectors proved to be problematic as well since the background sunlight completely overpowered laser luminance and saturated the receiver. Thus, the designed measurement system did not perform well in given circumstances, even though it was successfully tested beforehand in the small scale indoor experiment.   

On the positive note, fog production in the corridor proved to be very efficient, especially when the fog machine and signal flare were used. A single large fan, 
placed at the beginning of the tunnel, managed to produce a stable air flow down the entire corridor and the produced fog could be evenly distributed. Uniform distribution could not be 
achieved with dry ice, also produced fog was too dense to resemble any possible real fog scenarios. On the other hand the artificial fog produced by the fog machine appeared 
very realistic and uniform. Naked eye assessment and video analysis suggests visibility in the range 10m-1000m can be achieved without any problems. 

Due to numerous obstacles faced during the experiment only power data from the KORUZA units was recorded, which due to the link instability can not be used to correctly indicate 
the relationship between visibility and the link performance. Therefore the experiment should be redesigned and repeated. The following changes could potentially 
improve the performance and reliability of the experiment:

1. The experiment should be conducted inside, possibly in relative darkens or at least without presence of direct sunlight, to allow for easier alignment of units and prevent photodetector saturation of the visibility measurement system. Smaller temperature fluctuations are expected in such environment and thus more stable links. 

1. KORUZA link should be established before the tunnel is constructed, as the alignment process proved to be the most challenging part 
of the experiment, not just due to the low visibility of the green laser in the sunlight, but also due to limited space inside the tunnel itself.  

1. Visibility measurement systems should be redesigned; better quality green lasers should be used to allow for measurements down the length of the whole tunnel. Photo-detectors 
need to be changed as well, either better quality detectors should be used or a filter, permitting only 550nm wavelength, should be installed in front of the detector. 
As the experiment will be conducted in at least semi-darkness, the surrounding light is not expected to saturate detectors and could be taken into the account during the 
calibration of the system. 

1. Only the fog machine will be used for fog production, as the dry ice proved to produce very inhomogeneous, dens fog with relatively low staying power, that is hard to spread
even with the otherwise effective ventilation system. Fog machine on the other hand produced very real-like fog of proper density. 

We are actively working on improving the experimental setup and will be repeating it shortly.

[![fog]({{ site.url }}/post_files/fog-outdoor/exp1.JPG){: .img-half}]({{ site.url }}/post_files/fog-outdoor/exp1.JPG){: .img-open}
[![fog]({{ site.url }}/post_files/fog-outdoor/exp2.jpg){: .img-half}]({{ site.url }}/post_files/fog-outdoor/exp2.jpg){: .img-open}

[![fog]({{ site.url }}/post_files/fog-outdoor/tunel.jpg){: .img-half}]({{ site.url }}/post_files/fog-outdoor/tunel.jpg){: .img-open}
[![fog]({{ site.url }}/post_files/fog-outdoor/fog_test.jpg){: .img-half}]({{ site.url }}/post_files/fog-outdoor/fog_test.jpg){: .img-open}

[![fog]({{ site.url }}/post_files/fog-outdoor/fog_animated.gif){: .img-full}]({{ site.url }}/post_files/fog-outdoor/fog_animated.gif){: .img-open}

