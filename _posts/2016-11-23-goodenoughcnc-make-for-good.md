---
layout: post
title: "GoodEnoughCNC - Make for Good!"
description: "In the last year we proved that low-cost CNC milling and plasma cutting is technically feasible and that our approach of a »suitcase kit« works - we lowered the entry step in digital manufacturing and made it possible practically everywhere around the world.  That is why we are now exploring options how to distribute more GoodEnoughCNC Hybrid machines globally to empower (also currently underserved) communities for local digital manufacturing. In this blog post we are sharing our plan for GoodEnoughCNC for the next period and inviting all interested to get involved."
category: GoodEnoughCNC
tags: [goodenoughcnc, hybridcnc, digital fabrication, distributed manufacturing, open source, open hardware, making]
---
{% include JB/setup %}


In the last year we proved that low-cost CNC milling and plasma cutting is technically feasible and that our approach of a "suitcase kit" works - we lowered the entry step in digital manufacturing and made it possible practically everywhere around the world.  That is why we are now exploring options how to distribute more [GoodEnoughCNC Hybrid](http://goodenoughcnc.eu/hybrid-cnc/){:target="_blank"} machines globally to empower (also currently underserved) communities for local digital manufacturing. In this blog post we are sharing our plan for [GoodEnoughCNC](http://goodenoughcnc.eu/hybrid-cnc/){:target="_blank"} for the next period and inviting all interested to get involved. 

First, you can read a quick introduction into GoodEnoughCNC Hybrid, find out more about this open hardware machine and what was achieved with it in the last year. Then, we present the benefits of digital fabrication and the potential of distributed manufacturing for development countries, followed by a GoodEnoughCNC project plan overview for the next year. We will in collaboration with partners create a complete digital manufacturing pipeline for the production of useful solutions for the specific **shelter, thermal, water, waste, grow and electrical supply challenges**, which have the potential to significantly improve lives of underserved communities. For this purpose we will first identify the specific needs and corresponding open hardware solutions, then optimize the solutions for digital manufacturing, further improve GoodEnoughCNC and optimize it for the chosen use-cases, extensively document everything for effective know-how transfer and find ways to distribute more GoodEnoughCNCs to underserved communities and empower them for local manufacturing.

<h3>GoodEnoughCNC – What and Why?</h3>

Imagine having access to the tools and machines anywhere around the globe to build the things you need most?  Combining open hardware digital manufacturing tools and the power of collective open source knowledge and innovation this is possible. Now, one can connect with the international community of makers and get all the information and necessary knowledge to then build the machines and useful products locally.

GoodEnoughCNC machines are contributing to this paradigm shift in manufacturing by significantly lowering the entry barrier into digital manufacturing, offering an affordable baseline solution for companies and makers alike to create or improve their machining capabilities anywhere around the world and be able to produce useful objects.

Combining the best of open hardware solutions and innovating on the use of generally available standard parts, plus making sure any heavy parts - stock steel tubing- can be sourced locally, HybridCNC was developed. It is simple enough to construct for anyone requiring it, using only basic hand and power tools.

[![make-for-good]({{ site.url }}/post_files/make-for-good/making.jpg){: .img-half}]({{ site.url }}/post_files/make-for-good/making.jpg){: .img-open}
[![make-for-good]({{ site.url }}/post_files/make-for-good/goodenoughcnc-4.JPG){: .img-half}]({{ site.url }}/post_files/make-for-good/goodenoughcnc-4.JPG){: .img-open}

<iframe width="94.5%" height="360" src="https://www.youtube.com/embed/xZScY8QE78s" frameborder="0" allowfullscreen></iframe>

HybridCNC is a manufacturing baseline for CNC milling, plasma and laser cutting, with good enough precision for what an average maker needs. By introducing a [TolsinkCNC](https://github.com/IRNAS/ToslinkCNC){:target="_blank"} to our machine, an innovative, simple and low-cost plastic fibre optic CNC control system, as an answer to grounding and interference issues commonly experienced with DIY and low-cost CNC machines, robustness was achieved in all use-cases,  even with high voltage plasma cutting application.

**GOODENOUGHCNC Key advantages:**

**- simplicity of design,**

**- globally reproducible,**

**- affordable, entry level solution,**

**- modifiable and maintainable anywhere.**

---

<h3>Digital fabrication explained</h3>

To quickly recap for everyone not familiar with digital fabrication – [Opendesk](https://www.opendesk.cc/about/digital-fabrication){:target="_blank"}’s definition explains it very simply: Digital fabrication is a type of manufacturing process where the machine used is controlled by a computer. There are a huge range of digital fabrication techniques, but the important aspect that unifies them is that the machines can be programmed to make consistent products from digital designs. That means that when you have a design of a product ready it can be downloaded and made, reliably and repeatably as many times you want, all over the world, without a maker needing to have specialist equipment.

We know additive and subtractive digital manufacturing techniques, where the additive process deposits the material where the object is and the subtractive process takes away where the object isn’t, with the most common forms being:

- **CNC Machining:** a subtractive technology where shapes are cut out, typically out of wooden sheets

- **3D Printing:** an additive technology that builds a product from the bottom up, layer by layer 

- **Laser Cutting:** a subtractive technology where materials like metal or wood are burnt or melted by a laser beam

[![make-for-good]({{ site.url }}/post_files/make-for-good/3dprinting.JPG){: .img-half}]({{ site.url }}/post_files/make-for-good/3dprinting.JPG){: .img-open}
[![make-for-good]({{ site.url }}/post_files/make-for-good/goodenoughcnc-plasma-cutting.jpg){: .img-half}]({{ site.url }}/post_files/make-for-good/goodenoughcnc-plasma-cutting.jpg){: .img-open}

We can optimize and simplify the manufacturing process, achieve best results and be most effective at our work by combining different digital manufacturing tools, using the technique most suitable for the material we’re working with and the shape we want to create. When having a 2D design we would use subtractive method to cut or mill the shapes out and then build them into a 3D object, when for instance creating a piece of furniture or a house. Whereas with the 3D printing a very complicated 3D objects can be printed out in the desired shape directly by adding layers of material. One can even print out in a single piece an object that would otherwise have to be manufactured in several parts and then assembled.

To better illustrate this process of digital manufacturing, let’s take for an example our HybridCNC machine - all the metal parts can be in this case made the easiest using CNC plasma cutter whereas the connecting components (like linear guide mount for example) can be printed out in one piece. 

Combining several techniques you can really make almost anything!

---

<h3>Distributed manufacturing as a paradigm changer for developing countries</h3>

[Development researchers](https://www.jica.go.jp/jica-ri/publication/other/jrft3q0000005yj3-att/TransformativeInnovation.pdf){:target="_blank"} are recognizing that digital manufacturing together with fablabs might not solve every problem in low-income areas, but it is clear that they have the potential to strengthen local innovation eco-systems in the developing world since they offer specific technological infrastructure that support “contextualized innovation“ and a custom approach to local challenges, which reflect the ideas, designs, and needs of their makers. It can serve as stimulus for local entrepreneurship while enabling positive local spillover effects as well as the opportunity to connect with the broader global innovation community and open collective knowledge to come up with low-cost solutions to their local challenges. With digital fabrication people around the world no longer need to rely on complex supply chains and long distance shipping to get the products they need, but can with the power of internet and open source principles download the designs and manufacture the products locally as well as customize them depending on the specific needs and availability of local talent and materials.

A positive example of local digital manufacturing comes from largely rural and agricultural Bohol, Phillipini where the fab lab serves as a platform for creation and collaboration that has enabled local people and businesses to innovate new products, add value to existing ones and generate new streams of income (for example local chocolate entrepreneur and a local cooperative making water buffalo soap have used the machines to develop efficient and creative molds for their products, increasing distribution opportunities and profits). As well, they are creating upcycled fabrication materials from plastic waste to address the difficulty of recycling in that area, they also built a WikiHouse, which now serves as a day-care facility in an earthquake-affected area and experimented with making affordable prosthetics for amputees demonstrating the lab’s potential for enabling low-cost solutions to community needs.

Another important benefit of the use of 3D printing and CNC machining is affordable and local manufacturing of spare parts. This is enabling local repair of machines, since it is well known that a large number of donor-funded machines and facilities in developing countries are not functional due to lack of spare parts.

A very interesting and promising usage of digital fabrication we recognized talking to several people from India and elsewhere could also be the use of CNC for the production of windmill turbine blades from wood stock as there is a significant number of building operations in remote locations, which are now using only very basic tools, and could take advantage of cnc machining to simplify the production process.

---

<h3>Bringing manufacturing capabilities anywhere around the world!</h3>

Whereas 3D printers are already widely used all around the world due to their increasing affordability it is not the same for CNC machines, which are still relatively expensive, difficult to ship and subject to high import duties (some developing countries may charge significant, up to 60% import duties on products and machinery).

We have tackled this problem by developing a CNC machine, which can be shipped anywhere around the world as easily as any 3D printer. All essential parts for Hybrid CNC can be packed in a ["suitcase"](http://fabrikor.eu/goodenoughcnc-hybrid/goodenoughcnc-hybrid-suitcase-kit){:target="_blank"}  whereas the heavy and long components – steel tubing for the machine frame – can be sourced locally in most of the cases. This is optimal as it reduces the supply chain issues at the user side and is size and weight minimal, such that it can be mailed or taken on a plane as a carry-on. The machine can then be assembled at the location with the use of basic hand and power tools. We tested it and it works – during last year [Hybrid CNC was reproduced in this fashion in Nepal](http://irnas.eu/goodenoughcnc/2016/09/12/goodenoughcnc-empowering-nepal-community){:target="_blank"}, India and several western countries.

[![make-for-good]({{ site.url }}/post_files/make-for-good/goodenoughcnc-kit.JPG){: .img-half}]({{ site.url }}/post_files/make-for-good/goodenoughcnc-kit.JPG){: .img-open}
[![make-for-good]({{ site.url }}/post_files/make-for-good/goodenoughcnc-in-a-suitcase.jpg){: .img-half}]({{ site.url }}/post_files/make-for-good/goodenoughcnc-in-a-suitcase.jpg){: .img-open}

[![make-for-good]({{ site.url }}/post_files/make-for-good/goodenoughcnc-nepal-10.jpg){: .img-full}]({{ site.url }}/post_files/make-for-good/goodenoughcnc-nepal-10.jpg){: .img-open}

A team of local developers who has built [HybridCNC from a suitcase kit in Nepal](http://irnas.eu/goodenoughcnc/2016/09/12/goodenoughcnc-empowering-nepal-community){:target="_blank"} is now using it in post-earthquake rebuilding efforts. They are also manufacturing hospital bed parts with it and offering plasma cutting services to local hardware companies, as well as using it to circulate the CNC knowledge around the country. 

Another suitcase kit was carried to India, where they will use it in an educational/manufacturing setup to create wind turbine blades as well as teach about CNC machine operation and design.

---

<h3>What comes next?</h3>

Having a proof that low-cost CNC milling, plasma cutting is technically feasible and that our approach of a "suitcase kit" works, we are now exploring options how to distribute more machines globally to empower communities for local digital manufacturing.

We believe the next step to take is to shift the narrative - from the machines themselves to the useful and impactful products, which can be manufactured with these machines in the simplest possible way. 

Since only having a tool is never enough we want to achieve an effective know-how transfer by taking a »Lego« approach to digital fabrication, meaning that we are providing not only the machine (which is fully and openly documented and self-replicable) but also guidelines on how to use it to manufacture various different solutions for real life challenges. That’s how we want to show the full potential of digital fabrication, teach about the possibilities, enable the production of very useful products from the very beginning and achieve extensive understanding of manufacturing process to further spark local experimentation and innovation.

We are now establishing partnerships with organizations and communities around the world to create a complete digital manufacturing pipeline - from the specific local needs, open hardware designs, use of CAD and CAM software & digital manufacturing tools to useful solutions.
 
To achieve this we’ll together with our partners first determine 6 key challenges, then find matching open hardware projects, test, modify, upgrade and optimize the solutions for digital fabrication, optimize HybridCNC for these use-cases, document everything and transfer the know-how.

**Step 1: Learn about the conditions and needs in the field to respond to specific local challenges**

We want to get a good understanding of what is happening on the ground to identify the real challenges communities in different parts of developing world and post disaster zones are facing. With your help we we want to pick 6 open hardware projects, which are solving a specific shelter, thermal, water, waste, grow and electrical supply challenge for which we’re going to optimize HybridCNC, develop and document a complete pipeline from design to finished products to ensure easy and effective local replication.


__Goal:__ *Established relationships with partner organizations active on the field with identified solutions to the challenges*

**Step 2: Optimize open hardware solutions to identified challenges**

In this stage we will collaborate with current best practitioners on the field to optimize 6 open hardware solutions for digital manufacturing. An example of an open hardware project, which could be optimized for CNC manufacturing, is windmill turbine since there is already a significant number of building operations in remote locations, where there are using only very basic tools. 

__Goal:__ *Optimized solutions for digital manufacturing*

**Step 3: Hybrid CNC development and upgrades and optimization of the machine for use cases**

We will further improve the design of Hybrid CNC for maximal reliability and reproducibility and making an important upgrade to our robust Toslink CNC control system as well as modify the machine for effective production of open hardware designs defined in step 2. Over the past year of using GoodenoughCNC we have learned that further simplification is design is possible, reducing the number of different screws, making the metal parts simpler and improving the long term reliability with dust guards, further making the electronics more robust and a number of other things suggested by users.

__Goal:__ *Optimized version of the machine*

**Step 4: Testing, QA & Documenting**

To ensure effective production on the machine we need to extensively test it in different scenarios.  Hybrid CNC is already fully documented but we will need to modify and further improve the step by step building instructions after the upgrades and changes made as well as include the instructions on how to test and use the machine with different tools.

__Goal:__ *Published test results and open source documentation with instructions on how to build, test, use and troubleshoot Hybrid CNC.*

**Step 5: Useful and open source documentation of a complete manufacturing workflow**

Complete documentation of the manufacturing process workflow  - from open hardware designs to instructions on how to use CAD & CAM software tools and Hybrid CNC machine for the manufacturing of the open hardware solutions defined in Step 2.

__Goal:__ *Published documentation of complete manufacturing workflow*

**6. Make it good! - Transfer of the technology and know-how**

We'll distribute the machines through different channels – distribution through partner organizations with online support, selling to individuals with online support, GoodEnoughCNC Academy on the location. In each case the users will get the GoodEnoughCNC Hybrid kit and all the required know-how to effectively use the machine.

We'll distribute the machines through different channels – distribution through partner organizations with online support, selling to individuals with online support, GoodEnoughCNC Academy on the location. In each case the users will get the GoodEnoughCNC Hybrid kit and all the required know-how to effectively use the machine.

GoodEnoughCNC Academy will be designed specifically for organizations and makers working in developing countries and post disaster zones to acquire extensive knowledge about digital fabrication with GoodEnoughCNC. They will not only learn how to build the machine to then replicate it on their location but also learn how to locally establish the production of open hardware solutions established in Step 2. 

__Goal:__ *Ensured financing for the distribution of machines through partner organizations + established online and offline selling channels. Overall goal - at least 200 replications globally.*

Everyone interested in empowering for making and making for empowerment is invited to join us on this journey of creating an effective open source pipeline solution – from open-hardware designs and local digital manufacturing to useful solutions for the real life challenges –  and bringing the benefits of open source and distributed manufacturing to currently underserved communities. We are searching for partners, who have the extensive understanding of the situation in developing countries and disaster zones, organizations, companies and makers with the experience in development and production of open hardware solutions improving quality of life (windmill turbines, water filters, shelters, etc.) as well as CAM/CAD software providers and organizations providing financial and other support for the development activities around the world, to together form a consortium, which will have the capacities to bring the benefits of open source and distributed manufacturing around the globe. Please, get in touch to discuss collaboration possibilities and share this blog post with anyone who might be interested in getting involved in this initiative. We really appreciate your help!








