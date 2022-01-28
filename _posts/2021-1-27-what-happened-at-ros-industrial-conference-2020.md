---
author: Christoph Hellman Santos (Fraunhofer IPA)
comments: false
date: '2021-03-01 08:22:01+00:00'
slug: 2021-1-27-what-happened-at-ros-industrial-conference-2020
title: What happened at ROS-Industrial Conference 2020?
media_type: None
description: This year was a tough year for event organizers. Around the world, events
  needed to be moved online to react to the COVID-19 pandemic. The ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/1/27/what-happened-at-ros-industrial-conference-2020
---

This year was a tough year for event organizers. Around the world, events needed to be moved online to react to the COVID-19 pandemic. The pandemic also lead to ROS-Industrial Conference a being virtual venue, but did not affect the success of the event. With more than 250 attendees, the conference grew by 66% in attendance compared with previous years.

This year's conference featured mainly four different activities. There were topic specific technical one-hour presentation sessions, in which 2-4 speakers presented their newest developments and experiences with ROS. A small virtual exhibitor area enabled attendees to get in contact with organisations active in the ROS-Industrial community. In networking sessions, attendees had the possibility to meet each other and get to know each other. The ROS-Industrial Video Competition accompanied the conference and the winner's ceremony took place on the second day of the conference.

**Conquering the industry**
---------------------------

The conference kicked off with a session about ROS-Industrial and its current state. In this session, Christoph Hellmann Santos (Program Manager of the European branch of the ROS-Industrial Consortium) gave a motivating presentation about ROS and the Mission of the ROS-Industrial Consortium. He explains that low volume high variance production with robotics is a "Final frontier of robotics" and that pioneering in robotics is hard and lonely. According to Christoph Hellmann Santos, ROS and ROS-Industrial have a unique community, which helps with on the one side with reusing robot software and on the other side with being less lonely and getting support. With more than 80.000 developers that published more than 200.000 ROS packages on GitHub ROS is also the biggest open source robotics ecosystem that ever existed. For a long time industry said, ROS is not ready for industry – today thousands of robots controlled by ROS/ROS2 are running in 24/7 in our factories (BMW, Audi, MIR, ). Another chance states Christoph Hellmann Santos is that ROS/ROS2 is a prime platform for AI-based algorithm deployment in robotics.

As second presenter in this session, Carlos Hernandez Corbato (Project manager of the H2020 ROSIN project and assistant professor at TU Delft) presented the results of the H2020 ROSIN project. The project was established in 2017 as support project for the ROS-Industrial initiative. It had three major missions, which were making ROS better, business friendly and accessible. The ROSIN project itself was a great success more than 70 technical and educational projects for around the ROS-Industrial initiative were financed. In total, ROSIN generated 9M€ investment into new ROS packages. This was also visible throughout the conference as a number of the ROSIN FTP projects presented their results.

**The ecosystem is vibrant**
----------------------------

During the conference, many new and recently developed packages were presented. This started of with a session on visualization tools in which Rafael Luque (FADA) presented integration of laser projectors into ROS. Next Darko Lukic (Cyberbotics) gave details about ros2 and webots integration. Levente Tamas (Technical University of Cluj-Napoca) and Francisco Marin (Rey Juan Carlos University) went on and explained how to enable augmented reality in ROS using different tools.

In the industrial tools session, Johannes Meyer (Intermodalics) explained how the realtime robotics framework OROCOS can be integrated into ROS. Rafael Arais (INESC TEC) explained the package robin, which provides a ROS-CODESYS bridge. Luca Muratore (IIT) showed the ROS End-Effector framework, which abstracts end effector control and finally Alejandro Mosteo (Centro Universitario de la Defensa) presented RCLAda, an Ada implementation for ROS2.

