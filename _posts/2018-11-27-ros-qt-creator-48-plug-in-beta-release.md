---
author: Levi Armstrong (SwRI)
comments: false
date: '2018-12-07 01:50:07+00:00'
slug: 2018-11-27-ros-qt-creator-48-plug-in-beta-release
title: New Release of ROS Qt Creator 4.8 RC on Xenial and Bionic
media_type: None
description: We are pleased to announce the release of the ROS Qt Creator Plug-in
  for Qt Creator 4.8 RC on Xenial and Bionic. The ROS Qt Creator Plug-in ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/11/27/ros-qt-creator-48-plug-in-beta-release
tags: ros qt-creator ide ros-industrial
---

We are pleased to announce the release of the ROS Qt Creator Plug-in for Qt Creator 4.8 RC on Xenial and Bionic. The ROS Qt Creator Plug-in creates a centralized location for ROS tools to increase efficiency and simplify tasks.

![Picture obtained from Qt Blog](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1543328504297-P6QMLHZXITJ8OCV3HP5T/languageclient_py_hs.png)

Figure: *Picture obtained from [Qt Blog](http://blog.qt.io/blog/2018/10/11/qt-creator-4-8-beta-released/)*

Highlights:

* [Qt Creator 4.8](http://blog.qt.io/blog/2018/10/11/qt-creator-4-8-beta-released/) introduces several new rich features and improvements to existing capabilities.
	+ Generic Programming Language Support **(Python Support!)**
		- To use this feature, you must enable the Language Support Plugin
	+ C++
		- Compilation Database Projects!
		- Clang Format Based Indentation!
		- Cppcheck Diagnostics!
		- Simultaneously debugging one or more executables!
* [ROS Plug-in](https://ros-qtc-plugin.readthedocs.io/en/latest/) introducint a few new features and bug fixes
	+ Upgraded to Qt Creator 4.8
	+ Added catkin\_test\_results run step
	+ Added ROS Settings Page to configure default settings
	+ Bug Fixes
		- Issue [#284](https://github.com/ros-industrial/ros_qtc_plugin/issues/284) Package Wizard caused Qt Creator to crash if using when a ROS project is not loaded.
		- Issue [#289](https://github.com/ros-industrial/ros_qtc_plugin/issues/289) Clicking Help caused Qt Creator to crash

![qt-creator-ros-settings-page.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1543345585182-X8X308ITTUGAQNQTX0GA/qt-creator-ros-settings-page.png)


