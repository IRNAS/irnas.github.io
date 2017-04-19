---
layout: post
title: "Developing KORUZA Pro: Koruza Driver - Part 2"
description: "We've improved the real-time Koruza driver, making it much more fault tolerant."
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Koruza Driver, Real-Time Controller]
---
{% include JB/setup %}

We've come a long way since our [last blog post](http://irnas.eu/koruza/2016/11/25/developing-koruza-pro-koruza-driver-real-time-controller){:target="_blank"} on Koruza real time (move) driver with many improvements made to the system, including the changes to the real-time driver itself. The new structure of electronics is much more fault tolerant because of the simplicity and task distribution. The Koruza move driver is now just a simple board dedicated to only one true real-time task - moving the stepper motors. Although the board has only few components, and one "simple" task, it is still one of the crucial parts of the system. 

The main and only MCU on the board is the one and only [ATmega328P](http://www.microchip.com/wwwproducts/en/ATmega328P){:target="_blank"}, which is Arduino compatible. The MCU tasks are: driving the stepper motors, reading the switches and encoders, and communicating with the main board. For driving motors, there is one [high-current Darlington transistor array](http://www.ti.com/lit/ds/slrs027o/slrs027o.pdf){:target="_blank"}. On the board back, at the end of the motor shafts two magnetic encoders are positioned. Two encoders are [TLV493D](http://www.infineon.com/cms/en/product/sensor/magnetic-position-sensor/3d-magnetic-sensor/TLV493D-A1B6/productType.html?productType=5546d462525dbac401529cebc74f07b7){:target="_blank"} from Infineon, the [Arduino lib](https://github.com/IRNAS/TLV493D-3D-Magnetic-Sensor-Arduino-Library){:target="_blank"} for it is available on GitHub as usual. Besides two motor connectors and one programming connector, used only for flashing the bootloader for the first time, there is another connector used for communication between the boards and for powering the driver board. It has standard UART RX/TX pins with an additional reset pin so firmware upgrades can be done "over the air". Communication protocol stayed the same and typical input power is +9 V. Now, this board has a very interesting shape and it is a perfect fit for the inside of the KORUZA Pro unit, which you can see on the picture below. 

Separating the motor driver was a good idea for lots of reasons with one of the main ones being that by doing this we have created a simple upgradeable structure that can be restarted at any time. To conclude, the process of developing Koruza driver is a good example of how keeping things simple results in much greater resistance to failure.  

[![koruza-driver]({{ site.url }}/post_files/koruza-pro-dev/koruza-driver-2.jpg){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/koruza-driver-2.jpg){: .img-open}







