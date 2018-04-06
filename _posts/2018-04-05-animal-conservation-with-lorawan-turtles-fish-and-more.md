---
layout: post
title: "Animal Conservation with LoraWAN - turtles, fish and more"
category: Other Projects
tags: [IRNAS, Open hardware, Conservation, Animals Conservation, Arribada Initiative, ]
---
{% include JB/setup %}

[](){:target="_blank"}

Understanding the animal behavior, changes in the natural environment and effects of climate change on our ecosystems can be efficiently observed with the latest digital technologies and IoT devices. Over the past year we have been working in partnership with [the Arribada Initiative](http://blog.arribada.org/){:target="_blank"} to develop future-proof systems to empower researchers and conservation specialists to observe and measure effects in the natural environment and suggest policy changes to best preserve it.

[![peru]({{ site.url }}/images/conservation-tech/peru.jpg){: .img-half}]({{ site.url }}/images/conservation-tech/peru.jpg){: .img-open}
[![fmp]({{ site.url }}/images/conservation-tech/fmp.jpg){: .img-half}]({{ site.url }}/images/conservation-tech/fmp.jpg){: .img-open}

[![antarctica-apmp]({{ site.url }}/images/conservation-tech/antarctica-apmp-1.jpg){: .img-half}]({{ site.url }}/images/conservation-tech/antarctica-apmp-1.jpg){: .img-open}
[![pitstop]({{ site.url }}/images/conservation-tech/pitstop.jpg){: .img-half}]({{ site.url }}/images/conservation-tech/pitstop.jpg){: .img-open}
<div class="quiet">Copyright: The Arribada Initiative</div>

In the past months we have piloted new solutions in various environments, the [Arribada Arboreal Monitoring Platform](http://irnas.eu/other%20projects/2017/08/21/arboreal-monitoring-platform-for-amazon-rainforest){:target="_blank"} in Manu, Peru in tropical rainforest to monitor the wildlife passing through the canopies of the trees, the Arribada Fresh Monitoring Platform designed to measure the water level in a river and take periodic images of the area, the Arribada Penguin Monitoring Platform, rugged solar-powered camera unit providing year-round periodic snapshots of the surrounding area with edge-processing capabilities, monitoring annual penguin migration and nesting and exposing global warming effects and changes to the environment and the [PitStop Turtle tag](http://irnas.eu/other%20projects/2018/01/10/drone-assisted-ttn-network-roll-out-on-principe-island-for-green-sea-turtle-monitoring-Copy){:target="_blank"} to capture video on nesting green sea turtles, to best understand their behavior and feeding habits.

Future-proof hardware we have designed is common in these applications, tackling the key challenges in communication, power management and ease of development for the custom solution required in all of these environments. The core of each device is [PiRa power management system](http://irnas.eu/pira){:target="_blank"} and [Raspberry Pi Zero W](https://www.raspberrypi.org/products/raspberry-pi-zero-w/){:target="_blank"}, first delivering low power operation and second delivering high speed capabilities for image and video recording, network communication and edge processing.

[![pira]({{ site.url }}/images/pira/pira-zero-18.jpg){: .img-full}]({{ site.url }}/images/pira/pira-zero-18.jpg){: .img-open}

The communication strategy we have learned work best in these use-cases requires low-power management access in real time, allowing one to make sure all devices in a given area are operational and get instant notifications of events, implemented with [Lora](https://www.lora-alliance.org/){:target="_blank"} technology and [LoraWAN](https://www.thethingsnetwork.org/docs/lorawan/){:target="_blank"} infrastructure, typically using open infrastructure as part of [The Things Network](https://www.thethingsnetwork.org/){:target="_blank"}. High-speed communication for sending large amounts of data, video and images typically, is implemented with WiFi for local user access and WiFi 5 Ghz long-range systems, enabling real-time access to data. For very remote areas, devices can be extended with the [Iridium](https://www.iridium.com/){:target="_blank"} satellite modems, sending data from anywhere in the world. This empowers the users to have real-time control over the devices, schedule large data transfers of captured information and be up-to-date with the environment under investigation.

<iframe width="94%" height="315" src="https://www.youtube.com/embed/Um9AoUtObyI?rel=0&amp;controls=0" frameborder="0" allowfullscreen></iframe>

To best show the power of using these technologies in combination, we explore the use-case currently deployed at the island of Principe with the aim to monitor the sea turtles. This is deployed at a long sandy beach. There is a LoraWAN base-station at the beach, connecting to the internet via 3G mobile phone network (could be WiFi or Satellite as well) and listens for messages from various devices. Fresh Monitoring Platform uses LoraWAN to report water level and other measurements in real-time, and stores camera images locally. We can retrieve them once in a while when passing by or extend it with long distance communication modules. Arboreal monitoring platform is an upgrade of the solar powered autonomous system with long-range communication capabilities. PitStop tags are mounted on turtles and use LoraWAN to report when they are on the beach or surface nearby, so we can be notified when they can be collected. These tags record video for about two weeks between the return of the turtles in the nesting season. The marine guard hut houses a docking station for the tags, once removed from the turtle they are wirelessly charged in the docking station and connected via WiFi to the internet, such that all data can be retrieved remotely. Once charged in about a day, they can be installed on another turtle. Turtle nest monitor devices are placed within the nest to measure the temperature and detect vibration to recognize hatching, using LoraWAN to report data in real-time and enable to evaluate the whole beach and environmental effects on it.

Our solution for power management [PiRa](http://irnas.eu/pira){:target="_blank"} is at the heart of all above devices, from LoraWAN Gateway to PitStop tags and nest monitor devices, implementing low-power operation and wireless communication. This enables us to rapidly develop new applications responding to the specific challenge and support various conservation efforts.

Check [our web page](http://irnas.eu/conservation){:target="_blank"} to find out more about our IoT solutions for conservation and the development, manufacturing and consulting services we offer in this field. We also invite you to contact us with your conservation challenge to start a conversation on how we could join forces to best tackle animal and nature conservation problems.





