---
author: Guest User
comments: false
date: '2016-01-29 15:38:30+00:00'
slug: 2016-1-29-new-intrinsic-calibration-procedure
title: New Intrinsic Calibration Procedure
media_type: None
description: According to a ROS users [survey](http://www.ros.org/news/2014/04/ros-user-survey-the-results-are-in.html)
  that was conducted
layout: post
old_sp_link: https://rosindustrial.org/news/2016/1/29/new-intrinsic-calibration-procedure
---

According to a ROS users [survey](http://www.ros.org/news/2014/04/ros-user-survey-the-results-are-in.html) that was conducted
in 2014, the most popular hardware to integrate with
ROS is a camera. Cameras are often used to perceive
the environment or to localize robots and are a critical
component of the sense-plan-act capability that ROS enables.
Over the past two years, the ROS-I team has been working
to create an industrial calibration library that supports both
intrinsic and extrinsic calibration of vision sensors. What
is novel about the library is that is can handle groups of
heterogeneous sensors that may be static, or mounted to a
robot, or some combination thereof. And it coordinates with
MoveIt! to automate calibration procedures in which robot
motion is required during calibration. While the extrinsic
calibration routines are well in hand, the intrinsic calibration
algorithm, which is based on a popular lens distortion model,
resulted in higher parameter variance than was expected
based on residual errors. This is particularly true for the focal
length parameter, which is essential for correctly interpreting
the size of objects in the scene. The ROS-I team has
developed a novel camera intrinsic calibration technique that
is both computationally faster and provides superior results
to the methods commonly employed in machine vision.  

The optimization procedure outlined by Zhang and automated
by both OpenCV/ROS, and Matlab orchestrate the collection
of a set of images of a calibration target. Both the extrinsic
pose of the camera and the intrinsic parameters themselves
are determined by minimizing the re-projection error. Using
these methods, the residual re-projection error is on the
order of ¼ pixel/observation or less. However, the variances
of focal length and optical center are much higher, typically
being 20 pixels and 5 pixels respectively. This is due to
correlation between parameters of the distortion model with
the focal length parameter.  

The new procedure developed by the ROS-I team reduces parameter variance to be on par with the residual error. It requires only 10 to 20 images, but each is taken a known distance apart with little or no skew (refer to images). The new procedure estimates the extrinsic pose for the first
image, and constrains the optimization to use the known pose relationship for subsequent images. The focal length and optical center are significantly better constrained. Using the resulting intrinsic calibration parameters for a given camera yields significantly better extrinsic calibration or pose estimation accuracy. Try out the Intrinsic Camera
Calibration (ICC) tutorial that is posted on the [ROS-I wiki](http://wiki.ros.org/industrial_extrinsic_cal/Tutorials/Intrinsic%20Camera%20Calibration).

![The new intrinsic calibration procedure requires one to move the camera to known positions along an axis that is approximately normal to &nbsp;the calibration target.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1454081538709-T9MQ90M4S904JGHTRDFZ/Calibration_Target.png)

Figure: *The new intrinsic calibration procedure requires one to move the camera to known positions along an axis that is approximately normal to the calibration target.*


