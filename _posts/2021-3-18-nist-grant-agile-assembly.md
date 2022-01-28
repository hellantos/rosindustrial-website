---
author: Kevin Warburton (SwRI)
comments: false
date: '2021-03-18 17:07:40+00:00'
slug: 2021-3-18-nist-grant-agile-assembly
title: NIST Grant Awarded to SwRI for Agile Robotic Assembly
media_type: None
description: A grant from the National Institute of Standards and Technology (NIST)
  has been awarded to Southwest Research Institute (SwRI) with the goal of ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/3/18/nist-grant-agile-assembly
---

A grant from the National Institute of Standards and Technology (NIST) has been awarded to Southwest Research Institute (SwRI) with the goal of accelerating development of agile, robotic assembly processes for manufacturing. This complements internal research at Southwest Research Institute (SwRI) for developing robotic machine assembly capabilities (Figure 1).

![Figure 1: A peg-in-hole assembly task performed with a collaborative robot at SwRI. The parts used were from the Siemens Robot Learning Challenge, which involves assembly of a set of gears and shafts.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1616078711741-7CKNXZ8PWQRNULJ2U30E/Siemens+Challenge+Image.png)

*Figure 1: A peg-in-hole assembly task performed with a collaborative robot at SwRI. The parts used were from the Siemens Robot Learning Challenge, which involves assembly of a set of gears and shafts.*

The grant is inspired by the goals of NIST to promote agility within industrial robotics. Their recent efforts to promote agility, such as the [Agile Robotics for Industrial Automation Competition (ARIAC)](https://www.nist.gov/el/intelligent-systems-division-73500/agile-robotics-industrial-automation-competition), have extensively addressed challenges associated with robotic kitting. Previous ARIAC competitions have included teams competing in a simulation environment with judging metrics focused on efficiency, performance, and cost of sensors used. However, the new challenge for ARIAC 2021 will also involve assembly operations. In alignment with the competition, the goal of this new grant is to develop a software framework that will allow plug-and-play development of assembly algorithms, which will help users reach the hardware testing and implementation phase faster. The framework will consist of a software visualization to verify assembly processes and metrics to evaluate capabilities of the overall assembly solution. The Robot Operating System (ROS) will be heavily utilized with primary developments in ROS 2 to future proof the software framework.

For the eventual end users, we strive to enable manufacturers to dynamically reprogram robots with agility that meets the user's needs. This may include handling a variety of part types, adjusting to changing part size and scale, and adapting to task failures in real-time. To standardize the evaluation of assembly algorithm performance, the [NIST Assembly Task Board #1](https://www.nist.gov/el/intelligent-systems-division-73500/robotic-grasping-and-manipulation-assembly/assembly) (Figure 2) will be used to generate metrics that allow manufacturers to compare performance of different strategies. Therefore, end users can focus on improving their assembly strategy rather than building infrastructure to define robot capabilities, sensors, and evaluation methods.

![Figure 2: NIST Task Board #1 that will be used for testing and development of an robotic assembly framework.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1616079399289-Q5VZ9YV7PFNZXTLA1XYF/NIST%2BTask%2BBoard%2BImage.jpg)

*Figure 2: NIST Task Board #1 that will be used for testing and development of an robotic assembly framework.*

Collaboration with industry and research partners will be important to understand the needs of end users and desired features that would enable agile, robotic assembly implementations. Consequently, we want for the framework to be evaluated on specific tasks of interest for these partners. Soliciting industry interest and engaging in formal collaboration, such as a ROS-I Focused Technical Project, is the eventual desired outcome.


