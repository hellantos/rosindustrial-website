---
author: Guest User
comments: false
date: '2016-09-19 20:23:38+00:00'
slug: 2016-9-16-google-summer-of-code-project-
title: Google Summer of Code Project - ROS Interface for Impedance/Force Control
media_type: None
description: "Submitted by: Risto Kojcev, IIT and Scuola Superiore Sant'Anna"
layout: post
old_sp_link: https://rosindustrial.org/news/2016/9/16/google-summer-of-code-project-
---

Submitted by: Risto Kojcev, IIT and Scuola Superiore Sant'Anna

As part of Google Summer of Code (GSoC) 2016 directed by the Open Source Robotics Foundation (OSRF) and ROS-Industrial (ROS-I) Consortium, we have developed a user friendly ROS Interface to control and change a manipulator into Cartesian Impedance control mode. The external forces that the robot applies to the environment can also be set with the developed interface. 

Below are some of the technical details and relevant repositories that were developed as part of this project.

Our first goal was to create a set of common messages containing the necessary parameters for setting Impedance and Force control. This allows interaction between the ROS ecosystem and the ROS driver of the robot. The messages are created based on the commonly used parameters for Impedance/Force control and discussion with the ROS community. The relevant current set of ROS messages are available in the [majorana repository](https://github.com/ros-industrial-consortium/majorana). I would also like to encourage the Robotics community to contribute to this project by sharing their suggestions. I believe that this set of messages could still be more generalized and improved based on community input.

The second goal was to develop a user interface which allows the user to set the necessary parameters for Cartesian Impedance/Force Control and interactively switch between control modes. In this case I have expanded previous GSoC 2014 Project: [Cartesian Path Planner Plug-In for MoveIt!](http://rosindustrial.org/news/2014/9/5/cartesian-path-planner-plug-in-for-moveit). The [updated plugin](https://github.com/ros-industrial-consortium/fermi/tree/indigo-devel-impedance) now contains the relevant UI fields for setting Cartesian Impedance and Force Control. Depending on the implementation and the properties of the robot controller, this plugin also allows interactively switching between control modes during runtime. 

I would like to share my gratitude for the ROS-I community members and my mentor Shaun Edwards, who shared their suggestions during the project development. I hope that this project will find its place in many applications.

Relevant links:

* [UI for cartesian path planning and Impedance/Force Control](https://github.com/ros-industrial-consortium/fermi/tree/indigo-devel-impedance)
* [ROS messages for Cartesian Impedance/Force Control.](https://github.com/ros-industrial-consortium/majorana)
* [GSoC final results report.](https://docs.google.com/document/d/140NK1d3ZoY3MhfOzP2rE5i02hJJ4P0HuBD21fE9kBxI/edit?usp=sharing)

