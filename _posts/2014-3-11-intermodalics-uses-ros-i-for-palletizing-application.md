---
author: Guest User
comments: false
date: '2014-03-25 20:13:38+00:00'
slug: 2014-3-11-intermodalics-uses-ros-i-for-palletizing-application
title: Intermodalics Uses ROS-I for Palletizing Application
media_type: None
description: '[Intermodalics](http://www.intermodalics.eu/) is currently developing
  a depalletizing application for a client. The goal is to move an average of ...'
layout: post
old_sp_link: https://rosindustrial.org/news/2014/3/11/intermodalics-uses-ros-i-for-palletizing-application
tags: intermodalics ros ros-i robot industrial-robot palletizing
---

[Intermodalics](http://www.intermodalics.eu/) is currently developing a depalletizing application for a client. The goal is to move an average of 2,000 crates per hour from standard pallets to a conveyor belt. Additional challenges include: more than 10 different crate types can occur in varying colors, the crates are not necessarily empty and they are randomly stacked.

The application consists of a UR10 robot from [Universal Robots](http://www.universal-robots.com/), a 3D camera, an [Intermodalics Intelligent Controller](http://www.intermodalics.eu/services) (IIC) and an active pallet lift. The software for the application running on the IIC extensively uses [ROS](http://www.ros.org/) and the [OROCOS](http://www.orocos.org/) toolchain. OROCOS is a software framework for realtime, distributed robot and machine control which is seamlessly integrated with ROS and has both Industrial and Academic users worldwide.

For finding the crates' position and orientation, Intermodalics developed a crate localizer that builds upon the [PCL](http://www.intermodalics.eu/) library as well as on a set of in-house developed point-cloud processing algorithms. The ROS visualization tool [RViz](http://wiki.ros.org/rviz) proved absolutely invaluable during the realization of this product locator.

The use of the [ROS-Industrial](http://rosindustrial.org/) package for the UR robot allows both the motions and the application state machine to be simulated. This significantly facilitates the implementation of the whole application.

The integration of the UR controller and the IIC does not affect the inherent safety feature of the UR robot which makes the robot stop if it encounters excessive forces. If such a stop occurs, the application can be easily restarted by a simple human operator intervention.

Blog post provided by Bert Willaert of Intermodalics.


