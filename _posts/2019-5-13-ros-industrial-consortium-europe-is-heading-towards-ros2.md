---
author: Thilo Zimmermann (Fraunhofer IPA)
comments: false
date: '2019-05-13 15:55:55+00:00'
slug: 2019-5-13-ros-industrial-consortium-europe-is-heading-towards-ros2
title: ROS-Industrial Consortium Europe is heading towards ROS2
media_type: None
description: With the growing excitement and curiosity surrounding [ROS2](https://index.ros.org/doc/ros2/Releases/),
  ROS-Industrial Consortium Europe (RIC-EU) ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/5/13/ros-industrial-consortium-europe-is-heading-towards-ros2
tags: dds ros2 ric-eu tech-workshop stuttgart fraunhofer-ipa
---

With the growing excitement and curiosity surrounding [ROS2](https://index.ros.org/doc/ros2/Releases/), ROS-Industrial Consortium Europe (RIC-EU) had the pleasure to host the Spring 2019 edition of the [RIC-EU Tech Workshop](http://rosin-project.eu/event/ros-i-eu-spring-19-workshop). It took place on May 6th and 7th at Fraunhofer IPA in Stuttgart, Germany. Some of the main drivers of DDS and ROS2 developments personally presented their insights and gave hands-on sessions during the event. For this, participants were provided with USB sticks with Ubuntu Bionic and ROS Melodic and ROS Crystal pre-installed (just as for all our ROS-Industrial [trainings](https://www.ipa.fraunhofer.de/en/Events/ros_industrial_training.html)). The event has been free for [worldwide members of any ROS-Industrial Consortium](https://rosindustrial.org/ric/current-members) and was fully booked out with 40 people attending from all over Europe.

On Day 1, the workshop started with RIC-EU manager Thilo Zimmermann who welcomed the participants at Fraunhofer IPA and introduced the ROS-Industrial Consortium Europe and its EU project funding opportunity ([next cut-off dates June 14 and September 13, 2019](http://rosin-project.eu/ftps)).

As ROS 2 supports multiple [DDS/RTPS](https://index.ros.org/doc/ros2/Concepts/DDS-and-ROS-middleware-implementations/) implementations, RIC-EU proudly hosted one of the most popular DDS vendors, eProsima, to explain the main concepts of DDS and present [their stack](https://www.eprosima.com/index.php/products-all/eprosima-fast-rtps) at the workshop. During the five hours of presentations and hands-on workshops, Borja Outerelo Gamarra and Jaime Martin Losa covered topics like DDS Introduction, presentation of the standard and motivation of DDS & DDS Architecture, and DDS QoS. Attendees practised on a "hello world" example. ePROSIMA's slides can be found [here](/s/ROS-Industrial_workshop_ROS2.pdf).

![20190506_142557[1].jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557762581422-SXQ6AJGMPZ2QCGMTQUGW/20190506_142557%5B1%5D.jpg)

On Day 2, Ralph Lange from RIC-EU member BOSCH gave an in-depth presentation of the current status of ROS2. He included hands-on tasks using ROS2 and sow new features and also provided information on the upcoming [d-turtle "Dashing Diademata"](https://index.ros.org/doc/ros2/Releases/Release-Dashing-Diademata/) release on May 31, 2019. Ralph's presentation slides "Current Status of ROS2 - Hands-on Feature Overview" can be found [here](/s/2019-05-07_Current_Status_of_ROS_2.pdf).

![20190507_090637[1].jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557762657452-AV4EXOUCNSCB2NU3CVDB/20190507_090637%5B1%5D.jpg)

The second presentation by Ingo Lütkebohle, also from BOSCH Corporate Research, introduced the [micro-ROS](https://micro-ros.github.io/) activity. Ingo is one of the investigators of the EU funded [OFERA project](http://ofera.eu/), which ports ROS2 to "extremely resource constrained devices" (usually, microcontrollers) with the new DDS XRCE standard. He demonstrated this by using a [Cortex M4 board](https://micro-ros.github.io/docs/hardware_support/) mounted on a first generation Turtlebot. Ingo's presentation slides can be found [here](/s/2019-05-07_micro-ROS.pdf).

![20190507_113032[1].jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557762750934-ICC3ROHLLWEUJKIM9VSW/20190507_113032%5B1%5D.jpg)

After a lunch break, Ludovic Delval of Fraunhofer IPA gave a hands-on workshop on how to migrate ROS1 node to ROS2. Lastly, Harsh Deshpande, also from Fraunhofer IPA, previewed the porting of the ur\_modern\_driver to ROS2 and presented a proposal for the [action\_bridge](https://github.com/ipa-hsd/action_bridge), which currently bridges between ROS1 action client and ROS2 action server.

At the end of the workshop, participants and ROS-Industrial Consortium members agreed that 2019 is promising a lot of developments in ROS2. In April at ROS-I Consortium [Americas 2019 Annual Meeting](https://rosindustrial.org/news/2019/4/18/what-took-place-at-the-ros-i-consortium-americas-2019-annual-meeting), RIC members interacted and exhibited an interesting panel session titled "Is ROS2 Ready for the Factory Floor". In June, Ludovic Delval of Fraunhofer IPA will present the latest updates at [ROSCon France](http://roscon.fr/) in Paris and Harsh Deshpande at the ROS-Industrial [AP Workshop 2019](http://roscon.fr/) in Singapore. 

The next RIC-EU Tech Workshop is foreseen for [Fall 2019](https://rosindustrial.org/events/2019/05/06/ros-industrial-eu-19-fall-workshop) (tentative dates October 09-10). The 2019 edition of the [ROS-Industrial Conference](https://rosindustrial.org/events/2019/12/10/ros-industrial-conference-2019) is planned on December 10-12, 2019 (save the date!).


