---
author: Shaun Edwards (SwRI)
comments: false
date: '2014-07-03 02:59:56+00:00'
slug: 2014-6-30-ros-industrial-update
title: ROS-Industrial Update
media_type: None
description: The ROS-Industrial team has been very busy developing new functionality
  that I am very excited to share with you.
layout: post
old_sp_link: https://rosindustrial.org/news/2014/6/30/ros-industrial-update
tags: ros ros-i ros-inustrial ros-i-consortium shaun-edwards
---

The ROS-Industrial team has been very busy developing new functionality that I am very excited to share with you. 

ROS-Industrial Hydro Release!
-----------------------------

We officially released a few ROS-Industrial packages about six months back, and released the final package just a couple of months ago. A brief description of the new features/updates can be found [here](http://wiki.ros.org/Industrial/Roadmap#Hydro_Release). It's now possible to install from debians: *sudo apt-get install ros-hydro-industrial-desktop*. More detailed instructions can be found [here](http://wiki.ros.org/Industrial/Install). We typically lag ROS releases to ensure stability, but the switch to [catkin](http://wiki.ros.org/catkin) really delayed us. It feels like we transitioned to catkin twice, first to get source builds working and then a second time to get debian builds working. Having put the port to catkin behind us, I'm confident we will do better next release.

Robot Vendor Package Support
----------------------------

Early ROS-Industrial development was focused on developing robot specific [drivers](http://wiki.ros.org/Industrial#Vendor_Specific_Stacks). Some of these packages were developed from scratch, such as the [Fanuc](http://wiki.ros.org/fanuc) package, developed by [TUDelft](http://www.robotics.tudelft.nl/) and others were *acquired* as orphaned projects. In order to ensure the continued development and maintenance of these drivers, we are reaching out to the community for help. Recently, [Fraunhofer IPA](http://www.ipa.fraunhofer.de/index.php?L=2) has taken ownership of the [Universal Robot](http://wiki.ros.org/universal_robot). We appreciate the help of both TUDelft and IPA. We are actively looking for developers/maintainers for our other driver packages (if you are interested send an email to this [developers list](http://swri-ros-pkg-dev@googlegroups.com)).

Google Summer of Code
---------------------

We are participating in the Google Summer of Code ([GSoC](https://www.google-melange.com/gsoc/homepage/google/gsoc2014)) under the [OSRF](http://osrfoundation.org/) umbrella. GSoC pays students to perform open source development. ROS-Industrial has two projects: a cartesian planner GUI plugin for MoveIt ([repo](https://github.com/ros-industrial-consortium/fermi)) and an intuitive 3D interface for industrial painting ([repo](https://github.com/ros-industrial-consortium/galileo)). We are very excited to be part of this awesome program and are looking forward to what our students come up with. Stay tuned for posts from our students.

Special Thanks to the Community
===============================

It's no secret that ROS-Industrial is a community effort. I'm very proud to say that ROS-Industrial receives contributions from some of the best academic, research, and commercial organizations from around the world. Our current [stats](https://www.ohloh.net/p/ros-industrial) have us at 24 contributors in the last year and that's not even counting those who participate in code reviews and submit issues. I can honestly say I've worked with some of the greatest developers in my career through the ROS-Industrial program.


