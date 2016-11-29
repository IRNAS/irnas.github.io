---
layout: post
title: "Pivot system for lens movement"
description: ""
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Mounting system]
---
{% include JB/setup %}

[](){:target="_blank"}

Optical wireless system KORUZA operates by directing a collimated beam of light towards another unit to establish communication. To be able to precisely aim a beam of light with a millimeter precision when shining at a distant unit at 150 m away, one requires two key components; a precise motor drive (see blog about it) for mechanical displacement of a lever and a pivot point. For aiming in a 3 dimensional space, this must happen on the two perpendicular axes simultaneously, while having no rotation around its own axis. Additionally, in an optical system we wish to have the centre of rotation in the middle of the lens which limits the choice of mechanical solutions. For rotation around the single axis, a ball or a sliding bearing are a good choice, for rotation in two axis axes a round ball joint is typically used (as in KORUZA generation 2), however this moves the centre of rotation away from the lens centre as well as it requires a separate solution for the sealing of the moving part.

(diagram rotation)

Since KORUZA generation 3 on we used a rubber pad sandwiched between the two 3D printed parts with the lens in the middle, with which we have achieved the movement of the lens in both axes.  This system has proved to work very well on Koruza 1.0 for scientific research. But for the operation under harsh climate conditions we needed a solution that would be more reliable and insensitive resistant to extreme weather conditions. We needed to change the material of a the pad, since the rubber disintegrates when exposed to UV radiation. Polyurethane has proved to be very suitable for this application. We used the technology of baking the polyurethane sealing mass onto an aluminium plate. A flexible pivot point was then achieved by cutting out the ring around the lens mounting, cutting out the aluminium and keeping the polyurethane sealing mass like shown in the picture 2.

[![koruza-dev]({{ site.url }}/post_files/koruza-pro-dev/koruza-dev-1.JPG){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/koruza-dev-1.JPG){: .img-open}
[![koruza-dev({{ site.url }}/post_files/koruza-pro-dev/koruza-dev-2.JPG){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/koruza-dev-2.JPG){: .img-open}

When we started working on the prototypes we encountered several problems:
- It is very difficult to coat aluminium plates when larger in size (over 500 × 500 mm), because they need to be heat treated in a curing oven which bends the aluminium in the process.

- We needed an even, about 2 mm thick coat of polyurethane on the aluminium, which was difficult to achieve with bigger plates and resulted in an additional step in a the manufacturing process since we needed to grind the polyurethane to achieve even thickness.

- Because of the very good bendable properties, polyurethane is not suitable for face milling. The production process is more expensive and longer because of this.

We are working on this problem with our local manufacturer of PU plates. One solution to prevent unwanted bending could be baking only plates of smaller dimensions or each piece separately.

We’ve found an additional use of polyurethane baked on aluminium plate. It can be used as a seal flange. We used this technology on the Turtle tag project where we sealed the acrylic enclosure, reducing the need for special made gaskets. A big advantage of it when prototyping is that the lid with polyurethane can be cut in-house from a bigger plate, whereas silicone seals must be custom made.

[![koruza-dev({{ site.url }}/post_files/koruza-pro-dev/turtle-tag-enclosure.JPG){: .img-full}]({{ site.url }}/post_files/koruza-pro-dev/turtle-tag-enclosure.JPG){: .img-open}












