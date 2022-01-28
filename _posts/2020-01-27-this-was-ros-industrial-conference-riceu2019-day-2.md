---
author: Karin Roehricht (Fraunhofer IPA)
comments: false
date: '2020-01-27 13:19:48+00:00'
slug: 2020-01-27-this-was-ros-industrial-conference-riceu2019-day-2
title: 'This was ROS-Industrial Conference #RICEU2019 (Day 2)'
media_type: None
description: Seven years after the very first public event entirely devoted to discussing
  the potential benefits of a shared, open-source framework for ...
layout: post
old_sp_link: https://rosindustrial.org/news/this-was-ros-industrial-conference-riceu2019-day-2
---



![2019-12-ROS-02.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1579272240810-BEK4T8IES5NAKPAW4RZW/2019-12-ROS-02.jpg)

Seven years after the very first public event entirely devoted to discussing the potential benefits of a shared, open-source framework for industrial robotics and automation, Fraunhofer IPA hosted the 7th edition of the [ROS-Industrial Conference](https://rosindustrial.org/events/2019/12/10/ros-industrial-conference-2019) on December 10 to 12, 2019.

This is the **second** instalment of a series of **three** consecutive blog posts, presenting content and discussions according to the event days including the follwing sessions:

1. Day 1 with "EU ROS Updates" (watch all talks in this [YouTube playlist of Day 1](https://www.youtube.com/watch?list=PLXUpEXjGC63yw31SXDRaNykCeBIs6yu-w&v=-KLiGOnSxa0))
2. Day 2 with "Software and System Integration" & "Robotics meets IT" ([YouTube Playlist of Day 2](https://www.youtube.com/playlist?list=PLXUpEXjGC63zFoFyqMLZmplVoTORZ94eA))
3. Day 3 with "Hardware and Application highlights" & "Platforms and Community"

Day 2 Part 1: Software and System Integration
---------------------------------------------

The second day of the ROS-Industrial Conference featured speakers from several well-known companies that have been using ROS for a long time or started using it recently and are developing it further together with the community. While some companies already spoke at the conference in earlier years, there were also speakers from new contributors. This shows that the interest in ROS from the industrial side is still unbroken and increasing.

Matt Hansen from [Intel](https://github.com/intel-ros) opened the second day. He [presented](https://www.youtube.com/watch?v=4_U8lWWvQV0) the ROS developments of his company, which mainly include a Robot Development Kit (RDK) and navigation software. Intel especially focuses on the adoption of ROS2. The RDK supports the development and implementation of software components for mapping and planning, machine vision (point cloud generation, object detection, face and gesture detection and more) and intelligent handling or grasp detection. The comprehensive project navigation2 pursues the goals of providing a customizable (thanks to behavior trees), modular and extensible software. To ensure quality and maintainability, an automated system test was created. It uses Gazebo and a Turtlebot 3 model to test localization, transition into the ‘active' lifecycle state and navigation.

![Matt Hansen, Intel, giving a overview on ROS2 Robot Dev Kit and Navigation2](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1580129215751-WNWUW4W5L3ETZY0PZPVL/2019-12-ROS-36.jpg)

Figure: *Matt Hansen, Intel, giving a overview on ROS2 Robot Dev Kit and Navigation2*

ROS2 tracing was the topic of Ingo Lütkebohle from [Bosch](https://www.bosch.de/en/). Tracing is important because there are currently various problems in performance analysis and execution monitoring, for example: How long does my system take to react? How much resource is it consuming? Factors like distributed systems or repetitive periodic processing complicate performance analyses. Lütkebohle explained, which kind of information is recordable, which tracepoints exist in ROS2, and how static and dynamic tracing differ. In the end, he gave an example of a tracing installation and implementation process.

ROS as the basis for a framework with which industrial robots do no longer need to be programmed but can be intuitively instructed: Pablo Quilez from the startup [drag&bot](https://www.dragandbot.com/), whose first research activities took place at Fraunhofer IPA, spoke about this framework and first industrial projects. With the help of a graphical user interface, the user creates a robot program via drag&drop of function blocks. drag&bot is manufacturer independent, offers the same user interface for different robots, and does not require any expert knowledge in robotics. It is an open platform that third parties can extend, e.g. with ROS packages

Arne Roennau and his colleagues from [FZI Research](https://www.fzi.de/en/about-us/organisation/detail/address/roennau/) Center for Information Technology developed ROS based Cartesian controllers that enable motion, force, and compliance control for robotic manipulators. Cartesian control in task space is necessary for closed loop force control, direct teaching, contact-rich manipulation, manual guidance. That is why FZI worked on active Cartesian compliance using three controller modules and implemented them for a car door sealing assembly, a satellite assembly and many other applications. The goals here were to give the robot error correcting contact skills for autonomous execution that are transferable to different robots. 

More contributions to ROS presented Steve Peters from [Open Robotics](https://www.openrobotics.org/), an institution that has been supporting and evolving ROS and Gazebo since many years. In this context, Open Robotics offers several developer tools to facilitate the use and integration of open source software and supports upcoming ROS releases like Melodic (May 2023) and Noetic (2025), the latter probably being the last ROS1 distribution. Together with other companies in the ROS2 Technical Steering Committee, Open Robotics helps managing the roadmap, contributes development efforts and sets developer policies. Finally yet importantly, interfacing ROS and Gazebo has been on the agenda of Open Robotics for quite some years.

Gazebo simulations were also the main topic in the presentation of Musa Morena Marcusso Manhães. She works for [Bosch](https://www.bosch.de/en/) where she develops a Python library for scripting and rapid-prototyping of Gazebo simulations. So far, there are several application-dependent difficulties with respect to simulations (e.g. generation variations of worlds and models, scripting of world layouts and event-based actions). Marcusso's approach is the procedural generation, a technique from gaming development. It enables rapid-prototyping of simulation scenarios and abstractions to simulation entities, allows scripting of Gazebo simulations, extends templating options for robot descriptions and improves the conversion between URDF and SDF.

![Musa Morena Marcusso Manhães, BOSCH, presenting A Python library for scripting and rapid-prototyping of simulated Gazebo models and worlds called pcg_gazebo_pkgs](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1580129867238-WM2DVET9MV4DAJG8XGRU/2019-12-ROS-51.jpg)

Figure: *Musa Morena Marcusso Manhães, BOSCH, presenting A Python library for scripting and rapid-prototyping of simulated Gazebo models and worlds called pcg\_gazebo\_pkgs*

Nadia Hammoudeh Garcia from [Fraunhofer IPA](https://www.ipa.fraunhofer.de/en/expertise/robot-and-assistive-systems/software-engineering-and-system-integration.html) highlighted the potentials of the combination of model-driven engineering (MDE) and ROS. Among others, ROS developers can benefit from the definition of common design patterns and specifications, model checker techniques and automated code generators.Since there are already about 4000 hand-written open-source ROS packages, Hammoudeh not only develops tools to generate code but also to automatically extract ROS models from the existing code. She released an eclipse-based tooling with a graphical interface and model editors as well as domain-specific languages to the models. All her contributions are also part of the German research project "Service Robotic Network" (see presentation from day 1 for more information). 

Not only MDE can facilitate the deployment of ROS but also the tools from [MathWorks](https://www.mathworks.com/hardware-support/robot-operating-system.html), MATLAB and Simulink. Shashank Sharma presented how this works, which advantages the tools offer, and how they address common challenges of autonomous systems, e.g. multi-domain expertise, complexity, and performance evaluation. He also discussed the key advantages of Model-Based Design and how it can be applied to the robotics and autonomous systems. Therefore, MATLAB helps analyzing and visualizing ROS data and prototype algorithms. A Simulink model allows automated code (C and C++) and ROS node generation as well as prototyping new algorithms through the ROS interface. Finally, the tools from the company allow incorporate ROS in Model-Based Design workflows 

Day 2 Part 2: Robotics meets IT
-------------------------------

Robotics and IT are becoming more and more interlinked – this was already evident at the ROS-Industrial Conference 2018, when Roger Barga from Amazon Web Services ([AWS](https://aws.amazon.com/robomaker/)) was invited to present a new service for robot applications "Amazon Robomaker". Now, one year later, he presented the status of the service. It offers comprehensive functionalities for each of the three stages "design and develop" (storage, logging, metrics, image and video recognition etc.), "test and verify" (simulation tools for thousands of concurrent simulations and model training), and "deploy and update" (control and multiple deployments, manage robots across multiple brands, deployment over-the-air). In addition, AWS contributed source code to ROS2 core, along with tools for ROS2 to improve functionality and code quality. The company will continue these efforts. 

![Roger Barga, AWS Amazon web services, giving a keynote on The Robotic Edge](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1580130105664-MWYBOV97ATW1I92N7A96/2019-12-ROS-57.jpg)

Figure: *Roger Barga, AWS Amazon web services, giving a keynote on The Robotic Edge*

Andrei Kholodnyi from [Wind River](https://www.windriver.com/) addressed the problem that there is an increasing amount of robots using ROS but a decreasing amount of embedded software engineers. He stated that people do not want to program bit and bytes anymore. That is why Wind River provides the downloadable SDK VxWorks for non-commercial usage. ROS2 is built on top of the VxWorks SDK and developers can deploy and run it on ARM and Intel. 

[Canonical](https://ubuntu.com/blog/author/rhys-davies), as the company who publishes Ubuntu, gives developers support for simple, secure, and scalable robotic deployment in the field of ROS. Rhys Davies, a product manager for Canonical's robotics initiatives presented tools like Snaps, containerized software packages for all Linux distributions, the company's efforts for continued support for Python 2, and Extended Security Maintenance (EMS) for ROS, to maintain a robot past its usual lifetime. With these offerings, Canonical aims at supporting users to move to ROS2 and to facilitate the transition of robot systems already in practice. 

The company [eProsima](https://www.eprosima.com/), represented by Jaime Martin Losa, offers the open-source DDS for ROS2 "eProsima Fast RTPS". This DDS offers real-time behavior (static allocations, non-blocking calls, sync and async publishing), intra-process communication and discovery server. Martin Losa detailed performance features using the example of an iRobot framework and gave numbers with respect to benchmarking criteria like latency and throughput. More features are currently being developed with the help of project funding from ROSIN (see presentation from day 1 for more details). 

Besides Amazon, [Microsoft](https://www.microsoft.com/en-us/) was one of the most prominent companies presenting at ROS-Industrial Conference. Gunter Logemann talked about ROS applications with Visual Studio Code and Azure. Since June 2018, the IT giant has been contributing to the ROS development and since then, 279 ROS packages have been enabled on Windows. New features are for example the Azure IoT\_Hub connector, Azure Kinect ROS Node, and Windows ML node. The developer environment Visual Studio Code offers several ROS extensions like automatic workspace activation, starting, stopping, and viewing the ROS system status, and automatically discover build tasks. ROS2 support is also included.

Both offensive and defensive security aspects were presented by Endika Gil Uriarte and Victor Mayoral from [Alias Robotics](https://aliasrobotics.com/). They explained that the network and transport layers are the most vulnerable points in an OS and not ROS, ROS2 or the application itself. For them, security is a process and cannot be "finished" with a certain technology. The company offers a variety of security tools and has profound knowledge concerning vendors as well as ROS and ROS2 thanks to its public robot vulnerability database and to a robot security survey done in conjunction with Joanneum Research Robotics. One of the solutions to enhance security is the company's toolbox for robot security "alurity". Soon, there will also be RIS, the Robot Immune System for UR robots offering defensive robot security.

![audience at ROS-Industrial Conference 2019 at Fraunhofer IPA in Stuttgart, gErmany](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1580130731538-8GZBYCBPZPVY9R94A9WA/2019-12-ROS-37.jpg)

Figure: *audience at ROS-Industrial Conference 2019 at Fraunhofer IPA in Stuttgart, gErmany*

Analytics for autonomous driving and large-scale sensor data processing was the topic of Jan Wiegelmann working for [Autovia](https://autovia.ai/). The challenge here are the petabytes of data that are generated daily both from simulation and real-world sensor data. The Autovia Analytics Platform enables large-scale data processing for these use cases. Autovia IO is a data access layer that enables analytics apps to read ROS bags from local and cloud storage. It works for diverse platforms and does not require a ROS installation. Additionally, Autovia FS is a virtual file system with which all applications can read ROS bags from local and cloud storage. Autovia IDE completes the offer: It is an analytic toolbox running as managed service and addresses R&D engineers in automotive and aviation industry.

Christoph Hellmann Santos closed the second conference day and presented the EU initiative [agROBOfood](https://agrobofood.eu/), which aims at bringing ROS to the agro-food sector. This domain will have to cope with major changes like ageing population and less working population, climate change, less productiveness of ecological food… New methods like vertical or urban farming and the key topic sustainability are on the rise. Already now, we see quite many robot platforms on the fields that might help mastering these changes. In this context, agROBOfood has three offers: Firstly, ROS will be pushed to use it in agricultural applications. Main topics are functional safety for mobile agricultural robots, software architecture and development and organizational structures like working sponsors and adding groups. Second, the project addresses SMEs with an open call for funding ROS software developments. Third, service providers can join the agROBOfood network and benefit from access to technology maps, market knowledge, and standardization activities. Finally, they can get in contact with people from all areas of agrofood robotics.

In the evening of this conference day, the social dinner took place in the restaurant "Leonhardts" in direct neighborhood to Stuttgart's iconic TV tower. For some more impressions of the whole event please watch the [event video](https://www.youtube.com/watch?time_continue=1&v=Vd38e6Ly5cY).


