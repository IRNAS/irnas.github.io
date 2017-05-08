---
layout: post
title: "Collaborating with Safecast – Development and Fabrication of Solarcast"
description: "We’re happy to announce that also with our help the first version of Solarcast has been released."
category: 
tags: [Solarcast, Safecast, environmental monitoring, environmental data, open data, open source, open hardware, development]
---
{% include JB/setup %}

From the beginning of this year we have started, together with our fabrication company [Fabrikor](http://fabrikor.eu/){:target="_blank"},  several new partnerships with open hardware organizations within [Shuttleworth Foundation](https://www.shuttleworthfoundation.org/){:target="_blank"} and outside. One of the exciting projects we’ve been developing and manufacturing in collaboration with [Safecast](http://blog.safecast.org/){:target="_blank"} is a sensor device designed to operate off-grid and sense environmental parameters. We’re happy to announce that also with our help [the first version of Solarcast has been released](http://blog.safecast.org/2017/04/introducing-solarcast/){:target="_blank"}!

[![Solarcast-at-MIT-media-lab]({{ site.url }}/post_files/solarcast/Solarcast-MIT-Media-lab-roof-02.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/Solarcast-MIT-Media-lab-roof-02.jpg){: .img-open}
<p class="quiet"><a href="http://blog.safecast.org/2017/04/introducing-solarcast/" target="_blank">“Solarcast at MIT Media lab”</a> by <a href="http://blog.safecast.org/" target="_blank">Safecast</a> is licensed under <a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank">CC BY-NC 4.0</a></p>

The sensors included in the device:

- Air: Each Solarcast unit has an enclosed particulate sensor module which contains [Alphasense OPC-N2](http://www.alphasense.com/index.php/products/optical-particle-counter/){:target="_blank"} and [Plantower 5003](http://www.plantower.com/en/content/?108.html){:target="_blank"} particulate sensors, measuring PM10, PM2.5 & PM1.0.

- Temperature

- Humidity

- Radiation: Dual [LND 7317](http://www.lndinc.com/products/pdf/17/){:target="_blank"} 2” pancake GM tubes (same as in the bGeigie and Pointcast units) with Medcom iRover high voltage power supplies

[![Inside-Solarcast]({{ site.url }}/post_files/solarcast/Solarcast-inside-wcallouts01.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/Solarcast-inside-wcallouts01.jpg){: .img-open}
<p class="quiet"><a href="http://blog.safecast.org/2017/04/introducing-solarcast/" target="_blank">“Inside Solarcast”</a> by <a href="http://blog.safecast.org/" target="_blank">Safecast</a> is licensed under <a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank">CC BY-NC 4.0</a></p>

Read more about the features and the modules included in Solarcast box in [the Safecat’s Solarcast introduction blog post](http://blog.safecast.org/2017/04/introducing-solarcast/){:target="_blank"}.

The idea for Solarcast came out of Safecast’s experience on open environmental parameters monitoring and the challenges they faced – problem with access to power and internet for the devices they wanted to deploy on the field and complicated configuration requirements. That is how the idea for a totally wireless, solar powered, auto-configuring device that could be dropped anywhere and forgotten and it would just work was born. Original Safecast team member Ray Ozzie took the lead on all aspects of this project and we are really proud we could help him with the development and manufactured the first batch of Solarcasts in Fabrikor.

Our part in the process has been taking a single hand-built prototype of the Solarcast unit and turning it into a manufacturable system. Firstly the existing design has been evaluated and comprehensive requirements and module break down document has been prepared, which is available in [the repository](https://github.com/IRNAS/Solarcast){:target="_blank"}. To limit the development time and speed up the process, we have in parallel designed all the electronics subsystems and tested them individually prior to combining them into a completed system. Development of each module represented a number of interesting challenges.

[Geiger module](https://github.com/IRNAS/Solarcast/tree/master/geiger-module){:target="_blank"} measures radiation in the alpha, beta and gamma spectrum. We have for the first time implemented a novel assembly design developed by the Safecast community of using a stack of two pancake tubes, one acting as the shield for the other, such that a single channel can be used to measure gamma only radiation. We have designed a custom circuit board and a machined plastic part, such that stacking is reliable and most importantly is made waterproof, such that sensors mounted in the enclosure can be through an opening exposed to the outside environment.

[![Geiger module]({{ site.url }}/post_files/solarcast/geiger.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/geiger.jpg){: .img-open}

[Air module](https://github.com/IRNAS/Solarcast/tree/master/air-module){:target="_blank"} is a stand-alone environmentally isolated box within the main enclosure with the purpose of enabling controlled air circulation though two air sensors and protecting the rest of the electronics from external influences.

[![Air module]({{ site.url }}/post_files/solarcast/air-1.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/air-1.jpg){: .img-open}

[Communications module](https://github.com/IRNAS/Solarcast/tree/master/communications-module){:target="_blank"} is the main board of the system interconnecting all the individual modules and communication interfaces. The core is a low-power bluetooth module controlling the complete system through a system of data and power switched thus enabling very low power consumption in standby state. Into this board there is an Adafruit Fona 3G module plugged in for GSM connectivity and a LORA module for low power communication with a purpose built gateway.

[Gateway module](https://github.com/IRNAS/Solarcast/tree/master/gateway-module){:target="_blank"} is a dual-purpose design board, that is plugged into the communication module as well as a Raspberry Pi operating as a gateway that can for example be placed inside the building while the Solarcast is outside the building or in the garden.

[![Gateway module]({{ site.url }}/post_files/solarcast/gateway.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/gateway.jpg){: .img-open}

[Battery module](https://github.com/IRNAS/Solarcast/tree/master/battery-module){:target="_blank"} is a stand-alone circuit providing battery charging and voltage regulation to the system. Amongst available power packs we have decided to design a custom system for this application with maximal reuse for other projects and have called it the IoT battery pack. This way we have solved the charging, battery management and voltage regulation and can now use it in numerous ways.

All modules together in a waterproof enclosure with a tripod mount form [the Solarcast unit](https://github.com/IRNAS/Solarcast){:target="_blank"}.

[![Solarcast-packed]({{ site.url }}/post_files/solarcast/Solarcast-package-01.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/Solarcast-package-01.jpg){: .img-open}

[![Solarcast-testing]({{ site.url }}/post_files/solarcast/Solarcasts-testing-Maribor01-1.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/Solarcasts-testing-Maribor01-1.jpg){: .img-open}

<p class="quiet"><a href="http://blog.safecast.org/2017/04/introducing-solarcast/" target="_blank">“Solarcast testing and Solarcast package”</a> by <a href="http://blog.safecast.org/" target="_blank">Safecast</a> is licensed under <a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank">CC BY-NC 4.0</a></p>

It the delivery process we have faced the harsh reality of the impact shipping has on the devices as on the first few units the heavy battery pack came lose inside the case. We have quickly reiterated the mechanical process and implemented a significantly more reliable mount as well as used the opportunity this delay has created to implement a number of fixes and upgrades suggested by the Safecast team meanwhile. We have done our best also to validate in the upgraded version that units can handle even the most rough handling.

<iframe src="https://player.vimeo.com/video/215341662" width="94%" height="315" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p class="quiet"><a href="https://vimeo.com/215341662">Solarcast shipping stress test</a> from <a href="https://vimeo.com/safecast">Safecast</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

The Solarcasts are now being sent to all the deployment locations for testing. You’re invited to follow [the Solarcast blog](http://blog.safecast.org/news/){:target="_blank"} for the news on the performance of the devices.

[![Solarcast-testing]({{ site.url }}/post_files/solarcast/Solarcasts-Manchester-02.jpg){: .img-full}]({{ site.url }}/post_files/solarcast/Solarcasts-Manchester-02.jpg){: .img-open}
<p class="quiet"><a href="http://blog.safecast.org/2017/04/introducing-solarcast/" target="_blank">“Solarcast Testing”</a> by <a href="http://blog.safecast.org/" target="_blank">Safecast</a> is licensed under <a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank">CC BY-NC 4.0</a></p>

This project was for us a very important experience with a steep learning curve since it was a first bigger outside collaboration project done in our new fabrication facilities. We learned a lot and gained valuable experience, which are already helping us improve our project management and development & manufacturing process workflow.
