---
layout: post
title: "KORUZA alignment algorithm"
description: "We implemented the alignment algorithm, responsible for automated fine tuning of units in order to maintain optimal connection."
category: KORUZA
tags: [KORUZA, Alignment Algorithm]
---
{% include JB/setup %}



With the [KORUZA system](http://koruza.net/){:target="_blank"} being available for order as [a DIY kit or a fully assembled pair of units](http://fabrikor.eu/Koruza){:target="_blank"}, we have been working on improving the user experience by witting well formed set of [instructions](http://instructions.koruza.net/){:target="_blank"} equipped with graphical material, upgrading the [KORUZA interface](https://github.com/IRNAS/koruza-pi){:target="_blank"} for easier real-time monitoring of units and also implementing the alignment algorithm, responsible for automated fine tuning of units in order to maintain optimal connection.

[![KORUZA-alignment-algorithm-1]({{ site.url }}/post_files/koruza-alignment-algorithm/align1.png){: .img-full}]({{ site.url }}/post_files/koruza-alignment-algorithm/align1.png){: .img-open}

[![KORUZA-alignment-algorithm-2]({{ site.url }}/post_files/koruza-alignment-algorithm/align2.png){: .img-full}]({{ site.url }}/post_files/koruza-alignment-algorithm/align2.png){: .img-open}

[![KORUZA-alignment-algorithm-2]({{ site.url }}/post_files/koruza-alignment-algorithm/align3.png){: .img-full}]({{ site.url }}/post_files/koruza-alignment-algorithm/align3.png){: .img-open}

We identified two main use-cases for the algorithm: as a tool for automated initial alignment where two units are simultaneously aligned in coordinated manner, with no or little optical power detected in the beginning and also as aid for maintaining optimal connection, which may degrade over time due to various environmental factors, such as thermal expansion or various weather conditions. Algorithm structure is very similar to the previous [version]({{ site.url }}/koruza/2015/08/19/alignment-algorithm-revised){:target="_blank"}, already tested in simulated environment. Received power from both units is taken into account when determining optimal position. Additionally, alternating movement of units is employed to optimize the alignment process.


The progress of the alignment can be monitored via [KORUZA interface](https://github.com/IRNAS/koruza-pi){:target="_blank"}, where one can run and stop the alignment at any point and possibly combine it with manual movements. So far units have been successfully aligned in the case of initial misalignment. To asses performance in the case of gradual degradation of signal or misalignment due to environmental factors and potentially improve the algorithm, we are planing extensive tests in our [tunnel]({{ site.url }}/koruza/2015/12/21/koruza-testing-tunnel){:target="_blank"} and on other outdoor links for a longer period of time. 


