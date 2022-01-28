---
author: Thilo Zimmermann (Fraunhofer IPA)
comments: false
date: '2018-12-19 12:18:48+00:00'
slug: 2018-12-19-mopjvmjkyekqsqn4praorve9ls1ql0
title: 'ROS Industrial Conference #RICEU2018 (Session 1)'
media_type: None
description: From public funding opportunities to the latest technologies in software
  and system integration, the combination of robotics and IT to hardware ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/12/19/mopjvmjkyekqsqn4praorve9ls1ql0
---

From public funding opportunities to the latest technologies in software and system integration, the combination of robotics and IT to hardware and application highlights: This year's [ROS-Industrial Conference 2018](https://rosindustrial.org/events/2018/12/11/ros-industrial-conference-2018) offered a varied and top-class programme to more than 150 attendees. For the sixth time already, Fraunhofer IPA organized a ROS event in Stuttgart to present the status of ROS in Europe and to discuss existing challenges.

This is the **first** instalment of a series of four consecutive blog posts, presenting content and discussions according to the sessions:

1. EU ROS Updates (watch all talks in this [YouTube playlist](https://www.youtube.com/playlist?list=PLXUpEXjGC63xRrb7IGPRnKPhKc-IkjFEC))
2. Software and system integration
3. Robotics meets IT
4. Hardware and application highlights

Day 1 - Session "EU ROS Updates"
--------------------------------

![Mirko Bordignon (Fraunhofer IPA) opening ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1548780199383-105QILDCAGR1401ORX69/IMG_3902-bearbeitet.JPG)

Figure: *Mirko Bordignon (Fraunhofer IPA) opening ROS-Industrial Conference 2018*

The topic of open source software for robotics was present in the media throughout the year, and announcements that companies such as Google, Amazon and Microsoft would rely on ROS made waves outside the community, too. In addition, there is a booming robotics market. Martin Hägele ([Fraunhofer IPA](https://www.ipa.fraunhofer.de/robotsystems)) highlighted this in his opening talk based on current market figures and areas of application for industrial and service robotics. In this respect, it is not surprising that politics and research funding on a national and international level are becoming increasingly aware of ROS. The speakers on the first day of the conference presented the projects and activities currently underway here.

**ROSIN project overview**

Bringing ROS into industrial application in Europe is one of the main activities of the EU project [ROSIN](http://www.rosin-project.eu/) (ROS-Industrial Quality Assured Robot Software Components) that Carlos Hernandez Corbato of [TU Delft](https://tudelftroboticsinstitute.nl/) presented. This runs from 2017 to 2020 and is mainly involved in three fields:

1. Further development of ROS components within the framework of so-called Focused Technical Projects (FTPs)
2. Tools for software quality assurance
3. Education activities

Applications for FTPs can still be submitted until 2020. The next cut-off date is April 5th 2019. All information on the short application process can be found here. A decisive criterion: The project provides funding for developments for which there are concrete market requirements. For this reason, the project finances one third of the software development and the applicant takes over the other two thirds.

![Carlos Hernandez Corbato (TU Delft) at ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1548780453345-66PX21NEL47Z6EWSYW2P/IMG_3909-bearbeitet.JPG)

Figure: *Carlos Hernandez Corbato (TU Delft) at ROS-Industrial Conference 2018*

**Successful FTP examples Pilz, Nobleo, PPM and Roboception**

ROSIN granted already 20 applications for FTPs and 21 more are under review. Here are four examples of successful FTPs:

For [Pilz](https://www.pilz.com/en-GB), "Industrial Trajectory Generation for MoveIt!" was granted: Most industrial robot manipulators supported in ROS come with a MoveIt! configuration. The Motion Planning plugin for RViz allows simple and visualized planning and execution of free-space motion. Planning and obstacle avoidance work mostly out-of-the-box. This FTP addresses Cartesian motion: existing libraries for Cartesian trajectory generation lacked a user-friendly interface. The FTP implements a trajectory generator with a MoveIt!-interface for easy planning and execution of Cartesian standard-paths. In addition, the blending of multiple sequential motion commands is realized.

For [Nobleo Projects](http://www.nobleo.nl/), "Full Coverage Path Planning and Control" was granted: Many robotic applications need to plan a path that passes over all points of an area or volume of interest while avoiding obstacles. As soon as a path is planned, the next challenge is to control it. As neither ROS, nor ROS Industrial are currently providing needed packages incorporating this (complete) coverage path planning or trajectory tracking functionality, this FTP proposes to develop, verify and validate these packages.

For [PPM](https://www.ppm.no/ppm-Home), the FTP "ROSweld" was granted: It develops an innovative ROS based framework for planning, monitoring and control of multi-pass robot applications with an intuitive, user-friendly GUI. The framework is built upon components from the project partners' previous research and existing ROS modules. ROSWELD is demonstrated by the case study in heavy, multi-pass welding.

For [Roboception](https://roboception.com/en/), the FTP "Visard4ROS" was granted: Visard4ROS will provide a ROS interface to fully exploit the capabilities of the rc\_visard sensor and to easily integrate it into robotic products or research platforms. As part of the process, Visard4ROS will also provide documentation for integration of sensors with standard industrial interfaces such as GigE Vision and GenICam, plus examples and good practices for using separate libraries to build ROS-I hardware drivers.

**Education activities**

![Stephan Kallweit (FH Aachen) and Jonathan Hechtbauer (Fraunhofer IPA) at ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1548780564356-G74Q0SEI587EFK75ATT7/IMG_3951-bearbeitet.JPG)

Figure: *Stephan Kallweit (FH Aachen) and Jonathan Hechtbauer (Fraunhofer IPA) at ROS-Industrial Conference 2018*

The second goal of ROSIN are education activities. Stephan Kallweit ([FH Aachen](http://maskor.fh-aachen.de/en/)) and Jonathan Hechtbauer ([Fraunhofer IPA](https://www.ipa.fraunhofer.de/robotsystems)) presented the two formats with which the project conveys ROS knowledge. One of them is the ROS-I School. It addresses university students and young professionals to get an entry to the ROS-Industrial eco-system. Its teaching concept consists of seminars, tutorials and workshops. In addition, ROSIN has founded the ROS-I Academy. It consists of a ROS-I certified engineer program to assess certain skills within the ROS-Industrial software engineering eco-system. The certified skills comprise basic knowledge in ROS-Industrial, skills in code review and specialised ROS-Industrial topics. Check out the [website](http://rosin-project.eu/education) for upcoming events.

**Quality Assurance Tools**

The third main activity of the ROSIN project are measures and technologies to improve the quality of software. Adam Alami and Zhoulai Fu ([IT University of Copenhagen](https://pure.itu.dk/portal/en/organisations/computer-science(768f3a75-8ff6-46cf-8ab0-c09d1057ec3b).html)) presented the ongoing steps. On the one hand, a process and supporting tools are developed for quality assurance, where the quality of packages can be measured, assigned and displayed. Furthermore, ownerships for QA practices, tools and infrastructure will be appointed. Furthermore, code review practices are going to be reinstituted and a code scanning method and tool will be implemented. A quality hub [website](http://wiki.ros.org/Quality) is already online in order to create a source of knowledge for quality assurance. A source of collaboration for quality assurance offers this [page](https://discourse.ros.org/c/quality).

Another quality improvement measure is the automated code testing. Traditional platforms are not effective enough to provide the reliability that ROS needs today as they run the same and very few test harness for many times. However, a ROS package is reliable, when it works as expected for all run-time scenarios. That is why ROSIN aims at developing a reliability-oriented testing framework that will be integrated to the ROS ecosystem.

**Outlook: Further research activities thanks to RobMoSys and SeRoNet**

The conference day ended with two contributions on other research projects that also rely on ROS. Dennis Stampfer ([University of Applied Sciences Ulm](http://www.servicerobotik-ulm.de/drupal/)) presented [RobMoSys](https://robmosys.eu/). It aims at coordinating the community's efforts to realize an industry-grade software development European ecosystem that is open, sustainable and ensures industrial quality. This shall increase the scalability and quality of robotics software development, help to commoditize base functionality, such as motion control, navigation, software components of certifiable quality and achieve predictable system integration. It addresses user requirements like, among others, reduction of development time and costs, shorter time to market and safety via a model-driven approach. 

Björn Kahl ([Fraunhofer IPA](https://www.ipa.fraunhofer.de/en/expertise/robot-and-assistive-systems/)) presented [SeRoNet](https://www.seronet-projekt.de/en/home.html). This project intends to significantly simplify the design, development, and deployment of service robots in a variety of areas, from logistics, care, and healthcare to assembly support in manufacturing operations. Through an online platform, users, system integrators and component manufacturers of service robot solutions will be able to collaborate efficiently and jointly support solutions from requirements analysis to deployment. The SeRoNet platform (available from summer 2019) will bring together users and producers of robotic solutions and will create a market for service robot solutions, services and hardware as well as software components for application solutions.
Both projects will publish Open Calls in 2019, for which companies involved in robotics can apply for funding.


