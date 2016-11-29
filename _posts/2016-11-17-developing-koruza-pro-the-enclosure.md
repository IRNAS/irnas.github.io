---
layout: post
title: "Developing KORUZA Pro: The Enclosure"
description: "For Koruza Pro we developed a solution for the sealing, such that the units are easy to assemble, use small part count and are cheap for manufacturing."
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Enclosure]
---
{% include JB/setup %}

For [Koruza Pro](http://new.koruza.net/){:target="_blank"} we wanted to find a solution for the sealing, such that the units would be easy to assemble, use small part count and be cheap for manufacturing. Until the version 2.3.1 we used an independent internal supporting structure for the motorized alignment system and PCB supports, like shown in the picture 1. A rectangular, 2 mm thick aluminium profile was used for internal supporting, with a flange on both sides for the mounting to the front and the back lids. When tested, this system showed as inappropriate due to the sealing on the flanges and the expensive manufacturing.

[![the-enclosure]({{ site.url }}/post_files/koruza-pro-dev/koruza-2.2.2.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/koruza-2.2.2.JPG){: .img-open}
<p class="quiet">Koruza v. 2.2.2.</p>

The first step to a simplified design was eliminating the independent internal supporting structure. We used a thicker 4 mm profile for the enclosure, which also serves as a mounting structure for the motorized alignment system. Since the new profile was thick enough, we eliminated the back flange and sealed directly to the back lead, however the problem with the sealing on the base plate with lenses remained.

[![the-enclosure]({{ site.url }}/post_files/koruza-pro-dev/koruza-2.3.1.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/koruza-2.3.1.JPG){: .img-open}
<p class="quiet">Koruza v. 2.3.1</p>

A logical follow-up was to rethink the shape of the case on the lenses side. We decided to get rid of the roof for the lenses and replicate it with a separate bent aluminium metal sheet. The reason for this decision was that we wanted to apply the same sealing solution we used for the back lid also on the front base with lenses. Now, Koruza uses only three parts: aluminium 120 x 120 mm, 4 mm thick profile for the case and 5 mm plates as the back lid and the front base; and can be mounted into the enclosure just with 8 screws. We managed to get rid of the 6 machined aluminium parts and two assembly stations at production.

[![the-enclosure]({{ site.url }}/post_files/koruza-pro-dev/koruza-2.3.2.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/koruza-2.3.2.JPG){: .img-open}
<p class="quiet">Koruza v. 2.3.2</p>

This significant design change reduces the manufacturing complexity as well as makes the units more serviceable and easier to assemble, extending their lifetime, improving upgradeability and decreasing the cost.








