---
author: Thilo Zimmermann (Fraunhofer IPA)
comments: false
date: '2019-01-22 14:51:16+00:00'
slug: 2019-1-22-m48xan2qepan6ybkz1ebz56n1qo721
title: 'ROS Industrial Conference #RICEU2018 (Session 2)'
media_type: None
description: From public funding opportunities to the latest technologies in software
  and system integration, the combination of robotics and IT to hardware ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/1/22/m48xan2qepan6ybkz1ebz56n1qo721
tags: ros ros-industrial ros-industrial-consortium europe ros-industrial-conference
  fraunhofer-ipa stuttgart germany open-source-software robotics robot robot-operatin-system
---

From public funding opportunities to the latest technologies in software and system integration, the combination of robotics and IT to hardware and application highlights: [ROS-Industrial Conference 2018](https://rosindustrial.org/events/2018/12/11/ros-industrial-conference-2018) offered a varied and top-class programme to more than 150 attendees. For the sixth time already, Fraunhofer IPA organized a ROS event in Stuttgart to present the status of ROS in Europe and to discuss existing challenges.

This is the **second** instalment of a series of four consecutive blog posts, presenting content and discussions according to the sessions:

1. EU ROS Updates (watch all talks in this [YouTube playlist](https://www.youtube.com/playlist?list=PLXUpEXjGC63xRrb7IGPRnKPhKc-IkjFEC))
2. Software and system integration (watch all talks in this [YouTube playlist](https://www.youtube.com/playlist?list=PLXUpEXjGC63z7Zhe0gyk2tCkZvoEsADpg))
3. Robotics meets IT
4. Hardware and application highlights

Day 2 - Session "Software and System Integration Topics"
--------------------------------------------------------

![Dave Coleman (PickNik) at ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1548779515150-91QUT6JCU3197SIS74JG/2018-12-ROS-Industrial-Konferenz-02.JPG)

Figure: *Dave Coleman (PickNik) at ROS-Industrial Conference 2018*

The second day of the conference started with the session "Software and System Integration Topics". Dave Coleman, founder of [Picknik Consulting](https://picknik.ai/) and lead maintainer of [MoveIt!](https://moveit.ros.org/), opened the session with a very personal keynote about his commitment to open source software, from his student days to his role as an entrepreneur. He reported how he got in touch with the beginnings of ROS at Willow Garage and highlighted the unique spirit with which the project was incubated. He introduced the successful MoveIt! library, shared his lessons learned and the challenges which many open source projects face. As a proof of how Open Source and business can successfully coexist, he described the founding of PickNik and how the company is profitable without investors.

The following presentations were more technical and started with Víctor Mayoral Vilches, CEO of [Acutronic Robotics](https://acutronicrobotics.com/). He talked about his company's solutions for system integration in modular systems, through the device H-ROS SoM (System on Module), used as example. In his opinion, ROS already addresses many programming needs, but system integration goes far beyond programming and requires extensive resources for each new project. He therefore sees modularity as an essential improvement. Combining the features of a real-time capable link layer made of RTOS and the Linux Network stack, and ROS 2.0, he presented the challenges and developed solutions to achieve easier system integration. He also gave insights into the use of AI to further reduce programming efforts and to train the robot instead, a technology that is still in its infancy. As part of a [Focused Technical Project](http://rosin-project.eu/ftp/hrim) with [ROSIN](http://rosin-project.eu/), the company also worked on the interoperability of modules. 

![Jon Tjerngren (ABB) at ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1548779699603-HPF9H1ZEYQBYO3SLIKYI/2018-12-ROS-Industrial-Konferenz-12.JPG)

Figure: *Jon Tjerngren (ABB) at ROS-Industrial Conference 2018*

Jon Tjerngren presented how [ABB](https://new.abb.com/products/robotics) robots can be used with ROS. For this purpose, the company developed various ease-of-use packages with ROS that simplify and accelerate the setup of ABB robots. All of them are already freely available online: abb\_librws can be used to off-load of computational heavy tasks, e.g. image processing. abb\_libegm can be used for motion correction and as an StateMachine add-in for remote control.

ROS2 Embedded tailored to real-time operating systems was the topic of Ingo Lütkebohle's presentation from [Bosch Corporate Research](https://www.bosch.com/research/). He emphasized the importance that ROS must also be integrated into the firmware. This would better address four challenges: hardware access, latency, power savings, and safety. To this end, he presented a solution developed in the [OFERA](http://www.ofera.eu/) project with which ROS2 can be used in microcontrollers. 

André Santos from [INESC TEC](https://www.inesctec.pt/en) and [University of Minho](https://www.uminho.pt/EN), focused on software quality. More and more robot systems are safety-critical systems, which places very high demands on the quality of the software. Finding errors in the code early on reduces costs and development time. Although there are various static analysis tools, none offers ROS-specific analysis. This is why the [HAROS](https://github.com/git-afsantos/haros/blob/master/setup.py) (High Assurance ROS) framework was developed, which is capable of extracting and, to some extent, reverse-engineering the computation graph. It also provides a visualization of the extracted graph and enables property-based testing for ROS.

![Anders Billise Beck (UR) at ROS-Inudstrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1548779780938-XL4LOTGQ3CCBVC2O6I1T/2018-12-ROS-Industrial-Konferenz-23.JPG)

Figure: *Anders Billise Beck (UR) at ROS-Inudstrial Conference 2018*

Anders Billersoe Beck from [Universal Robots](https://www.universal-robots.com/) was the last speaker in the second session. He introduced the new UR e-series (with integrated force/torque sensor, 500 Hz controller frequency and more new features) and how ROS supports it. For this, a new driver is developed in a Focused Technical Project of [ROSIN](http://rosin-project.eu/ftps) together with the [FZI](https://www.fzi.de/en/home/), which will also remain open-source. The goal is to make a UR robot easy to use and enable plug-and-play with ROS. The driver should make two modes of operation possible: remote control and ROS URcap embedding. More supported features are calibration, a new safety system and easier programming. Beck concluded the presentation with some points that he believes are in need of improvement to make ROS ready for industrial applications. These are easier general use, proper handling of hard and soft real-time boundaries and supporting more control in edge devices.


