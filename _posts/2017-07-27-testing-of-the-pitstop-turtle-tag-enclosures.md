---
layout: post
title: "Testing of the Pitstop Turtle Tag Enclosures"
description: "Before moving to the next development cycle with a new iteration of Pitstop turtle tag enclosures, it needed to go through some additional testing to get relevant insight into its most important properties - durability and sealing."
category: Other Projects
tags: [IRNAS, Turtle tag, Turtle tag enclosure, Pitstop, Open hardware, Conservation, Arribada Initiative]
---
{% include JB/setup %}

Do you still remember an affordable [open source turtle tags](http://irnas.eu/other%20projects/2016/11/22/turtle-tag-and-turtle-camera-enclosure-development-to-help-save-sea-turtles){:target="_blank"}, used to track and acquire spatial and behavioral data of the endangered green sea turtles, we helped developed last year? This project is still very active and our collaboration with conservationist [Alasdair Davies](https://twitter.com/Al2kA){:target="_blank"} and his [Arribada Initiative](http://blog.arribada.org/){:target="_blank"} has extended into 2017. Before moving to the next development cycle with a new iteration of this solution, the turtle tag enclosure needed to go through some additional testing to get the relevant insight into its most important properties - durability and sealing.

Some sea turtles, on which the tags are mounted, are very big and can weigh up to 500 kg. They often clean their shells, where the tags are mounted, by rubbing them at rocks. Due to the high force on impact of the turtle with the rock, the tags have to be very durable. To simulate such a situation and determine what material can withstand high force at the given shape we created a test with a pendulum like construction. A lever was mounted on a table on one end, with a special two-sides construction on the other end – one side holding weights to increase the momentum of the swing and the other side with a small sphere that hits the enclosure. We tested four different materials - acryl, polyamide, oleamide, PA6 and calculated the momentum of the pendulum with the angle from which it hits the tags and the weight that was put on. The results were pretty surprising. The acrylic tag broke already with a very small momentum but the other three materials held up much more than we expected, making them a suitable choice for tag enclosures.

[![pitstiop-testing]({{ site.url }}/post_files/pitstop-testing/pendulum_front.png){: .img-full}]({{ site.url }}/post_files/pitstop-testing/pendulum_front.png){: .img-open}

[![pitstiop-testing]({{ site.url }}/post_files/pitstop-testing/polyamide.JPG){: .img-full}]({{ site.url }}/post_files/pitstop-testing/polyamide.JPG){: .img-open}

Some turtles can dive up to 200 m deep into the water where the water pressure is very high. The sealing of the tags has to keep their insides dry, so the water doesn't interfere with the electronics. To see what kind of sealing works best we put the enclosures into a pressure container filled with water and air under pressure. Four different sealing methods - foamed polyurethan O-ring string, rubber O-ring string, polyurethan sealing sheet and hard polyurethan sealing layer were exposed to 9 bars of pressure for 15 min. The results showed that none of the sealing could withstand the pressure except the rubber O-ring string, which stayed completely dry. We still have to test the sealing under 20 bars of pressure, which is the approximate pressure at 200 m underwater depth in the near future.

[![pitstiop-testing]({{ site.url }}/post_files/pitstop-testing/pressure_container.JPG){: .img-half}]({{ site.url }}/post_files/pitstop-testing/pressure_container.JPG){: .img-open}
[![pitstiop-testing]({{ site.url }}/post_files/pitstop-testing/polyamide_rubber_oring_2.JPG){: .img-half}]({{ site.url }}/post_files/pitstop-testing/polyamide_rubber_oring_2.JPG){: .img-open}

To conclude, we decided to use polyamide as the material for the tags enclosure in combination with the rubber O-ring string sealing. Polyamide wasn't the strongest material in our durability test but it was definitely strong enough for its purpose and it has the advantage of being very easy and clean to process with our CNC mill. 




