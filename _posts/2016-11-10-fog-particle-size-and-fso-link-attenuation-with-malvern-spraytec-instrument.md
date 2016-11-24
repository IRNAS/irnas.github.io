---
layout: post
title: "Fog particle size and FSO link attenuation with Malvern Spraytec instrument"
description: "With the help of Malvern and their Spraytec system, we determined correlation between size of fog particles and FSO link attenuation."
category: KORUZA
tags: [KORUZA, Testing Tunnel, Testing, Experiment, Fog]
---
{% include JB/setup %}

We are interested in how our wireless optical system [KORUZA](http://koruza.net/){:target="_blank"} operates in various environmental conditions and to better understand the signal loss mechanisms, we are conducting scientific experiments in our domain. Free Space Optical systems use visible or near IR wavelengths to wirelessly transmit data and are thus susceptible to ambient and weather influences that may cause temporal decrease in link performance. For terrestrial systems, primarily located in urban areas, offering mid-range connections, the leading cause of attenuation is presence of aerosols such as fog, smoke or dust in the atmosphere, due to scattering and absorption of the optical beam.

We have already conducted tests on the [KORUZA 1.0](http://koruza.net/){:target="_blank"} system in an indoor set-up, closely mimicking ambient conditions in the case of fog, smoke or [both](http://irnas.eu/koruza/2016/01/20/fog-experiment-first-results){:target="_blank"}. To reduce experiment costs and avoid usage of expensive methods to produce real, water based fog, a fog-like conditions were created inside the 50 m PVC [corridor](http://irnas.eu/koruza/2015/12/21/koruza-testing-tunnel){:target="_blank"} with help of a commercial fog machine and a signal flare. 

Measurements obtained on three bidirectional links and separate measuring system for attenuation, generally agreed with the existing models, linking IR attention to visibility in the case of fog, and indicated stable performance of the link in conditions where visibility is greater than 20 m. While results looked promising and did certainly provide reassurance in reliability of the system even in adverse weather conditions, we could not compare artificially produced fog to the real one, due to lack of data and research on particles produced by commercial fog machines.  

[![fog-spraytec]({{ site.url }}/post_files/fog-spraytec/fog-spraytec-1.jpg){: .img-full}]({{ site.url }}/post_files/fog-spraytec/fog-spraytec-1.jpg){: .img-open}

Thus we were very eager when opportunity to repeat the experiment in collaboration with Malvern Instruments, using their [Spraytec laser diffraction system](http://www.malvern.com/en/products/product-range/spraytec/){:target="_blank"}. Spraytec allows real-time measurements of air suspended particles and droplets size distribution in the range of  0.1 – 2000 microns. System utilises laser diffraction by measuring the intensity of light scattered as a laser beam passes through a spray to accurately determine particle size and changes in droplet size over time. Therefore, placed in the middle of the test tunnel it can determine size of aerosols produced either by fog machine or signal flare. 

[![fog-spraytec]({{ site.url }}/post_files/fog-spraytec/fog-spraytec-2.jpg){: .img-half}]({{ site.url }}/post_files/fog-spraytec/fog-spraytec-2.jpg){: .img-open}
[![fog-spraytec]({{ site.url }}/post_files/fog-spraytec/fog-spraytec-3.jpg){: .img-half}]({{ site.url }}/post_files/fog-spraytec/fog-spraytec-3.jpg){: .img-open}

Two different fog machines were tested; [a hazer machine](http://www.antari.com/index.php/web/Products_i/25){:target="_blank"}, producing more thinly dispersed fog and a normal fog machine used for producing more intensive fog effects. In both cases fog was produced and dispersed down the tunnel using ventilation system until link on all units was completely lost. One could notice that link was much less stable using first haze machine, even in better visibility conditions. Measurements obtained with the Spraytec system agreed with the observations. Particles produced by hazer did have diameter mean of 1.161 um (Fig 1), while aerosols produced by fog machine averaged at 0.8524 um (FIG 2), where first are more comparable in size to the wavelength used (1550/1310 nm) and thus cause more attenuation. 


<div class="col-sm-6">
<a class="img-open" href="{{ site.url }}/post_files/fog-spraytec/Fog1.jpg"><img class="img-full" src="{{ site.url }}/post_files/fog-spraytec/Fog1.jpg" alt=""></a>
<p class="quiet">FIG 1</p>
</div>
<div class="col-sm-6">
<a class="img-open" href="{{ site.url }}/post_files/fog-spraytec/Fog2.jpg"><img class="img-full" src="{{ site.url }}/post_files/fog-spraytec/Fog2.jpg" alt=""></a>
<p class="quiet">FIG 2</p>
</div>
<div class="clear"></div>

With average size of fog particles being between 1 and 5 um, hazer machine also offers better simulation of natural accruing fog. Experiment was also repeated with a signal flare,  finding even smaller particles of average diameter size 0.5219 um, causing least attenuation out of thee scenarios. 

Experiment gave us valuable insight in relation between particle size and link attenuation and did also validate the suitability of artificial fog for testing. Again, we thank [Malvern Instruments](http://www.malvern.com/en/){:target="_blank"} and their team for great assistance and help. 






