---
layout: post
title: "KORUZA router design"
description: ""
category: KORUZA
tags: [KORUZA, KORUZA Pro, Development, Mounting system]
---
{% include JB/setup %}


[KORUZA](http://koruza.net/){:target="_blank"} wireless optical system enables 1Gbps or 10Gbps communication with a collimated beam of light between two buildings. To interface and power the units, networking ports are required, we looked at a number of practices from various vendors. For throughputs up to 1Gbps the standard interface is wired RJ-45 ethernet. WiFi routers and other networking devices are often powered through the network cable itself with either passive PoE at 24V or active 48V PoE. [Wireless optical links by other manufacturers](https://github.com/IRNAS/FSO-systems){:target="_blank"} have a varied array of interfaces, some have the management interface and data link ports separate just as in KORUZA 1.0, thus operating as a transparent network bridge at Layer 1. While this is the most practical in many cases, it requires two network cables to the unit itself and separate management and routing networks. 

The main application of [KORUZA Pro](http://new.koruza.net/){:target="_blank"} is last-mile networking and as such we wish to simplify the installation process and make the units most practical. To best support a number of different configurations and have versatile connectivity options, we consider the following examples:

**KORUZA as an ethernet bridge: building-to-building**

KORUZA units are installed on two buildings and pointed at each-other. A cable from the networking cabinet/location is run to the outside and the unit is connected. For the 1Gbps version  power, data and management are best delivered via a single ethernet cat 6 cable. The 10Gbps system is more demanding, as we can either use only SFP direct attach cables to distances of up to about 7m, or must use fiber optic connections. In either case the power must be delivered to the unit with a cable, the simplest option is an ethernet cable. Currently, the routers capable of routing 10 Gbps, are rather expensive, therefore installing them in KORUZA Pro units would not be feasible. For that purpose it is best to make the 10 Gbps data path, a direct Layer 1 system via a SFP port, and management and power are delivered over ethernet and can be placed on a separate network.

- 1Gbps requirements: 1x ethernet port with PoE

- 10Gbps requirements: 1x ethernet port with PoE + 1x SFP port

**KORUZA as an ethernet bridge with backup: building-to-building**

For most demanding applications we may wish to have a backup link with WiFi for example, or actually have one link in place already and wish to add more capacity with KORUZA Pro. For the 1Gbps version we can use the KORUZA router to perform routing and automatic switching between links in all the cases. For this we require two wired ethernet ports, one delivering power, management and data to KORUZA and another from KORUZA to the WiFi device, delivering data and power. 

With the 10Gbps we are limited to the Layer 1 operation on the data link, however a WiFi backup option can still be employed via the KORUZA router, limiting the number of required cables going to the roof and simplifying installation.

- 1Gbps requirements: 2x ethernet port with PoE in and out

- 10Gbps requirements: 2x ethernet port with PoE in and out + 1x SFP port

**KORUZA as in last-mile mesh**

One of the most interesting applications is expanding the reach of wired fibre optic networks with KORUZA, quickly and effectively covering larger areas with ultra-fast broadband. In such a configuration, a multi-hop network is typically set up between customers, either branching out or in a loop, or some other more closed topology. This is most practical with the 1Gbps version as there is no additional cost of routing equipment, which is required with the 10Gbps system. An example configuration would be for each point in the network to have two KORUZA units connected between each-other and splitting off a portion of the total capacity to the user on a given location. To connect the user, the best option is definitely a wired one and placing an access point within the house. Should that be too difficult, the access point can also be placed outdoors next to KORUZA and simply power needs to be applied on the outside of the house.

- 1Gbps requirements: 3x ethernet port with PoE in and out

- 10Gbps requirements: 1x ethernet port with PoE + 1x SFP port

**Alternative uses of the router**

The current lack of open hardware routing solutions with complete openwrt support gives rise to alternative uses of this router in wireless networks and WISP configurations, most notably having one SFP port for isolation from the rest of the network to limit electrostatic damages,, as well as to have a versatile powering configuration, to best integrate with the network infrastructure itself. Thus we envision the router itself to be separate from the power board which can be adapted for many different PoE configurations and even extended with a battery for backup, which leaves the hands open to users to extend and improve on the basic platform.

**Complete router design**

To best satisfy the user requirements and scenarios, we have used the Mqmaker WiTi open hardware router as a reference design and prepared specifications available for comments for a new design. We have split it up into three individual boards, namely: main router board with 4x ethernet RJ-45, 2x SFP port (one internal for KORUZA and one external for connecting devices), power board for PoE electronics, regulation and other features and via an GPIO header an expansion, target specific board that can host co-processors such as Raspberry Pi or similar. We invite you to view our github repository with the requirements and comment on them.

[![koruza-application]({{ site.url }}/post_files/koruza-pro-dev/koruza-graphic-1.png){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/koruza-graphic-1.png){: .img-open}
[![koruza-application]({{ site.url }}/post_files/koruza-pro-dev/koruza-graphic-2.png){: .img-half}]({{ site.url }}/post_files/koruza-pro-dev/koruza-graphic-2.png){: .img-open}






