---
author: Guest User
comments: false
date: '2015-07-09 10:55:45+00:00'
slug: 2015-5-22-cooperative-research-with-nist
title: NIST/SwRI Collaborate on Open Source Software for Robotic Assembly
media_type: None
description: Over the past 6 months, the SwRI ROS-Industrial team has been executing
  a Cooperative Research program with the National Institute of Standards ...
layout: post
old_sp_link: https://rosindustrial.org/news/2015/5/22/cooperative-research-with-nist
tags: ros-i ros-industrial nist
---

Over the past 6 months, the SwRI ROS-Industrial team has been executing a Cooperative Research program with the National Institute of Standards and Technology ([NIST](http://www.nist.gov/)). From a [manufacturing perspective](http://www.nist.gov/manufacturing-portal.cfm), NIST's impact is quite diverse. It includes aspects from general [process improvement](http://www.nist.gov/process-improvement-portal.cfm) to specific manufacturing processes like [nano-manufacturing](http://www.nist.gov/nanomanufacturing-portal.cfm), and of course [robotics](http://www.nist.gov/robotics-portal.cfm).

A core theme of the NIST-supported ROS-Industrial program is agility. That is the ability of manufacturing systems to perform a diverse set of tasks, with the built in intelligence to re-task on the fly. Agility is the perhaps the greatest unrealized promise of robotics. With the support of NIST, it is this valuable and critical aspect of robotics that ROS-Industrial aims to enable. The research effort is broken down into several sub-tasks, outline below. The tasks vary, some with immediate impact and others with more long term goals. However, they all have the common theme of enabling robotic agility.

Robot Testing and Evaluation
----------------------------

Testing and evaluation (T&E) are very important for both measuring and comparing the performance of complex systems. Prior collaborative work was focused on test methods for Response Robots (think robots climbing around piles of rubble). Through these efforts a [standard test-suite for response robots](http://www.nist.gov/el/isd/ms/upload/DHS_NIST_ASTM_Robot_Test_Methods-2.pdf) was developed. This test-suite demonstrably pushed the state of the art in response robots. With the goal in mind of measuring and pushing the state of the art in robotic agility, SwRI is developing test methods for evaluating robots for complex tasks, such as assembly. 

![Peg-in-hole assembly test fixture is used to evaluate the ability of a complete robot system to perform this operations. &nbsp;Metrics including, success rates, and speed of insertion are capture in order to perform meaningful comparisons between sy…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1436393956950-PNETPW50DCO8VCQ2JPP8/image-asset.jpeg)

Figure: *Peg-in-hole assembly test fixture is used to evaluate the ability of a complete robot system to perform this operations. Metrics including, success rates, and speed of insertion are capture in order to perform meaningful comparisons between systems.*

Dual Arm Manipulator Development
--------------------------------

Dual arm manipulation is an exciting area of research. Such systems mimic human operations, giving robotic systems the ability to both hold an object with one arm and perform an operation with the other. With NIST support, SwRI researchers have developed ROS-Industrial Hilgendorf support software for the robot configuration shown below. The support software was [open sourced](https://github.com/ros-industrial-consortium/hilgendorf) to jump start dual arm manipulation research on similar setups. The Hilgendorf system configuration can be easily assembled from off the shelf components. ROS-I researchers will utilize Hilgendorf for developing dual arm applications.

![A dual arm manipulator built from two UR5s&nbsp;and two Robotiq grippers was built.&nbsp; The system allows researchers to experiment with various assembly T&amp;E tasks.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1436394099946-L09AUXI6H5JKVWD5EBAW/image-asset.jpeg)

Figure: *A dual arm manipulator built from two [UR5s](http://www.universal-robots.com/en/products/)and two [Robotiq grippers](http://robotiq.com/products/industrial-robot-gripper/) was built. The system allows researchers to experiment with various assembly T&E tasks.*

Calibration Library Improvements
--------------------------------

The [ROS-Industrial Calibration Library](https://www.youtube.com/watch?feature=player_embedded&v=MRvExKMOH1g) is a powerful tool for calibrating frame transformations between multiple robots and sensors. Improvements have been made to this library to make the data collection and calibration steps more streamlined. An additional goal of this effort was to evaluate the accuracy of a system calibrated with our library. System evaluation is a key part of the NIST mission. An example system with a network consisting of 6 cameras was calibrated with the ROS-Industrial Calibration Library using a target held by a UR10 robot. The system demonstrated pose variance for each camera better than 1/4 mm and 1/10th degree.

![The observations and camera pose geometry were&nbsp;used to predict the localization accuracy of the camera network.&nbsp;](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1436393623773-X9DOC9L0KVZQHUTLJSVF/image-asset.png)

Figure: *The observations and camera pose geometry wereused to predict the localization accuracy of the camera network.*

![The accuracy map is a slice of the working volume 0.4 meters above the table.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1436393652579-VU09MZJ5E0E4PI2EOSKI/image-asset.jpeg)

Figure: *The accuracy map is a slice of the working volume 0.4 meters above the table.*

Ontologies for Agile Planning in Manufacturing
----------------------------------------------

Past (and present) robotic automation is primarily used in high volume/low variation production applications, with the acceptations being driven by safety and environmental conditions. The obstacle that steers automation away from low volume/high variation production applications is the effort associated with teaching each part. The interest is to develop an ontology structure to represent the assembly process in a way that automated planning and assembly tasks can be executed. Current literature approaches the problem in a similar way to how a child learns to perform new task. There is a low level skill set (refer to the figure below) that needs to be taught, that then can be used to complete complicated tasks. The challenge is to formulate the skill primitives in such a way that they are robot independent and have the capability to store all information necessary for the robot to execute them efficiently. In the long term, such an ontology could enable highly dynamic and generic functionality within ROS-Industrial.

![Skill primitive library](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1436395040832-M6B4QLPOSORPWYAYUKQK/image-asset.png)

Figure: *Skill primitive library*

Descartes Joint Trajectory Planner for Semi-Constrained Cartesian Paths
-----------------------------------------------------------------------

This grant also supported development of the Descartes Path Planner. Please refer to our [previous post](http://rosindustrial.org/news/2015/6/26/descartes-path-planner-alpha-release) for a description and video of Descartes.

Acknowledgements
----------------

This work was conducted under NIST contract #70NANB14H226.


