---
author: Guest User
comments: false
date: '2020-10-20 12:18:17+00:00'
slug: 2020-10-20-first-impressions-using-tesseract-ignition
title: First Impressions Using Tesseract Ignition
media_type: None
description: I have a robotics application where I am using an ABB robot with a fairly
  simple environment and no complex motions expected. I decided this would ...
layout: post
old_sp_link: https://rosindustrial.org/news/2020/10/20/first-impressions-using-tesseract-ignition
---

I have a robotics application where I am using an ABB robot with a fairly simple environment and no complex motions expected. I decided this would be a good candidate for testing the new Tesseract Ignition tools and the new Tesseract command language feature that is currently in development on GitHub alongside the main master branch of Tesseract (also TrajOpt and Descartes are being updated to work with these new changes). After installing the Tesseract Ignition tools, I was able to put in our URDF which has a simple end effector on a standard ABB IRB 2400 URDF. The Tesseract Setup Wizard allowed me to easily generate an allowed collision matrix with a single click after loading in my URDF, and then the kinematic groups tool was also very easy to use to add my desired kinematic chain for the motion planner. From here I was able to have an srdf configuration file that would be usable in the Tesseract motion planning environment. 

![Picture1.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1603196024859-Z0PT82T5HR6KHJ1USZQ2/Picture1.png)

In software, I was then able to extend the new Tesseract Command Language planning server class and add my own planning profiles for freespace, transition, and raster motions that allow for parallel processing of motion plans in a variety of pre-made taskflow structures. Once finished I could easily load in a toolpath and quickly generate paths using the new planning server. The new Tesseract Ignition Visualization tool allowed me to visualize all the target waypoints and the robot motion. (Note I had to build Tesseract Ignition from source to get the visualization to work for now)

![Picture2.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1603196045054-29J7GS9POY784DYW2EKL/Picture2.png)

Overall this integration process has been user friendly and allows me to spend less time having to worry about the details of the motion planning process.

Editor's Note: Tyler Marr is a Research Engineer at Southwest Research Institute and has been developing and deploying ROS-based systems involving autonomous motion planning during his time at SwRI.


