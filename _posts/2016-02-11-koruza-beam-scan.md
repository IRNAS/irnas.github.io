---
layout: post
title: "KORUZA beam scan"
description: "The Wireless Battle of the Mesh is an event that aims to bring together people from across the globe to test the performance of different routing protocols for ad-hoc networks, like Babel, B.A.T.M.A.N, BMX, OLSR, and 802.11s."
category: KORUZA
tags: [KORUZA, beam scan, testing]
---
{% include JB/setup %}


The need for high alignment accuracy of two wireless optical system [KORUZA](http://koruza.net/){:target="_blank"} units to obtain and also maintain a viable wireless optical connection is a primary  challenge in advancement of a reliable wireless optical system. To develop efficient control system for tracking and acquisition, knowing characteristics of a NIR laser beam, i.e. its spatial energy distribution, optical path loss of the beam and receiver sensitivity to misalignment is crucial. 

To evaluate relationship between misalignment and link quality on the [KORUZA](http://koruza.net/){:target="_blank"} units, we performed a set of experiments where one unit was moved in a spiral fashion, while other remained at rest. Received optical power and position from both units was recorded. Experiment took place in the [test tunnel](http://irnas.eu/test-facility){:target="_blank"}, eliminating impact from environmental factors. 

Collected data confirmed that used IR beams are Gaussian; spatial distribution of an incident beam was determined from power readings on the moving unit. Fit to a standard 2D Gaussian distribution shows a good match, as seen on the figure below.

[![gauss-kaust-1]({{ site.url }}/post_files/beam-scan/gauss-kaust-1.png){: .img-full}]({{ site.url }}/post_files/beam-scan/gauss-kaust-1.png){: .img-open}

We also determined the effect of misalignment on both, moving and stationary unit, and calculated effect of angular movement on received power. Position of maximal power was taken for the centre, than for each movement distance from centre was determined and corresponding angle at which beam was moved calculated. For the 50 m link, angular movements of up to 0.1 deg from the optimal position should still result in functional link. 

[![power-kaust-1]({{ site.url }}/post_files/beam-scan/power-kaust-1.png){: .img-half}]({{ site.url }}/post_files/beam-scan/power-kaust-1.png){: .img-open}
[![angle-kaust-1]({{ site.url }}/post_files/beam-scan/angle-kaust-1.png){: .img-half}]({{ site.url }}/post_files/beam-scan/angle-kaust-1.png){: .img-open}

To extended the alignment margin a viable cost effective solution is using wider, slightly divergent beams, where higher path loss is a trade-off for ease of alignment and greater link stability. In the experiment otherwise collimated beam was de-focused to made wider, resulting in 7 dBu signal loss in the optimal position. As expected, functional link was maintained for increased range of motion of one unit. Tolerated angular movement increased to 0.2 deg. 

[![power-kaust-3]({{ site.url }}/post_files/beam-scan/power-kaust-3.png){: .img-half}]({{ site.url }}/post_files/beam-scan/power-kaust-3.png){: .img-open}
[![angle-kaust-3]({{ site.url }}/post_files/beam-scan/angle-kaust-3.png){: .img-half}]({{ site.url }}/post_files/beam-scan/angle-kaust-3.png){: .img-open}
