---
author: Colin Lewis (SwRI)
comments: false
date: '2021-12-17 16:27:50+00:00'
slug: 2021-12-17-process-planning-for-large-systems
title: Process Planning for Large Systems
media_type: None
description: Advances in robotic capabilities allow us to tackle bigger problems with
  autonomous systems. While extra degrees of freedom in large robots like ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/12/17/process-planning-for-large-systems
---

Advances in robotic capabilities allow us to tackle bigger problems with autonomous systems. While extra degrees of freedom in large robots like rail systems or mobile bases empower cutting edge work, they can cause challenges in process planning; the creation of the "useful" motion of a robotic system that is constrained by the application at hand. The ROS Industrial Consortium has addressed this problem by developing new process planners that can quickly plan process for robots with large degrees of freedom.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/2bd0204c-f5f2-43e3-9ffb-fdb82e2caa61/10-R6174+-+2021+Synopsis+-+Figure+1.jpeg)

Figure: *A full Dijkstra graph finds the optimal path through the graph by exploring every edge*

In the field of robotics, motion planning can be divided into two forms: freespace planning, which finds a collision free path between two points, and process planning, which governs the movement of the robot through its useful operations. When a robot has more ways of moving, the graph of positions that represents the joint positions that can reach a point in space begins to get large. So large, in fact, that it begins to resemble the discretized representations of real space used by freespace motion planning. This project exploited this similarity to speed up process planning using freespace planning algorithms.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/b9ac8b1c-606a-4d17-bc83-a199536d9cc8/ACRES.jpg)

Figure: *Example configuration that benefits from this alternate approach to solution searching*

At a high level, the new improvements in process planning allow for branching "depth first" searches, which will quickly find a solution for every position in the trajectory, instead of search "breadth first" to find the optimal configuration at each pose. This work is especially useful in situations with many valid solutions, where it is able to find a "good enough" configuration in a tiny fraction of the time used by more traditional, comprehensive searches.

This is currently implemented in the repository <https://github.com/swri-robotics/descartes_light>. We encourage interested parties to check this out, and provide feedback. We expect to migrate this to the ROS-Industrial GitHub organization int he coming months. Thanks to the community for providing feedback and use cases to support this work.


