---
author: Guest User
comments: false
date: '2018-06-15 12:40:49+00:00'
slug: 2018-6-15-a-brief-report-from-the-ros-industrial-eu-spring-workshop
title: A brief report from the ROS-Industrial EU Spring workshop
media_type: None
description: Thanks to the participation of several members of the ROS-Industrial
  community in Europe and of new participants interested in knowing more on the ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/6/15/a-brief-report-from-the-ros-industrial-eu-spring-workshop
---

Thanks to the participation of several members of the ROS-Industrial community in Europe and of new participants interested in knowing more on the topic, we are happy to report on a successful ROS-Industrial EU Spring'18 Workshop at Fraunhofer IPA.

During the two days of May 28-29, organizations within the ROS-Industrial consortium had the opportunity to present their current development projects to an audience of technical experts.

[Erle Robotics](http://erlerobotics.com), represented by Irati Zamalloa, presented the concept of a common interface for the description of robot modules and hardware sub-components allowing their reusability, composability and interoperability. The project is already publicly [available](https://therobotmodel.com/) as a ROS2.0 implementation. During the ensuing Q&A, feedback from participants pointed to the possibility of integrating such effort with a MDE approach, where the information could be semantically annotated and verified. Further feedback is welcome, with a [github repository](https://github.com/erlerobot/HRIM) setup for the purpose.

![DSC_0002.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1529066192602-TAMUZCNWZ13PC509DLXO/DSC_0002.JPG)

The second workshop session focused on ways to make ROS-based systems and PLCs interoperable. Sebastian Friedl from the [University of Stuttgart](https://www.isw.uni-stuttgart.de) gave an introduction to the OPC-UA architecture and the improvements that his institution is making on [this open source implementation](https://github.com/seronet-project/open62541) of the protocol. He also presented the ROS <-> OPC-UA gateway that is under development within the [SeRoNet](https://www.seronet-projekt.de) project. 

On a similar topic, Tiago Pinto from [INESC TEC](https://www.inesctec.pt/en) continued the session showing how his team approaches communication between CODESYS and ROS systems. The implemented wrapper is already being used for practical application within the project [ScalABLE 4.0](https://www.scalable40.eu/), with source code scheduled for public release in August. 

![DSC_0004.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1529066241196-95BDDCY72LQZKCYYL239/DSC_0004.JPG)

Wrapping up the topic, Ludovic Delval from Faunhofer IPA presented a survey of the existing ROS drivers implementations supporting different fieldbus protocols. The detailed overview was appreciated by the participants and is available as reference [here](/s/ROSI-Spring18_FraunhoferIPA.pdf).

As part of the efforts of the [ROSIN](http://rosin-project.eu/) project to make ROS-Industrial better and business-friendlier, partners of the consortia joined for the second day of the workshop to show the tools developed for the quality assurance on the ROS software development. Jonathan Hechtbauer from Fraunhofer IPA and Anthony Remazeilles from Tecnalia gave an update of the software efforts like the improvements on the [quality badge](https://discourse.ros.org/t/ros-wiki-announcing-extended-ci-badges-in-package-headers/4930), the [rosinstall time machine tool](https://github.com/rosin-project/rosinstall_generator_time_machine), and a generator for ROS packages. Preliminary code is available at the [github organization](https://github.com/rosin-project/) of the project.

Concluding the event, the ROSIN coordinator Carlos Hernández Corbato informed the audience about the [opportunities](http://rosin-project.eu/ftps) for ROSIN Focused Technical Projects. A grant up to 100K to fund your software development is available to institutions with a legal seat in the EU and associated countries. The application process is explained in detail at the [project page](http://rosin-project.eu/ftps).

Given the request from interested parties who could not join us in Stuttgart, we made the content and slides of this workshop publicly available under the following [link](https://rosindustrial.org/events/2018/5/23/ros-industrial-workshops-hrim-rosin-quality-hub-ftp-info-session).

We look forward to a second edition of the workshop in the fall!


