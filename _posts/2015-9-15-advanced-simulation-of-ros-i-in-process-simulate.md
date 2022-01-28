---
author: Guest User
comments: false
date: '2015-09-20 20:51:32+00:00'
slug: 2015-9-15-advanced-simulation-of-ros-i-in-process-simulate
title: Advanced Simulation of ROS in Process Simulate
media_type: None
description: Submitted by Mr. Moshe Schwimmer, Product Lifecycle Management, Siemens
  Digital Factory
layout: post
old_sp_link: https://rosindustrial.org/news/2015/9/15/advanced-simulation-of-ros-i-in-process-simulate
---

Submitted by Mr. Moshe Schwimmer, Product Lifecycle Management, Siemens Digital Factory

[Siemens PLM Software](http://www.plm.automation.siemens.com/en_us/) is a leading global provider of product lifecycle management (PLM) software. These PLM solutions can help make smarter decisions that lead to better products.

Since [my last post from December 2014](http://rosindustrial.org/news/2014/11/19/bxqx7o47u8uwckdeehh3gvtu25bjy9), featuring our R2-D2 and the maze using ROS and [Process Simulate](http://www.plm.automation.siemens.com/en_us/products/tecnomatix/manufacturing-simulation/assembly/process-simulate.shtml), we continued to explore ROS and the world of new, advanced and open source industrial robotics. 

In this post you'll find a demo (below) of a simulated hybrid industrial environment that I presented recently at both the yearly [ROS-Industrial Americas meeting](http://rosindustrial.org/news/2015/4/8/ric-americas-meeting-recap) and the [ROS-Industrial conference in Europe](http://rosindustrial.org/news/2015/6/16/recap-ros-industrial-conference-at-fraunhofer-ipa). It includes ROS-operated robots, classical robots (programmed by Process Simulate), a simulated human, and equipment. 

In the demo, I use Process Simulate to create an environment with both the UR robot which is operated directly by ROS and a KUKA robot, operated by Process Simulate. You'll see a simulated human and other equipment in use as well, and everything is synchronized by Process Simulate's simulated PLCs.

As you'll see in the demo, the UR robot picks boxes from a conveyor and moves them to the right container, according to color. The color is determined by the OpenCV package, which is loaded by ROS. Once a container is full, The KUKA robot picks it up and moves it to the removal area for the simulated human to take it away. 

The simulation uses proximity, light, and vision sensors to provide information that is gathered in Process Simulate. Some of it is processed locally and some of it is sent in real time, on each time interval, to the ROS environment. 

In the ROS environment, the only thing which is modeled is the UR robot. The ROS-controlled robot uses OpenCV and MoveIT packages to understand its surroundings and plan its path. ROS will send the information regarding the next location of the robot to Process Simulate on each time interval. 

The step forward, represented by the demo, is the collaboration between ROS packages and the Process Simulate environment, including use of simulated industrial robotics and equipment. 

On a related note, I'd also like to let you know about our Frontier Partner program: 

The Frontier Partner program grants leading robotics-focused startups developer licenses for a broad range of Siemens' PLM software (including Process Simulate), access to its technology partner program, and other development resources. Siemens is looking for partners with new approaches in robotics simulation, motion planning, robot interoperability, deployment and optimization in the field of industrial robotics, and especially startups that are developing on ROS. 

More details can be found here: <https://www.frontier.spigit.com/Page/Robotics>

If you are looking to share interesting view points, use cases and environment challenges which are related to ROS-I, contact me at: moshe.schwimmer (at sign) siemens.com 

Additional references:

* <http://www.plm.automation.siemens.com/en_us/products/tecnomatix>
* <https://www.facebook.com/Tecnomatix.NXforManufacturing>