In the session about planners, Kristofer Bengtsson (Chalmers University of Technology) presented a sequence planner for intelligent industrial automation using ROS. Allessandro Umbrico presented ROXANNE, which is a ROS package aiming at facilitating the integration of Artificial Intelligent Automated Planning and Execution techniques with robotic platforms. This package specifically supports the development of ROS-based deliberative architectures integrating timeline-based planning and execution capabilities. Finally César López ((Nobleo Technology) showed new implementations for coverage path planning and control.
In the control and path planning session, Jordan Palacios and Victor López (Pal Robotics) explained the new ros2\_control developments and showed a practical example. The next speaker was Henning Kayser (Picknik Robotics) who presented the newest developments around Moveit for ROS2. Finally, Gilles Chabert (IRT Jules Verne) talked about trajectory validation using interval computation. This session showed that ROS2 is getting ready for manipulation.

**Model-driven robotics and development solutions available**
-------------------------------------------------------------

ROS is also becoming a prime platform for model driven robot development. In the session about model-driven robotics, Ricardo Sanz (Polytechnic University of Madrid) explained how systems engineering knowledge can be used at runtime by their framework called mROS. Then Ansgar Rademacher (CEA List) presented the integration of ROS/ROS2 into Papyrus for Robotics, a model-driven development IDE. Finally, Shashank Sharma and YJ Lim (MathWorks) presented how MATLAB and Simlink can be leveraged for model-driven automated driving system development.

In the session, full stack solutions speakers presented solutions for developing robot software using ROS. Pablo Quilez (Drag & Bot GmbH) showed how their software makes developing industrial robot applications easy and robot manufacturer independent. Herb Kuta (LGE) talked about OpenEmbedded, meta-ros and webOS, which makes developing custom linux distributions for embedded systems that package ROS easy and automatable. Mathew Hansen (AWS) talked about AWS RobotMaker, which is a cloud based solution for robot development and lifecycle management.

**Software quality and Security are improving**
-----------------------------------------------

Industrial deployment of robot software requires high quality code. In the software quality session, Bainian Chen (ARTC) explained new features of industrial\_ci, which is a continuous integration solution for ROS and ROS2. Zhoulai Fu and Francisco Martinez (ITU) presented their experiences with fuzz testing ROS components.
Increased connectivity in automation leads to higher productivity but also to higher vulnerability for cyber-attacks. Therefore, security is a major factor for robot systems. In the security session, Victor Mayoral (Alias Robotics) presented how robot end-points can be protected against cyber-threats. Federico Maggi (Trend Micro) explained how legacy programming languages in robotics endanger robot security. Finally, Ulrich Seldeslachts (LSEC) gave a broader perspective on hardening industrial robotics installations.

**ROS 2-based real-time systems are in sight**
----------------------------------------------

Real-time is becoming a more and more pressing topic for spreading ROS in industry. ROS 2 now has real-time capable middleware and schedulers. Ralph Lange (Bosch Corporate Research) presented their implementation of a real-time and deterministic scheduler for ROS 2. Francesca Finocchiaro and Pablo Garrido (eProsima) presented how ROS 2 can be run on microcontrollers using µROS. Finally, Lennart Puck (FZI) presented how real-time systems can be created using ROS 2 as well as a benchmark of these systems. Lennart Puck stated that based on their benchmarks ROS 2 can meet real-time requirements. Katherine Scott (Open Robotics) talked about the transition from ROS 1 to ROS 2 and the general design decisions. The conclusion in general is that now is the time to switch to ROS 2. 

**Professional applications are expanding**
-------------------------------------------

Another part of the conference were three sessions around applications of ROS in professional scenarios or products. This was kicked of with a session on industrial applications on the first day of the conference, where ABB Corporate Research presented how ABB robots can be controlled with ROS and Tecnalia showed how scan & plan applications can be implemented on industrial robots using ROS. On the second day another session on industrial applications held presentations from Bosch, Sewts and Pilz. Timo Steinhagen (Bosch) presented the Locator, which was developed using ROS. Sewts presented their robot application for handling textiles, which is based on ROS. Pilz talked about their ROS-based service robotics portfolio. Another session focused on applications in agriculture. Here, Heiko Engemann (FH Aachen) presented their robot the ETAROB, which runs ROS. Felipe Neves dos Santos (INESC TEC) explained how they use ROS for robots for woody crops. Finally, Wilco Bonestroo (Saxion University of Applied Sciences) talked about using ROS for developing drones for agriculture.

**ROS-Industrial Video Competition**
------------------------------------

More proof of ROS in application was achieved by the ROS-Industrial Video Competition which asked for videos in the categories professional applications and cloud robotics. The cloud robotics category was sponsored by AWS. In total, 33 videos were submitted. In the category cloud robotics, **INESC TEC** won with the following submission.

The professional application category was won by the company **QuadSat**, which produces drones for antenna testing.

**Links & Videos**

All competition videos can be found here: <https://rosindustrial.org/rosindustrial-video-competition-2020>

The conference videos can be found here:

* [Day1](https://youtube.com/playlist?list=PLXUpEXjGC63xjgGfshB72t0ipiD8R1vgN)
* [Day2](https://youtube.com/playlist?list=PLXUpEXjGC63zg1D22KdjqifCQkOX85Kzf)

