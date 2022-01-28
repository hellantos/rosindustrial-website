---
author: Guest User
comments: false
date: '2013-08-06 09:51:56+00:00'
slug: 2013-8-5-ros-i-updates-new-webpage-move-to-github-and-catkin
title: 'ROS-I Updates: New Webpage, Move to GitHub, and Catkin'
media_type: None
description: We've been quiet on our social media outlets for a few weeks now, while
  significant ROS-I web and repository updates have been happening behind ...
layout: post
old_sp_link: https://rosindustrial.org/news/2013/8/5/ros-i-updates-new-webpage-move-to-github-and-catkin
---

We've been quiet on our social media outlets for a few weeks now, while significant ROS-I web and repository updates have been happening behind the scenes. These updates include:

* [ROSindustrial.org](http://www.rosindustrial.org) content has moved to the cloud
* ROS-I now uses the git Version Control System (VCS) and the ROS-I [repository](http://github.com/ros-industrial) has moved to GitHub
* We've updated all of the ROS-I code that is on GitHub so it works with the Catkin build system

The webpage move to the cloud allowed us to be more mobile device friendly. Now the menus and small fonts reformat when viewing from a mobile device. We also integrated the ROS-I tumblr blog with the site, so casual visitors are more likely tostumble onto this blog content. You should notice much more frequent blog posts in the future.

![New ROSindustrial.org home page](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1375747897842-1B7RYJF01DEQTSDPGBCK/ROS-I_Home.png)

Figure: *New ROSindustrial.org home page*

Next, to stay consistent with the ROS community, as of July the ROS-I repository has moved to GitHub and uses git VCS. Significantly, the change to GitHub means that there is tighter control and tracking of code changes, pull requests, and branches, all of which foster code quality and reliability. Since we've moved, we've seen greater community partipation with forks created by Fraunhofer, GA Tech, TU Delft, and Motoman. For the long list of why GitHub is great choice for a large open source community repo check out this [link](http://ros.org/wiki/RecommendedRepositoryUsage).

![ROS-Industrial GitHub Repository](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1375747095890-UKK47FO1DGYP9SRXI017/Git.png)

Figure: *ROS-Industrial GitHub Repository*

Lastly, we've updated all of the ROS-I core to use the Catkin build system in preparation to more tightly integrate with [MoveIt](http://moveit.ros.org)!. Catkin is the new build system introduced with ROS-Groovy. It enables users to more easily cross-compile and it makes ROS more portable. Note that a ROS build package (i.e. rosmake) can depend on a ROS-I Catkin packages, but not the other way around. Go here for more about [Catkin](http://ros.org/wiki/catkin).


