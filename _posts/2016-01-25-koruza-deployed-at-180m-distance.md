---
layout: post
title: "KORUZA deployed at 180m distance"
description: "This Friday we have deployed the latest KORUZA 1.0 units http://koruza.net/ at Institute Jožef Stefan, the Slovenian national research laboratory, between buildings at 180m distance, pushing KORUZA beyond the design limit. "
category: KORUZA
tags: [KORUZA, Deployment]
---
{% include JB/setup %}

This Friday we have deployed the latest [KORUZA 1.0 units](http://koruza.net/){:target="_blank"} at [Institute Jožef Stefan](https://www.ijs.si/ijsw){:target="_blank"}, the Slovenian national research laboratory, between buildings at 180m distance, pushing [KORUZA](http://koruza.net/){:target="_blank"} beyond the design limit. 


The [installation](http://instructions.koruza.net/user-manual#Koruza-Mounting){:target="_blank"} process was very straightforward, aiming the units at each other with green alignment lasers and performing the coarse alignment with the manual alignment mechanism that is a part of enclosure and requires only a metric 17 wrench. Just with that we managed to establish the optical link and only later used the motorized alignment to optimize it. 


[![koruza-lj-deployment-1]({{ site.url }}/post_files/koruza-lj-deployment/lj-deployment-1.jpg){: .img-half}]({{ site.url }}/post_files/koruza-lj-deployment/lj-deployment-1.jpg){: .img-open}
[![koruza-lj-deployment-2]({{ site.url }}/post_files/koruza-lj-deployment/lj-deployment-2.jpg){: .img-half}]({{ site.url }}/post_files/koruza-lj-deployment/lj-deployment-2.jpg){: .img-open}

[![koruza-lj-deployment-3]({{ site.url }}/post_files/koruza-lj-deployment/lj-deployment-3.jpg){: .img-half}]({{ site.url }}/post_files/koruza-lj-deployment/lj-deployment-3.jpg){: .img-open}
[![koruza-lj-deployment-3]({{ site.url }}/post_files/koruza-lj-deployment/green-laser.gif){: .img-half}]({{ site.url }}/post_files/koruza-lj-deployment/green-laser.gif){: .img-open}

The link has 20dB optical power margin. Now, we are monitoring stability and performance without the use of auto-tracking and will enable it afterwards to evaluate its benefit.

The experimental setup next to KORUZA units with TP-Link WR1043nd routers allows us to perform packet loss measurements, have a backup WiFi link for performance monitoring as well as two webcam units that will take regular snapshots to confirm failures due to fog.

[![koruza-lj-webcam-1]({{ site.url }}/post_files/koruza-lj-deployment/teslova-cam.PNG){: .img-half}]({{ site.url }}/post_files/koruza-lj-deployment/teslova-cam.PNG){: .img-open}
[![koruza-lj-webcam-2]({{ site.url }}/post_files/koruza-lj-deployment/ijs-cam.jpg){: .img-half}]({{ site.url }}/post_files/koruza-lj-deployment/ijs-cam.jpg){: .img-open}

You can see the real time performance of KORUZA link on Koruza Nodewatcher [Koruza Nodewatcher](https://nodewatcher.koruza.net/){:target="_blank"} ([ijs-1-1](https://nodewatcher.koruza.net/node/754adb9f-c79a-5e7f-865c-bad83c2954e7/){:target="_blank"} and [ijs-1-2](https://nodewatcher.koruza.net/node/e7e52a01-52f2-5e9e-8774-35b80619c999/){:target="_blank"}).