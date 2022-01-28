---
author: Shaun Edwards (SwRI)
comments: false
date: '2015-08-11 17:01:29+00:00'
slug: 2015-8-2-3d-automatic-path-planning-for-surface-machining
title: 3D Automatic Path Planning for Surface Machining
media_type: None
description: Most robot controllers cannot process large and complex data such as
  point clouds or meshes. Because of this limitation, it is not possible to ...
layout: post
old_sp_link: https://rosindustrial.org/news/2015/8/2/3d-automatic-path-planning-for-surface-machining
---

Most robot controllers cannot process large and complex data such as point clouds or meshes. Because of this limitation, it is not possible to automatically generate complex paths on surfaces using a robot controller. The [Institut Maupertuis](http://www.institutmaupertuis.fr/) decided to create a ROS library that automatically plans complex paths on 3D surfaces. The aim of the [Bezier project](https://github.com/ros-industrial-consortium/bezier) is to provide a simple, yet generic, library for this purpose. It heavily relies on the [Point Cloud Library (PCL)](http://pointclouds.org/) and [VTK](http://www.vtk.org/) to generate robot poses. The capability to generate variable height passes (instead of fixed height planar passes) on complex surfaces is key. At the moment the library is oriented towards milling applications. However we expect it can be utilized in other processes as well.

The planning method requires only input meshes (raw, CAD), tool parameters (height of pass, width) to generate a full 3D robot trajectory. The project was initiated in March 2015 and a first version was released publicly in July; the Institut Maupertuis demoed an automatic machining application on polystyrene using the Bezier library:

The library is in heavy development and every contribution and/or bug report is welcome. For more information about this project please visit the [Bezier repository](https://github.com/ros-industrial-consortium/bezier/blob/master/README.md#bezier).
To understand how Bezier works, please visit the [documentation](https://github.com/ros-industrial-consortium/bezier/blob/master/bezier_library/doc/README.md#how-b%C3%A9zier-works).


