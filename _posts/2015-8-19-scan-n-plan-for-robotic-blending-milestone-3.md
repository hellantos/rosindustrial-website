---
author: Jonathan Meyer (SwRI)
comments: false
date: '2015-09-01 01:32:16+00:00'
slug: 2015-8-19-scan-n-plan-for-robotic-blending-milestone-3
title: Scan-N-Plan for Robotic Blending Milestone 3
media_type: None
description: A team of developers from Southwest Research Institute, The Boeing Company,
  Caterpillar, Wolf Robotics, and TU Delft have recently completed the ...
layout: post
old_sp_link: https://rosindustrial.org/news/2015/8/19/scan-n-plan-for-robotic-blending-milestone-3
---

A team of developers from Southwest Research Institute, The Boeing Company, Caterpillar, Wolf Robotics, and TU Delft have recently completed the third milestone of the Scan-N-Plan for Robotic Blending Focused Technical Project. Sponsors for this milestone include The Boeing Company and Caterpillar, Inc. 

[Scan-N-Plan](http://rosindustrial.org/scan-n-plan/) technologies are a suite of open-source software tools that enables automated process-planning and execution based on 3-D scan data. The Robotic Blending project is focused on bringing these Scan-N-Plan capabilities to the world of surface finishing.

In many factories today, a part fresh from a CNC machine will require a manual post-processing step to ensure that the surface is sufficiently smooth to eliminate fatigue crack growth factors and/or to prepare the surface for painting. The physical labor of smoothing the surface is frequently accomplished using hand-held power tools and these actions, over time, can cause repetitive stress injuries. Robotic automation is a desirable alternative, but programming for each unique part's geometry and surface defects is not cost effective.

The goal of the Robotic Blending project is to allow an operator to place a part requiring surface processing into a robot work cell and have the robot automatically generate a plan and execute it. Using a simple 4-button software interface, the operator follows a step-by-step procedure to scan, preview, blend, and inspect a part in only a few minutes (see the video). The operator's only input to the system is to instruct the robot where to look for parts, what surfaces should be processed, and to give approval to the generated process plans. An administrator menu is also provided to adjust process parameters (e.g. feeds, speeds, tool geometry, QA tolerances, etc.).

The current system can process flat surfaces at arbitrary, but reachable, position and orientation. Process path generation and robot trajectory planning is very fast: roughly one second per surface. Milestone 3 saw the inclusion of a vastly improved user interface (including the operator interface mentioned previously), an improved laser scanner driver, adjustable process parameters, new support for ABB robots, and robot simulations/previews. In addition, demonstrations of the Milestone 3 software were independently and successfully performed at Boeing and Caterpillar facilities (on different robots) the week of July 27, 2015.

The next milestone will expand the capabilities of the system to deal with more complex/non-flat parts, to perfect the blending process, and to "close the loop" between the QA scoring and process planning by reworking the part until it objectively meets a given quality metric.

Special thanks to the following software developers who contributed to this milestone:

* Adam Clark - Boeing
* Chris Sketch - Caterpillar
* Gijs van der Hoorn - TU Delft
* Jonathan Meyer - SwRI
* Matthew West - Caterpillar
* Zach Bennett - Wolf Robotics

