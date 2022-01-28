---
author: Guest User
comments: false
date: '2016-09-12 14:44:10+00:00'
slug: 2016-9-12-3d-automatic-path-planning-for-surface-grinding
title: 3D Automatic Path Planning for Surface Grinding
media_type: None
description: Submitted by:** Victor Lamoine, Institut Maupertuis
layout: post
old_sp_link: https://rosindustrial.org/news/2016/9/12/3d-automatic-path-planning-for-surface-grinding
---

**Submitted by:** Victor Lamoine, Institut Maupertuis

The Bezier library is a ROS tool that allows users to plan complex trajectories on 3D surfaces, and while it can be used for many purposes, it was created to generate 3D grinding trajectories. To demonstrate the usefulness of this library to industrials, we applied our latest developments on a demonstrator.

The demonstrator consists of a Fanuc robot with a grinding end effector and a table on which a shackle is laid and maintained in position. The robot first takes multiple scans with a 3D sensor to determine the position and orientation of the shackle. When the scan is over, the user can choose the grinding parameters and generate the trajectory. It is possible to simulate the trajectory before running it on the robot. The user is then able to launch the trajectory on the robot. All of these steps are summarized in this video:

This demonstrator was created as part of the Bezier project at the [Institut Maupertuis](http://www.institutmaupertuis.fr/). You can find more information about the Bezier library on [the official repository](https://github.com/ros-industrial-consortium/bezier).

Note that the library is modular and can be used for other tasks such as painting, deburring, 3D printing, or any other application that requires complex 3D path planning.


