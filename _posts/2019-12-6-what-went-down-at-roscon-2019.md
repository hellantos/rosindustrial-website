---
author: Matt Robinson (SwRI)
comments: false
date: '2019-12-06 14:08:16+00:00'
slug: 2019-12-6-what-went-down-at-roscon-2019
title: What Went Down at ROSCon 2019
media_type: None
description: ROS-Industrial representatives from the three global regions attended
  and
layout: post
old_sp_link: https://rosindustrial.org/news/2019/12/6/what-went-down-at-roscon-2019
---

ROS-Industrial representatives from the three global regions attended and
presented at ROSCon Macau 2019, held from Oct. 31 to Nov 1.

The booth was supported by all the three consortia from Asia Pacific, Americas
and Europe. Some initial changes were the introduction of workshops ahead of the
formal agenda, including a very good workshop on "Day 0" on the ecosystem (ROS
is getting bigger and bigger, how do we get those people more into an active
role?).

This year, the ROS-Industrial team presented the demonstration titled *"Robotic
Pick & Place with Augmented Reality"* which was made to showcase the
interoperability of ROS by allowing robots to perform tasks by learning from an
operator input using an intuitive augmented reality interface – removing the
need for programming of robots.

As far as exhibitors along with ROS-I, it was noticed that there was a
noticeable increase in exhibitors (~40) with more companies
attending/supporting ROSCon, so this speaks to the growth and evolution of the
community and for the event itself.

Obvious recruitment, seeking of ROS-skilled professionals, part of "we are
hiring", even more so than in past years. While another hot topic, or maybe the
red ribbon of the event, was "we need more and complete documentation of ROS2."

As such with such full in content events, or how long the coffee breaks, they
are never sufficient to meet and greet everybody.

![IMG-20191030-WA0063.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1575640145526-DVCMJYLV2KLCOC3LJDTP/IMG-20191030-WA0063.jpg)

*Photo : Ng Wei Kien & Dejanira Araiza at the ROS-Industrial Booth showcasing
the demo.*

The ROS-I teams were selected and gave three talks:

Levi Armstrong and Chris Lewis presented on *"Industrial Manufacturing
Automation Leveraging ROS"* and Dejanira Araiza-Illan on the topic *"PackML2:
State Machine Based System Programming, Monitoring and Control in ROS2"* with
Michael Ripperger presenting on *"Flexible Framework for Quantitative
Reachability Analysis."*

![IMG-20191031-WA0000.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1575640242668-R2LYTO30HEOUPQEREO33/IMG-20191031-WA0000.jpg)

*Photo : Levi Armstrong, ROS-I Americas/SwRI presenting Industrial Manufacturing Automation Leveraging ROS .*

There was also one of the major keynote presentations on the Robotics Middleware Framework (RMF) about roadmap to adopt robotic solutions and smart systems in Singapore's public healthcare sectors.

A brief summary of presentations that stood out to the teams present:

* ROS Real Time Workshop
	+ Both hardware and software requirements
		- Real-time kernel, messaging, etc.
	+ Lots of effort required to setup/run real-time Linux kernel
	+ Security and real-time conflict of interest?
	+ Timing and determinism
		- TCP/IP can meet determinism
		- UDP can meet timing
		- Neither meet both
	+ Large effort by various companies to benchmark timing, processing speed, memory usage, latency, etc. of ROS2 with various DDS implementations
	+ Very important for mobile robotics and autonomous applications
	+ Benefits of this effort will likely be available by the time most industrial manipulation applications we work on care about this functionality
* ROS2 on VxWorks
	+ ROS2 dependencies installed
	+ Run ROS2 on an RTOS
* ROS2 migration of Navigation Stack
	+ Re-design of the architecture to leverage ROS2 features
		- Component and life-cycle nodes
	+ Run-time definable behavior trees for decision-making in fault scenario
