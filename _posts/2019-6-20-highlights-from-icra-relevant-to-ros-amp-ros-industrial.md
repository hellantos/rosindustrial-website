---
author: Josh Langs (SwRI)
comments: false
date: '2019-06-20 22:43:01+00:00'
slug: 2019-6-20-highlights-from-icra-relevant-to-ros-amp-ros-industrial
title: Highlights from ICRA relevant to ROS &amp; ROS-Industrial
media_type: None
description: The International Conference on Robotics and Automation, commonly known
  as ICRA, is one of the premier global events for showcasing the latest and ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/6/20/highlights-from-icra-relevant-to-ros-amp-ros-industrial
tags: icra ros-i ros
---



![icra-2019.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1561069942493-95P6EBJDZ486RMDGLCX8/icra-2019.png)

The International Conference on Robotics and Automation, commonly known as ICRA, is one of the premier global events for showcasing the latest and greatest results in robotics research. This year ICRA was held in Montreal, Canada, back in North America for the first time since Seattle in 2015.

ICRA is largely a forum for academic research labs to showcase their most recent results, which aim to be exploratory and forward-looking rather than off-the-shelf solutions ready for immediate adoption into industry. Nevertheless, there was still quite a bit of noteworthy technology and results on display. It was very impressive to see the huge variety of areas that researchers are exploring within robotics and the large amount of creativity on display in new approaches and algorithms.

The scale of ICRA was enormous this year, with over 1,200 papers presented over the course of the three-day conference. Along with the plenary sessions, keynote talks, and industry exhibitions, there was far too much to see and do. With such a high volume of content, a classic conference format of multiple tracks where each author presents to a sitting audience was simply not possible. Instead, the organizers opted for an interesting alternative of interactive presentations where the authors stood by a poster describing their work and conference attendees were free to spend as much time as they wanted discussing the work with the author. The new twist that I hadn't seen before was that all presentations took place in the same large exhibition hall simultaneously, in sessions that each contained about 130-150 posters. The posters were spread throughout the hall on the outside of free-standing structures that had partitioned spaces for each poster, which were called the PODS. The PODS all being colocated in a single room created a very casual atmosphere with a lot of exploration and discussion with the paper authors.

![USC.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1561070093173-115K0PATFFDA0FZM2WN1/USC.JPG)

Photo courtesy of Rishi Malhan, University of Southern California

To conclude, I wanted to highlight a few contributions that are interesting for the use of ROS or for connections to ROS-Industrial. Definitely keep an eye out for these papers to appear on IEEE Xplore soon and take a look!

Reinforcement Learning on Variable Impedance Controller for High-Precision Robotic Assembly

Jianlan Luo, Eugen Solowjow, Chengtao Wen, Juan Aparicio Ojea, Alice Agogino, Aviv Tamar, Pieter Abbeel

Here the authors address the problem of autonomous and intelligent robotic assembly, and had presented this work at the most recent ROS-Industrial annual meeting. They use a Rethink Robotics Sawyer robot (which is controlled through ROS) to perform precision assembly of a set of gears using reinforcement learning and neural networks. The core idea is that successful completion of assembly tasks requires knowledge about the types of contacts and constraints involved, such as aligning a peg with the axis of a hole before it can be inserted. Rather than having the system designer spend time and effort providing manual descriptions of these constraints, their method allows them to be learned directly from the robot's experience. As can be seen in the video below, the robot is able to quickly learn how to deal with a number of different contacts when performing multiple different assembly tasks. This is a great demonstration of bringing machine learning into robot behaviors for industrial tasks and it will be fascinating to see how this area develops in the near future.

[Assembly Video](https://youtu.be/kqA1tlPaT8E)

CartesI/O: A ROS Based Real-Time Capable Cartesian Control Framework

Arturo Laurenzi, Enrico Mingo, Luca Muratore, Nikos Tsagarakis

In work that follows their participation in the DARPA Robotics Challenge, the authors introduce a framework for performing real-time Cartesian control of platforms with many degrees-of-freedom within a ROS system. The framework is designed to support having the controller solver run inside the real-time control loop so that the robot can react immediately to any change in the desired input. Each Cartesian controller is specific to a particular platform and particular task, but the authors provide interface layers to abstract away much of common logic that would have to be repeatedly implemented in different implementations. By supporting the ROS URDF format, constraints or desired behaviors can be specified for links. Furthermore, each task will have an auto-generated ROS API available that enables very high level input about the task goals and provides information about the current task status. This allows a user to perform basic scripting of robot behaviors using something a simple as a short Python script, for example. This framework can be seen driving the 28 DoF COMAN+ humanoid and the 39 DoF CENTAURO quadruped robots in the video below.

[CartesI/O Video](https://www.youtube.com/watch?v=eVmDBVL83WY)

MoveIt! Task Constructor for Task-Level Motion Planning

Michael Görner, Robert Haschke, Helge Joachim Ritter, Jianwei Zhang

Here the authors provide a software tool and framework for extending MoveIt to more naturally handle planning of entire robot tasks. For nontrivial tasks, the overall robot motion is typically broken into multiple distinct pieces, each of which has its own set of planning challenges. For example, when performing a pick-and-place task, the robot has to separately create plans for approaching the object, grasping it, moving the object to the place area, and releasing it at the place point. The authors formalize a framework for each of these stages and how each one may depend on others. For example, the grasp selection will affect where the manipulator should move to at both the pick and place positions. The framework is arbitrarily scalable and allows system designers to create descriptions of entire tasks that MoveIt can solve with relative ease. The authors have open-sourced the software on GitHub (<https://github.com/ros-planning/moveit_task_constructor>) and are hopeful the framework will go on to become a central tool for task planning using MoveIt.

![Moveit.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1561070147669-A12OA152NXDIOF8ZRVFB/Moveit.JPG)

Planning a pouring task with displays for how the robot picks up the bottle (center), creates the pouring motion (left), and places it back on the table (right)


