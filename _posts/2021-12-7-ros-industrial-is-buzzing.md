---
author: Christoph Hellman Santos (Fraunhofer IPA)
comments: false
date: '2022-01-14 12:24:55+00:00'
slug: 2021-12-7-ros-industrial-is-buzzing
title: ROS-Industrial is buzzing
media_type: None
description: This year's ROS-Industrial Conference took place on December 01-02, 2021
  as a virtual event. With more than 300 registrants it was the largest ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/12/7/ros-industrial-is-buzzing
---

*This year's ROS-Industrial Conference took place on December 01-02, 2021 as a virtual event. With more than 300 registrants it was the largest conference of the so far 9 conferences that have been organized since 2012. In this article, we try to capture the major developments around the ROS-Industrial initiative presented during the conference.*

**More and more companies are starting to deploy ROS in their industrial applications.**

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/8c1dee86-d6ab-44b2-a22e-aeb79be88603/d%26b.png)

Figure: *Operator using Drag & BOt to program robot*

At the conference **drag&bot** explained how their system for easy robot programming is being used by industry and showed a number of example applications. Their software is based on ROS and enables programming different industrial robots using a simple drag and drop interface. Drag & Bot also offers an interface for integrating external ROS programs and can be used by developers to deploy their ROS based solutions to industry. 

Another company that has today more than 450 mobile robots running their ROS based Navigation is **Node Robotics**. Robots running Node Robotics software are deployed in BMW's production facilities and in other companies. Node Robotics software offers easy integration of mobile robots of different types into one fleet and enables software systems for operating a single AMR, for data sharing between AMRs as well as fleet management systems and their software systems are based on ROS. The companies first deployment were of freely navigating AMRs was in 2016 in a plant of the automobile producer Audi.

**Enabling safety and towards real-time execution with ROS**

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/65822aa0-37a8-4312-8cfb-fc1070a65516/psenscan_bg.jpg)

Figure: *PSENscan LaserScanner developed by pilz with ROS Integration*

The ROS-Industrial ecosystem is producing a number of cutting edge solutions integrating ROS with industry. **Pilz** is providing a portfolio of safety components that can be used to build a safety system around ROS based mobile robots. The center of the portfolio is the laser scanner PSENscan that can monitor configurable safety zones for the robot. The PSENscan also offers functionalities for integrating speed monitoring and it integrates with ROS via an open source driver.

Progress has also been made with regards to real-time execution in ROS2 systems. Andrei Kholodnyi (**Wind River**) co-lead of the ROS2 real-time working group presented the groups work. Members of the working group have developed a number of new real-time optimized ROS2 executors. Another available component provided by the working group is a Raspberry PI4 based real-time benchmarking system with RT\_PREEMPT kernel for Ubuntu 20.04. ROS2 developers that are not satisfied with the real-time performance of RT patched Linux can also choose to switch to Wind River's vxWorks or Blackberry's QNX, both systems executing ROS2 applications.

**Towards integration into industrial robot software platforms**

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/7f050545-adf4-4695-8379-fffbf3c8e002/URpic.jpg)

Figure: *Universal Robots teach pendant that has been enhanced with ROS support*

As previously mentioned, drag & bot's software offers one way to integrate ROS into an industrial robotics platform but more solutions are becoming available. Another approach was presented by **Universal Robots (UR)** and **Forschungszentrum Informatik (FZI)** who have been collaborating to develop an advanced ROS interface for UR's robots. The work enables direct integration of externally running ROS-based applications into URScript programs running on the robot. During the conference they showed a new interfaces that enable cartesian control and speed scaling for industrial robots from within ROS. UR also showed a prototype of a URCap that enables integration with ROS at the conference. The goal of the development is to leverage ROS' capabilities for UR's robots and making them available via URCaps.

**Canonical** the publisher of Ubuntu also presented their solutions for deploying robot software. Their solution mainly consists of snap and Ubuntu Core. snap is a solution to create containerized and easily deployable software applications. Canonical claims that snaps have advantages for embedded systems other solutions such as docker because they are more easily integrated with embedded hardware. Ubuntu Core is a minimal operating system including application packages which is based on snap containers which enables a modular and simple architecture for embedded systems. The Canonical software solutions are optimized for ROS and they are already used in industry e.g. in Bosch Rexroth's CtrlX. snap are becoming another way of integrating ROS in industrial control systems and software platforms of the future.

*Integration with 5G and hardware acceleration*

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/243672b2-0c9c-4588-b217-18b5341f87b7/xilinx.png)

Figure: *Board with Hardware Acceleration support in ROS*

**Erricsson** and **eProsima** presented their work of integrating ROS2 with 5G systems and thus moving ROS2 towards enabling distributed real-time systems. The two organizations collaborated on developing an interface for ROS2 and the underlying DDS middleware implementations to enable creating separate IP flows for specified ROS2 communications (previously only a seperate IP flow was created by DDS implementations) and setting 5G quality of service parameters for these IP flows. The interface has been integrated in eProsima's FastDDS. FastDDS is also the default middleware for the next longterm release ROS2 Humble (May 2022) which means integration of ROS2 with 5G quality of service is becoming simple.

