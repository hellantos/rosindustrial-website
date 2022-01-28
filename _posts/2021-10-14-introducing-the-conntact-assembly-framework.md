---
author: John Bonnin (SwRI)
comments: false
date: '2021-10-19 16:32:17+00:00'
slug: 2021-10-14-introducing-the-conntact-assembly-framework
title: Introducing the ConnTact Assembly Framework
media_type: None
description: This is a cross-post hosted over at the AI for Manufacturing Robotics
  Blog hosted by NIST as part of their initiative to set up a community hub ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/10/14/introducing-the-conntact-assembly-framework
---

*This is a cross-post hosted over at the AI for Manufacturing Robotics Blog hosted by NIST as part of their initiative to set up a community hub for researchers and practitioners of AI for Manufacturing Robotics, who are interested in staying current on research trends or finding new projects and collaboration opportunities. You can learn more about this initiative and other activities about AI for Manufacturing Robotics at:* <https://sites.google.com/view/ai4manufacturingrobotics/>

**The Challenge of Assembly**

When assembling precision-tolerance parts, humans have an ideal set of capabilities. Combining geometrical understanding, visual guidance, tactile confirmation, and compliant force/torque (F/T) control, it is possible for a human to quickly assemble components despite micrometer tolerances. We take this remarkable suite of abilities for granted. To prove it, just recall that the number-one cliché child's toy is all about fitting blocks through matching holes in a box. Our babies can do assembly tasks with ease.

Now, the moment you consider handing the child's block off to a modern industrial robot, you start to encounter some of a robot's greatest disadvantages. A robot is, by design, a highly rigid precision machine. The robot must be fed very precise information about the orientation and position of the goal - the box in this case - and it cannot correct mid-action to comply as nearly-aligned pieces try to slide into place. If provided erroneous measurements - even ones that are just a few millimeters off - it will quite simply crush the box, the block, and possibly itself. Rigidity is inherently a difficult obstacle to performing mechanical assembly when high-accuracy measurement and fixturing are impractical.

![ConnTact guiding a UR10e robot through an assembly algorithm. The system can successfully insert a peg into the NIST taskboard despite up to 1cm error in position instructions](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1634240052642-O7RXRWJ2UUJUY23NQAJ6/peg+insertion-reduced.gif)

Figure: **ConnTact guiding a UR10e robot through an assembly algorithm. The system can successfully insert a peg into the NIST taskboard despite up to 1cm error in position instructions**

**Compliant Control**

Despite these difficulties, a respected method has been developed for robots to imitate human flexibility and responsiveness, called compliant feedback control. By rapidly controlling the motion of the robot in response to 6DOF F/T information, a robot can imitate the soft compliant behavior of a human grip. This can be achieved with any modern robot using an after-market 6-axis load cell mounted between the tool flange and the gripper.

This feedback enables detection of F/T "wrenches" acting on the gripper, so the control system can smoothly move to comply. Pressing on the front of the gripper makes the robot retract. Twisting the gripper makes the robot turn. The robot very convincingly pretends to be much less rigid. When displaced, it applies a constant gentle force toward its desired goal position and patiently waits until permitted to reach it.

This permits the use of tactile methods of operation - the use of touch to sense the environment and make decisions. The system can correlate data about reaction forces, robot position, and robot velocity to detect the collision mode which best describes the interaction of the robot and the environment. For instance, collision with a flat surface may be identified by sharp resistance in one direction but negligible friction in other directions. The alignment of a cylindrical peg with a receptacle may be detected by resistance in all directions except one, the vector parallel with the receptacle axis. By characterizing these interactions, a reliable understanding of the contact state between the robot and workpiece can be formed.

Researchers have been experimenting with and implementing compliant assembly systems for years. The Kuka iiwa comes pre-installed with certain compliant features built in. Other companies such as Franka Emika have designed robots specifically to achieve high performance in feedback-based assembly. And on the software side, open-source libraries exist which can control hardware through high-level position or velocity interfaces. In particular, our work makes extensive use of the cartesian\_controllers libraries, developed at the FZI Research Center for Information Technology.

![Compliance example: the robot is configured to respond to forces and torques applied to the gripper. After the disturbance ends, it returns to its assigned task.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1634240147097-PCF73C1XOPGZDRZZSOC4/Distrurbancerecovery+reduced.gif)

