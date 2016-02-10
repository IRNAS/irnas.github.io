---
layout: post
title: "KORUZA 1.0 progress update"
description: "Development of the past month following our scientific workshop has been focused on improving the design for more reliable construction as well as optimized instructions and documentation for assembly of KITs."
category: KORUZA
tags: [KORUZA, Focus adjustment, Instructions]
---
{% include JB/setup %}

Development of the past month following our [scientific workshop](http://irnas.eu/koruza/2015/11/27/first-koruza-workshop){:target="_blank"} has been focused on improving the design for more reliable construction as well as optimized instructions and documentation for assembly of [KITs](http://fabrikor.eu/){:target="_blank"}.

Key upgrade to the mechanical design of [KORUZA 1.0](http://koruza.net/index.html){:target="_blank"} is the upgrade of the focus adjustment axis and motorized drive. The old approach has been based on a stepper motor driving an M4 screw with a compression spring on it, moving the sliding mount closer and further away from the lens. Two issues have dominated the reliable reproduction of the setup, namely the spring snagging on the screw threads and the increase in force required as the spring has been compressed, effectively limiting the movement range to a few millimeters and making the setup prone to stepper motor losing steps during operation.

New solution solves these problems by altering the approach. The sliding mount has now a fixed long nut through which a screw is threaded. On one side of the screw a stepper motor is mounted with a flexible coupler, and on the other side mounted with a flanged ball bearing to the base housing the lens. The force to rotate the screw is now constant along the whole movement range that has been increased to well over 20mm from previous 5mm with much more reliable rotation.

[![koruza-focus]({{ site.url }}/post_files/koruza-update/koruza-focus.jpg){: .img-half}]({{ site.url }}/post_files/koruza-update/koruza-focus.jpg){: .img-open}
[![koruza-interface]({{ site.url }}/post_files/koruza-update/koruza-interface.PNG){: .img-half}]({{ site.url }}/post_files/koruza-update/koruza-interface.PNG){: .img-open}

We have upgraded the web interface to have all essential functions included and to allow for simple control of the units, while adding backend support for auto-alignment algorithms to maintain alignment. These features are now actively developed and upgrades are available directly from [GitHub](https://github.com/IRNAS/koruza-pi){:target="_blank"} by running a single command on the RaspberryPi.

The immediate plan for [KORUZA 1.0](http://koruza.net/index.html){:target="_blank"} is offering full support to anyone trying to replicate and construct units through our [forum](http://forum.irnas.eu/){:target="_blank"} or [chat](https://chat.irnas.eu/home){:target="_blank"} as well as improving documentation with video step-by-step instructions. To optimize the collaboration on creating good quality instructions, we have devised XML based documentation based on [GitHub repository KORUZA-instructions](https://github.com/IRNAS/KORUZA-instructions){:target="_blank"} that is served directly on [http://instructions.koruza.net](http://instructions.koruza.net/){:target="_blank"} allowing anyone to propose and push changes to every step of instructions and enable improvements by a larger community following best practices from software development.

We invite you to check out the source documents of [KORUZA 1.0](http://koruza.net/source/){:target="_blank"} and consider constructing and testing units as well as contributing to the development.



