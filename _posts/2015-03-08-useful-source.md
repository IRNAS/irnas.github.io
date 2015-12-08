---
layout: post
title: "Useful-source open hardware"
description: "Introducing a new concept of open hardware."
category: Other Projects 
tags: [Useful Source, Open Source Hardware]
---
{% include JB/setup %}

Useful-source is a step beyond open-source for hardware, focusing on empowering, enabling reproduction and the use of such freely available designs by large populations. We are proposing this concept, to improve the current best practices and to make sure our developments are as useful as possible.

The motivation arises from the experience of reproducing a number of open hardware projects, with each one demanding greater then expected involvement and improvisation to make it work. This in general manifests as slow adaptation of open hardware on larger scales and preferential use of well tested and integrated closed-source systems. Open hardware must thus become better in all aspects and offer the end users something more. In the open source software world these problems are not as significant, because there are many projects like for example Ubuntu, creating stable releases by integrating community developed modules and applying testing and documentation efforts to them. Additionally we can in an oversimplified manner claim that the compilation process in software is a repeatable and reproducible process, while in small batch hardware production the compilation process occurs through human interaction with assembly parts. Thus we propose the following approach:

Useful-source is the knowledge & documentation bridge between an open hardware project presentation & description and the source files, aiming to empower anyone reproducing the design with all the information to make educated choices and understanding the reasoning and interaction between assembly parts.

Useful-source goals:

 * Complies with [Open Hardware Definition](http://www.oshwa.org/definition/).
 * Present the system in a tree-like manner, starting from one page system overview and breaking it down into simple modules, with enough information one can understand the basics of how it works. 
 * Assembly instructions with clearly defined steps and assembly instructions, extended with basic description what the part does. The function of every assembly part must be clearly expressed so one can consider alternatives.
 * Parts for assembling the system are split into logical and physical parts. The system is assembled of logical parts and every logical part has one or more suitable physical parts associated. For example, two pieces of wood with a hole should be joined with a screw, that fits through the hole, is longer then X and shorter then Y... The physical part associated would be then M8x16, countersunk and HEX head.
 * Off-line useful format, we suggest XML. Displayed with a stylesheet on any browser and suitable for modifications through version control repositories.
 
Useful-source from user perspective:

 * Seamless process from learning about a project to reproducing it
 * Reliable and tested sources and documentation
 * Reproducible with open-source tool-set
 * Simple contribution to documentation and translatable to local languages
 
We are currently in the process of trailing this approach with KORUZA and our other projects, but it builds towards the greater goal of [open hardware workflows and standards](http://opensourceecology.org/open-source-hardware-development-method/) with a work team initiated by [Open Source Ecology](http://opensourceecology.org/).
 
 