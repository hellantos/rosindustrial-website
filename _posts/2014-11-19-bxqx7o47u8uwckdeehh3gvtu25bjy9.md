---
author: Guest User
comments: false
date: '2014-12-01 22:21:47+00:00'
slug: 2014-11-19-bxqx7o47u8uwckdeehh3gvtu25bjy9
title: Demonstrating the Integration of ROS with Siemens' Process Simulate
media_type: None
description: '[Siemens PLM Software](http://www.plm.automation.siemens.com/en_us/)
  is a leading global provider of product lifecycle management (PLM) software. ...'
layout: post
old_sp_link: https://rosindustrial.org/news/2014/11/19/bxqx7o47u8uwckdeehh3gvtu25bjy9
---

[Siemens PLM Software](http://www.plm.automation.siemens.com/en_us/) is a leading global provider of product lifecycle management (PLM) software. Those PLM solutions, can help make smarter decisions that lead to better products.

As always, we at Siemens PLM Software are looking for new areas that will allow us to understand the future of robotics in the industrial sector. After we came across [The Robot Operating System (ROS)](http://www.ros.org/) and [ROS-Industrial](http://rosindustrial.org/), I was sent to take a closer look. In June, I participated in the "ROS Industrial Basic Developers Training Class" held at Southwest Research Institute (SwRI) to understand more about the ROS ecosystem and tools. Since then, I have been experimenting with ROS libraries and tools and thinking about a connection between ROS Industrial and our own Process Simulate software.

From what I learned, ROS Industrial has interesting potential in the area of industrial robotics by providing the following:

* Standardization for robotic languages.
* Real time path planning and collision avoidance.
* A huge library of open source components.

For the above reasons, we believe that ROS-I has the potential to play a significant role in the industry and we should be a part of it.

After a few experiments, I compiled the demo (refer to video above) which shows how Process Simulate can provide a full simulation environment for a ROS controlled robot ([R2-D2](http://en.wikipedia.org/wiki/R2-D2) believe it or not). In the demo, you'll see that R2-D2 has three proximity sensors which are mounted on the right, front and left (their signal values can be seen in real time on the top left of the screen). R2-D2's objective is to leave the maze using the simple algorithm of "always try to turn to the right". But to make its life a little more interesting, we added red barriers which are removed manually at the start of the simulation to create a more dynamic environment.

![As you can see from the rqt_graph above, the sensory information received from Process Simulate is processed on the ROS side and information about the robot's new location is sent back to Process Simulate (the objects in red are Process Simulate com…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1417362960893-79A6V4RCHHERHEJ7WLSY/rqt_graph)

Figure: *As you can see from the rqt\_graph above, the sensory information received from Process Simulate is processed on the ROS side and information about the robot's new location is sent back to Process Simulate (the objects in red are Process Simulate components).*

Along the way, I overcame a couple of interesting challenges such as:

* Having to write a robotic program using third party tools.
* Connecting between Windows-based Process Simulate and Linux-based ROS.

After discovering some real added value of linking ROS Industrial with Process Simulate, I'm going to explore further capabilities, like Vision, and working with more complicated environments using advanced Process Simulate and ROS Industrial software packages (PLC and welding in Process Simulate and OpenCV and MoveIt in ROS-I).

If you are looking to share interesting view points, use cases and environment challenges which are related to ROS-I, contact me at: moshe.schwimmer (at sign) siemens.com

Additional references:

<http://www.plm.automation.siemens.com/en_us/products/tecnomatix>

<https://www.facebook.com/Tecnomatix.NXforManufacturing>


