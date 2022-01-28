---
author: Shaun Edwards (SwRI)
comments: false
date: '2013-11-11 02:08:27+00:00'
slug: 2013-11-9-ros-industrial-mtconnect-integration-program-completes
title: ROS-Industrial – MTConnect Integration Program Completes
media_type: None
description: '> *This work was conducted under Grant Opportunity Number 2012-NIST-MSE-01
  for the Intelligent Systems Division of the National Institute of ...'
layout: post
old_sp_link: https://rosindustrial.org/news/2013/11/9/ros-industrial-mtconnect-integration-program-completes
tags: ros ros-i ros-industrial mtconnect swri industrial-robots fanuc-robot
---


> 
> *This work was conducted under Grant Opportunity Number 2012-NIST-MSE-01 for the Intelligent Systems Division of the National Institute of Standards and Technology ([NIST](http://www.nist.gov/)) in collaboration with [AMT](http://amtonline.org/) (Association for Manufacturing Technology), [Mazak USA](http://www.mazakusa.com/), [NCDMM](http://ncdmm.org/) (National Center for Defense Manufacturing and Machining), [SwRI](http://www.swri.org/) (Southwest Research Institute), and [System Insights](http://www.systeminsights.com/).*
> 
> 
> 

Program Summary
===============

The ROS-Industrial – [MTConnect](http://www.mtconnect.org/) Integration program, completed this past summer, had a goal to create a bridge between the MTConnect and ROS-Industrial and demonstrate the capability with a robotic machine tending application. Similar to ROS messaging, MTConnect is a standard that describes both the symantic data definition and method of communication between devices in a manufacturing environment. The [ROS-Industrial/MTConnect bridge](http://wiki.ros.org/mtconnect) allows devices that use either comms/messaging system to communicate seamlessly. The practical application of the bridge is to create plug-and-play capability between MTConnect devices and any robot that is supported by ROS-Industrial. The final deliverable for the program was a machine tending demonstration with a ROS-Industrial-controlled robot (Fanuc) and a MTConnect-controlled CNC (Mazac CNC Lathe). The MTConnect standard pre-defined the communications and system interactions between the robot and CNC, allowing an integration with significantly less programming than would be required from a traditional implementation. (for more information see the video below).

Importance to ROS-Industrial
============================

While the final demonstration of the program may not be a new application, the real value in this program was to provide a method for ROS-Industrial devices to communicate with other devices (even other ROS-Industrial devices) using an industry standard. With this capability, the vision of a factory floor with intelligent industrial systems all communicating and interacting seamlessly could be realized. This is a capability that is not traditionally supported by ROS. There have been efforts at creating a [multi-master system](http://wiki.ros.org/sig/Multimaster), but these efforts are not appropriate for an industrial application. Such approaches require every system to be ROS-aware which is not practical for all the systems in an industrial environment. Many devices are too simple for the overhead of ROS. Thus MTConnect provides a pragmatic solution for device-to-device communications.

In addition to this important capability, several ancillary capabilities were developed or prototyped as part of this effort.

* [Robot Task Description Format (RTDF)](http://github.com/mtconnect/ros_bridge/tree/master/mtconnect_example/mtconnect_task_parser)– A standard ROS format for capturing robot moves and
way-points in a human-readable format.
* [Standard Control System State Machine and GUI](https://github.com/mtconnect/ros_bridge/tree/master/mtconnect_example/mtconnect_example_gui)– The vast majority of industrial control systems follow very similar
behavioral concepts, including common states such as idle, waiting, in-process,
stopped, reset, etc... With the adoption
of common states, a similar GUI structure emerges. While these concepts are not new, powerful tools
like those available with ROS-I now allow developers to take advantage of them.

![industrial_GUI.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1384051358404-YF6UZ30Z8WXFOJJURVPY/industrial_GUI.jpg)

The ROS-Industrial - MTConnect Integration Program provided many benefits to the ROS-Industrial program, including new capabilities and a real world demonstration of a robotic machine tending application. We are excited to see how others will build upon these new capabilities for their own applications.


