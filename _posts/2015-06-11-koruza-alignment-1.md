---
layout: post
title: "KORUZA alignment algorithm development setup"
description: "Alignment algorithm to retain KORUZA link operation under various environmental disturbances"
category: KORUZA
tags: [Alignment algorithm, KORUZA, Development]
---
{% include JB/setup %}

Currently, we have been working on the optimisation and development of the alignment algorithm component for wireless optical system KORUZA, responsible for fine tuning the direction of the optical output and thus optimize the optical link margin between two KORUZA units in an coordinated manner. This algorithm aims to align the units after installation and then maintain (and also update) optimal position. 

The development process of the algorithm has been broken down in a three stage process, transitioning from computer simulation to implementation on the embedded controller. 

Firstly, we have developed and tested the design ideas in GNU Octave/Matlab environment, as it offers straightforward visual representation and simple implementation. In particular, we developed a behavioural model of KORUZA that simulates the relationship between motor movement in the unit and the optical received power at the opposite unit. Hereby we have assumed the optical output has Gaussian distribution, which we replace with a realistic feedback from the units at a later stage.

Once a stable algorithm design was obtained, we have implemented the algorithm in an embedded system using Energia environment and Tiva C Launchpad ARM board. The algorithm as such has them been run on the embedded system, but all the inputs and KORUZA unit behaviour fed from the GNU Octave/Matlab via serial communication as [introduced in blog]({{ site.url }}/2015/06/04/serial-octave-arduino/) . We were able to verify the correct implementation of the algorithm accounting for all errors prior to trailing it on a operational unit, where the complete system is run on the embedded processor, while returning the data to computer for performance monitoring purpose.

At this stage, algorithm has proved to be functional in some situations, where initial misalignment is minor. Future development now aims to increase the robustness of the design for all possible cases. We have experienced how vital it is to implement a reliable and stable communication between the two units for the algorithm operations between units to synchronise them and this boost motivation for development of [enhanced management link]({{ site.url }}/2015/05/20/koruza-electronics-modules/) .

[![algorithm]({{ site.url }}/downloads/KORUZA_algorithm/alignment_plan.png){: .img-full}]({{ site.url }}/downloads/KORUZA_algorithm/alignment_plan.png){: .img-open}