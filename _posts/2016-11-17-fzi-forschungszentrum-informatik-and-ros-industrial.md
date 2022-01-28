---
author: Guest User
comments: false
date: '2016-11-17 16:26:29+00:00'
slug: 2016-11-17-fzi-forschungszentrum-informatik-and-ros-industrial
title: FZI Forschungszentrum Informatik and ROS-Industrial
media_type: None
description: 'Submitted by: Arne Rönnau, FZI'
layout: post
old_sp_link: https://rosindustrial.org/news/2016/11/17/fzi-forschungszentrum-informatik-and-ros-industrial
---

Submitted by: Arne Rönnau, FZI

![the ros-i powered fanuc m710 on display at Automatica 2016](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1479399176309-CAC8QK2P5EMD7ITOLX3Y/image-asset.jpeg)

Figure: *the ros-i powered fanuc m710 on display at Automatica 2016*

The [FZI Forschungszentrum Informatik](https://www.fzi.de/en/home/) (FZI Research Center for Information Technology), an independent research institute associated with the Karlsruhe Institute of Technology in Karlsruhe, Germany, has a long standing history of working with various robotic frameworks for a number of robot platforms. From special kinematics, like a six-legged walking robot or two-armed service robot with body joints on a mobile platform, to service and industrial robots like the UR 10 and the Fanuc M710. Since 2000, FZI has developed its own robotic framework MCA (Modular Controller Architecture) which later became [MCA2](http://mca2.fzi.de/wiki/index.php/Main_Page) and which is still used on many robot systems today also outside of FZI. With the increasing popularity and maturity of ROS, however, the focus has shifted towards using and expanding ROS rather than further improving the in-house framework (which is still used for many low-level tasks).

With the release of ROS Diamondback, FZI started to use ROS on the robotic Platforms [KAIRO III](https://www.fzi.de/en/research/projekt-details/kairo/), a snake-like inspection robot, and [LAURON IV](https://www.fzi.de/en/research/projekt-details/lauron/), a six legged walking robot in conjunction with MCA2. The FZI UAV fleet consisting of Parrot AR-Drones and the Asctec UAVs Pelican and Falcon 8 used ROS Fuerte as the main framework from the start. It was also commonly used to analyze data of the autonomous car [CoCar](https://www.fzi.de/en/research/projekt-details/cocar/), for which the available visualization tools proved to be very valuable.

The development efforts of ROS components by FZI also increased together with its extended usage. During the preparation of LAURON V for the first SpaceBot Cup by the German Aerospace Center DLR in 2013, initial fixes were provided for libraries such as the SMACH viewer and the robot\_web\_tools, as they were used extensively to enable autonomous exploration by the walking robot of a Mars-like environment. In October 2014 a larger contribution, the schunk\_svh\_driver package, was released on behalf of Schunk. It is providing hardware support for one of the most mechanically advanced robotic hands today. In 2016 a driver for the LWA4P with CanOpen support followed. Today the FZI also offers workshops teaching ROS to companies when developers need a concise introduction or just specific help with their projects.

ROS has also become a major research topic in public funded projects. The Human Brain Project (HBP), which FZI takes part in, relies heavily on gazebo as a simulation environment, for which tools like a blender-based intuitive robot designer are being developed. The project [ReApp](http://www.reapp-projekt.de/) (Reusable robotic Applications for flexible robots), puts ROS-Industrial at its core, and is in fact a team effort with other ROS-focused institutions like Fraunhofer IPA. By adding semantically-enriched models to ROS packages, ReApp further enhances the already reuse-friendly structure of ROS by enabling easier search and automatic replacement of packages. During preparations for Automatica 2016, FZI used the ROS Industrial stack for a Fanuc M710 and implemented the ROS-Industrial-IO REP for Fanuc robots as first contribution to the ROS-Industrial community, which is currently being finalized.

Since August 2016 FZI is part of the ROS-Industrial Consortium Europe, through which it plans to further increase its activities around ROS and ROS-Industrial. 


