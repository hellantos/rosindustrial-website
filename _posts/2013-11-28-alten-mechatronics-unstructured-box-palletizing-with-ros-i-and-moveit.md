---
author: Guest User
comments: false
date: '2013-12-05 11:28:46+00:00'
slug: 2013-11-28-alten-mechatronics-unstructured-box-palletizing-with-ros-i-and-moveit
title: Alten Mechatronics Unstructured Box Palletizing with ROS-Industrial
media_type: None
description: '[Alten Mechatronics](http://www.alten.nl/en/alten-mechatronics/), in
  collaboration with [CSi ...'
layout: post
old_sp_link: https://rosindustrial.org/news/2013/11/28/alten-mechatronics-unstructured-box-palletizing-with-ros-i-and-moveit
tags: ros ros-i ros-industrial alten-mechatronics csi-palletising
---


[Alten Mechatronics](http://www.alten.nl/en/alten-mechatronics/), in collaboration with [CSi Palletising](http://www.csiportal.com/en/palletisingsystems) systems, developed a demonstrator using an ABB IRB6640 robot to show that a system based on [ROS-Industrial](http://rosindustrial.org/) can easily cope with unknown products and uncertainties in the environment. Very little setup time was required for the actual hardware.

Two pallets were placed in the workspace of the robot. On one of these pallets three boxes of unknown size were randomly placed. The size, position and orientation of the boxes were determined using a Kinect, the Openni package and the PCL library. Based on this information, a path was calculated by [MoveIt!](http://moveit.ros.org/wiki/MoveIt!) and was then sent to the robot controller using the ABB ROS-Industrial package.

To make offline testing of the connection between the ROS-pc and the ABB motion controller possible, Alten Mechatronics developed a setup in which a ROS-pc was connected to a pc running the official ABB [ABB RobotStudio software](http://wiki.ros.org/abb/Tutorials/RobotStudio). This reduced the hardware set up time to less than one day. The current implementation reached a grasping accuracy of approximately 1cm, which indicates the accuracy of the vision system can be improved. This can be done by using more accurate sensors (e.g., laser triangulation, Time of Flight cameras) and more advanced filtering algorithms. For this demonstrator, the existing ABB drivers had to be adapted to allow controlling the gripper using the I/O interface of the IRC5 controller, which indicates a the need for a standardized Robot I/O interface in ROS-Industrial, to make implementation even easier.

By: Berend Kupers, [Alten Mechatronics](http://www.alten.nl/en/alten-mechatronics/).
Contact: rosindustrial(at-sign)alten.nl


