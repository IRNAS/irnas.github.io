---
layout: post
title: "Integrated version of Safecast bGeigie"
description: ""
category: Other Projects
tags: [Safecast, Other Projects, Shuttleworth fellows,bGeigie]
---
{% include JB/setup %}

We created [an integrated version of the bGeigie device](https://github.com/IRNAS/bGeigieIntegrated){:target="_blank"}, a mobile survey Geiger counter, by Safecast, who are working to empower people with data about their environments.

Our PCB is based on [original design by Safecast](https://github.com/Safecast/bGeigieNanoKit){:target="_blank"}. We removed various breakout boards and instead placed most of the components directly to the PCB. Our design uses RedBear Duo(https://github.com/redbear/Duo) as a central processing unit, instead of Arduino Fio as used on the original board. The entire circuit can be powered through USB connector on RedBear, or from a 3.7V LiPo battery. The circuit also includes a battery charger, we used MAX1555 from Maxim Integrated. For the control of the Geiger gas tube the iRover is being used, just like in the original design. A high-brightness LED and a piezo buzzer signalize the incoming pulses from the tube. FGPMMOPA6H GPS receiver from Adafruit retrieves the current position of the device and an accelerometer/magnetometer (LSM303C form ST Microelectronics) measures acceleration and orientation of it. Data is being logged to a micro SD card for postprocessing. A socket for the XBee module is also included, which enables connection to an external logger. A monochrome, 128x32 pixels wide OLED graphical display from Adafruit(https://www.adafruit.com/product/938) displays a simple graphical user interface. A rotary encoder with built-in pushbutton is included to enable user to control the device. Accelerometer/magnetometer uses an I2C interface. SD card and OLED display communicate via SPI. XBee and GPS module are both using UART interfaces.

All functions of the device have been tested (except XBee) and firmware is currently under development.

[![Safecast-bGeigie]({{ site.url }}/post_files/gaiger/bGeigi-2.JPG){: .img-full}]({{ site.url }}/post_files/gaiger/bGeigi-2.JPG){: .img-open}
[![Safecast-bGeigie]({{ site.url }}/post_files/gaiger/bGeigie-1.JPG){: .img-full}]({{ site.url }}/post_files/gaiger/bGeigie-1.JPG){: .img-open


 
 



