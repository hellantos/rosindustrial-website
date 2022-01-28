---
author: Levi Armstrong (SwRI)
comments: false
date: '2017-08-08 15:29:22+00:00'
slug: 2017-8-8-final-in-series-on-ros-i-development-process-publishing-installation
title: Final in series on ROS-I development process – Publishing & Installation
media_type: None
description: This is the last post in a series detailing the ROS-Industrial software
  development process. We will discuss publishing and installing software. ...
layout: post
old_sp_link: https://rosindustrial.org/news/2017/8/8/final-in-series-on-ros-i-development-process-publishing-installation
---



![ROS-Development-BlogPost-01-ARTC Update.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1505409857143-4JGOI1X62JEADOAY4BDR/ROS-Development-BlogPost-01-ARTC+Update.png)

This is the last post in a series detailing the ROS-Industrial software development process. We will discuss publishing and installing software. The [first post](http://rosindustrial.org/news/2016/8/26/ros-industrial-development-process-contribution) described the process of contributing code to a project (item 1-3 in the figure above). The [second post](http://rosindustrial.org/news/2016/11/9/series-on-ros-industrial-development-process-code-review) described the process of Continuous Integration, Pull Request (PR) peer review , and the release of a given repositories packages by the maintainer (item 4-7). Note that the starred numbers in the software development process illustrated above correspond to the outline below. 

8. The publishing of the released packages (item 8) is managed by OSRF and is not on a set schedule. This usually happens when all packages for a given distro are built successfully and stable. The current status for the distro kinetic can be found [here](http://repositories.ros.org/status_page/ros_kinetic_default.html) . Navigating to other distros can be done by changing the distro name in the link.
9. Once the package has been published, it is available to be installed by the developer (item 9).
10. After the install of a new version, the developer may have questions, experience issues or it may not have the necessary functionality which should all be reported on the packages GitHub repository as an issue (item 10). If an issue is identified or there is missing functionality that the developer requires, the cycle starts back at (item 2).

The full series has been compiled and is now located on ROS-Industrial website [here](http://rosindustrial.org/developmentprocess/)
