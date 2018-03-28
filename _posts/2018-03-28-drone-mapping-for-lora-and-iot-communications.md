---
layout: post
title: "Drone Mapping for LoRa and IoT Communications"
category: Other Projects
tags: [IRNAS, The Things Network, LoRaWAN, Drone mapping, TTN, TTN mapper]
---
{% include JB/setup %}


In the last decade drones and Unmanned Aerial Vehicles (UAVs) in general have proven to be one of the great technological developments with a range of applications from recreational hobby use to commercial applications such as monitoring, parcel delivery and filming. UAVs are very useful to capture high quality aerial data at affordable cost compared to alternative approaches, resulting in development of several 3D and elevation modelling applications. The IoT low-power long-range networks, that have recently become very useful in various applications, have a common problem of a challenging mapping and difficult understanding of coverage in more complex scenarios, which would allow for effective deployments at a scale.

Gateways in LoRa and LoraWAN networks are the interface between a large area with a significant number of nodes and the cloud. There are a number of scenarios for network coverage provisioning, ranging from public gateway infrastructure to dedicated gateways for specific project and private networks for a particular deployment or a scale deployment of pico gateways. The common factor when rolling out a reliable network is understanding the existing coverage in a given area and determining what coverage has been achieved once gateways have been deployed.

[![]({{ site.url }}/post_files/drone-mapping/drone-mapping.jpg){: .img-full}]({{ site.url }}/drone-mapping/drone-mapping.jpg){: .img-open}

Thus, we have developed an automated drone mapping solution, useful for evaluation of the performance of gateways to determine the exact coverage and to understand the effect of the environment on the signal coverage. The developed solution, consisting of both hardware and software components, can be applied to any mid-size, widely available drone with the sufficient flight stability and autonomous flight support.

Thus, we have developed [an automated drone mapping solution](http://irnas.eu/iot-drone-mapping){:target="_blank"}, useful for evaluation of the performance of gateways to determine the exact coverage and to understand the effect of the environment on the signal coverage. The developed solution, consisting of both hardware and software components, can be applied to any mid-size, widely available drone with the sufficient flight stability and autonomous flight support.

In the particular set-up a drone mapper - LoRaWAN compatible device, sending regular transmissions, pushed to the [TTN mapper](https://ttnmapper.org/){:target="_blank"} application for the later analysis - is attached to the drone, DJI Mavic Pro. Drone path in the form of concentric circles at a fixed height for coverage mapping, or a sphere around the antenna for pattern measurement, is generated before the flight by selecting specific mapping location. LoraWAN gateway is connected to the [The Things Network](https://ttnmapper.org/){:target="_blank"} system and uses the TTN mapper site to collect measurements in real-time.

[![]({{ site.url }}/post_files/drone-mapping/drone-mapping-1.jpg){: .img-full}]({{ site.url }}/post_files/drone-mapping/drone-mapping-1.jpg){: .img-open}

Once the flight is completed flight log from the drone and signal log from the TTN mapper are used to create the coverage map and antenna pattern.  Obtained drone measurement data consisting of GPS longitude, latitude and altitude position, time-stamp and other flight parameters, needs to be combined with the TTN mapper measurement log containing data on received signal and time. Based on the two flight modes drone path is either a 2D mesh at the same altitude around the antenna, or a 3D sphere mesh with the antenna at its central position. 

<h3>2D coverage</h3>

Gateway coverage in 2D is most applicable when determining and planning the coverage for a range of devices in a certain area, either connected to one or multiple gateways. When imported into GIS software one can observe effects of the environment, such as shadowing of the trees and other obstacles as well as the coverage contributions of individual gateways.

[![]({{ site.url }}/post_files/drone-mapping/drone-mapping-2d-coverage-1.png){: .img-half}]({{ site.url }}/post_files/drone-mapping/drone-mapping-2d-coverage-1.png){: .img-open}
[![]({{ site.url }}/post_files/drone-mapping/drone-mapping-2d-coverage-2.jpg){: .img-half}]({{ site.url }}/post_files/drone-mapping/drone-mapping-2d-coverage-2.jpg){: .img-open}

<h3>Antenna radiation pattern</h3>

The 3D spherical data is used to determined 3D antenna radiation pattern and corresponding x-y azimuth plane cut and the x-z elevation plane cut. Data is first filtered, eliminating all measurement points during landing stage that could alter the result and then converted to spherical coordinates for further analysis. Signal values are normalised. All points are assumed to be located on a surface of a sphere thus having constant radius, where all points located outside set tolerance bound are discarded. Measured signal is then interpolated on a spherical mesh, then a 3D surface plot can be produced, using interpolated polar and azimuthal angles and signal as the radius. 

[![]({{ site.url }}/post_files/drone-mapping/3D_antenna1.png){: .img-half}]({{ site.url }}/post_files/drone-mapping/3D_antenna1.png){: .img-open}
[![]({{ site.url }}/post_files/drone-mapping/3D_antenna2.png){: .img-half}]({{ site.url }}/post_files/drone-mapping/3D_antenna2.png){: .img-open}

[![]({{ site.url }}/post_files/drone-mapping/pattern1.png){: .img-half}]({{ site.url }}/post_files/drone-mapping/pattern1.png){: .img-open}
[![]({{ site.url }}/post_files/drone-mapping/pattern2.png){: .img-half}]({{ site.url }}/post_files/drone-mapping/pattern2.png){: .img-open}

Luka talked about Drone assisted deployment and mapping in remote areas for animal conservation purposes at [The Things Network Conference](https://www.thethingsnetwork.org/conference/){:target="_blank"} in Amsterdam. Check the video below, find out more [here](http://irnas.eu/iot-drone-mapping){:target="_blank"} and get in contact if you are looking for drone mapping technology expertise

<iframe width="94%" height="315" src="https://www.youtube.com/embed/v5_CT-1VuV4?rel=0&amp;controls=0" frameborder="0" allowfullscreen></iframe>




