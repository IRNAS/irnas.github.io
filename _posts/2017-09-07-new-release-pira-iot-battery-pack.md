---
layout: post
title: "New Release – PiRA IoT Battery Pack"
description: "We’re announcing a new open hardware release,  PiRA, a universal, modular IoT battery pack, developed as a response to the lack of IoT suitable battery pack or powerbank systems that can be easily and rapidly integrated into target applications."
category: Other Projects
tags: [IRNAS, Fabrikor, IoT, Iot device, Battery pack, PiRA, Solar powered IoT ]
---
{% include JB/setup %}

We’re announcing a new open hardware release, [PiRA](http://irnas.eu/pira){:target="_blank"}, a universal, modular IoT battery pack, developed as a response to the lack of IoT suitable battery pack or powerbank systems that can be easily and rapidly integrated into target applications, designed to reduce the development time and costs of bringing IoT devices from idea to functional prototypes creating a cost and convenience benefit for developers and manufacturers of IoT systems. 

**This solution is handling all commonly required features:**

- charging,
- battery monitoring, 
- voltage regulation, 
- power scheduling, 
- battery protection, 
- standard LiPo cell usage, 
- optional on board processor. 

Due to the modular structure one can either use this as a set of modules to be included in the target application or simply pack a mother board with a number of modules required for a particular system.

[![pira-iot-battery-pack]({{ site.url }}/images/pira/modular-iot-battery-pack.png){: .img-full}]({{ site.url }}/images/pira/modular-iot-battery-pack.png){: .img-open} 

[PiRA is available as prototyping kit](http://fabrikor.eu/all-products/pira-power-in-responsive-applications-iot-battery-pack){:target="_blank"} with all functions implemented on the general purpose motherboard and with the full-featured setup.

<h3>Why PiRA?</h3>

At Institute IRNAS we work with a range of leading experts in various field and are constantly challenged to develop customized solutions in short periods of time. PiRA has been designed as a solution for ourselves, based on the integrated version we developed for [Safecast Solarcast sensor device](http://irnas.eu/other%20projects/2017/05/08/collaborating-with-safecast-development-and-fabrication-of-solarcast){:target="_blank"}, but has since grown into a more widely useful system that is by following best open hardware practices enhanced and expanded with every project.

Development time and costs are significantly reduced by using this tested and constantly improved open hardware design, allowing for idea to prototype batch time to be under a month. PiRA thus enables everyone to be very responsive to the needs and quickly implement an optimized and verified solution.

<h3>For whom?</h3>

PiRA enables almost anyone to build a robust standalone battery powered IoT system. We envision its usage in a number of ways:

1. Prototype development and test batch construction (0-10 units): Combine existing modules on one of the existing motherboard designs to best suit the required application and complete the design in minimal time.

2. Application specific mainboard (20-100 units): Use existing modules on a custom developed motherboard for the particular situation to best integrate a proven solution for your application.

3. Fully integrated solution (100+ units): Use the existing open hardware design to create an unified circuit board with the features combined in application specific setup. 

At Institute IRNAS and Fabrikor we provide development of all these types of solutions and their manufacturing. We invite you to [get in contact](http://fabrikor.eu/index.php?route=information/contact){:target="_blank"} for more information.

<h3>PiRA Modules</h3>

PiRA is typically used with multiple LiPo battery cells in parallel in 1SxP configuration, generally with 1-12 battery cells. Such configuration simplifies the battery management and charging and enables the installed capacity to vary from device to device. Multiple Charging modules can be used in parallel to charge the battery, creating anything from solar-only solution to solar-backed uninterruptible power supply for most critical applications.

Find out more about the available modules, which can be combined on the motherboard in a number of ways on [PiRA presentation webpage](http://irnas.eu/pira){:target="_blank"}.

[![pira-iot-battery-pack]({{ site.url }}/images/pira/pira-5.jpg){: .img-half}]({{ site.url }}/images/pira/pira-5.jpg){: .img-open}
[![pira-iot-battery-pack]({{ site.url }}/images/pira/pira-12.jpg){: .img-half}]({{ site.url }}/images/pira/pira-12.jpg){: .img-open} 

<h3>Applications</h3>

**1. Low-power system with high-current intermittent loads**

Many IoT devices operate in very low power regimes for majority of the time, while intermittently requiring significant amounts of power, such when using 2G or 3G module modems, power hungry sensors or actuators. This requires a low standby power consumption, which is under 100 uA of total battery drain with active 3.3 V output in PiRA and up to 10 A current delivery to the load through MOSFET controlled output module.

**Use case: Solarcast**

PiRA v1 is used in [Safecast Solarcast devices](http://irnas.eu/other%20projects/2017/05/08/collaborating-with-safecast-development-and-fabrication-of-solarcast){:target="_blank"} as a standalone module that is dropped in with batteries included. Solarcast main board has been significantly simplified as only the application specific features were implemented, regulated voltage outputs and power switching is provided by PiRA.

[![pira-iot-battery-pack]({{ site.url }}/images/pira/solarcast-pira.jpg){: .img-full}]({{ site.url }}/images/pira/solarcast-pira.jpg){: .img-open}

**2. Scheduling power hungry devices**

Using RaspberryPi microcomputer and WiFi router is due to their cost-effective and widely supported range of features becoming more significant in industrial sensing applications. Due to the power constraints in off-grid deployments however powering these devices can represent a challenge. PiRA with a processor installed enables smart scheduling of these loads based on voltage levels, external sensors or other inputs and can significantly prolong the battery life.

**Use case: AAMP**

PiRA v2 is used in [AAMP camera devices](https://github.com/IRNAS/arribada-amp){:target="_blank"} for off-grid solar operation in the jungle. Based on ambient light, PIR sensor and other inputs it calculates when Raspberry Pi with a camera should be turned on and then in regular intervals powers up a 5GHz long-range WiFi router to upload the captured information. PiRA processor used in this application is ESP8266 with built-in WiFi and using ESPEasy firmware one can simply configure the scheduling through a web interface in a matter of minutes and deploy the application as well as optimize it on-site or remotely.

The modular design of the system is very crucial for this particular deployment, because every feature is a standalone module, one can in a matter of seconds replace them and service any potential problems in the field, recombine modules for a new application or re-use them if new motherboards are developed for a different application.

[![pira-iot-battery-pack]({{ site.url }}/images/pira/pira-3.jpg){: .img-full}]({{ site.url }}/images/pira/pira-3.jpg){: .img-open}

<h3>Development costs and history</h3>

PiRA IoT battery pack has been first designed for use with Safecast Solarcast device[](){:target="_blank"} in January 2017 and version 1 built-in 30 Solarcast devices now deployed around the globe. Following the success of the design, version 2 has been designed for use with AAMP project now being deployed in Peruvian Amazonian forest. The development, testing and prototyping cost up to this point is about 20000 EUR that has been funded by Ray Ozzie, [Safecast](https://blog.safecast.org/){:target="_blank"}, [Arribada Initiative](http://blog.arribada.org/){:target="_blank"} and Institute IRNAS, all great open source open hardware supporters and organizations. Through sales of device and integration services we wish to recover these costs and contribute them back to these projects for more awesome open hardware. 

You can order PiRA at [fabrikor.eu](http://fabrikor.eu/all-products/pira-power-in-responsive-applications-iot-battery-pack){:target="_blank"} and find out more about the design on [Github](https://github.com/IRNAS/IoT-battery-pack){:target="_blank"}. If you require additional help bringing your idea for an IoT device to a functional prototype we can [help you out](http://fabrikor.eu/s-iot){:target="_blank"}, we invite you to let us know about your requirements and we’ll do our best to find the most suitable solution for you. 