Figure: **Compliance example: the robot is configured to respond to forces and torques applied to the gripper. After the disturbance ends, it returns to its assigned task.**

**The ConnTact Framework**

NIST hopes to expand the realm of assembly research to smaller developers with less abundant resources and permit a much more agile workflow. To that end, NIST is collaborating with SwRI to develop an open-source framework for compliant assembly tasks, called ConnTact. This framework is meant to provide tools which create a bridge directly from hardware configuration to the real algorithmic development required to accomplish difficult tasks. It also standardizes interfaces to permit the community to share solutions and re-implement them with new hardware for new applications. The framework takes in information about the robot and task location and provides an environment where the user can easily develop tactile algorithms. The overall goal is to significantly ease the load on an end-user who wants to develop a new assembly applications anywhere on the spectrum from straighforward repeatable tasks to complex problems that leverage AI and reinforcement learning methods.

The key to this framework is the simplification of interfaces. This permits any robot with force sensing and compliance control features to be used with any algorithm. To configure for a given robot, a developer must feed live force, torque, and position data into the Assembly Tools package. In addition, for each task, the task frame, or approximate location and rotation of the task relative to the robot, must be imported. With this basic input, the package provides a development framework with 3 major features: Generalization, Visualization, and Modularity.

![The user provides a set of "user configuration" information and connects their preferred robot to the input/output interface. ConnTact then processes this configuration and runs the user's algorithm as configured, providing rich visual/logging feedback.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1634241673318-VHPC6RPOMATBV9VEVFQT/ConnTact+Framework+Diagram.png)

Figure: **The user provides a set of "user configuration" information and connects their preferred robot to the input/output interface. ConnTact then processes this configuration and runs the user's algorithm as configured, providing rich visual/logging feedback.**

**Main Features**

Generalization: The framework seeks to generalize algorithms to any location or task. This is accomplished by transforming all inputs - robot pose, force, and torque inputs - into task space, that is, it converts all spatial measurements to be relative to the task frame. For example, in the case of an Ethernet connector insertion task, given the location of the Ethernet socket relative to the robot, the development environment would provide position data to the algorithm relative to the socket. A command to move the plug to position (x,y,z) = (0,0,0.05) would place the Ethernet plug 5cm from the socket. A force of (0,0,10) always indicates that the gripper is experiencing a force away from the socket and parallel to its axis, even if the socket were upside-down on the underside of a workpiece. This allows the user to focus their efforts on algorithm development with the confidence that their work is applicable to any task location or orientation.

Visualization: The framework provides visualization options using Python plotting libraries familiar to any modern programmer. Input position and forces are mathematically processed to provide reliable speed, force, torque, and position data streams which are easily displayed at runtime. This built-in visualization is meant to equip every program with a greater degree of transparency.

Modularity: Finally, we facilitate modular algorithm development with a state machine-based control loop. The example implementation specifies a finite number of states and provides the conditions needed to transition between them. The user can reuse existing algorithmic motion routines from the open-source repository to rapidly produce useful programs. They can also develop their own algorithm modules and easily add them to existing program structures.

Some sample algorithm modules currently included:

* Moving in a linear direction until a flat surface is detected.
* Searching in a spiral pattern across a surface for a low spot, such as a connector falling a short way into its socket.
* Moving compliantly in a specified direction until colliding with a rigid obstacle.
* Probing in different directions to determine rigid constraint locations.

![Left: Top-down/side-on motion and force readings are displayed live.Right: The robot streams data to RViz (a ROS-specific model suite) to show live pose and live F/T vectors.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1634241730187-JJBTYH18S1ZTROIHR0RK/logging+reduced.gif)

Figure: **Left: Top-down/side-on motion and force readings are displayed live.*

*Right: The robot streams data to RViz (a ROS-specific model suite) to show live pose and live F/T vectors.**

**Code Release**

The basic WIP framework is being made available publicly now at <https://github.com/swri-robotics/ConnTact>, and work will proceed over the coming months to add features and documentation. NIST and SwRI welcome any feedback to improve the framework. We aim to make a simple, straightforward, and powerful system to bring agile compliant robotic assembly to a wider developer community and bring tactile robot sensing to the forefront.


