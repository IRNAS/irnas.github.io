---
layout: post
title: "Building Hardware Following Open Source Principles"
description: ""
category: IRNAS
tags: [IRNAS,]
---
{% include JB/setup %}

[](){:target="_blank"}


Since the beginning of this year we at Institute IRNAS and [Fabrikor](http://fabrikor.eu/){:target="_blank"} fabrication lab have started several exciting collaborations with organizations from around the world, helping them bring to life useful products by providing our expertise in open hardware development and manufacturing.

This blog post serves as an introduction into a series of posts on open hardware development collaborations coming up in the following months, where you’ll be able to learn how we integrate and use open technologies to build new useful and open projects in practice, as well as follow the progress updates of these open projects, from our KORUZA wireless networking solution, citizen science environment monitoring devices, endangered species monitoring and conservation platform to open medical equipment.

We are taking the projects from the idea and research stage to scale manufacturing. To better explain our work flow we prepared the following diagram, where you can see how we work as well as how we’re applying open source principles along the way.

[![open-hardware-development-diagram]({{ site.url }}/post_files/open-hardware-dev/workflow-diagram.png){: .img-full}]({{ site.url }}/post_files/open-hardware-dev/workflow-diagram.png){: .img-open}
<p class="quiet">Hardware development and fabrication following open principles workflow diagram</p>

Choosing our default style of working when developing a new product — by open source principles — benefits all parties involved as transparency holds everyone accountable and aligned with agreed values. And it is not only beneficial for us and our clients but for broader community as well.

<h3>Openness is what helps us move fast in all stages of the development process.</h3>

The initial **research phase**, when we test an idea, check its feasibility and try out a number of solutions is best done when we can peek into a number of existing products and solutions, learning from each one of them to form our solution. When devices are open hardware, it becomes almost trivial to learn from them.

**Building an operational prototype of hardware** is an exciting step, significantly empowered with an open hardware systems ranging from Arduino, Raspberry Pi and a bulk of different small modules available online. This immense library of modular solutions, which enables rapid prototyping, is sometimes tedious due to poor documentation of some systems, but significantly faster and more cost effective then other options.

**Product development** as such is a detailed process when aiming for product manufacturing, having an insight into how existing products are built enables the discovery of best practices, speeding up the development and educating developers in the process.

Also for the **after sales activity and users support** openness proves itself as beneficial since it leads to direct understanding of the user and makes serviceability of the devices easier, but most importantly, empowers the communication with the developers to collaboratively identify the improvements, changes and features for the upcoming versions.

[Koruza 1.0](http://scientific.koruza.net/){:target="_blank"} for scientific applications and our now [KORUZA Pro](http://www.koruza.net/){:target="_blank"} for professional users are both examples of how we are applying open source principles in the development and fabrication process.

In [the series of blog posts](http://irnas.eu/category/koruza/){:target="_blank"} on [KORUZA Pro](http://www.koruza.net/){:target="_blank"} development you can learn about the design choices we made for our new robust telecommunication solution. In KORUZA Pro we have successfully integrated several open source technologies, for example — Arduino based modules for the [Koruza driver](http://irnas.eu/koruza/2017/04/19/developing-koruza-pro-koruza-driver-part-2){:target="_blank"}, as well as some standard and commonly available parts — for instance commercially available binoculars, which we customized for our need and built cost effective [aiming mechanism with camera module](http://irnas.eu/koruza/2016/11/04/developing-koruza-pro-camera-module){:target="_blank"}.

[![open-hardware-koruza-driver]({{ site.url }}/post_files/open-hardware-dev/koruza-driver-2.jpg){: .img-half}]({{ site.url }}/post_files/open-hardware-dev/koruza-driver-2.jpg){: .img-open}
[![open-hardware-development-diagram]({{ site.url }}/post_files/open-hardware-dev/camera-module-2.jpg){: .img-half}]({{ site.url }}/post_files/open-hardware-dev/camera-module-2.jpg){: .img-open}
<p class="quiet">KORUZA Pro Driver | Standard binocular used for outdoor activities used as monocular for KORUZA Pro Camera module</p>

Of course, we are keeping the project well documented with all the source files published on [Github platform](https://github.com/IRNAS){:target="_blank"}. (You can learn more on how we’re using Github for documenting hardware design in [irnas-hardware-workflow repository](https://medium.com/r/?url=https%3A%2F%2Fgithub.com%2FIRNAS%2Firnas-hardware-workflow){:target="_blank"}.) [Similarly as in the previous version of Koruza](http://instructions.koruza.net/){:target="_blank"}, we are also preparing complete manuals for efficient use of KORUZA Pro since the first batch is about to come out of production and will be delivered to the first users in the upcoming weeks.

[![open-hardware-koruza-testing]({{ site.url }}/post_files/open-hardware-dev/testing.JPG){: .img-full}]({{ site.url }}/post_files/open-hardware-dev/testing.JPG){: .img-open}
<p class="quiet">The first batch of KORUZA Pro is in production</p>

<h3>Openness is not only empowering development and manufacturing process but it is also bringing very practical outcomes for our customers and their final users.</h3>

**Openess comes together with Total ownership** allowing full use and repair of existing products as a complete insight into operation is available.

**It ensures the devices are Future proof**, since they are are designed and documented such that users are empowered to innovate, explore and upgrade them outside the original specification. The lifespan of devices is extended, their reuse encouraged and their open hardware documentation an enabling component in communication between all parties involved.

**It also simplifies collaborative design**, bridging the gap between the development, manufacturing and use of a device, enabling evolution of the product to be optimal for everyone involved.

[![open-benefits]({{ site.url }}/post_files/open-hardware-dev/open-benefits.png){: .img-full}]({{ site.url }}/post_files/open-hardware-dev/open-benefits.png){: .img-open}
<p class="quiet">Practical outcomes of Openess for the final users</p>

We are finishing this introduction with a sneak peak into the next week story. We’ll be introducing a very interesting project in which we’re taking part — together with [The Crees Foundation](https://www.crees-manu.org/){:target="_blank"}, [the Zoological Society of London](https://www.zsl.org/){:target="_blank"} and [the Arribada Initiative](http://blog.arribada.org/){:target="_blank"} we are going to build a monitoring network on a very particular and important location of our planet. More next week. Stay tuned!

*From now on you can follow the stories on collaborative open hardware development also on [Medium platform](https://medium.com/@IRNAS){:target="_blank"}.*

