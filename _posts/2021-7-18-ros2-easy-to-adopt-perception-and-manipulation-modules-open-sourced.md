---
author: Sheila Suppiah (A-Star)
comments: false
date: '2021-07-19 04:53:00+00:00'
slug: 2021-7-18-ros2-easy-to-adopt-perception-and-manipulation-modules-open-sourced
title: ROS2 Easy-to-Adopt Perception and Manipulation Modules Open Sourced
media_type: None
description: ROS-Industrial has developed the [easy\_perception\_deployment (EPD)](https://github.com/ros-industrial/easy_perception_deployment)
  & ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/7/18/ros2-easy-to-adopt-perception-and-manipulation-modules-open-sourced
---

ROS-Industrial has developed the [easy\_perception\_deployment (EPD)](https://github.com/ros-industrial/easy_perception_deployment) & [easy\_manipulation\_deployment (EPD)](https://github.com/ros-industrial/easy_manipulation_deployment) ROS2 packages to accelerate the industries' effort in training and deployment of custom CV models and also provide a modular and configurable manipulation pipeline for pick and place tasks respectively. The overall EPD-EMD pipeline is shown in Figure 1.

![Figure 1. Overall EPD-EMD Pipeline](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626664365151-KYZS8DJ4397V8Q0YMWB8/pipeline.jpg)

*Figure 1. Overall EPD-EMD Pipeline*

The EPD ROS2 package helps accelerate the training and deployment of Computer Vision (CV) models for industrial use. The package provides a user-friendly graphical user interface (GUI) as shown in Figure 2 to reduce the time and knowledge barrier so even end-users with no prior experience in programming would be able to use the package too. It relies on open-standard ONNX AI models, hence eliminating the overreliance on any given ML library such as Tensorflow, PyTorch, or MXNet.

![Figure 2. Startup GUI of EPD](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626665878531-TF7NQTFTLSVP4CUR20SP/epdgui1.gif)

*Figure 2. Startup GUI of EPD*

EPD itself runs on a deep-learning model as a ROS2 interface engine and outputs object information such as the object name and location in a custom ROS2 message. This can be used for use cases such as object classification, localization, and tracking. To train a model for custom object detection, all a user needs to prepare are the following:

* .jpgs/.pngs Image Dataset of custom objects. (Approx. 30 images per object required)
* .txt Class Labels List

The expected output will be: 

* .onnx trained AI model

![Figure 3. EPD Training to Deployment Input &amp; Output](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626666877385-TT5TDKQEJ96SLNT02891/epdtrain_deploy.JPG)

*Figure 3. EPD Training to Deployment Input & Output*

To cater to the different use cases for different end-user's requirements, the package also allows for customizability in 3 different profiles.

• Profile 1 (P1) – fastest, but least accurate

• Profile 2 (P2) – mid-tier

• Profile 3 (P3) – slower, but most precise output

EPD caters to 5 common industrial tasks achievable via Computer Vision.

1. Classification (P1, P2, P3)
2. Counting (P2, P3)
3. Color-Matching (P2, P3)
4. Localization/Measurement (P3)
5. Localization/Measurement/Tracking (P3)

![Figure 4. An output of EPD at Profile 3, with OIbject Localization and operating at 2 FPS](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626667315727-BYKS8XTDHBE8XS0U86JD/epdoutput.gif)

*Figure 4. An output of EPD at Profile 3, with OIbject Localization and operating at 2 FPS*

The EMD ROS2 Package is a modular and easy to deploy ROS2 manipulation pipeline that integrates perception elements to establish an end-to-end industrial pick and place task. Overall, the pipeline comprises 3 main components in which are:

1. **Workcell Builder**

The Workcell builder as shown in Figure 5 essentially provides a user-friendly graphical user interface (GUI) to allow users to create a representation of their robot task space to provide a simulation of the same robot environment as well as the initial state for trajectory planning using motion planning frameworks like MoveIt2.

![Figure 5. Workcell Builder from EMD](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626668044484-AUIGAHZVJUS64YMA4T64/emdworkcell.png)

*Figure 5. Workcell Builder from EMD*

**2. Grasp Planner**

The Grasp Planner subscribes to a topic published by a given perception source and outputs a specific grasp pose for the end-effector using a novel, algorithmic depth-based method. The generated pose is then published as a ROS2 topic. As shown in Figure 7, The grasp planner currently supports and provides a 4 degree-of-freedom (DOF) pose for both multi-finger and suction array end effectors, apart from the traditional two-finger and single suction cup grippers.

![Figure 6. POINCLOUD TO GRASP POINT GENERATION](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626669342866-QSRRZVIRL5ZYWRZ45TU3/pclemd.png)

*Figure 6. POINCLOUD TO GRASP POINT GENERATION*

![Figure 6. Grasp Planner](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626668377652-OAKZ52PSI24W1SNWJ259/emdgraspplanner.png)

*Figure 6. Grasp Planner*

It aims to eliminate the pain points that users face when deploying machine learning-based grasp planners such as:

• Time Taken for Training & Tedious Dataset Acquisition and Labelling

Current datasets available such as the Cornell Grasping Dataset and Jacquard Grasping Dataset generally account for two-finger grippers and training on generic objects. For customized use cases, datasets need to be generated and labeled manually which requires a lot of time. Semantic description of multi-finger grippers and suction arrays may be hard to determine as well.

• Lack of On-The-Fly End Effector Switching

In a high mix, low volume pick-and-place task, different end effectors are required to be switched around to cater for the grasping of different types of objects. The changing of end efforts would translate for users to re-collect a new dataset, re-label and re-train the dataset and models before deploying them.

**3. Grasp Execution**

The Grasp Execution was developed to allow for a robust path planning process in navigating the robot to the target location for the grasping action. It serves as a simulator that uses path planners from the motion framework MoveIt2, as well as the output generated by the Grasp Planner. Figure 7 demonstrates that various items are picked successfully. 

![Figure 7. Grasp Execution on different objects using different end-effectors](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626671473782-P4V965LOI6DZYFHJ5APV/emdgrasp_blur.jpg)

*Figure 7. Grasp Execution on different objects using different end-effectors*

Overall, it benefits users by providing seamless integration with the grasp planner, as the grasp execution package communicates with the grasp planner through subscribing to a single ROS2 topic with the GraspTask.msg type. Apart from this, the grasp execution package also takes into account dynamic safety, which is important as collaborative robots often operate closely in a dynamic environment with human operators and other obstacles as well. 

![FIGURE 8. Improved grasp execution - dynamic safety architecture](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626669632554-GUDOTSDP7GFGPOX0XJBY/DYNAMICSAFETY.png)

Figure: *FIGURE 8. Improved grasp execution - dynamic safety architecture*

![FIGURE 9.  dynamic safety zones](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1626669649929-GPKQOF2RNPQ0KHDHWEYE/dynamicsafetyzones.JPG)

Figure: *FIGURE 9. dynamic safety zones*

There is a need for the robot to be equipped with such capabilities to address safety concerns and detect possible collisions in its trajectory execution to avoid any obstacles. Users are provided with a vision based dynamic collision avoidance capability through the use of Octomaps, whereby when a collision has been deemed to occur within the trajectory of the robot, the dynamic safety module will be triggered to either stop the robot or account for a dynamic replanning of its trajectory given the new obstacles within the environment.

Both of these packages have been formally released and open sourced on the ROS-Industrial github repository, and the team would also like to acknowledge the Singapore Government for their vision and support in funding this R&D project "Accelerating Open Source Technologies for Cross Domain Adoption through Robot Operating System (ROS), supported by the National Robotics Programme (NRP).


