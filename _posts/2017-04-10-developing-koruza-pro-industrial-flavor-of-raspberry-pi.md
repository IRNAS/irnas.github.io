---
layout: post
title: "Developing KORUZA Pro: Industrial Flavor of Raspberry Pi"
description: ""
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Raspberry Pi]
---
{% include JB/setup %}


Effective iteration cycles are very important part of the development of a new device. By doing a new version/iteration of the product you can enhance it in many different ways, which was done very successfully with the Koruza electronics/embedded system. [Koruza Pro](http://www.koruza.net/){:target="_blank"} is in this manner growing to become a high-grade robust industrial telecommunication system. 

The main advantage of the previous [Koruza 1.0](http://scientific.koruza.net/){:target="_blank"} system was the usage of commonly available parts to build the final product. With this idea in mind we've been developing also the Koruza Pro. Of course, we needed to work on it extensively for the system to be reliable and robust to meet all the professional users needs.

The best example of this is the Koruza main control unit. The previous Koruza system used [Raspberry Pi 2/2B/3B](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/){:target="_blank"} for monitoring the system and giving the user all the necessary information. In Koruza Pro we've upgraded it to [Raspberry Pi Compute Module](https://www.raspberrypi.org/blog/raspberry-pi-compute-module-new-product/){:target="_blank"} (CM). The CM is DDR2-SODIMM-mechanically-compatible System on Module (SoM) containing a processor, memory, eMMC Flash and supporting power circuitry. So, basically it is an industrial Raspberry Pi solution. We've created our own base board for the CM, with all necessary interfaces, like USB port, Ethernet port with PoE, SFP port, etc. All design files are available in the [GitHub repository](https://github.com/IRNAS/koruza-compute-module){:target="_blank"}, with the [schematics file](https://github.com/IRNAS/koruza-compute-module/blob/board_0.2/koruza-compute-module-board/koruza-compute-module-board.pdf){:target="_blank"} being the best place to start exploring the new design. 

At the moment we are testing already the third version of the board (v0.3), which has some additional electrical and mechanical enhancements. We did not have to match space on the board, but as usual, we tried to make it as modular as possible since you never know what your costumers might want as a new feature in the future.

To conclude this post - keep your designs modular and iterate as fast as you can, this will keep the space open for innovation and great ideas coming in.

[![mounting-system]({{ site.url }}/post_files/koruza-pro-dev/koruza-pro-dev-raspberry-p.jpg){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/koruza-pro-dev-raspberry-p.jpg){: .img-open}







