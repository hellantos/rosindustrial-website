---
author: Guest User
comments: false
date: '2018-01-08 13:00:30+00:00'
slug: 2018-1-8-announcing-ros
title: Announcing ROS#
media_type: None
description: This is a guest blog post by Martin Bischoff on behalf of his employer
  Siemens AG. Thanks to Martin for the update, and to Siemens for its ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/1/8/announcing-ros
---

This is a guest blog post by Martin Bischoff on behalf of his employer Siemens AG. Thanks to Martin for the update, and to Siemens for its generous support to the ROS-Industrial Consortium!

---

We are happy to announce that we published ROS# on [github.com/siemens/ros-sharp](https://github.com/siemens/ros-sharp)!

![RosSharpLogo.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1515408827633-HXS6EXY148JKRLNPEB39/RosSharpLogo.png)

...is a set of software libraries and tools in C# for communicating with [ROS](http://www.ros.org) from .NET applications, in particular [Unity](http://unity3d.com).

ROS# consists of:
-----------------

* [RosBridgeClient](https://github.com/siemens/ros-sharp/tree/master/RosBridgeClient), a .NET API to ROS using rosbridge\_suite on the ROS side.
* [UrdfImporter](https://github.com/siemens/ros-sharp/tree/master/UrdfImporter), a URDF file parser for .NET applications.
* [RosSharp.unitypackage](https://github.com/siemens/ros-sharp/tree/master/Release), a Unity Asset package providing Unity-specific extensions to RosBridgeClient and UrdfImporter.

ROS# helps you to:
------------------

* **Communicate** with ROS from within your Windows app: subscribe and publish topics, call and advertize services, set and get parameters and use all features provided by rosbridge\_suite.

![CodeExample.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1515407820408-PVB1626LQFY60XTFJEVI/CodeExample.png)

* **Import** your robot's URDF model as a Gameobject in Unity3D. Import the data either directly from the ROS system using the robot\_description service or via a URDF file that you copied into your Unity Asset folder.

(click on the images for videos)

[![UrdfImport.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1515407895863-R4Q5PJTSFPPP3W5KD9GQ/UrdfImport.png)](https://youtu.be/EhSbufLlvvc)

* **Control** your real Robot via Unity3D.

[![Teleoperation.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1515408194648-0PI48UU6EUI1FWKHR0FM/Teleoperation.png)](https://youtu.be/OytzagQirrk)

* **Visualize** your Robot's actual state and sensor Data in Unity3D.

[![RVizUnity.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1515408350962-3SABOJSOCJ2FWG77MVS6/RVizUnity.png)](https://youtu.be/wo3hwsPFEPY)

* **Simulate** your robot in Unity3D with the data provided by the URDF and without using a connection to ROS. Beside visual components as meshes and textures, also Joint parameters and masses, CoMs, Inertia and Collider specifications of Rigidbodies are imported.

[![Simulation.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1515408477214-UKTEXLCRN1U6GG1DJVQ5/Simulation.png)](https://youtu.be/cjp75A_HBSs)

* **And much more!** ROS# is useful for a wide variety of applications. Think about Machine Learning, Human-Machine Interaction, Tele-Engineering, Virtual Prototyping, Robot Fleet Operation, Gaming and Entertainment!

Got Interested?
---------------

Please do not hesitate to try it out yourself and to get in touch with us! We are very interested in your feedback, applications, improvement suggestions, and contributions!

ROS# Development Team ([ros-sharp.ct@siemens.com](mailto:ros-sharp.ct@siemens.com)), Siemens AG, Corporate Technology, 2017


