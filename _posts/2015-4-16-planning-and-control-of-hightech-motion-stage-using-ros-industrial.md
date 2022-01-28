---
author: Guest User
comments: false
date: '2015-04-16 22:14:41+00:00'
slug: 2015-4-16-planning-and-control-of-hightech-motion-stage-using-ros-industrial
title: Planning and Control of High-Tech Motion Stage using ROS-Industrial
media_type: None
description: Alten Mechatronics, in cooperation with Bosch Rexroth and FEI, created
  a motion planner application for a 5-DOF motion stage in a Transmission ...
layout: post
old_sp_link: https://rosindustrial.org/news/2015/4/16/planning-and-control-of-hightech-motion-stage-using-ros-industrial
---

Alten Mechatronics, in cooperation with Bosch Rexroth and FEI, created a motion planner application for a 5-DOF motion stage in a Transmission Electron Microscope (TEM).

The application is a little outside the scope of other application of ROS-Industrial (i.e. robots), but the problems in these high-tech system can benefit hugely from advanced in robotics. In this case motion planning libraries from MoveIt! were implemented to generate collision free paths for the 5-DOF motion stage moving in a cluttered environment ([refer to our 20 October 2014 blog post](http://rosindustrial.org/news/2014/10/12/3umkjjpcdmnlilmo8uy4c2m6vj4m4m)).

Building on earlier simulations, the application was extend to control the physical hardware. For this a communication was set up between ROS and the motion controller of the motion stage: [The Bosch Rexroth NYCe 4000 motion controller](http://www.boschrexroth.com/en/xc/industries/factory-automation/semiconductor-and-electronics/products-and-solutions/electric-drives-and-controls/nyce-4000/index). A driver for this platform was created in accordance to the [simple message protocol](http://wiki.ros.org/simple_message), so that no development on the ROS side was needed: The NYCe controller acts as any other robot controller already supported by ROS-Industrial.

The result is application with ROS tooling (MoveIt!, RVIZ, etc.) and a high-tech motion platform able to plan and execute complex motions and increasing the speed of path execution with a maximum factor of 5 compared to current implementation.

More possibilities are open, like [optimizing paths](https://youtu.be/XOttWDxerMY) or planning constrained paths using the [Descartes planner](https://github.com/ros-industrial-consortium/descartes).


