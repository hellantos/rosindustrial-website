---
author: Thilo Zimmermann (Fraunhofer IPA)
comments: false
date: '2019-10-21 12:19:39+00:00'
slug: 2019-10-21-tech-workshop-on-moveit-security-skill-oriented-programming-with-ros
title: Tech Workshop on MoveIt, security &amp; skill oriented programming with ROS
media_type: None
description: The Fall edition of [ROS-Industrial EU Tech Workshop](https://rosin-project.eu/event/ros-industrial-eu-fall19-workshop)
  took place at Fraunhofer ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/10/21/tech-workshop-on-moveit-security-skill-oriented-programming-with-ros
tags: ros2 ric-eu tech-workshop stuttgart fraunhofer-ipa sros moveit
---

The Fall edition of [ROS-Industrial EU Tech Workshop](https://rosin-project.eu/event/ros-industrial-eu-fall19-workshop) took place at Fraunhofer IPA on October 09th and 10th, 2019. 

We were glad to host two European [MoveIt maintainers](https://moveit.ros.org/about/), namely Henning Kayser of ROS-Industrial Consortium member [PickNik Robotics](https://picknik.ai/team/) and Michael Görner from [University of Hamburg](https://tams.informatik.uni-hamburg.de/people/goerner/). They gave us an insight into the latest developments of MoveIt (incorporating motion planning, manipulation, 3D perception, kinematics, control & navigation), current and planned developments for ROS2 (MoveIt2), and a hands-on on ROS(1)-based 'bare-metal to product'. First they presented an inside-view of the manipulation framework. Providing complementary academic and industrial perspectives, they shared their views and experiences on MoveIt's overall structure, practical deployment of planning-based pipelines, complex manipulation planning using the MoveIt Task Constructor, and upcoming future projects and ideas for a ROS2 migration. The workshop concluded with a practical session that guided the participants to setup a functional Pick&Place pipeline from a custom bare robot description. Slides and code examples are available at <https://github.com/henningkayser/ROS-Industrial_EU_Fall19_MoveIt> .

![20191009_112123.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1571657295949-RQNIKS27IE59LJZI22OA/20191009_112123.jpg)

The first session on day 2 of the ROS-Industrial EU Fall'19 Workshop was about security in ROS where Sebastian Taurer from JOANNEUM RESEARCH presented his work on a penetration testing tool for ROS1, called 'ROSPenTo', and gave an introduction on how to use SROS2 to secure communications in ROS2. In the first part of the session ROSPenTo was introduced to provide basic information on how it works and what a user can do with it. During the hands-on section the participants were guided through a step-by-step manual showing how to analyse, penetrate and modify a running ROS1 system using ROSPenTo. In the second part of the session ROS2's security tools (a.k.a. SROS2) were explained and used to setup and configure a security infrastructure. The provided examples demonstrated the creation of all necessary security artefacts (e.g. keys, certificates, etc.) and also the procedure to securely distribute the artefacts to different machines. All the related information as well as the workshop tutorial can be found here: <https://github.com/jr-robotics/ROS-Industrial_EU_Fall19_Workshop> 

![EGg33rKWoAAHuv5.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1571661319298-J2FZVWNV9WWP2HWWHFV8/EGg33rKWoAAHuv5.jpg)

The ScalABLE4.0 session at the ROS Industrial EU Fall'19 Workshop focused on presenting the set of technologies which are enabling flexibility in production lines in two industrial pilots of the automotive sector: PSA Peugeot Citroën and Simoldes Plásticos. Within the project, a complete digital manufacturing software stack is being developed, entitled 'Open Scalable Production System' (OSPS). The OSPS aims to be applied to efficiently and effectively visualize, virtualize, construct, control, maintain and optimize production lines through a tight integration of the enterprise information systems with transformable automation equipment paired up with the necessary open interfaces for optimized solutions on all hierarchy levels ([slides](/s/ScalABLE40_ROSIN_Presentation.pdf)). 

![20191010_091701.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1571657418802-XVJLQMK6DPONW9W20F1S/20191010_091701.jpg)

During the workshop, attendees were introduced and got a chance to test, interact and develop with the set of components that compose the OSPS, namely: (i) The Advanced Plant Model, which is responsible for virtually integrating data from the industrial shop floor in a centralized digital twin; (ii) The Production Manager, which is a cloud-based software module that issues and supervises the execution of manufacturing tasks; (iii) SkiROS and Task Manager, which are distinct ROS-based approaches to orchestrating the behaviour of robotic systems; (iv) The Skill-based Robot Programming methodology, which enables the reutilization and adaptation of ROS-based robotic applications to different purposes, platforms, and environments; (v) and, finally, the ROS-CODESYS bridge (ROBIN - <https://github.com/ScalABLE40/robin>), which enables horizontal integration between robots and automation equipment.

As part of the Scalable project, Bjarne Grossmann from AAU and cofounder of RiACT presented their skill-based robot control software SkiROS v2 ([slides](/s/ROS-Industrial-SkiROS-workshop.pdf)). Their technology is based on extended behavior trees that allows the definition of reactive behavior for highly flexible manufacturing environments. The framework is backed by a semantic database for inference and support of task planning to automatically generate complex tasks. In the hands-on session, Bjarne demonstrated the system with a SkiROS-implementation of the classical ROS turtlesim demo. He showed that SkiROS can be easily used to create complex behavior (and not only for turtles). The demo can be found on the git repository <https://github.com/Bjarne-AAU/skiros-demo>. Soon, there will be an official open source release of the software. Stay tuned on www.riact.eu!

Next European expert workshops will be organized in Spring and Fall 2020. We will keep you posted!

PS: Some links to upcoming events in this respect:

* Oct. 30- Nov 01, 2019, ROSCon 2019 in Macao: [roscon.ros.org/2019/](https://roscon.ros.org/2019/)
* Nov. 02, 2019, MoveIt Workshop Macao: [moveit.ros.org/moveit/ros/2019/09/19/moveit-workshop-macau.html](https://moveit.ros.org/moveit/ros/2019/09/19/moveit-workshop-macau.html)
* Nov. 20, 2019, World MoveIt Day (WMD2019): [moveit.ros.org/moveit/ros/2019/07/31/world-moveit-day-2019.html](https://moveit.ros.org/moveit/ros/2019/07/31/world-moveit-day-2019.html)
* Dec. 10-12, 2019, ROS-Industrial Conference 2019 in Stuttgart: [rosindustrial.org/riceu2019](https://rosindustrial.org/riceu2019)

