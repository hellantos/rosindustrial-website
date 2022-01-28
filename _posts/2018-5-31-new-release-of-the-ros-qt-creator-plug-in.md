---
author: Levi Armstrong (SwRI)
comments: false
date: '2018-06-01 17:39:46+00:00'
slug: 2018-5-31-new-release-of-the-ros-qt-creator-plug-in
title: New Release of the ROS Qt Creator Plug-in
media_type: None
description: We are pleased to announce the release of the ROS Qt Creator Plug-in
  for [Qt Creator 4.5.1](http://blog.qt.io/blog/2018/02/13/qt- ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/5/31/new-release-of-the-ros-qt-creator-plug-in
---

We are pleased to announce the release of the ROS Qt Creator Plug-in for [Qt Creator 4.5.1](http://blog.qt.io/blog/2018/02/13/qt-creator-4-5-1-released/) on Trusty and Xenial. The ROS Qt Creator Plug-in creates a centralized location for ROS tools to increase efficiency and simplify tasks.

Highlights:

* The installation has changed from using a debian installation method to using the Qt Installer framework. This change is to facilitate tighter integration with existing ROS capabilities and libraries within Qt Creator.

![image1.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1527796228032-U2AIHUFZMKSRUCY5MYOI/image1.png)

* A set of new [video tutorials](https://aeswiki.datasys.swri.edu/qtcreator_ros/downloads/tutorials/videos/introduction/) were contributed by [Nathan George](https://github.com/nathangeorge1) broken down into five parts:
	+ Installation
	+ Import, Build, and Run Settings
	+ Create Hello World C++
	+ Building Hello World
	+ Indexing, Auto Complete and Code Style
* Updated [wiki](http://ros-industrial.github.io/ros_qtc_plugin/) using Sphinx and GitHub Pages to provide a richer wiki.
* In an effort to make it simpler when using the dugger within Qt Creator for ROS an "Attach to unstarted process" run step was created as shown below.

![image2a.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1527796935112-PNCXY9OXDWCO6TY6TOVS/image2a.png)

* A set of existing ROS templates were added to simplify adding ROS specific files within Qt Creator.

![image3.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1527796981411-6RJ9237FIKLG7IEN87JX/image3.png)

* Additional changes
	+ Show hidden files/folder like .clang-format and .rosinstall.
	+ Support for catkin tools partial build capabilities.

