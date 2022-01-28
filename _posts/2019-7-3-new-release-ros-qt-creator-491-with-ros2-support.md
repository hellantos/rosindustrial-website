---
author: Matt Robinson (SwRI)
comments: false
date: '2019-07-03 14:02:16+00:00'
slug: 2019-7-3-new-release-ros-qt-creator-491-with-ros2-support
title: New Release - ROS Qt Creator 4.9.1 with ROS2 Support!
media_type: None
description: We are pleased to announce the release of the ROS Qt Creator Plug-in
  for Qt Creator 4.9 on Xenial and Bionic. The ROS Qt Creator Plug-in creates a ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/7/3/new-release-ros-qt-creator-491-with-ros2-support
---

We are pleased to announce the release of the ROS Qt Creator Plug-in for Qt Creator 4.9 on Xenial and Bionic. The ROS Qt Creator Plug-in creates a centralized location for ROS tools to increase efficiency and simplify tasks.

![Perf Flame Graph (Tutorial)](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1562160273321-MLK3RYPHBDDM45W4ZDDY/flame_graph.png)

Figure: *Perf Flame Graph [(Tutorial)](https://ros-qtc-plugin.readthedocs.io/en/latest/_source/Performance-Analysis.html)*

Highlights:

* [Qt Creator 4.9](https://blog.qt.io/blog/2019/04/15/qt-creator-4-9-0-released/) introduces several new features and improvements to existing capabilities.
	+ Generic Programming Language Support **(Python Support!)**
		- This was experimental in 4.8 but is now fully supported.
	+ Perf Profiling
		- This a powerful tool for profiling software running on linux.

* [ROS Plug-in](https://ros-qtc-plugin.readthedocs.io/en/latest/) introduces a few new features and bug fixes
	+ Upgraded to Qt Creator 4.9
	+ Added **ROS2 Colcon Support!**
	+ Added support for custom installations for ROS. These setting can be configured in the setting page.
	+ Ability to modify the build environment under build settings
		- Qt Creator does not load environment variables from the .bashrc so they need to be added to the build environment manually.
	+ Updated Documentation
		- [FAQ - How to set C++ code style to match ROS Style](https://ros-qtc-plugin.readthedocs.io/en/latest/_source/FAQ.html#how-do-i-set-the-c-code-style-to-match-the-ros-style)
	+ New tutorials
		- [Perf Performance Analysis](https://ros-qtc-plugin.readthedocs.io/en/latest/_source/Performance-Analysis.html)
		- [Running test from Qt Creator](https://ros-qtc-plugin.readthedocs.io/en/latest/_source/Performance-Analysis.html#bonus-running-tests-from-qtcreator)

![ROS settings - Add custom ROS install location](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1562160658623-ZVAAE89AGDC4YFNYBAIE/ros_qtc_settings.png)

Figure: *ROS settings - Add custom ROS install location*


