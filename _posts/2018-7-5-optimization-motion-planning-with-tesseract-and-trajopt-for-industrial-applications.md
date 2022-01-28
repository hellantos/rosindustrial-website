---
author: Levi Armstrong (SwRI)
comments: false
date: '2018-07-10 04:13:34+00:00'
slug: 2018-7-5-optimization-motion-planning-with-tesseract-and-trajopt-for-industrial-applications
title: Optimization Motion Planning with Tesseract and TrajOpt for Industrial Applications
media_type: None
description: Southwest Research Institute launched an internal R&D project to integrate
  the existing motion planner TrajOpt (Trajectory Optimization for Motion ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/7/5/optimization-motion-planning-with-tesseract-and-trajopt-for-industrial-applications
---

Summary
=======

Southwest Research Institute launched an internal R&D project to integrate the existing motion planner TrajOpt (Trajectory Optimization for Motion Planning) into ROS. TrajOpt was created at UC Berkeley as a software framework for generating robot trajectories by local optimization. The integration of TrajOpt necessitated new capabilities that spawned the creation of several new packages: tesseract and trajopt\_ros. The tesseract package contains a new lightweight motion planning environment designed for industrial application, while the trajopt\_ros package contains packages specific to TrajOpt. We will demonstrate how these tools complement existing planners, like OMPL or Descartes, to solve complex problems quickly and robustly.

Description
===========

The original implementation of TrajOpt was developed using OpenRave for Kinematics and Bullet for contact checking. The first step was to replace OpenRave with MoveIt! Kinematics and second replace the collision environment with MoveIt!'s Collision environment. Early on in the process several limitations were found in both MoveIt!'s Kinematics and Collision environment.

TrajOpt requires the ability to calculate specific information about the robot not provided by MoveIt!, but it turns out KDL, which is one of the kinematics libraries used by MoveIt!, provides methods for obtaining the required information. This resulted in the development of a custom kinematics library built on KDL for both kinematic chains and non-kinematic chains. Secondly TrajOpt leverages specific characteristics of convex to convex contact checking to provide the minimum translation vector to move two objects out of collision. In the process of integrating with MoveIt!, it was determined that it did not provide detailed distance information. Also, after further evaluation it was found that MoveIt! does not support convex to convex collision checking requiring significant API changes across multiple repositories. Since the IR&D was time-sensitive, it was determined to not use MoveIt! and create a light-weight Motion Planning Environment (Tesseract).

The Tesseract environment was designed to support SwRI's work in complex industrial motion planning applications where flexibility and modularity are key to adapting to new applications. Packages include: 

* **tesseract\_core** – Contains platform agnostic interfaces and data structures to be used. tesseract\_ros –ROS implementation of the interfaces identified in the tesseract\_core package, currently leverages Orocos/KDL libraries.
* **tesseract\_collision** – ROS implementation of a Bullet collision library. It includes both continuous and discrete collision checking for convex-convex and convex-concave shapes.
* **tesseract\_msgs** – ROS message types used by Tesseract.
* **tesseract\_rviz** –ROS visualization plugins for Rviz for both the environment state and trajectories.
* **tesseract\_monitoring** – Provides tools for monitoring the active environment state and publishing contact information. This is useful if the robot is being controlled outside of ROS, but you want to make sure it does not collide with objects in the environment. Also includes the environment monitor, which is the main environment facilitating requests to add, remove, disable and enable collision objects, while publishing its current state to keep other ROS nodes updated.
* **tesseract\_planning** – Contains interface bridges between Tesseract Environment and motion planners OMPL and TrajOpt.

After the creation of Tesseract all necessary capabilities were available to finish the integration of TrajOpt into ROS. The new motion planner was evaluated against the following use case while minimizing joint velocity, acceleration and jerk cost along with collision avoidance cost: 

* Fully Constrained Cartesian Path
* Semi-Constrained Cartesian Path
* Free Space Path
* Semi-Constrained Free Space Path
* Free Space + Constrained Cartesian Path

Only a few of the above case will be discussed below. The first is a Semi-Constrained Free Space Path where a KUKA iiwa needs to plan around a sphere while maintaining tool orientation with the z-axis rotation free to rotate. Each step of the optimization is shown in Figure 1. Note that once the robot is out of collision the remaining iteration are spent minimize joint velocity, acceleration and jerk.

![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530794922689-YSY3VEJ3FQC24LTLBH4W/Screenshot+from+2018-07-05+07-48-11.png)![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530794922689-YSY3VEJ3FQC24LTLBH4W/Screenshot+from+2018-07-05+07-48-11.png)

*Figure 1 - KUKA iiwa (7 DOF) TrajOpt free space planning round sphere*

The next use case was a complex industrial application. It is an 8 DOF problem, where the robot picks up a seat off of a conveyor and loads the seat into a car. This is a very challenging task, given the amount of manipulation required to pass through the doorway and set the seat without colliding with the car structure. The final trajectory, found in 0.482 seconds using TrajOpt with continuous collision checking enabled, is shown in Figure 2.

![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530795122965-Y4KJ9MHCCVRZ9INCWP3C/Screenshot+from+2018-07-05+07-51-51.png)![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530795122965-Y4KJ9MHCCVRZ9INCWP3C/Screenshot+from+2018-07-05+07-51-51.png)

*Figure 2 - TrajOpt Car Seat Installation Example*

One significant advantage of the Tesseracts implementation of the Bullet Collision Library is the ability to perform continuous collision checking. An example demonstrating the use of continuous collision with TrajOpt is shown in Figure 3. Each red box represents a state in the trajectory with the green box being the collision object to avoid during planning. Under discrete collision checking each state would be found to be collision free even if the motion between states was not. With continuous collision checking enabled, it can be seen that a collision is detected when transitioning between state 2 and state 3 resulting in a collision-free trajectory.

![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530795195923-QQ2DH1DK73O6Z552D51D/Screenshot+from+2018-07-05+07-53-07.png)![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530795195923-QQ2DH1DK73O6Z552D51D/Screenshot+from+2018-07-05+07-53-07.png)

*Figure 3 - Planar Box (2 DOF) TrajOpt free space planning with continuous collision checking*

The remaining application to discuss is a complex Semi-Constrained Cartesian path with 437 poses each with 5 Degrees Of Freedom (DOF) fixed and the tool z-axis free to rotate. The application is performing a deburr operation on a complex puzzle piece shown in Figure 4. Also the problem includes a 7 DOF robot and a 2 DOF positioner for the spindle making it a non-fixed base kinematic chain. This requires the use of Tesseract's joint kinematic model developed for this particular use case. The TrajOpt motion planner problem contains roughly 3,000 constraints and was able to solve in 4.4 seconds.

![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530795288812-HGKAFZ4WJOAM3T26F1KV/Screenshot+from+2018-07-05+07-54-37.png)![Figure <span style='font-size:11.0pt;line-height:
107%;font-family:"Calibri",sans-serif;mso-ascii-theme-font:minor-latin;
mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;mso-hansi-theme-font:
minor-latin;mso-bidi-font-family:Ca…](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530795288812-HGKAFZ4WJOAM3T26F1KV/Screenshot+from+2018-07-05+07-54-37.png)

*Figure 4 – Semi-Constrained Cartesian Planning Problem*

TrajOpt has shown itself capable of solving very difficult problems but, as an optimization, it can be sensitive to its initial conditions. This presentation will explore several strategies for seeding the solver, including the integration of sampling planners like OMPL and Descartes. These planners can coarsely and quickly sample the space of a problem to generate candidate solutions that can be refined by TrajOpt. If that should fail, a new robot configuration is selected from the sampled problem-space and the process repeated. For some problems this results in a planner finding a true global optimum.

References
==========

1. [Tesseract Repository](https://github.com/ros-industrial-consortium/tesseract)
2. [TrajOpt ROS Repository](https://github.com/ros-industrial-consortium/trajopt_ros)
3. [Examples](https://github.com/ros-industrial-consortium/trajopt_ros/tree/kinetic-devel/trajopt_examples) (Tesseract and TrajOpt ROS)
4. Videos
	* [TrajOpt Puzzle Piece with Positioner](https://youtu.be/Bg0wQLNEANk)
	* [TrajOpt PR2 Planning Around Table](https://youtu.be/xz0MCLqQfpc)
	* [TrajOpt Glass Up Right Planning](https://youtu.be/MjdkQeGidmQ)
	* [TrajOpt Continuous Collision Checking Planning](https://youtu.be/WVxZL5YEIU4)

