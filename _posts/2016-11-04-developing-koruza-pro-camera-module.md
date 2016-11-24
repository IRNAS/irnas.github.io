---
layout: post
title: "Developing KORUZA Pro: Camera Module"
description: "Wireless optical system KORUZA and other FSO systems require that the units are pointed at each-other to be able to receive the collimated beam of light that transfers the data between them. We have created a new solution for KORUZA Pro - coupling the optical scope with a webcam."
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Camera Module]
---
{% include JB/setup %}

Wireless optical system [KORUZA](http://new.koruza.net/){:target="_blank"} and other FSO systems require that the units are pointed at each-other to be able to receive the collimated beam of light that transfers the data between them. Typically an infrared and invisible to the human eye beam is used and thus we can not simply see where one unit is pointing. To solve this, generally two types of solutions have been used - an optical scope mounted to the unit, such that the one who is installing the system can look though it and point the unit or a visible beam of light, for example a green laser source as in [KORUZA 1.0](http://koruza.net/about-koruza-1.0/){:target="_blank"} systems thus-far. Both options have a significant drawbacks, the optical scope can only be used when units are turned off to be eye safe and the visible laser can not simply be seen during daylight therefore requiring installation at night. As neither is practical, we have created a new solution for KORUZA Pro and coupled the optical scope with a webcam, such that we can use the system during the day, it remains eye safe as well as enables a number of new features, starting with the link protection mechanism, which shows us what happened in the case of failure.

The new aiming mechanism consists of a camera module coupled with 10 x magnification. We can access its output through a web interface of a mobile phone app and thus simply install and align a [KORUZA](http://new.koruza.net/){:target="_blank"} link.

We are using lens system with 10 x magnification, 21 mm objective lens with focal length of 68 mm and 5 megapixel web USB camera. In order to avoid the cost of custom-made binoculars we used commercially available binoculars and customized them for our needs. We bought standard binocular used for outdoor activities and reassembled it to use only one monocular per Koruza unit. 

[![camera-module]({{ site.url }}/post_files/koruza-pro-dev/camera-module-1.jpg){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/camera-module-1.jpg){: .img-open}
[![camera-module]({{ site.url }}/post_files/koruza-pro-dev/camera-module-2.jpg){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/camera-module-2.jpg){: .img-open}

[![camera-module]({{ site.url }}/post_files/koruza-pro-dev/camera.png){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/camera.png){: .img-open}

To mount camera onto eyepiece lens, we used 3D printed adapter. We found out that the accuracy of positioning of the camera is very important to prevent black spots on the image. 3D printed part was not accurate enough to enable this. Solution that we found useful was to 3D print blank full block with the outline shape and then use the milling machine to drill the hole for the eyepiece lens mount and the holes for the screws that will hold camera in correct place above the lens. We used the same manufacturing process also for other 3D printed parts in [KORUZA Pro](http://new.koruza.net/){:target="_blank"} because it allows us to combine more complex shapes with high precision tolerances where needed. This type of manufacturing - combining 3D printed technology with classical manufacturing processes is suitable mostly for micro and small series production.



