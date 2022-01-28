---
author: Colin Lewis (SwRI)
comments: false
date: '2020-04-20 15:44:48+00:00'
slug: 2020-4-16-building-out-a-ros2-mobile-scan-n-plan-demonstration
title: Building Out a ROS2 Mobile Scan-N-Plan Demonstration
media_type: None
description: As part of the ROS Industrial Consortium Americas 2020 Annual meeting,
  SwRI demonstrated a mobile robot application bridging ROS 2 with ROS 1 ...
layout: post
old_sp_link: https://rosindustrial.org/news/2020/4/16/building-out-a-ros2-mobile-scan-n-plan-demonstration
---

As part of the ROS Industrial Consortium Americas 2020 Annual meeting, SwRI demonstrated a mobile robot application bridging ROS 2 with ROS 1 drivers for a mobile application. The exercise refined our capabilities with ROS2 systems, and many lessons learned along the way will inform later work in collaboration between mobile bases and industrial manipulators.

![ROS2 Mobile Scan-N-Plan Node Diagram](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1587093965292-BQL0Z0UDBXSPWKI5EO9J/Node+Diagram.png)

Figure: *ROS2 Mobile Scan-N-Plan Node Diagram*

Our demonstration leveraged the Clearpath Ridgeback and a Kuka Iiwa. Based on previous work with the Iiwa, we chose to use the ROS1 driver available for the robot. To integrate this into the system, both the input and output of the robot had to be bridged to the ROS2 system. This was achieved with a modified version of the ROS action bridge, which enabled joint command actions to be streamed to the robot, and a standard implementation of the ROS message bridge, to retrieve telemetry information from the Iiwa. With the support of ClearPath, we updated the OS of the Ridgeback to support ROS Melodic, an important stepping stone towards future application bridging the mobile base to a greater ROS2 system.

![ROS-I Americas Annual Meeting attendees ask questions after observing demonstration](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1587094161528-5HT13NT3LVWBK154A190/20200304_133653.jpg)

Figure: *ROS-I Americas Annual Meeting attendees ask questions after observing demonstration*

The demonstration itself was an expansion on the normal [Scan'N'Plan](https://rosindustrial.org/scan-n-plan) framework. The mobile platform was driven to a position of interest; in this case, an aircraft fuselage segment. A scan path, generated in the robot frame, was run and fed into [YAK](https://rosindustrial.org/news/tag/YAK) to create a model of the target. Once the scan was complete, alignment and tool path generation was done using a hybrid perception tool to remove masked features. Hybrid perception leverages machine learning classification on 2D data sets overlayed on 3D data, where both are available from the perception sensor set up, in this case an Intel® RealSense™ D435.

These tool paths were then streamed to the robot in the same manner as the scan path. However, our end effector (in this case, an array of lasers) would toggle on and off using segmentation described above, to protect regions of interest.

We hope all present enjoyed this demonstration. We look forward to applying the lessons learned here to future work with mobile robots!


