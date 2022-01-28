---
author: Guest User
comments: false
date: '2016-10-21 23:16:14+00:00'
slug: 2016-10-18-google-summer-of-code-project-workspace-analysis-and-base-placement
title: Google Summer of Code Project – Workspace Analysis and Base Placement
media_type: None
description: 'Submitted by: Abhijit Makhal, Idaho State University'
layout: post
old_sp_link: https://rosindustrial.org/news/2016/10/18/google-summer-of-code-project-workspace-analysis-and-base-placement
---

Submitted by: Abhijit Makhal, Idaho State University

For the Google Summer of Code Project (GSoC) 2016, with coordination with Open Source Robotics Foundation (OSRF) and ROS-I Consortium, a toolkit Reuleaux, has been developed for the purpose of workspace analysis and base placement for a specified task. The workspace analysis is highly beneficial for any robotic system as it provides information about the reachability of the manipulator. The base placement system uses the workspace analysis tool and provides optimal base position for a specified task providing predefined end-effector positions.

The first project goal was to develop a tool that can define reachability of any manipulator with existing robot definition such as URDF (Unified Robot Description Format). With an URDF of the robot and resolution based on user needs, the tool can provide multiple maps representing the information about the workspace such as a reachability map, capability map and inverse reachability map. Several new ROS messages have been generated for workspace analysis which represents the coordinates of the workspace spheres, poses in the spheres and reachability of that spheres.

Reachability Map
----------------

The reachability map describes the reachability of a given robot model by discretizing its environment, creating poses in the environment and calculating valid IK solutions for the poses. The poses which are reachable by robot are associated with discretized spheres. The reachability of each sphere in the environment are parameterized by a reachability index. The output is saved as an hdf5 file.

![Reachability map colored by reachability index (left), and solid colors (right).](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1477090477673-3LN2IRL6V3GW42H2TAOH/map+colored+by+RI+and+solid.jpg)

Figure: *Reachability map colored by reachability index (left), and solid colors (right).*

![Reachable positions for a robot (left), and 6 DOF poses superimposed on reachable positions (right).](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1477090506161-2T01IBRQSAK4CTCR9VW0/image-asset.jpeg)

Figure: *Reachable positions for a robot (left), and 6 DOF poses superimposed on reachable positions (right).*

Capability Map:
---------------

The capability map is an extension of reachability where the outer spheres of the reachability map, is set as cones. So the reachability limit of the robot is well visualized. All the outer spheres are decided for a principal axes and iterates over different values for opening angles for cones.

Inverse Reachability Map
------------------------

The purpose of the inverse reachability map is to find suitable base positions for a robot with given task poses. The inverse reachability map is a general inverse transformation of all the reachable poses of the reachability map of the robot. The inverse Reachability map is dependent on generated reachability map.
With a visualization toolbox for Reuleaux, the workspace can be visualized in RViz. The visualization tool also provides scope of representing the workspace with different structures (spheres, cones, cylinder and box), colors (based on reachability or solid colors) and reachability index (spheres with high/low reachability)

![Spheres with low Reachability (left), and high reachability (right)](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1477090954146-76P9WV7TBX4TFDZX2HZ5/spheres+with+high+and+low+RI.jpg)

Figure: *Spheres with low Reachability (left), and high reachability (right)*

![Dense cross-section of the workspace (left), and sparse Cross-Section &nbsp;(right)](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1477090969000-IPX12YQCBYLNUB1HA44A/image-asset.jpeg)

Figure: *Dense cross-section of the workspace (left), and sparse Cross-Section (right)*

The second goal of the project was to develop a user interface by which the user can provide task poses needed for a specified task and the system will try to find optimal base position/ positions for that task from where the robot can reach all the positions. The system tries to create a combined inverse reachability map of all the task poses and finds optimal base location by one of the following methods. 

1. Principal Component Analysis (PCA)
2. Grasp reachability score
3. Ik solution score

![Magenta arrows represent the task positions and green arrows are possible base placement positions (left, center). Combined inverse reachability map for three task poses (right).](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1477091274438-XZ4DZE2EQAPX4E2PJC8U/base+placement+interface.jpg)

Figure: *Magenta arrows represent the task positions and green arrows are possible base placement positions (left, center). Combined inverse reachability map for three task poses (right).*

At this time, the Reuleaux toolkit is far away from completion. There are various scopes of improvement for the tool in terms of visualization, algorithm and computation. I would like to encourage the Robotics Community to contribute to this project by providing suggestions and improvements. Detailed information and instructions for running the tool can be found at: <http://wiki.ros.org/reuleaux>

Please let me know if there is any issue in running the codes or if you have any suggestions: [makhabhi@isu.edu](mailto:makhabhi@isu.edu)

I would like to share my gratitude for the ROS-I community members and my mentor Alex K. Goins and Shaun Edwards, who shared their valuable suggestions during the project development and guided me in the right direction. I hope that this project can be very useful for robotics community.

Some useful links for Reuleaux:
-------------------------------

* Documentation about map creation can be found at: <https://github.com/ros-industrial-consortium/reuleaux/tree/master/map_creator>
* Documentation about workspace visualization can be found at: <https://github.com/ros-industrial-consortium/reuleaux/tree/master/workspace_visualization>
* Documentation about the base placement planner can be found at: <https://github.com/ros-industrial-consortium/reuleaux/tree/master/base_placement_plugin>

