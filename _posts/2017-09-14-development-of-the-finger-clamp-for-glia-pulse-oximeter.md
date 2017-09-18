---
layout: post
title: "Development of the finger clamp for Glia Pulse Oximeter"
description: "We are developing hardware and software for open source Glia Pulse Oximeter, project run by Tarek Loubani."
category: Other Projects
tags: [IRNAS, Open hardware, Glia, Pulse Oximeter, Open medical care]
---
{% include JB/setup %}

On this blog we haven’t shared anything about a very promising initiative we’ve been involved in for a couple of months now. In the beginning of the year we’ve been approached by [Tarek Loubani](https://twitter.com/trklou?lang=en){:target="_blank"} to help him develop and optimise a [Pulse Oximeter](https://github.com/GliaX/pulseox){:target="_blank"}.  Tarek is a Palestinian-Canadian emergency medicine doctor who has decided to apply his medical skills to develop high-quality, low-cost, open-source, universally accessible medical hardware to increase the accessibility of medical supplies in places where such moves are necessary (e.g. Gaza) and end the asymmetry of care. He started with a [$3 stethoscope](http://www.independent.co.uk/news/world/middle-east/gaza-doctor-tarek-loubani-creates-3d-printed-stethoscopes-to-alleviate-medical-supply-shortages-10495512.html){:target="_blank"} that meets the same standards as a $300 one. Through his [Glia project](https://github.com/GliaX){:target="_blank"}, he is now expanding the pool of designs and testing them in the field.

[Pulse Oximeter](https://github.com/GliaX/pulseox){:target="_blank"} is a project aiming to create a research-validated pulse oximeter whose plans are available freely and openly. The goal is for the device to cost under USD$25 to produce. Our role in the development of Pulse Oximeter includes both hardware and firmware development. All the work was done by our engineers Vojislav, Luka, Musti, Jernej and Benjamin as a student intern. 

In general, devices in medical field must be reliable allowing very accurate data analysis and therefore their design is often complex. Because of that, advanced manufacturing and assembly infrastructure is essential for successful production of these devices. Designing a product with a comparable performance yet keeping it simple and affordable at the same time is undoubtedly a challenge of special sort.

The idea of Glia open source devices is that they can be manufactured and assembled with basic equipment and standard tools. Their users are no experts in engineering computer aided design or manufacturing. Therefore, these devices must be well-designed, such that no mistake can be made by the non-trained user during manufacturing and/or assembly if they follow the instructions carefully.

Secondly, special care has to be taken during the design in terms of availability of components since Glia medical equipment is meant to be utilized in places where parts are not easily accessible for political or economic reasons. Therefore, our engineers were bound to using components and techniques that are as standard as possible.

In this blog post you can read about the process of designing a finger clamp for Glia Pulse Oximeter.

The hardware for our pulse oximeter project contains a 3D printable finger clamp and an enclosure containing the main PCB, a battery and a display. The finger clamp should be comfortable enough to be kept on the finger for a longer period of time without causing any discomfort while still pressing firm enough to not fall off or distort the signal if the patient undergoes a light natural arm/hand movement during the measurement.

The design has to be as modular as possible to ensure easy repair or replacement of components. At the start of the finger clamp development we looked at some existing ones for inspiration and made our first prototype. We wanted to try a single piece clamp with 2 joints to adapt perfectly to the finger, which was a failure. The material was too thick and not elastic enough and it was overall too big to be practical. The next version was a huge improvement since it was small and light, but it didn't have room for any electronics and it easily fell of the finger at slight movement. In the next few versions we optimized the pressure that is applied on the finger by changing the shape of the loop that connects the upper and bottom parts. We also tested different widths and added rounded walls on the sides to hold it in place better. After about 20 iterations we were satisfied with the basic shape of the clamp. With a solid, promising-looking base we already have a few ideas for the future improvements to make.

[![pulse-oximeter]({{ site.url }}/post_files/pulse-oximeter/finger_clamp_v11.jpg){: .img-half}]({{ site.url }}/post_files/pulse-oximeter/finger_clamp_v11.jpg){: .img-open}
[![pulse-oximeter]({{ site.url }}/post_files/pulse-oximeter/case_v1.jpg){: .img-half}]({{ site.url }}/post_files/pulse-oximeter/case_v1.jpg){: .img-open}

We kept the design for the enclosure very simple and compact. It’s open on the top where the display is mounted and we added a hole on the side so that the user can reach to the ON/OFF switch and the display backlight button. The enclosure has been optimised to fit all the necessary components, can be assembled with ease and is very compact.

Shortly, first fully-working Glia Pulse Oximeter V1 prototype will make it’s way overseas to Tarek for testing. In the upcoming months we’ll keep you updated on the progress of this project. Meanwhile, if you want to collaborate on Gliax open source medical equipment, you can join the conversation and contribute on [Github](https://github.com/GliaX/pulseox){:target="_blank"}.

<iframe width="94%" height="315" src="https://www.youtube.com/embed/9c5PuEUazFI?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>
