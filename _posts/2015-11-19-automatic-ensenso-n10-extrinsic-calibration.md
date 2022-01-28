---
author: Guest User
comments: false
date: '2015-11-19 15:26:04+00:00'
slug: 2015-11-19-automatic-ensenso-n10-extrinsic-calibration
title: Automatic Ensenso N10 extrinsic calibration
media_type: None
description: Submitted by Victor Lamoine, Institut Maupertuis
layout: post
old_sp_link: https://rosindustrial.org/news/2015/11/19/automatic-ensenso-n10-extrinsic-calibration
---

Submitted by Victor Lamoine, Institut Maupertuis

The [Ensenso N10](http://www.ensenso.com/portfolio-item/n10/) is an industrial 3D sensor using two cameras and the stereo-vision principle. One interesting feature is that the sensors works in infrared wavelengths and an IR projector projects a random pattern to allow scanning uniform surfaces (where the stereo-correspondence would fail otherwise).

I integrated the Ensenso N10 in the Point Cloud Library (1.8.0 version, not yet released), and you can find a tutorial [here](http://www.pointclouds.org/documentation/tutorials/ensenso_cameras.php#ensenso-cameras). The PCL EnsensoGrabber API is available [here](http://docs.pointclouds.org/trunk/classpcl_1_1_ensenso_grabber.html#details).
This camera is very easy to use yet not very fast (only 4 FPS through PCL !) because of an unknown reason (it should be much faster).

I have made a package allowing fully automatic extrinsic calibration of the sensor mounted on a robot. It should be easy to change the robot and the setup (eg: fixed camera):
[https://github.com/InstitutMaupertuis/ensenso*extrinsic*calibration](https://github.com/InstitutMaupertuis/ensenso_extrinsic_calibration)

The extrinsic calibration relies on Ensenso SDK internals; there is no dependency on the *industrial\_calibration* package.

So if you plan on using such a camera on a robot, it should be very easy with this package! Don't hesitate to leave a message here or on the issue tracker if you have problems understanding how it works, making it work...

**Update from Victor (Nov. 19):**

I did not choose the EnsensoSDK over the *industrial\_calibration* package.

In fact I began to work with the EnsensoSDK calibration in early 2014, at that time I didn't even know about ROS-Industrial!

So I just wanted to go to the simplest solution for the Ensenso and use my work (PCL integration of the Ensenso) to automatically calibrate the sensor.

I have began working (well.. understanding first!!) with the *industrial\_calibration* package because I want to calibrate the David SLS-2 on the robot (and their SDK does not provide any calibration procedure).

So in short, the next package will be *sls\_2\_extrinsic\_calibration* and it will depend on *industrial\_calibration.*


