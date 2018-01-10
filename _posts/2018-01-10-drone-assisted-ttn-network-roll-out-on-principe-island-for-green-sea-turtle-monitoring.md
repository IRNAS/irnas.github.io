---
layout: post
title: "Drone assisted TTN network roll-out on Principe Island for Green Sea Turtle monitoring"
description: "We have we have developed a solution based on The Things Network infrastructure to provide a low-cost long-range network coverage in a remote part of the world for real-time monitoring and tracking of endangered green sea turtles."
category: Other Projects
tags: [IRNAS, Turtle tag, Open hardware, Conservation Technologies, Arribada Initiative, The Things Network, LoRaWAN, Drone mapping, Principe Island, Green Sea Turtle]
---
{% include JB/setup %}


Green sea turtles are an endangered species and most vulnerable during the nesting period when they converge on sandy beaches. Working with [the Arribada Initiative](http://blog.arribada.org/){:target="_blank"} and Principe trust we have designed and in past December deployed a camera based tag to capture on video the turtle’s behaviour in space and time. Understanding their swimming, feeding habits and their interaction with the environment is critical to implement informed conservation strategies. See a video from the turtles below and check this [post, published on Raspberry Pi blog](https://www.raspberrypi.org/blog/sea-turtles/){:target="_blank"}, for more details on the tagging.

[![Principe Island]({{ site.url }}/post_files/turtle-tagging/principe-island.png){: .img-half}]({{ site.url }}/post_files/turtle-tagging/principe-island.png){: .img-open}
[![Green Sea Turtle]({{ site.url }}/post_files/turtle-tagging/green-sea-turtle.png){: .img-half}]({{ site.url }}/post_files/turtle-tagging/green-sea-turtle.png){: .img-open}

<iframe width="94%" height="315" src="https://www.youtube.com/embed/OZ2aXCvQ2hk?rel=0&amp;controls=0" frameborder="0" allowfullscreen></iframe>

The challenge lies in efficiently and quickly providing a low-cost long-range network coverage in a remote part of the world for real-time monitoring and tracking. A green sea turtle is equipped with a tag when laying eggs on the beach and in about two weeks when it returns with 12-15 h of recorded video (~80 GB) the tag is removed and replaced with a fresh one. This opportunity must not be missed and thus a mechanism is required to know when the turtle comes on the beach. Moreover during the two week period turtles stay in proximity of the beach and surface every few hours to breathe, which is a perfect opportunity to send some data. Furthermore, monitoring the temperature of the sand, water level or tide on the beach and turtle nest temperature all give very valuable insight in how successful the nesting is and how environment affects it.

[LoRaWAN](https://www.thethingsnetwork.org/wiki/LoRaWAN/Home){:target="_blank"} is the most suitable solution to address the needs of this project and thus we have developed a solution based on [The Things Network](https://www.thethingsnetwork.org/){:target="_blank"} infrastructure, answering our infrastructure needs as well as providing an open access for other solutions in the area we may be deploying in the future years and for general use.

We have deployed battery back-up gateways with WiFi connectivity to test out the system requirements in real-world and to figure out the best strategy to roll-out the network. Given that internet access is limited, and building WiFi links to best gateway locations is expensive, we have discovered the best strategy is to deploy off-grid solar powered 3G connected TTN gateways that can be put on trees, float on water or be placed anywhere.

Coverage of gateways on land, remote beach areas as well as over the water on a very versatile coast is difficult to map. Therefore, we have created [a drone mapping solution](https://github.com/IRNAS/lora_drone_mapper){:target="_blank"}, coupling a DJI Drone with TTN mapper capabilities, with which we can in a matter of minutes determine the coverage of large areas of land and water, fly at canopy level if sensors are going to be deployed there as well as test placement of nodes and gateways automatically. See a video of a drone mapping test, Principe Island TTN gateway deployment and some other very interesting shots of this amazing Island. 

<iframe width="94%" height="315" src="https://www.youtube.com/embed/K-OUrnSvS4E?rel=0&amp;controls=0" frameborder="0" allowfullscreen></iframe>




