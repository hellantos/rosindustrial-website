---
author: Guest User
comments: false
date: '2014-09-05 20:00:27+00:00'
slug: 2014-9-5-cartesian-path-planner-plug-in-for-moveit
title: Cartesian Path Planner Plug-In for MoveIt!
media_type: None
description: Dear ROS-I Community,
layout: post
old_sp_link: https://rosindustrial.org/news/2014/9/5/cartesian-path-planner-plug-in-for-moveit
---

Dear ROS-I Community,

My name is Risto Kojcev, a joint PhD student between the BioRobotics Institute at Scuola Superiore Sant'Anna and MicroBio Robotics Institute at the Italian Institute of Technology, in Pisa Italy.

This year I was participating in the Google Summer of Code (GSoC) directed by the Open Source Robotics Foundation (OSRF) and ROS-Industrial (ROS-I) Consortium. The title of my project was [Cartesian Path Planner Plug-In for MoveIt](https://www.google-melange.com/gsoc/project/details/google/gsoc2014/rkojcev/5741031244955648).

In this blog post I would like to share the vision behind the GSoC project and its usefulness in the real robotic applications.

**Technical Details of the Plug-In**
====================================

The project aim was to develop a user friendly Cartesian Path Planner Plug-In for MoveIt!. In the current version of the project, the user can simultaneously interact with a Qt Widget and the RViz environment to define and set Cartesian Way-Points, which can then be passed to the Cartesian Planner of the MoveIt package and executed both on a simulated and real robot. [Cartesian waypoints can also be loaded externally from a yaml file.]

For the User Interaction in the RViz environment the Interactive Marker package was used. The plug-in offers two types of Interactive Markers. The first one is called Interaction Marker and is used to add the second type of Interactive Marker, the actual Cartesian Way-Points. The Cartesian Way-Points can be moved around freely in the RViz environment, and a menu that offers additional components for removing the Way from the Cartesian Plan and more detailed 6DOF control is available for each Way-Point. The color of the Way-Points lets the user know if a certain Way-Point is within the range of the Inverse Kinematics (IK) solution for the loaded robot model. In the case when the point is within the range of the IK Solution the color of the way-point is blue and yellow otherwise.

The user can also interact with the Cartesian Planner through a Qt Widget. In this widget all the Way-Points are displayed, offering additional details about each Way-Point Pose, which can be edited and adjusted by the user. Furthermore, the user can perform the same operations as in the RViz environment: adding a new Way-Point or removing it. The Way-Points can be saved to a file and the Plug-in also offers the user to load a previously saved way-points file.

The Cartesian Planner part of this Plug-in offers the user a means to adjust the parameters of the Cartesian Planner and execute a Cartesian Path set from the previously added Way-Points.

More detailed tutorials and description of the Plug-in can be found on the [moveit\_cartesian\_plan\_plugin wiki page](http://wiki.ros.org/moveit_cartesian_plan_plugin). For the source code of the project, reporting bugs and further development suggestions, please visit the [github repository](https://github.com/ros-industrial-consortium/fermi).

**Applications and Future Development**
=======================================

The design goals behind the Cartesian Plug-in was to create a simple and user friendly environment, which targets larger groups of users, from ROS beginners to more ROS experienced users. It is envisioned to find its applications in a lot of industrial applications, for example welding, painting or performing more complex actions. This Plug-in is a good starting point for future development of other applications, not just in the industrial robotics area, where Cartesian path planning is useful. For example to even further automate the creation of Way-Points an external perception system can be used which would generate Cartesian Way-Points and then the user can review the Cartesian Path, correct it and execute it, or even save it if necessary.

I would like to conclude this blog post by sharing my gratitude towards all the ROS-I community members and my mentor Shaun Edwards, who shared their suggestions during the project development. I am very happy that I had the chance to participate in this awesome program and this was a great experience for me and most of all I had lot of fun working on this project. I hope that this project would find its place in many applications and it would be useful for lot of users.


