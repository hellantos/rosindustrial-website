---
author: Guest User
comments: false
date: '2016-10-24 20:54:47+00:00'
slug: 2016-10-24-the-nuclear-robotics-group-goes-public
title: The Nuclear Robotics Group Goes Public!
media_type: None
description: 'Submitted by: Dr. Andrew Zelenak and Dr. Mitch Pryor, UT Austin Nuclear
  and Applied Robotics Group (NRG)'
layout: post
old_sp_link: https://rosindustrial.org/news/2016/10/24/the-nuclear-robotics-group-goes-public
---

Submitted by: Dr. Andrew Zelenak and Dr. Mitch Pryor, UT Austin Nuclear and Applied Robotics Group (NRG)

Cross posted from: <http://robotics.me.utexas.edu/nuclear-robotics-group-goes-public>

We are happy to announce a code release!
The Nuclear Robotics Group at UT-Austin was an early adopter of ROS software, but until recently, most of our software was private. However, our main sponsor (Los Alamos National Laboratory) recently gave the green light to open-source our code. With that approval, we are slowly rolling code over to a [public repository](https://github.com/UTNuclearRoboticsPublic) and will be indexing the packages with ROS as appropriate. This was first announced to the ROS-Industrial community in [June 2016](http://rosindustrial.org/news/2016/6/14/ros-i-community-web-meeting-june-2016). A couple little gems which might already be useful for the public include:

* The [netft\_utils package](http://wiki.ros.org/netft_utils) for ATI force/torque sensors:
	+ Set the data collection rate
	+ Transform force data between TF frames as a robot moves
	+ Compensate for gravity forces on the end-effector
* A driver for [LeapMotion](https://github.com/UTNuclearRoboticsPublic/leap_motion_controller)
	+ The LeapMotion hardware tracks a human's hands, making for some really cool demos and user interfaces
* A driver for the [Griffin Powermate](https://github.com/UTNuclearRoboticsPublic/griffin_powermate) user interface device
A [contact control GUI](https://github.com/UTNuclearRoboticsPublic/contact_control)

In the future, we'll be open-sourcing even more, so keep your eyes open! 
The video below shows a little demo incorporating the above-mentioned packages.


