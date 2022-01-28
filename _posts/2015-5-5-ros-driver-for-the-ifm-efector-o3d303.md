---
author: Guest User
comments: false
date: '2015-05-05 21:38:20+00:00'
slug: 2015-5-5-ros-driver-for-the-ifm-efector-o3d303
title: ROS Driver for the IFM Efector O3D303
media_type: None
description: 'Submitted by: Tom Panzarella, [Love Park Robotics, LLC](http://loveparkrobotics.com)'
layout: post
old_sp_link: https://rosindustrial.org/news/2015/5/5/ros-driver-for-the-ifm-efector-o3d303
---

Submitted by: Tom Panzarella, [Love Park Robotics, LLC](http://loveparkrobotics.com)

Love Park Robotics has taken part in an early beta test of the new IFM Efector O3D303 3D camera system. This sensor was officially released in Germany on April 13, 2015. The O3D303 is a time-of-flight sensor, specifically designed for use in industrial environments and automation applications. The 176x132 element detector features a relative accuracy of +/-4mm. In addition to the robust design, it is able to operate in illumination conditions ranging from complete darkness to sunlight. It is also affordable, at a per-unit cost of $1250 USD. A picture of the O3D303 is shown below along with a point cloud of an imaged pallet (taken in an office environment) to highlight the quality of the sensor data.

![o3d303](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1430861788640-5NUQ0SBY0D37A2Y2LO1G/o3d303)

![pallet](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1430861548105-DPZUAS4SRZU6QLFDGKT0/pallet)

As part of our beta test period, Love Park Robotics developed a software interface to the O3D303 that allows us to utilize the sensor within software frameworks such as [PCL](http://pointclouds.org), [OpenCV](http://opencv.org), and [ROS](http://ros.org). This code has been made available as open-source on Github in the following repositories: [libo3d3xx](https://github.com/lovepark/libo3d3xx) and [o3d3xx-ros](https://github.com/lovepark/o3d3xx-ros). Additionally, we are working with the ROS Industrial community to make binary debian packages available as part of the core ROS and ROS-I distributions.

As mentioned above, the software is split across two separate repositories. `libo3d3xx` is the core C++ interface to the hardware making the 3D data available as a PCL point cloud and the depth, confidence, and amplitude images available as OpenCV images. `o3d3xx-ros` is a ROS wrapper around `libo3d3xx` making it convenient to launch the camera as a node that will participate in a larger ROS computation graph making the data available on published topics and exposing services to configure and introspect the camera settings. The reason we split the code across two distinct projects is in recognition of the fact that not all users of the O3D303 will be operating within a ROS environment yet they will likely want to take advantage of the state-of-the-art computer vision algorithms available in PCL and OpenCV. We expect that this separation of concerns will also make the code easier to maintain and port to new platforms. The Github repositories have much more technical information available that you can use to get started.

To date, Love Park Robotics has been testing the ROS interface to the O3D303 as a primary navigation sensor for a medical mobility application and as an object recognition sensor for industrial automation applications. We plan to keep the code current to hardware changes as the O3D3xx series of sensors evolve. To that end, we have been keeping in close communication with the sensor vendor, IFM Efector. The code will remain open-source and our process will remain transparent -- for now, we are using the Github issue tracker to document our roadmap for the software. We invite the ROS-I community to join us in making sure this software represents the most robust interface to this new and exciting sensor for industrial applications. We look forward to seeing how you put it to work.


