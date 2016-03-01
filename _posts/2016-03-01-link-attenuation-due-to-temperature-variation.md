---
layout: post
title: "Link attenuation due to temperature variation "
description: "Most materials are susceptible to some amount of thermal expansion. As optical wireless system KORUZA is a high precision device, even a small change in position due to thermal expansion can cause misalignment and thus degradation of signal or even complete link loss."
category: KORUZA
tags: [KORUZA, testing, experiment, attenuation]
---
{% include JB/setup %}

Most materials are susceptible to some amount of thermal expansion. As optical wireless system [KORUZA](http://koruza.net/){:target="_blank"} is a high precision device, even a small change in position due to thermal expansion can cause misalignment and thus degradation of signal or even complete link loss. In past months, trend of cyclic change in signal power was observed in units, deployed in geographical regions associated with high daily temperature fluctuations. Below we can see an example of daily power fluctuation due to temperature variation over one week period.    

[![temperature-variation-attenuation]({{ site.url }}/post_files/temp/temp.png){: .img-full}]({{ site.url }}/post_files/temp/temp.png){: .img-open}


To design appropriate software alignment mechanism, to counter the effect of thermal expansion, the effect of change in outdoor temperature on the received power needed to be study first. Temperature variation was simulated in a [50 m indoor test tunnel setup](http://irnas.eu/test-facility){:target="_blank"}. The tunnel can be entered trough double opening located on both sides and in the middle. A several FSO links have been mounted on solid vertical poles. One side of the tunnel with the FSO units is enclosed in a chamber with small windows for the optical beams, that can be heated without affecting temperature of the free-space channel in the tunnel itself. Received power and temperature data were collected, while chamber was heated, creating up to 15&#176;C temperature variation of SFP units in time-span of few hours, resembling outdoor conditions. Once maximal desired temperature was reached, heating system was turned off and chamber was left to slowly cool down.

[![koruza-10gbps]({{ site.url }}/post_files/temp/network-tunnel.png){: .img-full}]({{ site.url }}/post_files/temp/network-tunnel.png){: .img-open}

Data analysis showed that power has significantly decreased on the non-heated unit, while heated did not experience significant change, suggesting physical movement on the heated side. In particular 15&#176;C increase in temperature of the SFP module resulted in almost 10 dB power loss. Signal was partially restored once temperature returned to its initial value, settling 4 dB below optimum. Received power on local (heated) and remote (non-heated) units for increasing and decreasing temperature in the chamber is shown below.

[![koruza-10gbps]({{ site.url }}/post_files/temp/inc-1.png){: .img-half}]({{ site.url }}/post_files/temp/inc-1.png){: .img-open}
[![koruza-10gbps]({{ site.url }}/post_files/temp/dec-1.png){: .img-half}]({{ site.url }}/post_files/temp/dec-1.png){: .img-open}


Since previous [beam analysing](http://irnas.eu/koruza/2016/02/11/koruza-beam-scan){:target="_blank"} suggested a slightly divergent beam offers much higher misalignment tolerance at cost of increased path loss and lower optical power. Indeed divergent beam performed significantly better. While initial received power was much lower, link remained stable throughout the whole process, only small degradation was detected over period of several hours as illustrated below.

[![koruza-10gbps]({{ site.url }}/post_files/temp/inc-2.png){: .img-half}]({{ site.url }}/post_files/temp/inc-2.png){: .img-open}
[![koruza-10gbps]({{ site.url }}/post_files/temp/dec-2.png){: .img-half}]({{ site.url }}/post_files/temp/dec-2.png){: .img-open}

Above results indicates that thermal expansion is one of the substantial causes of attenuation for FSO system [KORUZA](http://koruza.net/){:target="_blank"}. As seen, using slightly divergent beam is a viable option to diminish fluctuation of received optical power, however at the cost of reduced signal and link margin. Thus a fast responsive tracking algorithm could be a better option monitoring and adjusting position of the beam, without sacrificing power. 