* Reactive programming
	+ Paradigm for handling asynchronous data streams
	+ RxROS (ROSin funded): *<https://github.com/rosin-project/rxros>*
* ROS in Jupyter Notebook
	+ Essentially an online IDE that can compile and run code
	+ Alternative for industrial training (Python)
	+ C++ support?
* High Assurance ROS
	+ Static analysis for ROS system
	+ Looks at unconnected topics, etc.
	+ *<https://github.com/git-afsantos/haros>*
* Reactive Jogger
	+ UT Austin Robotics Lab
	+ Teleoperation robot jogger with singularity avoidance, signal filtering, reactive control
* Cartesian Controllers
	+ Cartesian motion, compliance and force controllers
	+ Position and velocity control
	+ \_<https://github.com/fzi-forschungszentrum-informatik/cartesian_controllers>\_
* OMPL constrained planning
	+ Requires equality constraint function and gradient
	+ Performs search on constraint manifold instead of full configuration space
	+ <https://ompl.kavrakilab.org/constrainedPlanning.html>
* MoveIt Task Constructor
	+ Framework for defining tasks with multiple valid success paths
	+ \_<https://github.com/ros-planning/moveit_task_constructor>\_
* Pilz Industrial Motion Control
	+ Deterministic motion planners for industrial move types (MoveL, MoveJ, MoveC)
	+ Include blending parameters

![20191102_115204.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1575641073347-KNH4CI0US7XIQBM26P4Y/20191102_115204.jpg)

*Photo : Michael Ripperger, ROS-I Americas/SwRI, presents processes planning framework at the MoveIt Workshop.*

Things to take away…

* High level observations:
	+ Majority of attendance/presentations related to mobile robots in logistics space and autonomous driving
	+ Lots of people care about real-time capability
	+ Lots of people diving deep into the RMW and DDS layers to fix bugs and improve performance
	+ Lots of people care about scaling robot operations
		- Discussion around how ROS fits into fleet deployment framework
		- System of systems architecture approach
	+ Not much about manipulation
		- One half of one day
		- Not a lot of manufacturing-centric content outside of ROS-I

* Interesting Information
	+ TRAC\_IK has mutliple objectives for driving gradient
		- Speed: default (joint speed?)
		- Distance: minimizes joint distance from seed
			* Should probably be preferred to minimize configuration changes
		- Manipulability
	+ BioIK
		- <https://github.com/TAMS-Group/bio_ik>
	+ ROS2 Life-cycle nodes
		- State-machine for nodes
	+ ROS2 component nodes
		- Similar to nodelets
		- Can share memory with other component nodes in the same container
	+ Use MoveIt planning objects in favor of the MoveGroup
	+ Microsoft is releasing HoloLens v2.0 that are "industrial grade"

Thoughts relative to ROS-I...

* We should become more familiar with ros\_control capability
	+ Trajectory replacement
	+ Cartesian and force control capability
	+ Create some compelling demos
	+ Real-time interaction with external devices
* We need to be more active/supportive of core ROS repositories
* Creation of ROS Calibration GitHub organization
	+ We should move our calibration libraries here to make them more discoverable
	+ We can still brand them thoroughly as ROS-I developed

Finally, it is clear that ROS2 development, including for navigation, and optimization of the DDS/transport layer and discussion of real-time capabilities are making great progress. However, there are challenges, particularly related to areas that ROS-I seeks to address. Capabilities for manipulation/path planning for manipulators, documentation, and significant progress on ease of use, to enable manufacturing-centric organizations to really jump in. In the interim there is enough tech industry engagement to fill the void, to provide additional tools and offer solutions to meet industry needs. Now is the time to create compelling ROS2 demonstrations/reference applications that drive further end-user engagement. ROSCon always lights a fire of inspiration, now to just set to the work of getting that fire to spread. Looking forward to 2020!

Content provided by Sheila Suppiah, ROS-I AP, Thilo Zimmerman, ROS-I EU, and Michael Ripperger, ROS-I Americas.


