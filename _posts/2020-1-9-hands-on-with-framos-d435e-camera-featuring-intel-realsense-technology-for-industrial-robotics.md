---
author: Guest User
comments: false
date: '2020-01-09 17:53:47+00:00'
slug: 2020-1-9-hands-on-with-framos-d435e-camera-featuring-intel-realsense-technology-for-industrial-robotics
title: Hands on with FRAMOS D435e camera featuring Intel® RealSense™ technology for
  industrial robotics
media_type: None
description: It has been nearly 10 years since the release of the XBOX Kinect camera,
  and
layout: post
old_sp_link: https://rosindustrial.org/news/2020/1/9/hands-on-with-framos-d435e-camera-featuring-intel-realsense-technology-for-industrial-robotics
---

It has been nearly 10 years since the release of the XBOX Kinect camera, and
things have certainly changed. Gone are the days of using reverse-engineered
software drivers or soldering on USB cables. We have arrived in a time of 3D
perception plenty. Multiple vendor-supported 3D camera options exist utilizing
different depth camera technologies, to such an extent that picking one can
often be difficult. The ever-popular [3D camera survey](https://rosindustrial.org/3d-camera-survey) has grown to over 20 cameras, and
it is still growing. Nevertheless, the ROS-I team is committed to testing as
many of these sensors as possible and putting them through their paces.

One option that I have recently become fond of is the Intel RealSense. In my
mind it is a sort of industry standard. Released and actively supported by ROS-I
consortium member Intel, the RealSense is inexpensive, available off the shelf,
and works reliably across a wide variety of operating conditions. Combine that
with a stellar ROS (and ROS 2) driver, and you have a winner. The convenience of
being able to just plug in the camera, bring up RealSense-viewer, and then tune
or debug the camera cannot be overstated. It is a camera for the robot masses.
However, it does have a problem. The Intel RealSense is USB 3.

![intelrealsense1.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1578589062796-7PB0DSYSF6E1OLL723I6/intelrealsense1.png)

For industrial automation tasks USB cameras have long been an issue. We often set up robotic wrist cameras at Southwest Research Institute. With a [properly calibrated](https://rosindustrial.org/news/2016/4/11/calibration-updates) depth camera on a robot wrist we are able to [reconstruct large parts](https://rosindustrial.org/news/tag/YAK) and automate complex industrial tasks. USB complicates this setup. Flaky connections can plague a setup like this, leading developers to ritualistically disconnect and reconnect USB cables whenever something goes wrong. Further, cable runs quickly exceed the length that USB can handle leading to the use of sometimes-suspect USB-ethernet extenders. If only there was a camera option that had the software backing of the Intel RealSense with the industrial readiness of POE. Meet the [FRAMOS Industrial Depth Camera D435e](https://www.framos.com/en/news/framos-launches-an-industrial-3d-gige-camera-based-on-intel-s-realsense-technology). Based on the Intel RealSense technology, FRAMOS has packaged this D435e 3D GigE camera in an IP66 enclosure and replaced the USB-C connector with an industrial-ready M12 GigE connection. While it certainly isn't going to replace the Intel RealSense as the camera for the robot masses, it might be the camera for the industrial robot masses.

![20191118_165810s.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1578592287901-OHANY7UVDSY5UAX3R6UW/20191118_165810s.jpg)

The ROS-I team recently got the chance to work with the camera hands-on, deploying it on an industrial scan-and-plan project. The setup for the FRAMOS RealSense is straightforward if a little quirky. On Linux one must simply install the FRAMOS CameraSuite Software and then install their custom version of the librealsense SDK. Then upon configuring the network settings for the camera, it behaves just like the USB RealSense. ROS doesn't know the difference, and the RealSense-viewer behaves in the same way. However, using it has not been without its difficulties. ROS support for this camera was released October 29, 2019. We began integrating it on our system on November 4, 2019. As such, there were some problems. The software suite only allowed a limited set of the parameters to be set and required a custom version of libglf3w. This caused an issue where the camera mysteriously stopped working after an unrelated package was updated, and the only apparent solution was to reinstall the software suite. However, a few weeks later a new version of the software was released that fixed both issues.

Overall, using this camera has been troublesome but to an ever-decreasing degree. To some extent, the convenience and maturity of the Intel RealSense makes it easy to complain about any small thing that goes wrong on new hardware, but I personally have high hopes for the FRAMOS Realsense. When debugging, their software support was quick to respond, and the software seems to be in a state of continued improvement. We still run into occasional crashes, but similar issues plagued the Intel RealSense a mere year ago that have since been resolved. The necessity of the custom version of librealsense SDK is its biggest oddity, but with continued collaboration between FRAMOS and Intel this may be resolved someday.

Ultimately, when I think about the ideal camera for a ROS-I system, I imagine a POE camera with easy to use software, rock-solid vendor support, and an active ROS community. While there will always be cameras that excel at one application or another due to depth of field, resolution, or sensing technology, for medium to large scan and plan applications, the FRAMOS RealSense is well on its way to achieve that goal. Others will undoubtedly join the market, but regardless it is an exciting time for 3D perception in industrial applications!


