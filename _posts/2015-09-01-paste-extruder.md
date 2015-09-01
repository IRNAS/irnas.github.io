---
layout: post
title: "High precision ceramic paste extruder"
description: "High precision ceramic paste extruder design update."
category: 
tags: []
---
{% include JB/setup %}

Ceramic objects are waterproof, very rigid, stiff and able to stand extremely high temperatures, which gives them a wide spectrum of applicability. Mostly one associates ceramic with tableware (plates, cups, vases etc.) however, ceramic is, due to its robustness, often used for other much more subtle applications. 

Combining ceramic material properties with 3d printing technology allows creating stiff and rigid structures of any shapes and sizes (of course, limited to the technology). Recently, ceramic began to be used as a biomaterial for printing bone and tooth tissue and also implants, which opened a whole new horizon to medicine. With this in mind it is obvious that ceramic 3D printing often requires extremely high precision, which is a complicated, very hi-tech procedure, that is hard to achieve with current technology.

Ceramic can be printed using various [technologies](http://www.jbioleng.org/content/9/1/4) (Stereolitography, selective laser sintering, 3D plotting etc.). There are numerous high precision ceramic 3D printers available on the market that reach the precision standards but cost between tens of thousands of dollars up to a few hundred thousand dollars. High precision technologies usually require several different tools that are all embedded into a system which machine the ceramic to its final, polished, ready-to-use stage.  These processes are very sophisticated and it would be a big challenge making them low cost. 

3D plotting in this case is an exception as it is based on extruding liquid (or paste) materials from a syringe to create desired 3D objects. Paste extrusion is meant to be a technology where a 3D printed object always needs post processing (heating it up to very high temperatures). This technology also often gives lower resolution than others mentioned above. 

At IRNAS our goal and challenge are (as always) to combine high precision and robustness with low cost. For this the [MiniCNC]({{ site.url }}/2015/08/28/mini-cnc/) mechanics will be used where spindle will be replaced by the paste extruder. We spent a few weeks developing a prototype of a paste extruder.
 
Ceramic paste is produced by mixing a type of ceramic powder (Zirconia, Alumina etc.) with a binder, stiffener and propan-2-ol, making a liquid solution. Once the solution is well stirred, the propan-2-ol is evaporated until a dense paste-like texture is achieved. It is then loaded into a syringe which is later attached to the extruder of the 3D printer. The paste extrusion is controlled via stepper motor which rotates a threaded rod. This gives us a very accurate translational movement mechanism ([example](http://www.thingiverse.com/thing:539490)).

Because of high pressure required during the process plastic syringes are not adequate. Instead, metal syringes are supposed to be used however they cost 300$-500$ on the market. We avoided this issue by purchasing a 40$ of-the-shelf pneumatic cylinder and modifying it so that it works like a syringe, extruding paste through a stainless steel nozzle. In the near future we will optimize its performance even further.
Main features: 

 * Attachable to MiniCNC framework,
 * Robust, accurate,
 * Can be driven from the same stepper controller as MiniCNC as the 4th axis.
 
The first prototype was machined out of MDF wood using a CNC drill.

![paste-extruder]({{ site.url }}/post_files/paste_extruder/img1.png)
![paste-extruder]({{ site.url }}/post_files/paste_extruder/img2.png)

Future steps:

 * We will modify the cylinder to enable easy (re)fill.
 * We will tweak the mechanics to keep it robust but reduce weight and cost.
 * We will try to make the whole system easy to assemble, using only basic tools.
 
Due to high cost of ceramics, the extruder will first be tested using chocolate cream and other substances that have similar texture as the ceramic paste.


 
