---
author: Christoph Hellman Santos (Fraunhofer IPA)
comments: false
date: '2020-07-13 15:27:01+00:00'
slug: 2020-6-23-how-to-securely-control-your-robot-with-ros-industrial
title: How to securely control your robot with ROS-Industrial
media_type: None
description: Trend Micro and Politecnico di Milano (Polimi) recently brought up a
  security issue with controlling industrial robots using ROS-Industrial ...
layout: post
old_sp_link: https://rosindustrial.org/news/2020/6/23/how-to-securely-control-your-robot-with-ros-industrial
---

Trend Micro and Politecnico di Milano (Polimi) recently brought up a security issue with controlling industrial robots using ROS-Industrial drivers. We have worked fast to describe the mitigation for the security problem uncovered. Actually, it is quite simple, by following basic security guidelines on how to setup your network you can eliminate the described security risk at the source. Here we show how to setup secure communication between your ROS PC and your industrial robot. 

In ROS-Industrial robots are connected to the ROS PC using so called motion servers. These are programs written in the OEM specific programming language that are running on the robot controller and enable receiving target values (typically axis positions) from and sending actual values as well as the robot status to the robot's ROS driver. The interface used for this communication differs from one robot OEM to another. The problem is that as of now robot OEMs do not provide interfaces that provide a security layer or authentication methods for these interfaces and no such measures can be added to the motion servers running on the robot controllers. Therefore, it is possible for intruders to attack the communication interface between ROS-Industrial robot driver and the motion server running on the robot controller. TrendMicro and PoliMi claim to have succeeded in sending motion commands to the robot controlled by a ROS-Industrial robot driver from another device that is connected to the same network as the controlled robot and the ROS-Industrial robot driver (Figure 1). This behavior can be potentially exploited by malicious network participants. 

![Figure 1. Typical setup of a ROS-Industrial robot driver and vulnerable communication](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1594403143582-65KDXAMDV7SYOI1L0P9Q/Figure1.png)

*Figure 1. Typical setup of a ROS-Industrial robot driver and vulnerable communication*

To minimize the risk of this potential attack vector on the interface between the device running ROS and the robot controller the network needs to be setup correctly. The connection between the ROS PC and the robot controller needs to be isolated from other networks that might be connected to the ROS controller. Figure 2 shows how to set this up correctly, so that a bad actor will have a hard time exploiting this vulnerability. Isolation of the connection between ROS PC and robot controller means that if you want to connect your ROS PC to another network in a secure way, you will need two network cards. One is used to connect to the robot controller, the other is used to connect to the outer network. Figure 3 shows an example for a vulnerable network setup that you should avoid at all cost. 

![Figure 2. Correct network setup to avoid security vulnerabilities](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1594402611929-MAGN43T46G5KRR1X5C6E/Figure2.png)

*Figure 2. Correct network setup to avoid security vulnerabilities*

Currently, the vulnerability has only been tested with drivers for Kuka and ABB but it could also be exploited with other industrial robot drivers.
If you isolate the connection between the ROS PC and your robot controller but connect your ROS PC to a network with potentially malicious participants on another network card we strongly recommend following the instructions on <http://wiki.ros.org/Security> and if you use Ubuntu the instruction provided by Canonical (<https://ubuntu.com/engage/securing-ros-on-robotics-platforms-whitepaper>) to ensure your ROS PC protected. 

![Figure 3. Vulnerable network setup that should be avoided.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1594402639448-FI3NPI0J57NQAF1B7OBF/Figure3.png)

*Figure 3. Vulnerable network setup that should be avoided.*


