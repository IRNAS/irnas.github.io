---
layout: post
title: "We developed a turtle tag enclosure and helped saving green sea turtles"
description: "Do you remember turtle tag enclosures we worked on in the beginning of this year? In collaboration with Alasdair Davies of the Zoological Society of London we developed an open source turtle tag enclosure and produced a small series for testing purposes for the Principe Trust and researchers from the University of Exeter. Open source solution to track endangered green sea turtles turned out to be a great alternative to traditional expensive tags."
category: Other Projects
tags: [Turtle Tag]
---
{% include JB/setup %}


Do you remember [turtle tag enclosures](http://irnas.eu/other%20projects/2016/01/14/turtle-tag-enclosure){:target="_blank"} we worked on in the beginning of this year? In collaboration with [Alasdair Davies](https://twitter.com/Al2kA){:target="_blank"} from [Zoological Society of London](http://www.zsl.org/){:target="_blank"} we developed an open source turtle tag enclosure and produced a small series for testing purposes for the [Principe Trust](https://www.facebook.com/Pr%C3%ADncipe-Trust-305010556356808/){:target="_blank"} and researchers from the University of Exeter. Open source solution to track endangered green sea turtles turned out to be a great alternative to commercial tags.

[![turtle-tag-enclosure-1]({{ site.url }}/post_files/turtle-tag-enclosure/turtle_tagging_1.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/turtle_tagging_1.jpg){: .img-open}


**Some background**

Green sea turtles today are classified as Endangered by the IUCN Red List of Threatened Species. Threats include habitat destruction and the loss of their nesting beaches, plastic pollution in the ocean (plastic bags can be mistaken for jelly fish by sea turtles and are responsible for a great number of deaths) and bycatch through commercial fishing practices.

We were invited to get involved with [ZSL London](http://www.zsl.org/){:target="_blank"} and [Principe Trust](https://www.facebook.com/Pr%C3%ADncipe-Trust-305010556356808/){:target="_blank"}, which is promoting the sustainable development of Principe island through research into nature conservation, tropical agriculture and education. With their unique project they want to reduce the cost of tagging green sea turtles and to acquire spatial and behavioral data using open source principles and technologies in order to achieve greater impact. Traditionally, it is very expensive to tag sea turtles and collect spatial data since you need a robust waterproof enclosure capable of protecting the electrical components at great depths, satellite connectivity and advances such as salt water switch triggers and fast GPS acquisitions to achieve a GPS lock within seconds when the sea turtles come up to the surface to take a breath. Commercial tags cost more than $2,000, and although well suited for the job and used extensively, there was a wish to explore how new advances in open source manufacturing and technologies could achieve the same results, but at a lower cost. Our role in this was to develop affordable, open source solution for tag enclosures to host a low cost Mataki tag and AX3 accelerometer.


**What was the process?**

1. By utilising our [GoodEnoughCNC](http://goodenoughcnc.eu/){:target="_blank"} open hardware toolset and fast prototyping approach we were able to design and 3D print a prototype enclosure at a fraction of the cost when compared to typical commercial prototyping. First prototype was 3D printed on our [Troublemaker](http://goodenoughcnc.eu/troublemaker-3d/){:target="_blank"} to evaluate the initial enclosure design, ensure that we could load the tag with a payload of electronics and to confirm that they could be positioned correctly.

	[![turtle-tag-enclosure-2]({{ site.url }}/post_files/turtle-tag-enclosure/casing_1.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/casing_1.jpg){: .img-open}

2. A rubber base plate was cut and attached to assess the optimum drilling positions and base plate size. The tag was designed to be placed upon a base plate, that was then attached to the sea turtle using an epoxy solution - hence the tag’s code name “the pit stop tag”.

	[![turtle-tag-enclosure-3]({{ site.url }}/post_files/turtle-tag-enclosure/casing_2.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/casing_2.jpg){: .img-open}

3. The completed 3D printed enclosure was taken to a sealant specialist to evaluate the use of polyurethane to form a seal between the acrylic lid and the tag’s base.

	[![turtle-tag-enclosure-4]({{ site.url }}/post_files/turtle-tag-enclosure/casing_3.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/casing_3.jpg){: .img-open}

4. The polyurethane seal was devised by [Tesnila Bogadi](http://www.bogadi.si/){:target="_blank"} by pouring a liquid solution directly onto a thin aluminium plate and allowing it to cool before being cut to size and used to create each individual tag.

	[![turtle-tag-enclosure-5]({{ site.url }}/post_files/turtle-tag-enclosure/seal.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/seal.jpg){: .img-open}

5. A completed tag with a connecting base plate can be seen in this CAD render. Later, the footprint was extended of the base plate so it was flush with the tag above to reduce the chance of potentially snagging on discarded fishing line when at sea.

	[![turtle-tag-enclosure-6]({{ site.url }}/post_files/turtle-tag-enclosure/casing_5.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/casing_5.jpg){: .img-open}

The tags hold a Mataki, developed by Dr Robin Freeman of the Institute of Zoology at ZSL, which is capable of transmitting logged data wirelessly via radio to Mataki base stations within proximity.

The idea was to place the base stations on the known nesting beaches, tag the turtles with the new low cost tag and automagically acquire the logged data recorded by the Mataki when they returned to their nesting beaches. The tag had a nickname, the “Pit stop tag” as it was designed to be removable via a base plate, enabling researchers and beach guards to “swap” a tag out and replace it with a freshly charged tag without needing to apply fresh epoxy to attach and fix the tag in position.

[![turtle-tag-enclosure-7]({{ site.url }}/post_files/turtle-tag-enclosure/tag_on_turtle.jpg){: .img-full}]({{ site.url }}/post_files/turtle-tag-enclosure/tag_on_turtle.jpg){: .img-open}

The tag was trialled in January (2016) together with researchers from the University of Exeter. Green sea turtles will lay clutches of eggs 4 – 5 times every 10 – 14 days, so they tagged a turtle on its third clutch (knowing that it was loyal to the beach) and waited patiently for it to return. When it did, they were delighted to successfully communicate with the tag and download its logged data.

[![turtle-tag-enclosure-8]({{ site.url }}/post_files/turtle-tag-enclosure/base_station_layout.jpg){: .img-half}]({{ site.url }}/post_files/turtle-tag-enclosure/base_station_layout.jpg){: .img-open}
[![turtle-tag-enclosure-9]({{ site.url }}/post_files/turtle-tag-enclosure/base_station_power.jpg){: .img-half}]({{ site.url }}/post_files/turtle-tag-enclosure/base_station_power.jpg){: .img-open}
 
5 base stations were deployed to cover the entirety of the nesting beach. Each base station could pick up a returning sea turtle at up to 400 – 500m (LOS) once the turtle starts its haul from the water. Each base station is powered by a 6 watt solar panel and is capable of communicating with a returning Pit Stop Tag at up to 400 – 500m away (868mhz).

**Open source is the future**
 
The tag’s enclosure costs ~$50 and the internal electronics $200, which is a dramatic cost reduction. The next challenge is to explore and include an open source approach to rapid GPS acquisition and include a salt water switch to acquire reliable GPS locks when the turtles surface at sea.

This project showed a great potential for future where open source technologies and the sharing of knowledge will revolutionize the monitoring of species. Through the introduction of affordable and effective open solutions that are accessible to all, we can better collect, understand and analyse data, and act upon the knowledge acquired to make informed conservation decisions and ultimately protect and conserve endangered species such as green sea turtle.

**Read more:**

- [How Open Source Technologies Could Dramatically Reduce the Cost of Tagging Green Sea Turtles](https://www.wildlabs.net/resources/case-studies/how-open-source-technologies-could-dramatically-reduce-cost-tagging-green-sea){:target="_blank"},  [wildlabs.net ](https://www.wildlabs.net/){:target="_blank"}

- [How open source technologies could dramatically reduce the cost of tagging green sea turtles.](https://www.zsl.org/blogs/conservation/how-open-source-technologies-could-dramatically-reduce-the-cost-of-tagging-green){:target="_blank"},  [zsl.org](https://www.zsl.org/){:target="_blank"}

- [Where Sea Turtles and Open Source Meet](http://animals.oreilly.com/where-sea-turtles-and-open-source-meet/){:target="_blank"}, [animals.oreilly.com](http://animals.oreilly.com/){:target="_blank"}
 

**Photos credits:** [Alasdair Davies](https://twitter.com/Al2kA){:target="_blank"}
