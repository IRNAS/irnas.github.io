---
layout: post
title: "Useful source implementation DocuBricks and OpenPlant Open Technology Week Workshop"
description: "Participation in the Open Technology Week"
category: KORUZA 
tags: [Events, KORUZA]
---
{% include JB/setup %}

Open Technology Week is an annual effort of [OpenPlant](http://openplant.org) and [OpenLabTools](http://openlabtools.eng.cam.ac.uk/) initiatives of University of Cambridge to bring together scientists primarily with backgrounds in plant sciences and biology that use open hardware to conduct their experiments. We have been represented by Luka Mustafa who gave a talk on Repeatable replication and reliable operation of open hardware, introducing the basic concepts of [wireless optical system KORUZA](http://koruza.net) and other development projects through which the discussion on open hardware documentation quality has been opened with key points:

* Large number of open projects, few of good quality suitable for reliable reproduction
* A significant number of projects designed for scientific use fail to provide calibration methodology
* No well established methodology for creating high-quality open releases
* Every open hardware replication is a fork and thus unique

Earlier this year we have introduced the [Useful Source]({{site.url }}/2015/03/08/useful-source) concept addressing exactly these issues with the goal to introduce good practices enabling:

* Well-defined documentation flow from first information about the project to sources and replication instructions
* Automatic wizard-like tools for documenting a project with minimal effort
* Modularized design improving the understanding of the design and re-use in other projects
* Distinction between functions (logical parts) and their implementation (physical parts) such that replication is possible even with variations in part availability
* Designed for releasing and sharing stable releases

We have started the collaboration with a team from Cambridge that has devices [DocuBricks](http://docubricks.com) implementing the useful source vision to enable:

 * Implementation of useful source concept
 * Multi-level tree-structured XML based documentation of bricks consisting of
  * Functions (logical parts)
  * Implementations (physical parts or design files)
  * Documentation builder application for easiest use
  * Companion mobile app to track steps taken by the replicator for purpose of feedback and simple community based debugging
 * All documentation is offline and standalone such that can be version controlled through GitHub or similar
 * An online system creating a database of such releases with DUIs allocated to projects for citations and referencing in the scientific community
 * API for inclusion of documented projects in their home websites
 
Through ongoing development we are actively testing the system with our own projects as well as with collaborators from a number of different fields. We are aiming to release the first version of DocuBricks later this year.

Slides from Open Technology Week Workshop are [available here]({{site.url }}/downloads/presentations/OpenHardwareDay-2015-Koruza.pdf).



 
