---
author: Guest User
comments: false
date: '2020-08-04 14:25:44+00:00'
slug: 2020-8-4-real-time-trajectory-planning-for-industrial-robots
title: Real-Time Trajectory Planning for Industrial Robots
media_type: None
description: Picture an industrial application where we want to do some work on large
  parts.
layout: post
old_sp_link: https://rosindustrial.org/news/2020/8/4/real-time-trajectory-planning-for-industrial-robots
---

Picture an industrial application where we want to do some work on large parts.
The work is performed in a series of bays, and the parts to be processed are
rolled into the bays on carts. The work bays typically have one or two people in
them doing various manual tasks, or perhaps just passing through. However, one
of the process tasks is difficult for a human to do. Maybe this task carries a
risk of repetitive motion injuries, or maybe it requires reaching an area that
is hard to reach from a standing position. It would be very desirable to
automate this task using a robot, but there are some challenges that limit the
applicability of traditional industrial automation:

1. There are people in the work area. Maybe this is a small company with only a
few bays, and they can't permanently cordon off the entire bay with light
gates and proximity sensors for an industrial robot. They need the robotic
system to safely work alongside humans.
2. Since the parts that need processing are just rolled in on carts, they are
positioned inconsistently. Even the parts themselves may have variation that
is not reflected in CAD data.
3. The environment is dynamic and constantly changing. Carts are constantly
being rolled in and out, and parts that are currently being processed could
be bumped and shifted.

Collaborative robotic hardware does not address all the challenges with this
type of application: **we need collaborative software as well**. Just as a human
walking down a hall does not plan every step in advance and then close their
eyes to execute the motion, our industrial automation systems need the ability
to adapt and plan in an "online" manner. In our application above, the system
needs to be constantly perceiving the environment and avoiding (and perhaps
predicting the motion of) moving collision obstacles all while tracking the part
that it is processing.

To this end, researchers at Southwest Research Institute have added online path
planning capability to the ROS Industrial ecosystem through updates to the
Tesseract (<https://github.com/ros-industrial-consortium/tesseract>) motion
planning framework and the TrajOpt
(<https://github.com/ros-industrial-consortium/trajopt_ros>) trajectory
optimization library. TrajOpt uses the Sequential Quadratic Programming (SQP)
method for motion planning. This algorithm works to solve the highly nonlinear
motion planning problem by approximating it as a quadratic and solving the
resulting Quadratic Program (QP) until the optimization converges to a local
minimum. The online planning capability is implemented by continuously
regenerating and solving the QP as the environment is updated with new
information about the robot's surroundings.

![manual_moving_demo.gif](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1596552906488-ZF3IVWP221EXHTTI41HC/manual_moving_demo.gif)

The examples below show the results. In these examples, a 6-DOF robot arm is
underslung on a 2-DOF gantry. A red cylinder surrounds the robot, representing a
boundary that the robot should keep away from humans and other unexpected
obstacles. In the first example, the robot dynamically avoids a human that walks
into its work area. The second example demonstrates the robot following a moving
target pose. Both animations are displayed in real-time, and the system easily
achieved a 1000Hz update rate for this example while running on a consumer
desktop PC. A simplified version of these examples is available in the
tesseract\_ros repository
(<https://github.com/ros-industrial-consortium/tesseract_ros>) so that you can
run it yourself.

![Dynamically avoiding a human entering working space](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1596552995646-N4DDEE681LZ1NZUIW9IZ/pacing.gif)

Figure: *Dynamically avoiding a human entering working space*

![moving target pose](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1596556021103-GR7LZ1IZ2N1PZS4RQ2AJ/target_moving.gif)

Figure: *moving target pose*

There is still a lot work to be done before we could deploy this in an application like the one in our example. One remaining question is what level of on-the-fly flexibility is desirable for a given application. Does the robot have free reign to adapt its path anywhere within its joint limits, or do we constrain it to only deviate by some amount from a given preplan? Creating a framework to represent this kind of high-level logic as well as the infrastructure involved in execution is the next step in the process. We look forward to deploying a system with this feature set on hardware using something simlilar to the joint\_trajectory\_controller within ros-control (<http://wiki.ros.org/joint_trajectory_controller>).

Editor's Note: This work and subsequent blog entry made possible through contributions by Levi Armstrong and Joseph Schornak. Thanks to Matthew Powelson for his contributions to ROS-Industrial during his time at Southwest Research Institute, we wish him the best on his next robotics adventure!


