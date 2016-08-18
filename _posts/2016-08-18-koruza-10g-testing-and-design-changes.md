---
layout: post
title: "KORUZA 10 G testing and design changes"
description: "KORUZA 1.0 10 G version enables across-the street connectivity at 10 Gbps rates, however connecting at these rates is somewhat more challenging or typically expensive. We have devised a low-cost setup for testing it and demonstrated some connectivity options."
category: KORUZA
tags: [KORUZA, 10Gbps, testing]
---
{% include JB/setup %}


[KORUZA 1.0](http://koruza.net/){:target="_blank"} 10 G version enables across-the street connectivity at 10 Gbps rates, however connecting at these rates is somewhat more challenging or typically expensive. We have devised a low-cost setup for testing it and demonstrated some connectivity options.

The key difference between KORUZA 1 G and 10 G versions is the network port configuration, both having one 100 Mbps ethernet port with PoE for powering and management and 1 Gbps ethernet port or SFP socket respectively. Connecting to 10 G unit can thus be done either with SFP modules and fiber optical cable or using SFP-SFP direct attach cables at short distances. They come in two options, passive and active, the difference only being in their maximal length. Based on our experience passive direct attach cables are a better option if feasible at the desired distance.

Testing a 10 Gbps network link at low-cost is rather challenging since even low-cost devices such as [Mikrotik CRS210-8G-2S+IN](http://routerboard.com/CRS210-8G-2SplusIN){:target="_blank"} featuring two 10 G ports can not generate 10 Gbps of real data. The link can be established at that speed, however routing and packet generation are limited to lower speeds. For example using the Mikrotik Bandwidth test on this device will produce a traffic peak of about 450 Mbps. This may be sufficient for studying packet loss over a 10 G link, however noting that the true BER can not be determined this way. It is important to note as well that some packet loss may be generated in the routers itself if we try to push too much data, especially when using UDP modes.

To test packet loss via KORUZA optical link we have developed two options. One based on openwrt and TP-Link WDR4300ND routers using [neatmeasured](https://github.com/wlanslovenija/netmeasured){:target="_blank"} utility to measure packet loss at a millisecond interval rate. The [second option](https://github.com/IRNAS/KORUZA-testing/blob/master/packet_loss_testing/README.md){:target="_blank"} is using Mikrotik CRS210-8G-2S+IN device with 10 G ports and testing packet loss or throughput at about 100 ms intervals.

[![koruza-10g-diagram]({{ site.url }}/post_files/koruza-10g/koruza-10g-diagram.png){: .img-full}]({{ site.url }}/post_files/koruza-10g/koruza-10g-diagram.png){: .img-open}
[![koruza-10gb-test-setup]({{ site.url }}/post_files/koruza-10g/koruza-10gb-test-setup.JPG){: .img-full}]({{ site.url }}/post_files/koruza-10g/koruza-10gb-test-setup.JPG){: .img-open}

Due to the design of KORUZA and SFP modules themselves with a hysteresis link disable threshold, we can observe the module breaking the communication prior to any significant packet loss appearing on the link, such that it does not operate in the lossy range.

A key hardware improvement required for 10 G operation was removing the media converter and creating a SFP back to back extension circuit. The 1 G version is using a SATA cable which suffices at that speed, however for 10 Gbps a better solution was required. Thus a 10 G SFP socket board has been designed using coaxial cables for high speed connection. In this configuration operation up to 40 Gbps should be supported.

[![10g-hardware-improvement]({{ site.url }}/post_files/koruza-10g/10g-improvement.jpg){: .img-full}]({{ site.url }}/post_files/koruza-10g/10g-improvement.jpg){: .img-open}
