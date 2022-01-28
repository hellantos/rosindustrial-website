---
author: Nomean At Gmail
comments: false
date: '2021-11-05 21:23:26+00:00'
slug: 2021-11-5-c1cxmfoceczk7gfpq0mpfhezfje2zk
title: Hands on with the DreamVu PAL Mini
media_type: None
description: I've been testing an evaluation kit for a new camera from DreamVu. The
  PAL Mini is a tiny 360-degree 3d camera with a software package for object ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/11/5/c1cxmfoceczk7gfpq0mpfhezfje2zk
---

I've been testing an evaluation kit for a new camera from DreamVu. The PAL Mini is a tiny 360-degree 3d camera with a software package for object detection and avoidance. It has ROS support and is intended for use with mobile robots. 

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/3403d774-e579-4623-9989-e7b1f21c967d/xbox.jpg)

Figure: *They're not kidding when they say it is small. Here is the camera compared to an Xbox One controller.*

The camera connects to an Nvidia Jetson, offloading the computationally heavy task of rectifying the image and generating a ROS navigation compatible LaserScan message. The Jetson can run ROS and may be sufficient for a completely controlling a mobile robot. DreamVu provides samples for mapping and navigation with a TurtleBot. 

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/df86a9b1-4c2a-402e-8835-cd1c239e9d62/jetson.jpg)

Figure: *The camera connects to the Nvidia Jetson with a USB-C cable. There are ample remaining ports for other devices.*

The Jeston can be connected to a host pc via ethernet and stream the resulting laser scans and rgb images. A simple ROS node is provided to convert to standard cv::Mats and publish them. A remote ROS master is not required for this.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/7c87c392-2f94-4462-8b85-017244559dd9/rviz.png)

Figure: *A laser scan is generated, along with a panoramic image. The laser scan is combined with the image making it easy to see what and where and obstacle is.*

As with any new product I ran into some issues during testing. I prefer to use the camera by streaming the results to my host PC, which most likely wasn't their main focus while developing a camera designed to mount on mobile robots. Their support was able to resolve the issue quickly and took my suggestions on how to improve the reliability of their ROS package.

More information is available on their [website](https://dreamvu.com). You can also check their [Github](https://github.com/DreamVu/ODOA) (coming soon). Contact DreamVu for information on Object Detection and Avoidance, and other applications of their 360-degree view cameras and solutions. 


