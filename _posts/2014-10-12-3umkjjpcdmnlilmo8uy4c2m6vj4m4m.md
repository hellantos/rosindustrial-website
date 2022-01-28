---
author: Guest User
comments: false
date: '2014-10-20 18:37:29+00:00'
slug: 2014-10-12-3umkjjpcdmnlilmo8uy4c2m6vj4m4m
title: Alten Mechatronics Applies Robotic Technology in FEI Transmission Electron
  Microscopes (TEM)
media_type: None
description: Submitted bySimon Jansen, Alten Mechatronics
layout: post
old_sp_link: https://rosindustrial.org/news/2014/10/12/3umkjjpcdmnlilmo8uy4c2m6vj4m4m
---

  

Submitted bySimon Jansen, Alten Mechatronics

[FEI](http://www.fei.com)designs, produces and supports a wide variety of high performance microscope systems, which can visualize details up to the picometer scale.

In their small dual beam (SDB) systems, a moving stage platform is present. This stage platform needs to be positioned in eight degrees of freedom (DOF). Next to the stage, the microscope contains a lot more components such as an electron and ion column, multiple detectors and a gas injection system. These SDB systems are not only used as pure microscopes, but also as nano workshop systems. It is possible to use these systems to add or remove material of a sample, while the sample is being inspected.

Because these microscopy system have such a wide variety of applications, the microscopy chamber gets rather full with components and parts. Therefore positioning and moving the eight DOF stage becomes more and more challenging.

In current systems, an in-house developed solution is used to plan the motion trajectories for the stage. The most important requirement is that the stage moves collision free between two configurations. Using the current solution, each movement between stage configurations is programmed by hand. In some cases, this planning problem is just too complex and the current in-house developed solution is not able to find a solution. In other cases, the found solution takes too much time because axes can only be moved sequentially. This consumes a lot of time when moving eight axes and is therefore not feasible.

FEI is investigating alternative solutions to perform motion planning for their stage. For these alternatives it is important that the stage moves collision free within a certain time. This time should be minimized to obtain the highest possible throughput. A benefit of using motion planning is the possibility to move axes in parallel instead of sequentially.

[Alten Mechatronics](http://www.alten.nl/en/alten-mechatronics/) performed a proof of principle study in which a simulation model of the microscope was developed. By using the motion planner MoveIt! collision free paths were generated for different stage configurations. Three cases were selected and compared to the current solution. One case was meant to benchmark the new motion planner, the two other cases to show the capabilities of the motion planner in extreme situations.

Alten showed that by using MoveIt! it became possible to calculate stage trajectories up to five times faster than trajectories found by using the in-house developed solution. For the other cases, it became possible to find trajectories that were not possible when using the in-house developed solution.

By using MoveIt! it is possible to realize complex stage movements which are guaranteed to be collision free and are resulting in a much higher throughput.

For the next phase, the results of the first ROS-Industrial Focused Technical Project (<http://rosindustrial.org/ftp-status/>) will be used to improve the performance of planner. In the first phase, MoveIt sometimes generated sub-optimal paths, which had to be rejected. With the optimization of the FTP, we will be able to guarantee near optimal solutions and be able to predict a lower reliable cycle time.

Mark Geelen & Simon Jansen *Contact:* rosindustrial(at-sign)alten.nl


