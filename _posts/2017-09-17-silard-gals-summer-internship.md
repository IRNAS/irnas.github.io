---
layout: post
title: "Silard Gal’s Summer Internship "
description: "Today we are sharing Silard Gal's experience as an intern at IRNAS. He has spent one very fruitful month at IRNAS's Novi Sad office."
category: irnas
tags: [irnas, internship, intern, pira]
---

{% include JB/setup %}

In one of the previous blog posts we wrote about [a young prodigy Gabriela](http://irnas.eu/irnas/2017/09/12/gabi-got-the-krka-research-prize){:target="_blank"}, who was researching in our [Symbiolab](http://irnas.eu/symbiolab){:target="_blank"}. Today we’d like to share the story of another really talented young student, who is now enrolling to his last year of high school and whose main interests lie in the field of electronics - Silard Gal. He has done a month-long internship at IRNAS in Novi Sad, Serbia and this is a blog post about his experience working with us.

<hr>

My internship started on July 31st for which I was very excited since I was looking forward to gaining new skills and experience. A month later I can confirm that I have definitely achieved that.

I got a warm welcome to the company by Luka Mustafa[](){:target="_blank"}, who made my internship possible, as well as all other team members. In the following weeks I worked mainly with Vojislav Milivojević[](){:target="_blank"}, who is based in Novi Sad and was my mentor for the time of the internship. 

The projects I worked on were [LoRa 3D mapping](https://github.com/IRNAS/Lora-signal-mapping){:target="_blank"}, [Raspberry Pi PiRA Resin Framework](https://github.com/IRNAS/PiRA_resin){:target="_blank"} & software for [BQ2429x](https://github.com/IRNAS/bq2429x){:target="_blank"} and [MAX1720x](https://github.com/IRNAS/max1720x){:target="_blank"}. 

I was greeted with the [LoRa 3D mapping project](https://github.com/IRNAS/Lora-signal-mapping){:target="_blank"}, which was quiet challenging, because I haven’t worked on a project like that before. The main components of this project are Arduino, LoRa, GPS and SD Card modules and the goal was to make Arduino read the LoRa signal strength and report back the GPS coordinates live as well as write them to the SD Card. As a result in Google Earth we can view the device’s live position and the logged route. It is displayed as a 3D map including the signal strength.

[![]({{ site.url }}/post_files/internship/3d_googleearth.png){: .img-half}]({{ site.url }}/post_files/internship/3d_googleearth.png){: .img-open}
[![]({{ site.url }}/post_files/internship/outdoor_lora_gps.jpg){: .img-half}]({{ site.url }}/post_files/internship/outdoor_lora_gps.jpg){: .img-open}

My next project was the [Raspberry Pi PiRA Resin Framework](https://github.com/IRNAS/PiRA_resin){:target="_blank"}. This wasn’t that new to me, because I already had experience with the Raspberry Pi and python programming, but the project was more challenging than the previous one. However, with Vojislav's and the team's assistance I completed it successfully. The hardware part of this project was already done. The only thing missing was the Raspberry Pi’s I2C connection to the battery pack. So, the software was at the center of this project. First I started with a basic python script, which was built by Docker and uploaded to the Resin framework through Git. After I got comfortable with the framework, I built the software for the BQ2429x LiPo charger and the MAX1720x fuel gauge chips. For testing the fuel gauge I used high and low value resistors, as shown on the second picture. 

[![]({{ site.url }}/post_files/internship/pi.jpg){: .img-half}]({{ site.url }}/post_files/internship/pi.jpg){: .img-open}
[![]({{ site.url }}/post_files/internship/resistor_pi.jpg){: .img-half}]({{ site.url }}/post_files/internship/resistor_pi.jpg){: .img-open}

My last project, which consisted of two parts was the easiest of them all, because most of the code was already written and the additional code that needed to be implemented was ready in Python, designed for the [PiRA](http://irnas.eu/pira){:target="_blank"} Resin Framework. My job was to convert the Python code into C/C++ and to format it. I was testing the code on the ESP8266 as shown on the picture. 

[![]({{ site.url }}/post_files/internship/esp.jpg){: .img-full}]({{ site.url }}/post_files/internship/esp.jpg){: .img-open}

To conclude, I can definitely confirm that my time as an intern at IRNAS was very rewarding. I had an opportunity to learn more about wireless technology, the Raspberry Pi, microcontrollers etc.. By working on the assigned projects I have gained a lot of experience and skills relevant for my field. 

I'd like to give special thanks to [Vojislav Milivojević](https://twitter.com/_vojam){:target="_blank"} and [Luka Mustafa](https://twitter.com/slomusti){:target="_blank"} for making my 1 month internship possible.

<hr> 

Same here! We are also very grateful Silard Gal has joined us in August and we are truely hoping for the future collaboration beyond this internship. 

If you’d also like to join our team or find out more about internship/job opportunities at our company, you can always write us to [hr@irnas.eu](mailto:hr@irnas.eu){:target="_blank"}. We are looking forward to reading about your interests, skills and experience.
