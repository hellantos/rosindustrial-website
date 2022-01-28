---
author: Guest User
comments: false
date: '2014-12-10 15:54:16+00:00'
slug: 2014-12-10-demonstration-of-the-fraunhofer-ipa-ros-i-driver-for-yaskawa-motoman-dual-arm-robots
title: Demonstration of the Fraunhofer IPA ROS-I Driver for Yaskawa Motoman Dual Arm
  Robots
media_type: None
description: 'Submitted by: Thiago de Freitas and Ulrich Reiser, Fraunhofer IPA'
layout: post
old_sp_link: https://rosindustrial.org/news/2014/12/10/demonstration-of-the-fraunhofer-ipa-ros-i-driver-for-yaskawa-motoman-dual-arm-robots
---

Submitted by: Thiago de Freitas and Ulrich Reiser, Fraunhofer IPA

Under the cooperation between Fraunhofer IPA, Yaskawa Smart Robotics Center in Japan and Yaskawa Motoman Robotics, a ROS-I driver to support multi-groups control for the Motoman Robots was developed.

The first industrial dual-arm manipulator to run the driver was the Motoman SDA10F with an FS100 controller. 
The driver provided the capability for generating synchronous and asynchronous movements from the ROS side that could be send to the FS100 controller and then executed by the real robot groups (left arm, right arm and torso). Also, support packages were setup including driver configuration files, URDF and MoveIT! configuration files.

The driver was also demonstrated during ROSCON 2014, using a Motoman BMDA3 robot. [Remarkably, the driver worked with the hardware despite the SwRI software team never having access to the hardware prior to the event.] The demo was organized by Yaskawa Motoman and SwRI.

![Erik Nieves (Yaskawa Motoman USA) Grooves with&nbsp;the BMDA3 at ROSCon 2014 in Chicago](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1418225857184-21TPWLVC2GJ3TFNKMCY2/Erik+w+BMDA3)

Figure: *Erik Nieves (Yaskawa Motoman USA) Grooves withthe BMDA3 at ROSCon 2014 in Chicago*

![Paul Hvass (SWRI/ ROS-Industrial Consortium PM) "running" with the BMDA3](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1418225905363-A9ZJZSS5U4BW1DCZ9VGS/IMG_1896.JPG)

Figure: *Paul Hvass (SWRI/ ROS-Industrial Consortium PM) "running" with the BMDA3*

Some tutorials are recommended for getting a better overview of the driver usage and system configuration:

* [Installation procedure](http://wiki.ros.org/motoman_driver/Tutorials/indigo/InstallServer)
* [Creating a dual-arm system](http://wiki.ros.org/motoman_driver/Tutorials/Creating%20a%20Dual-Arm%20System)
* [Dual-arm system example](https://github.com/ros-industrial/motoman/tree/hydro-devel/motoman_sda10f_moveit_config)

Some additional information:

* The initial release is a [source-only](https://github.com/ros-industrial/motoman/tree/hydro-devel) release for Hydro. The Indigo Binary Release is going to follow in Q1 2015.
* Please direct your public questions to the ROS-I developers list ([swri-ros-pkg-dev@googlegroups.com](http://swri-ros-pkg-dev@googlegroups.com))

