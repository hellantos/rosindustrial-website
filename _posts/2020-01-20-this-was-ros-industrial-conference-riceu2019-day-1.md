---
author: Karin Roehricht (Fraunhofer IPA)
comments: false
date: '2020-01-20 09:11:36+00:00'
slug: 2020-01-20-this-was-ros-industrial-conference-riceu2019-day-1
title: 'This was ROS-Industrial Conference #RICEU2019 (Day 1)'
media_type: None
description: Seven years after the very first public event entirely devoted to discussing
  the potential benefits of a shared, open-source framework for ...
layout: post
old_sp_link: https://rosindustrial.org/news/this-was-ros-industrial-conference-riceu2019-day-1
---



![2019-12-ROS-02.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1579272240810-BEK4T8IES5NAKPAW4RZW/2019-12-ROS-02.jpg)

Seven years after the very first public event entirely devoted to discussing the potential benefits of a shared, open-source framework for industrial robotics and automation, Fraunhofer IPA hosted the 7th edition of the [ROS-Industrial Conference](https://rosindustrial.org/events/2019/12/10/ros-industrial-conference-2019) on December 10 to 12, 2019.

This is the **first** instalment of a series of **three** consecutive blog posts, presenting content and discussions according to the event days including the follwing sessions:

1. Day 1 with "EU ROS Updates" (watch all talks of Day 1 in this [YouTube playlist](https://www.youtube.com/watch?list=PLXUpEXjGC63yw31SXDRaNykCeBIs6yu-w&v=-KLiGOnSxa0))
2. Day 2 with "Software and System Integration" & "Robotics meets IT"
3. Day 3 with "Hardware and Application highlights" & "Platforms and Community"

Day 1: Updates from ongoing activities in the EU
------------------------------------------------

Already for the seventh time, [Fraunhofer IPA](https://www.ipa.fraunhofer.de/en/expertise/robot-and-assistive-systems/software-engineering-and-system-integration/open-source-in-robotics.html) invited to a big ROS-Industrial-Event. Meanwhile, the conference – for several years now scheduled shortly before the Christmas break – has established itself as *the* [European](https://rosindustrial.org/ric-eu) event on the topic of [ROS](https://www.ros.org/), where developers, researchers, companies and all interested parties can learn about the current status of the free Robot Operating System ROS and have the chance to network and exchange information. Last December, some 150 participants came to Stuttgart and benefited from around 40 presentations from academia and industry.

The first day was dedicated to "EU Updates". There is a lot to report here because extensive national and EU funding is flowing into research projects that directly serve further developments of ROS and, in particular, work towards industrial suitability. The projects cooperate closely with the existing community and are strongly networked with each other because they pursue a common goal despite their different approaches: the creation of an [EU Digital Industrial Platform for Robotics](https://robmosys.eu/newsrobmosys-rosin-towards-an-eu-digital-industrial-platform-for-robotics/).

The lectures started with an opening by Thilo Zimmermann, Manager of the ROS Industrial Consortium Europe, as well as by Christoph Hellmann Santos, Group Leader at Fraunhofer IPA, and Werner Kraus, Head of the department [Robot and Assistive Systems](https://www.ipa.fraunhofer.de/en/expertise/robot-and-assistive-systems.html), also at Fraunhofer IPA. Kraus gave an overview of the current robotics market and presented growing market figures from the statistics of the "International Federation of Robotics" on both industrial and service robotics. The latter in particular often relies on ROS, because with utilizing existing open source software like ROS, the first prototypes can be created much quicker without having to reinvent the wheel and expend too many own resources. 

![Werner Kraus, head of department of robotics and assistive systems at Fraunhofer IPA](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1579273495333-7WFJQHLNCTYAHNT0Q3ZX/2019-12-ROS-19.jpg)

Figure: *Werner Kraus, head of department of robotics and assistive systems at Fraunhofer IPA*

**Updates on EU project ROSIN**

The largest funding project for ROS is currently [ROSIN](https://rosin-project.eu/), which will come to an end in December 2020. First, Carlos Hernandez Corbato from TU Delft gave an introduction to the project, which has two objectives: 1) assuring the availability of high-quality robot software tools and components, and 2) creating a sufficiently large European user- and developer base. To this end, the project is particularly active in three areas: quality assurance of software development and components, continuing education for students and professionals, and financial support for ROS components in the context of "focused technical projects" ([FTPs](https://rosin-project.eu/results)). In more than 50 FTPs, more than three million Euros of funding have already been granted. 

In order to improve [software quality](https://rosin-project.eu/software-quality-assurance), ROSIN continues to develop technologies and methods like continuous integration, model-driven development and model-in-the-loop, automated test generation and code scanning. In this context, Andrzej Wasowski presented the topic "[Reactive] Programming with [Rx]ROS". Reactive programming raises the abstraction level comparing to the standard ROS API, by making the flow of information explicitly stand out in the source code. 

As far as further [education](https://rosin-project.eu/education) measures are concerned, 530 students and 436 professionals have already been trained in ROS-I schools and ROS-I academies, as Stephan Kallweit from FH Aachen reported. The project goal of 1000 participants has thus already been almost reached and ROSIN has been very successful as a multiplier of ROS knowledge. In addition, in "educational projects" (EPs), formats such as web-based interactive tutorials, ROS training centers or applied training events by 3rd parties are financially supported. The last project year is to be used in particular to create ROS2 training content.

![Carlos Hernandez Corbato, professor at TU Delft and coordinator of EU project ROSIN](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1579273603230-W7SDJE98Q9AS9I8XQ8MY/2019-12-ROS-21.jpg)

Figure: *Carlos Hernandez Corbato, professor at TU Delft and coordinator of EU project ROSIN*

**Insights in „Focused Technical Projects"**

As mentioned above, ROSIN has already promoted more than 50 FTPs addressing specific industry needs. Possible FTP contents were algorithms, e.g. a SLAM algorithm, application templates, improvement of existing components, process-related work, e.g. code security audits, improvement of documentation or the integration with other software frameworks. Five FTPs presented their work at the conference:

* Rafael Arrais from the research institute INESCTEC talked about „[ROBIN: The ROS-CODESYS Bridge](https://rosin-project.eu/ftp/robin)". It focusses on developing and releasing a bidirectional, reliable and structured communication bridge between ROS and CODESYS, a softPLC that can run on embedded devices and that supports a variety of fieldbuses, and even OPC UA. The developed software will allow the parametrization of ROS modules through IEC61131-3 programming languages and also streamline the interoperability between ROS and robotic hardware or automation equipment, fully empowering the Industry 4.0 paradigm of Plug'n'Produce.
* The Norwegian company PPM, represented by Trygve Thommesen, developed [BLACKBOX](https://rosin-project.eu/ftp/blackbox-ros-based-monitoring-system), an automated trigger-based reporting, data recording and playback unit, collecting data from robot and manufacturing systems. It takes error reporting and recovery of industrial robot systems to a new level, by developing and utilizing the innovative ROS based framework. The framework is built upon components from the project partner's previous research and existing ROS modules.
* The Spanish CATEC worked on a robust and reliable [GPS-free localization algorithm for aerial robots applied to industrial applications](https://rosin-project.eu/ftp/robust-and-reliable-gps-free-localization-algorithm-for-aerial-robots-applied-to-industrial-applications). As Paloma Carrasco told, it focuses on safety and computational efficiency. This ROS library helps to foster the development of drone-based solutions for industrial inspections.
* Olivier Michel, CEO at Cyberbotics, presented [cross-platform ROS simulation for mobile manipulators](https://rosin-project.eu/ftp/cross-platform-ros-simulation-for-mobile-manipulators). This FTP aims at developing a simulation framework for training pilots of robots used for intervention in case of a nuclear incident. These robots include industrial arms and will be controlled using ROS. The project will contribute to the ROS-Industrial community with a new open-source, cross-platform, high-performance simulator compatible with ROS for industrial robots.
* Finally, Luca Muratore from IIT in Italy talked about [ROS End-Effector](https://rosin-project.eu/ftp/ros-end-effector). It provides a ROS-based set of standard interfaces to command robotics end-effectors in an agnostic fashion. Nowadays, end-effectors are controlled using customized software wrappers and specific frameworks: ROS End-Effectors aims to design and implement a universal ROS package capable to communicate with different end-effectors. The project will be ROS2 compatible and will work both in simulation (Gazebo environment) and in the real hardware.

The session ended with a lecture by Olivier Stasse, LAAS-CNRS. He reported on the use of ROS in robots that are to be used for partial automation in aircraft construction. This domain requires lightweight, safe, mobile, and versatile manufacturing cells that enable human-robot collaboration. Stasse is developing this within the framework of the "[Rob4Fam](https://www.laas.fr/public/fr/rob4fam-un-laboratoire-commun-airbus-laas-cnrs)" lab (Robots For the Future of Aircraft Manufacturing). Implemented technologies are real-time/interactive planning, torque control, SLAM algorithm and balance so that robots could climb stairs, screw, or drill. All will be ROS controlled. Also, ROS facilitates the integration between lab and industry. 

**More projects boosting ROS**

Besides the research project ROSIN, there are other national or European research efforts building on or improving ROS components. One of them is the EU project [RobMoSys](https://robmosys.eu/), represented at the conference by Dennis Stampfer from Ulm University of Applied Science. It aims at developing composable models and software for robotic systems and uses a model-driven engineering approach as key enabler for complex software and system integration and for integrating existing technologies. A key component is MROS: Metracontrol for ROS2 systems, a RobMoSys-integrated technical project. Carlos Hernandez Corbato from TU Delft talked about this project that enables models@runtime to drive and architectural adaption for reliable autonomy.

On the national level, there is the German project "Service Robotic Network" ([SeRoNet](https://www.seronet-projekt.de/en/home.html)) that aims at building a community-driven platform for a more efficient development of service robots. With the technology behind, the design, development, and deployment of service robots in a variety of areas, from logistics, care, and healthcare to assembly support in manufacturing operations shall be made much easier than today. Through the online platform "[robot.one](https://www.robot.one/)", users, system integrators and component manufacturers of service robot solutions will be able to collaborate efficiently and jointly support solutions from requirements analysis to deployment. In 2020, two open calls offer funding opportunities: The first call, open until late March, adresses companies that aim to make their software or hardware components compatible to the SeRoNet platform. The second call, in summer 2020, addresses end users and system integrators to propose and implement novel service robot solutions using SeRoNet technology.

Last but not least there is the project [RoboPORT](https://roboport.io/). Within this project, an online development platform for service robotics with an extensive library of open source robotics hardware is being created. New collaborative processes such as open innovation, crowd engineering and similar methods will be mapped on the platform to support a continuous and distributed development process. Also, the project supports ideation processes, hackathons and makeathons and offers a network of highly motivated domain experts that help realizing specific project ideas.

**ROS is leaving shop floors**

The EU activities around ROS are not only focused on the use of free software in production environments. The presentation by [Gonzalo Casas](http://www.dfab.ch/twofolio/gonzalo-casas/) from ETH Zurich showed how ROS can be used for architecture and digital fabrication in the construction industry. For example, a robot can use the path planning software MoveIt to build a wall with bricks. 

![Gonzalo Casas of ETH Zurich presented how ROS for architecture and digital fabrication in the construction industry](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1579273731415-MGWA0HSQ26DVBWVD83IO/2019-12-ROS-34.jpg)

Figure: *Gonzalo Casas of ETH Zurich presented how ROS for architecture and digital fabrication in the construction industry*

Finally, it is the agricultural and food sector where robotic applications are increasingly in demand, including those using ROS. Fraunhofer IPA is also very active in this area, for example in the lead project at Fraunhofer "Cognitive Agriculture" ([COGNAC](https://www.ipa.fraunhofer.de/de/referenzprojekte/cognac.html)) for sustainable and at the same time profitable agriculture. At EU level, the [agROBOfood](https://agrobofood.eu/) project is currently gaining momentum with the aim of building the European ecosystem for the effective adoption of robotics technologies in the European agrifood sector. These agricultural activities are not the first ones related to ROS. As [Andreas Linz](https://www.hs-osnabrueck.de/de/forschung/recherche/laboreinrichtungen-und-versuchsbetriebe/labor-fuer-mikro-und-optoelektronik/) from Hochschule Osnabrück presented, there were projects like BoniRob and elwoRob that already built on ROS. The advantages are manifold: ROS is modular, expandable, reusable, has a huge and active Community and offers over 3000 nodes for nearly all use cases and a large collection of helpful tools, i.e. Rviz. Also, many companies provide ROS compatible drivers and software tools for their hardware, and the integration with other open source libraries like PCL (Point Cloud Library), OpenCV or Gazebo is possible.

The BoniRob system is a modular Robot Platform for agricultural applications using an app concept. Depending on the task, different hardware and software modules can be installed. So far, there is a phenotyping app and a soil2data app measuring the nutrients in the soil. Furthermore, there is the robot elWobot for maintenance in orchards and vineyards and there are robots for education and demonstration. For all these, ROS plays a crucial role.

The first conference day ended with a welcome reception and several ROS demonstrators at the Stuttgart research campus "[ARENA2036](https://www.arena2036.de/en/)" for future car manufacturing.

For some more impressions of the whole event please watch the [event video](https://www.youtube.com/watch?time_continue=1&v=Vd38e6Ly5cY).  


