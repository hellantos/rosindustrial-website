---
author: Guest User
comments: false
date: '2016-05-25 16:48:38+00:00'
slug: 2016-5-25-legal-aspects-and-best-practices-of-open-source-clearing-doubts
title: Legal aspects and best practices of open-source
media_type: None
description: On April 19-20 Fraunhofer IPA hosted an [event](/s/OSSProgram.pdf) organized
  in collaboration with [euRobotics AISBL](https://eu-robotics.net/) on ...
layout: post
old_sp_link: https://rosindustrial.org/news/2016/5/25/legal-aspects-and-best-practices-of-open-source-clearing-doubts
---

On April 19-20 Fraunhofer IPA hosted an [event](/s/OSSProgram.pdf) organized in collaboration with [euRobotics AISBL](https://eu-robotics.net/) on the best practices and legal aspects of Open-Source Software (OSS) in robotics and automation. The rationale behind the event was that while OSS is an established and accepted factor in "software-heavy" business domains like enterprise IT systems and smartphones, its inner workings are less understood in industries where software in now shifting from a component with ancillary role to one with high added-value. With the changes poised to happen in industrial robotics and automation by the advances in robotics science on one hand (just think of the progress in autonomous driving and its underpinning achievements in perception, planning, control) and by government-mandated initiatives like Industrie4.0 on the other, the ROS-Industrial team believes that OSS is a great opportunity to accelerate this process. However, to foster its adoption we understandably need to identify and clear also non-technical obstacles such as possible legal, economic and regulatory aspects.

![IMG_9888.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1464193400725-MR62TMPU061GNK76RYNQ/IMG_9888.JPG)

![IMG_9891.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1464193522237-P2HZYDD30FFKH86MSPTZ/IMG_9891.JPG)

#block-yui\_3\_17\_2\_1\_1464193149000\_42640 .sqs-gallery-block-grid .sqs-gallery-design-grid { margin-right: -20px; }
#block-yui\_3\_17\_2\_1\_1464193149000\_42640 .sqs-gallery-block-grid .sqs-gallery-design-grid-slide .margin-wrapper { margin-right: 20px; margin-bottom: 20px; }

During the event the speakers described to the audience how OSS is already part of established business practices at large companies in the industrial domain; how digital economies are being shaped thanks also to OSS; which regulatory and legal aspects we need to take into account in terms of safety standards, licensing and compliance processes.

![IMG_9923.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1464193899571-7CN19OZPCYOW7V9Q3V5W/IMG_9923.JPG)

![IMG_9989.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1464193931151-VGIET45H178JR3RQ6D48/IMG_9989.JPG)

![IMG_9993.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1464193960476-5IMXFH4VHKGZICN97SJE/IMG_9993.JPG)

![IMG_9999.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1464193988074-73UULPTYOVJIYKXHXIOP/IMG_9999.JPG)

#block-yui\_3\_17\_2\_1\_1464193149000\_59943 .sqs-gallery-block-grid .sqs-gallery-design-grid { margin-right: -20px; }
#block-yui\_3\_17\_2\_1\_1464193149000\_59943 .sqs-gallery-block-grid .sqs-gallery-design-grid-slide .margin-wrapper { margin-right: 20px; margin-bottom: 20px; }

Takeaway messages that we want to highlight as they are instrumental in removing unfounded but long-standing critiques of OSS for industrial robots and machinery are:

* the kind of functionalities that ROS is typically used for, and which sit at the OS/middleware and the application software levels, can be carried out by non-certified software as they live in a "sandbox" protected by the underlying safety-compliant foundation and which includes the electrical/mechanical and safety device/PLC level layers. As I like to say, we do not necessarily aim to replace the software in your robot's control box with ROS (although the software to do that [is available](http://wiki.ros.org/ros_control)), but rather to provide higher-level functionalities like perception-driven, online trajectory generation to let the robot operate in dynamic environments, thing not possible (or very difficult to perform) with the limited sets of preprogrammed motions typical of current automation
* OSS has a long history of adoption in industrial automation; Linux (especially Linux RT) is a good example of this, and shows that using OSS in commercial products is not only possible, but also beneficial
* having a compliance process in place (e.g. [OpenChain](http://www.linuxfoundation.org/collaborate/workgroups/openchain)) can ensure that licensing matters are properly dealt with

Given the interest and the feedback collected after the event, we plan on following-up on these topics at the [ROS-Industrial Conference](http://rosindustrial.org/events/2016/11/3/2016-ros-industrial-conference) next fall, whose program will be made available in the coming weeks.