Another interesting development was presented by **Xilinx**. Xilinx and AMD are working on providing prime hardware acceleration support for ROS2. The development of hardware acceleration interfaces is driven by the ROS2 hardware acceleration working group. Xilinx is developing the Kria Robotics Stack based on the open interfaces defined by the working group. Major features of the development are easy integration of embedded targets into the ROS2 build system and tools and an API for defining which parts of the ROS2 computation graph is run on CPU or e.g. FPGA. This development promises to make ROS2 a prime platform for deterministic and lightning fast computations that are needed for future robotics applications. Other companies such as NVIDIA are also targeting ROS2 for their hardware acceleration solutions as Katherine Scott (Open Robotics) stated in her presentation.

*Tackling the industrial security challenge*

Manufacturing systems are becoming a target for cyber criminals. As robots are deployed in all kind of systems that are essential for a countries economy they can even become a prime target in potential cyberwar scenarios. The ROS-Industrial community is aware of the arising problems and members **Alias Robotics, Trend Micro** as well as **Canonical** have presented research findings, solutions and services for ROS developers. Alias Robotics provides solutions such as the Robot Immune System (End point protection) as well as services for identifying potential risks in robotic products such as Threat Modeling. Alias Robotics and Trend Micro have together analyzed the DDS standard which is ROS2's prime middleware and used in a wide range of applications such as medical, automotive and space. A number of security issues where discovered and reported. Canonical provides longterm support for end of life ROS distributions with security updates and the previously described deployment toolchain based on Ubuntu Core and snap which simplifies security updates during production. 

*Advanced motion planning: Mobile manipulation, hybrid planning, collision avoidance and welding*

Advanced manipulation has always been a strong suit of the ROS ecosystem. This years conference made abundantly clear that this is also true for ROS2. **PickNik** main driver behind moveit2 gave an overview of new features currently being developed, notably mobile manipulation and hybrid planning. A mobile manipulation demonstration for moveit2 was developed together with HelloRobot ([workshop](https://moveit.ros.org/events/rosworld-2021-workshop/)). A demonstrator for hybrid planning which integrates a global planner and local planner is being developed together with Fraunhofer IPA and targeting multi-layer welding. The goal is to perform scanning, welding and local planning at the same time to achieve higher process quality. Another talk focusing on robotic welding was contributed by **IRT Jules Vernes** that presented how they leveraged ROS for building a lightweight welding robot for mobile welding applications from scratch. They were able to design hardware and controller within a year and create a working prototype. **SwRI** has developed a ROS2 demonstrator for Scan & Plan applications (workshop).

**ARTC** is developing a software tools for collision avoidance in dynamic environments. Currently, obstacle avoidance during motion is not easily available for robot arms in ROS2. Therefore, ARTC has developed a dynamic safety joint trajectory controller, that integrates with motion planning solutions such as moveit2 and tesseract. The controller includes collision checking, speed scaling and re-planning and average execution frequencies of more than 200 Hz are possible on commercial-off-the-shelf hardware. 

*Model-driven robotics development with ROS*

Software for modern robot systems is becoming more and more complex. Development and testing is becoming more and more difficult. It is time to work on handling the rising complexity of robotics development. **Fraunhofer IPA** presented their work on a model-driven development toolchain for ROS-based systems. The toolchain enables extracting models from available handwritten ROS components, defining ROS systems of existing and new components using a graphical tool and deploying the defined systems in different fashions i.e. ROS package or a complete docker container. The toolchain is currently in alpha state and heavily worked on.

*SpaceROS and other news*

* The space industry in the US is on the rise and with it is the interest in robotics solutions for space. ROS is already deployed in a number of non-critical space applications. **Open Robotics and PickNik** are plotting the next big step for ROS - **SpaceROS** - qualifying ROS and moveit for mission critical space applications.
* TurtleBot4 is coming in 2022 with a base from IRobot

**Summary**

This year's conference showed that ROS is being commercially deployed in industry and we are seeing that industrial robotics platform providers (UR, drag&bot) are opening their platforms for ROS. Additionally, a number of supplier companies are providing key technologies for building safety systems around ROS-based robot applications. Furthermore, ROS2 has many configuration options for achieving real-time performance and industrial operating system developers such as Blackberry and Wind River are supporting ROS2. ROS2 is becoming a prime robotics platform for new technologies such as 5G and hardware acceleration thus enabling the robot applications of the future. ROS2's security is moving in the focus of and being monitored by the security research community and a number of specialized security solution providers are available. With ROS2's cutting edge motion planning capabilities this means building industrial robotics applications with ROS2 and deploying them to industry is becoming much easier.


