---
author: Guest User
comments: false
date: '2016-02-23 15:13:14+00:00'
slug: 2016-2-23-ros-bridges-for-common-field-busses
title: ROS Bridges for Common Field Busses
media_type: None
description: Hardware interfaces are particularly important for any
layout: post
old_sp_link: https://rosindustrial.org/news/2016/2/23/ros-bridges-for-common-field-busses
---

Hardware interfaces are particularly important for any
future integration of ROS-I with production systems. During
2015, we noted four new repositories emerged that span
the range of prominent industrial field busses:  

**• CANOPEN™:** CANOPEN is a fieldbus with origins in
automotive applications (CAN), but applied to automation.
We are grateful for the efforts of Mathias Lüdtke and
Florian Weisshardt from Fraunhofer IPA for the [ros\_
canopen](https://github.com/ros-industrial/ros_canopen) package.  

**• EtherNet/IP™:** EtherNet/IP is an Ethernet-based real-time
communication bus standard that was created by
Allen-Bradley (Rockwell Automation). Thank you ClearPath Robotics for developing and releasing a
ROS driver for [EtherNet/IP](https://github.com/ros-drivers/odva_ethernetip/).  

**• EtherCAT™:** Probably the first fieldbus supported in
ROS for the PR2, EtherCAT is an Ethernet-based realtime
communication bus standard that was created by
Beckhoff Automation. We appreciate Intermodalics for
maintaining the [EtherCAT](https://github.com/smits/soem) package for ROS.  

**• PROFINET™:** PROFINET, an open automation standard
and part of IEC 61158 is fully compatible with all the
features of standard Ethernet, and also capable of
real-time performance. We recognize the efforts of
[package](https://github.com/ros-industrial/siemens_experimental) developer Frantisek Durovsky from the Technical
University of Kosice in Slovakia along with his mentor
Shaun Edwards (SwRI), the financial support of Google
Summer of Code program, and technical support from
Siemens.


