---
author: Matt Robinson (SwRI)
comments: false
date: '2020-11-05 17:15:35+00:00'
slug: 2020-11-5-hbxkihnrz8hjiwidgr16m9hrd4faa7
title: Collaborative Robot Sanding with ROS2 for Aerospace Applications
media_type: None
description: Starting in mid-2019, a project led by Spirit AeroSystems and funded
  by the [ARM Institute](https://arminstitute.org/) kicked-off around an idea ...
layout: post
old_sp_link: https://rosindustrial.org/news/2020/11/5/hbxkihnrz8hjiwidgr16m9hrd4faa7
---

Starting in mid-2019, a project led by Spirit AeroSystems and funded by the [ARM Institute](https://arminstitute.org/) kicked-off around an idea to develop a complete Collaborative Robotic Sanding application. The goal was to have the robot do the 80% of the repetitive sanding tasks, while the process experts performed the detailed work and oversaw the robot's work and could identify areas that needed additional processing. The objective was to find an effective balance between the benefits of automation and highly skilled manufacturing personnel.

This effort involved multiple organizations in which the [Southwest Research Institute (SwRI) team](https://www.swri.org/industries/industrial-robotics-automation), led by Jorge Nicho, sought to leverage a number of the emerging developments around ROS2, and create a complete and functional application in ROS2 that could be a stake in the ground for how to build industrial applications in ROS2. It had been noted at a prior ARM Institute meeting that the stakeholders were interested in the development and maturation of ROS2, so this project became a great opportunity to step forward and build an application in ROS2.

In parallel with this project, from the SwRI/ROS-I Americas perspective, was also the providing of a ROS-Industrial training, and assisting the Wichita State University partner, in identifying suitable curriculum elements around ROS to be incorporated into their academic programs. A key outcome would be the pilot of a ROS-based introduction to advanced robotics systems to be provided as part of the technical program at Wichita State. Such a program would assist in the realization of technician skills relative to working with ROS-based systems.

New Capabilties Developed within the Program
--------------------------------------------

As far as the application development, two new features needed to be developed. The first was the ability for the robot to apply a [constant force and tool speed during the execution of the sanding process trajectories](https://youtu.be/AP72OJT5doE). The selected robot, Universal Robots UR10e, has force-feedback feature, but simultaneous control of constant force while executing a trajectory at a constant velocity was not readily available out of the box. A recent [blog post](https://www.swri.org/industry/industrial-robotics-automation/blog/collaborative-robot-force-control-through-process) over at the SwRI Innovations in Automation blog details that specific development.

Second, in order to enable human to robot collaboration, it was desired that the operators could mark directly on the part in order to indicate an area that needed additional processing. Then the system would recognize the marks and only process within the marked regions. There will be more details on those two new developments forthcoming.

![figure 1. Gazebo View of the collaborative Robotic Sanding application](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1604595217921-5MGJ4UKYGXQD7DSNL0CF/Gazebo.png)

*figure 1. Gazebo View of the collaborative Robotic Sanding application*

![](media/e25f8e68e2928e10950597a8a555ee02.png)

The ROS2 application leveraged Gazebo, Figure 1, to allow for richer emulation of the depth sensors and robot trajectory execution. This aided with development and verification of the localization technique, as the parts could be easily located within the working envelope of the simulated system. The [ros\_scxml](https://github.com/swri-robotics/ros_scxml) package was utilized for creation of the application state machine, Figure 2, simplifying the state machine creation process, and allowing for more efficient updating as the application matured.

![](media/b7a757ebc8dda8a867d9fb2af6cd9921.png)

![Figure 2. SCXML node diagram](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1604595299689-JYPIE9XH5E61M5OAS8VR/SCMros.png)

*Figure 2. SCXML node diagram*

Some other additional features, such as the ability to understand reachability in the context of the part were included and the output can be seen in the below figure.

![FIgure 3. Reachability assessment within the application gui](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1604595394956-OP58RLOAJ3R7S0X61BZZ/reachability.png)

Figure: *FIgure 3. Reachability assessment within the application gui*

![](media/3f5e441b505f05444a199c0f2b03b177.png)

The development resulted in an application, complete with Graphical User Interface, Figure 4, integrated at WSU (Wichita State University) and in collaboration with Spirit AeroSystems. Post integration, the system was tested against the requirements for successful sanding of the part in [TRL 6](https://www.nasa.gov/directorates/heo/scan/engineering/technology/txt_accordion1.html) testing trials. Initially there were some performance limitations. First, when using the manipulator for application of force it was found that performance of the force application degraded as the manipulator extended into a near-singularity configuration. This has an impact on what regions may be effectively processed, as for optimal force application and execution there is a relationship between the efficiency of the force response and the configuration of the arm, i.e. the arm being fully extended outward from the base attempting to process a distant surface area.

![Figure 4. APplication GUI](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1606334639588-IIMFQEPEPJC1AEVHP3M9/Screenshot%2Bfrom%2B2020-11-25%2B13-00-52.jpg)

*Figure 4. APplication GUI*

Bridging ROS2 with ROS1-Based Manipulator
-----------------------------------------

Additionally, the manipulator currently only has a ROS1 interface. Since the application was built in ROS2 then the team had to leverage the ROS-to-ROS2 bridge. While this works to drive basic functionality, there were issues with the reliability of the communication between the application and the manipulator. This has been [established as an area for continuous improvement](https://github.com/UniversalRobots/Universal_Robots_ROS_Driver/issues/69) and an effort to support the development of a ROS2 interface for Universal Robots is underway, with support from PickNik, Spirit AeroSystems, TU Delft, FZI Research, SwRI, and of course Universal Robots.

Overall, this was a successful program, and the key metrics for the top-level program were realized once it was understood how to best leverage the solution as developed. A final demonstration video, included below, was produced by the Spirit AeroSystems team. We believe the software-side of the application will be a complete example of a ROS2-based industrial application and we hope that the community will find it of interest. The application repository may be currently found at: <https://github.com/swri-robotics/collaborative-robotic-sanding>

Thanks to our partners at Spirit AeroSystems and Wichita State University for their collaboration, feedback, and partnership on this project. Thanks to the ARM Institute as well for their support. 


