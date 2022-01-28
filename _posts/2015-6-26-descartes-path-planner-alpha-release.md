---
author: Guest User
comments: false
date: '2015-06-29 16:09:31+00:00'
slug: 2015-6-26-descartes-path-planner-alpha-release
title: Descartes Joint Trajectory Planner for Semi-Constrained Cartesian Paths
media_type: None
description: Current MoveIt!/ROS path planners are focused on collision-free pick
  and place applications. In the typical pick and place application, the ...
layout: post
old_sp_link: https://rosindustrial.org/news/2015/6/26/descartes-path-planner-alpha-release
---

Current MoveIt!/ROS path planners are focused on collision-free pick and place applications. In the typical pick and place application, the starting and goal positions and collision models are the only inputs to the planner. By contrast, many industrial applications must follow a pre-defined Cartesian path, where the path in between matters as well. Some common examples of this are blending, painting, machining, sanding, sealing, and welding. Unfortunately, solving the Cartesian path planning problem by simply applying an inverse kinematics solution results in an artificially limited solution set that doesn't take advantage of the process flexibility/tolerance allowances. In reality, Cartesian paths are typically semi-constrained. For example, in a machining application a five degree-of-freedom (DOF) path is required, where the sixth DOF, the orientation about the tool, is not defined (doesn't matter). Joint trajectory planners that fail to take advantage of these open constraints, such as inverse kinematics (IK) based planners, limit the likelihood of finding a valid solution, even though one could exist in the semi-constrained space. The [Descartes](https://github.com/ros-industrial-consortium/descartes) planner library was initiated in Summer 2014 with NIST and ROS-Industrial Consortium Americas support to address semi-constrained Cartesian industrial processes. Descartes has already been demonstrated in a [robotic routing](https://www.youtube.com/watch?v=cZxt00uoyBo) and [blending/sanding](http://youtu.be/iEXQekoQkaY) applications. Key capabilities of Descartes include, path optimization, collision avoidance, near instantaneous re-planning, and a plug-in architecture.

The Descartes library saw its first use in early 2015, and was alpha-released at the ROS-Industrial Community Meeting at ICRA 2015 on May 26, 2015. The focus of recent development has been on making the library more user friendly, better able to capture process requirements, and more computationally efficient. A recent addition with a strong impact on all of these areas is process velocity consideration. Descartes can use this extra knowledge to improve its search for the optimal process path.

At the time of the ROS-Industrial Community meeting in January, a 6DOF robot following a semi-constrained (5DOF) Cartesian path of approximately 800 points took 30 seconds to plan. Today that same path can be solved in a fraction of a second. A specific implementation for the robot blending application has seen speed increases of a factor of 1000 as compared to testing in January. Looking toward the future, Descartes will continue to see improvements to its usability and performance. Active areas of research and development include high degree of freedom ( > 7 DOF) planning for both single and dual arm configurations, and hybrid planning, where free space motions (such as those found in a pick and place application) are combined with well defined process paths. 

Descartes documentation can be found at the ROS [wiki](http://wiki.ros.org/descartes). For working examples, please refer to the Descartes [tutorials](http://wiki.ros.org/descartes/Tutorials/Getting%20Started%20with%20Descartes) and [ROS-I Training Session 4](http://wiki.ros.org/descartes).


