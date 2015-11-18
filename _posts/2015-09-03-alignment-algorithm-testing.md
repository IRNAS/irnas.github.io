---
layout: post
title: "KORUZA alignment algorithm - Software in Loop testing "
description: "Testing procedures for the new alignment algorithm."
category: 
tags: []
---
{% include JB/setup %}

Recently we have started with the development of a revised version of the [alignment algorithm]({{ site.url }}/2015/08/19/alignment-algorithm-revised/), designed to automatically fine-adjust pointing direction in order to optimise the link margin, either during initial alignment process or on operating link. Before implementation on the new [KORUZA 1.0 system]({{ site.url }}/2015/07/06/koruza-v10-redesign/), we performed rigorous testing of the algorithm in simulated environment in different stages, to guarantee optimal performance.

The first step was to designed a model of the KORUZA system, simulating behaviour of two operational units in Matlab environment. Then Model in Loop (MIL) based testing was used to verify that the algorithm design is functional and implementable. Simultaneous alignment of two units was performed under various conditions, such as gradual signal loss, sudden change in position of the unit and and gradual movement due to temperature variations. Basic stopping and starting conditions were developed based on the response in those situations. 

Due to satisfactory performance we proceeded to the next stage, namely Software in Loop (SIL) based testing. Software code, that is going to run on the KORUZA processor, was developed in C programming language. Same Matlab model of the KORUZA system was employed and the C code adjusted so that it could be called directly from the Matlab environment. Such approach was chosen as Matlab allows for straightforward visual representation of the alignment procedure and simple detection of problems in the algorithm structure. In particular, some adjustments in C code were made to create a mex file, detailed structure and guidelines for construction of which can be found [here](http://www.mathworks.com/help/matlab/matlab_external/introducing-mex-files.html?refresh=true). 

![alignment-algorithm]({{ site.url }}/post_files/alignment-algorithm/fig1b.jpg)
![alignment-algorithm]({{ site.url }}/post_files/alignment-algorithm/fig2b.jpg)
![alignment-algorithm]({{ site.url }}/post_files/alignment-algorithm/fig1a.jpg)
![alignment-algorithm]({{ site.url }}/post_files/alignment-algorithm/fig2a.jpg)

Alignment before and after signal was moved on both units. 



Algorithm was then tested under similar conditions as before, again showing positive results. Shortly we are planing to perform the final testing stage, where the algorithm will be implemented directly on the controller and then tested in the Matlab model environment, exploiting serial port communication. 