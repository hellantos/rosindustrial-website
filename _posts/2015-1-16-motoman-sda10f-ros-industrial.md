---
author: Guest User
comments: false
date: '2015-01-16 20:38:24+00:00'
slug: 2015-1-16-motoman-sda10f-ros-industrial
title: Motoman SDA10F & ROS-Industrial
media_type: None
description: Cross-posted from the [Smart Robotic Systems blog](http://www.smartroboticsys.eu/?p=675&lang=en)
layout: post
old_sp_link: https://rosindustrial.org/news/2015/1/16/motoman-sda10f-ros-industrial
---

Cross-posted from the [Smart Robotic Systems blog](http://www.smartroboticsys.eu/?p=675&lang=en)

Author: Frantisek Durovsky

At the Department of Robotics we've spent several weeks testing the new ROS-Industrial [driver](https://github.com/ros-industrial/motoman) for SDA10F since it's announcement on Dec 10th 2014. As mentioned in the [original post](http://rosindustrial.org/news/2014/12/10/demonstration-of-the-fraunhofer-ipa-ros-i-driver-for-yaskawa-motoman-dual-arm-robots), the driver was developed by Fraunhofer IPA in cooperation with Yaskawa Smart Robotics Center in Japan, Yaskawa Motoman Robotics and is designated to control dual arm Motoman robots. Even though only the hydro version of driver has officially been released so far, we have also scucessfully managed to test the current indigo branch in combination with Ubuntu 14.04 LTS.

Motoman SDA10F Support and Moveit Config packages follow standard ROS-Industrial naming convention so all config and xacro files are located as usual. Roslaunching "test*sda10f.launch" from "motoman*sda10f\_support" folder provides simple interface to check basic robot's model behaviour and orientation of particular axes.

To read the full blog post please browse here: <http://www.smartroboticsys.eu/?p=675&lang=en>


