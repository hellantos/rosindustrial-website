---
author: Guest User
comments: false
date: '2014-10-01 16:09:29+00:00'
slug: 2014-9-24-industrial-calibration-library-update-and-presentation
title: Industrial Calibration Library Update and Presentation
media_type: None
description: 'By Dr. Chris Lewis, SwRI:'
layout: post
old_sp_link: https://rosindustrial.org/news/2014/9/24/industrial-calibration-library-update-and-presentation
---



By Dr. Chris Lewis, SwRI:

Robotics and automation systems are increasingly reliant on both 2D and 3D imaging systems to provide both perception and pose estimation. Calibration of these camera/robot systems is necessary, time consuming, and often a poorly executed process for registering image data to the physical world. SwRI is continuing to develop the [industrial calibration library](http://wiki.ros.org/industrial_extrinsic_cal) to provide tools for state-of-the-art calibration with the goal to provide reliably accurate results for non-expert users. Using the library, system designers may script a series of observations that ensure sufficient diversity of data to guarantee system accuracy. Often interfaces to motion devices such as robots may be included to fully automate the calibration procedure.

As a vision systems developer one may ask the following questions with regards to both intrinsic and extrinsic camera calibration.

1. How many images of the calibration target are needed?
2. At what ranges?
3. At what angles?
4. How many near the center of the field of view vs at the edges?
5. What accuracy is achievable?
6. What accuracy was achieved?

With our framework, a user may rapidly explore these questions.

Our framework is built using [Google's Ceres Solver](http://ceres-solver.org/) which is a state of the art non-linear optimization tool specifically designed to solve Bundle Adjustment problems efficiently. Our framework consists of five main parts.

1. The main script processing code which
	* Collects observations
	* Runs the optimization
	* Installs the results
2. A library of Ceres compatible cost functions.
3. The camera observer interface which ties your cameras to the system and automatically triggers the camera and locates common calibration targets within specified regions of interest.
4. The scene trigger interface which provides interfaces to motion hardware such as robots. It may also serve to communicate with users to specify how to configure each scene.
5. Transform interfaces which provide the means by which kinematic values may be fed into and out of the calibration system. Updates to these extrinsic kinematic parameters is immediate and persistent.

Using this framework, we have demonstrated three distinctly different calibrations:

* Extrinsic calibration of a camera mounted on the tool of a robot
* Extrinsic calibration of a network of cameras
* Extrinsic calibration of a static camera to a robot

In addition, the ROS-I team is currently developing an intrinsic calibration script whereby a robot moves the calibration target to create a repeatable set of calibration images. In the near future, we will be developing kinematic calibration procedures for robots using cameras to better estimate robotic joint parameters.

Additional links:

* Wiki documentation: [industrial\_extrinsic\_cal](http://wiki.ros.org/industrial_extrinsic_cal)
* [Tutorials](http://wiki.ros.org/industrial_extrinsic_cal/Tutorials)
* [One-shot calibration video](http://youtu.be/AMMNXYtox_E)
* [Presentation slides](http://roscon.ros.org/2014/wp-content/uploads/2014/07/LewisPresentation.pdf)

