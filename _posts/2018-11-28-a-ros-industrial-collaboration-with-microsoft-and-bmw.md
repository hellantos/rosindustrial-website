---
author: Matt Robinson (SwRI)
comments: false
date: '2018-11-30 00:44:27+00:00'
slug: 2018-11-28-a-ros-industrial-collaboration-with-microsoft-and-bmw
title: A ROS-Industrial Collaboration with Microsoft and BMW
media_type: None
description: ROS-Industrial recently had the opportunity to collaborate with Microsoft,
  BMW and Open Robotics on an automation solution that was featured in ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/11/28/a-ros-industrial-collaboration-with-microsoft-and-bmw
tags: ros ros-industrial microsoft bmw
---

ROS-Industrial recently had the opportunity to collaborate with Microsoft, BMW and Open Robotics on an automation solution that was featured in Season 3 of the Decoded show on YouTube. This enabled the ROS-I Consortium to realize sustainable gains on the team's vision for greater efficiency and visibility with respect to logistics and material management challenges in assembly plants.

![Mobile Robot.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1543443950958-9CF79TO345RZIBXUTJVM/Mobile+Robot.png)

BMW has set forth a vision where they break down the barriers between the historical automation paradigms and the challenges with interacting with the largely manual operations of their ever-increasing high-mix assembly operations. Historically, materials are delivered to the line for human operators to consume and exact quantities and status are lost at that point of consumption. The idea is to leverage intelligent autonomous operation to give better visibility to what is where, while leveraging cloud technologies to create a tighter loop and connection to the order delivery systems. The goal is to enable a leaner operational buffer within the workflow, reducing carried inventory and driving greater efficiency. 

This is where Microsoft came into the picture, with their Azure solutions and
client support team to do rapid development sprints to enable tighter coupling
between their SAP work order environment to the "to-be deployed" autonomous
robotic fleet.

BMW has built a home-grown start transport robot that runs on the same battery
used in the i3 model car they produce. However, there needed to be coordination
of these assets over the long term with a richer simulation environment as the
platform's capability increased. This is where the Microsoft team came to
deliver.

![Close Up.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1543444037371-0WQE63MNLZ6SL8M7N8PO/Close+Up.png)

Originally, the Southwest Research Institute (SwRI) ROS-I team support was
around navigation and evaluation of Gazebo in manufacturing environments
supporting many mobile robots. It became clear as the Microsoft team got to work
that Gazebo would not support spinning up multiple mobile robots in one
instance. In fact, due to how Gazebo is structured, even a handful of robots
brought Gazebo processing to a crawl. This led to the implementation of
[Argos](https://www.argos-sim.info/), an open-source simulator that also has the
capability to include physics as the scale BMW was interested in. A container
strategy was developed and, in the end, the ROS-I team ended up learning quite a
bit from the Microsoft team through the week-long development hack on SwRI's
campus. This development week really furthered the understanding of capability
with regard to richer simulation capabilities, including the physics, which
supports the ROS-I vision of tighter process performance and management of
non-rigid bodies within the planning cycle.

As things got going in Germany, as the Decoded episode shows, the Microsoft team
worked closely with BMW's ROS and Manufacturing Execution System (MES)
developers, tightly coupling the SAP functionality along with the fleet
management and navigation tuning functionality that was required along with the
Argos implementation. In the end, this led to a functional, if not sustainable,
solution for the BMW team as they continued to refine the performance of the
specific ROS-based robot, leveraging the Azure environment to assure SAP to
simulation, to robot action within the Azure platform.

![VPLogistics.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1543444088529-WGEF7DY7BNH9U8WX4IFQ/VPLogistics.png)

We hope those who watch this Decoded episode agree this demonstrates that
collaborations between for-profit entities such as Microsoft, and nonprofits –
such as SwRI, Open Robotics and Fraunhofer IPA, as well as open-source projects
such as ROS-I – can enable end-users such as BMW to create their own
sustainable, high performing solutions. We believe the open-source contributions
will enable others to leverage the development and hopefully expand the
capability. This idea of a pre-competitive foundation that enables
interoperability and flexibility without generating silos is key if we are to
move the ball forward with respect to operational efficiency gains at the scale
we need.

As we have seen in recent months, robotics development and IT are entering a new
phase, where more teams and individuals can grasp their own destiny and
ROS-Industrial is excited to be a part of that journey!

Thanks to Microsoft and BMW as well as the Decoded team for making this project
possible.


