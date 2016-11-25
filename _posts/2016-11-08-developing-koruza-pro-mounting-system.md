---
layout: post
title: "Developing KORUZA Pro: Mounting System"
description: "To best cover all the possible installation scenarios for our new KORUZA Pro and provide user friendly installation process, we are exploring and innovating on its mounting system."
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Mounting system]
---
{% include JB/setup %}

Our next generation device [KORUZA Pro](http://new.koruza.net/){:target="_blank"} will enable a versatile construction of last-mile networks to people’s homes and thus deliver them a faster internet service. To best cover all the possible installation scenarios and provide a user friendly installation process, we are exploring and innovating on the mounting system.

The mounting system needed to be smaller than the mount on previous [KORUZA 1.0](http://koruza.net/about-koruza-1.0/){:target="_blank"}  to minimize the offset of KORUZA unit from the mounting structure and thus improve mechanical stability as well as to be aesthetically pleasing. We have designed a mount for KORUZA to be blended into surroundings and which does not significantly alter the architectural value of the buildings. The main KORUZA enclosure has a number of mounting slots that can be interfaced with various mounting brackets optimized for specific use-cases. We have opted to use a mounting base into which a round rod is attached, allowing the pivot during installation. This solution enables us to just slightly tighten the screws and freely move KORUZA in all directions and when it's in the desirable position, fully tighten the screws to stop all movement.

The mounting system is composed of five main structural parts:

- Two mounting brackets onto which mounting jaws come attached 
- Mounting jaws that are used for mounting KORUZA onto pipes and poles
- Pivot rod 
- Mounting base that is attached to the mounting-system 

[![mounting-system]({{ site.url }}/post_files/koruza-pro-dev/mounting-system-1.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/mounting-system-1.JPG){: .img-open}

All parts excluding mounting jaws are made out of aluminium. We decided to use this material because it is easy to work with on CNC milling machines, which was good enough for prototypes and test versions. But we discovered a problem when making pivoting assemblies, where both parts are made of aluminium: when the aluminium hinge has higher surface roughness at the point of the contact or if two surfaces have foreign objects  in between, such as sand or metal particles, the hinge binds together and becomes unusable. We temporarily solved this problem with lubricating the hinge. For use on a massive scale aluminium hinges are still not suitable. For another production batch we will change the bmaterial of the pivot rod to stainless steel with high surface finish.

Another issue that was discovered when test mounting KORUZA, was the danger of it falling off of the mounting brackets when it's not tightened all the way while adjusting the position of the unit. The problem was solved by installing a spring pin into the mounting base, which locks in U groove on the pivot rod.

[![mounting-system]({{ site.url }}/post_files/koruza-pro-dev/mounting-system-2.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/mounting-system-2.JPG){: .img-open}






