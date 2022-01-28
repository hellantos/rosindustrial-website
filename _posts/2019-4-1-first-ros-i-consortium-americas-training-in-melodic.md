---
author: Matt Robinson (SwRI)
comments: false
date: '2019-04-01 19:54:47+00:00'
slug: 2019-4-1-first-ros-i-consortium-americas-training-in-melodic
title: First ROS-I Consortium Americas Training on Melodic
media_type: None
description: During the first week in March a ROS-I training event was held at the
  Southwest Research Institute campus in San Antonio, Texas. As per recent ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/4/1/first-ros-i-consortium-americas-training-in-melodic
---

During the first week in March a ROS-I training event was held at the Southwest Research Institute campus in San Antonio, Texas. As per recent tradition, both a Basic and an Advanced track were offered. However, the Advanced track did not have any registrants, so only the Basic was held. This however, was still a milestone of note as it was the first training class in ROS Melodic. 

![Students working through Exercise 3.0 - Intro to URDF](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1554147757039-G2J5JOJR0E2YMUK5DN24/20190306_090105.jpg)

Figure: *Students working through Exercise 3.0 - Intro to URDF*

Students were guided through a number of exercises, such as; "how to create a simple urdf" and "transforms using TF". A significant amount of work went into getting the materials for the training, including all the exercises to work properly in Melodic. 
Day 2 focused on motion planning introduction and exercises that introduced the cartesian planner Descartes, and a high-level introduction into Perception. The final day of the training was a lab day, where various exercises were completed, and students could test their application on the available hardware. Feedack to date was that the training functioned well, and issues were limited.

![trjopt training.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1554147816721-SOYXUWSMF5WD432XP1T2/trjopt+training.JPG)

In addition to the training being on ROS Melodic, a new training module was created, and though it was part of the "Advanced" topic, that was not held, I wanted to take a moment to introduce and drive awareness for a new functional demonstration.

This demonstration titled "[Optimization Based Path Planning](https://industrial-training-master.readthedocs.io/en/latest/_source/demo3/Introduction.html)", seeks to provide users with a full working example that enables those interested in optimization of motion plans, to leverage the tools within the newly released package TrajOpt. The exercise steps through several steps leveraging template code, understand the procedure for building a problem and adding costs, solving for a trajectory, and then move to a real sensor and an actual robot leading to successful demonstration execution on hardware.

This exercise, with full demonstration environment, is open source and included over at the ROS-Industrial training website. We look forward to conducting this Advanced topic in future ROS-I Consortium Training offerings and hope in the interim that this demonstration becomes a useful tool to those interested in exploring optimization based path planning.

Please keep an eye for additional improvements to the training materials and demonstrations, including new exercises and demonstrations around topics such as a ROS-I introduction to ROS2, where relevant considerations will be included to enable interaction with path planners, and realizing robot motion.

As always if you have questions about ROS-I Consortium training and are curious about upcoming events, nad their locations, please do not hesitate to contact us, or start a conversation over at <https://discourse.ros.org/c/ros-industrial>.


