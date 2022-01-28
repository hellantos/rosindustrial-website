---
author: Guest User
comments: false
date: '2017-03-14 21:26:01+00:00'
slug: 2017-3-14-road-map-for-ros-industrial
title: Road Map for ROS-Industrial
media_type: None
description: One of the purposes of the ROS-Industrial Consortium is to generate and
  maintain the technical road map for ROS-Industrial. This effort started in ...
layout: post
old_sp_link: https://rosindustrial.org/news/2017/3/14/road-map-for-ros-industrial
---

One of the purposes of the ROS-Industrial Consortium is to generate and maintain the technical road map for ROS-Industrial. This effort started in earnest in 2014 using a process that roughly follows the [Sandia National Lab Fundamentals of Roadmapping technique](https://github.com/ros-industrial-consortium/roadmapping/blob/master/SandiaFundamentalsOfRoadmapping.pdf). In summary, the steps include:

1. Define the scope and participants
2. Create a common vision for the product/technology
3. Identify stakeholder requirements
4. Define technology areas
5. Identify alternatives and gaps
6. Recommend path(s) forward
7. Evaluate roadmap
8. Develop implementation plans

The participants in the roadmapping were [members of the ROS-Industrial Consortium](http://rosindustrial.org/ric/current-members/) who are typically involved in manufacturing on a daily basis. The Vision for ROS-Industrial (step 2) is to provide an open and flexible framework for manufacturing automation development that:

* Supports advanced robotics capabilities for manufacturing
* Standardizes interfaces for cross-platform compatibility
* Modularizes and scales components to larger systems
* Enables a collaborative development environment
* Develops the workforce through training curriculum and hands-on classes
* Transfers technology and reduces implementation costs via open source license
* Advances manufacturing productivity
* Improves worker well being

To identify stakeholder requirements for the technology (step 3), we began by collecting example high-priority present and future robotic automation [use cases](https://github.com/ros-industrial-consortium/roadmapping/blob/master/UseCases.md) that needed advanced software to enable them. From there we worked backwards, reverse engineering each application to enumerate the technical building blocks that would be needed to assemble a solution (refer to the Mobile Material Handling example below).

![Example decomposition of building blocks for the mobile material handling application.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1489499368337-7QTC1D37AGGRZAAXHKDK/Mobile_Material_Handling)

Figure: *Example decomposition of building blocks for the mobile material handling application.*

 We then looked for commonality among those building blocks as a means to define technology areas (step 4) and to prioritize them (below).

![Technology areas identified&nbsp;](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1489517630724-WR7UBPZRY8PTJWC7J0RQ/image-asset.jpeg)

Figure: *Technology areas identified*

The resultant [roadmap document](https://github.com/ros-industrial-consortium/roadmapping/blob/master/RoadmappingDocument.md) identifies alternatives and gaps for each technology area and makes recommendations (steps 5-6). To visualize the roadmap, we presented the data as a traditional timeline (refer to picture below). And while we've made progress in most of the anticipated areas, it is not possible to guarantee specific progress without a similarly guaranteed budget.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1489517784471-TM3F23TXLN3RC3PCL61A/image-asset.jpeg)

In 2016, after receiving additional input from our international collaborators and new members, we sought to refresh this roadmap, and generated the attached infographic to blend the technology areas with the arrow of time in a single graphic (below). Technical thrusts are arranged vertically in order of priority (foundational capabilities starting at the bottom, and ascending toward higher-complexity and/or dependent goals near the top). We also added the orthogonal axis with software quality and reliability characteristics to indicate cross-cutting goals for all capabilities. In early 2017, this vision for ROS-I infographic was ratified by a vote of our Consortium Advisory Committee.

[![ROS Timeline-infographic2016TABLOID_v2.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1489524102196-LYKKS9UYMG0N00L9E1ZT/ROS+Timeline-infographic2016TABLOID_v2.png)](/s/ROS-Timeline-infographic2016TABLOID_v2.png)


