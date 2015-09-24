---
layout: post
title: "KORUZA modular electronics"
description: "Control electronics for KORUZA 1.0"
category: 
tags: []
---
{% include JB/setup %}

Wireless optical system [KORUZA](http://koruza.net) is now at final stages of optimization from the electronics perspective, finalizing the overall system. Now finally implemented [modular electronics]() approach enables optimized and versatile assembly of the system, while enabling maximal reuse for other applications.

![koruza electronics]({{ site.url }}/post_files/KORUZA-1-0/koruza_electronics.jpg)

KORUZA 1.0 electronics now consists of the following modular stack of electronics:

* RaspberryPi 2B microcomputer
* KORUZA Raspberry Pi shield (interfacing SFP optical modules, motors and distributing power)
* Passive PoE power module (providing adjustable 9V and 5V outputs from up to 36V input)
* Universal Unipolar Stepper driver (controlling motors and green laser modules) - [repository] (https://github.com/IRNAS/UniversalUnipolarStepperController)
* SFP extension plug and socket and plug (interfacing SFP modules with media converter and KORUZA Pi Shield)

Currently we are finalizing the control code and verifying correct operation prior to the release.

