---
author: Guest User
comments: false
date: '2014-04-01 23:36:26+00:00'
slug: 2014-4-1-a-universal-pendant-could-elucidate-the-interface-to-industrial-robot-manipulators
title: A Universal Pendant Could Elucidate the Interface to Industrial Robot Manipulators
media_type: None
description: A guest post by Dr. Mitch Pryor, [UT Austin Nuclear and Applied Robotics
  Group](http://robotics.me.utexas.edu/)
layout: post
old_sp_link: https://rosindustrial.org/news/2014/4/1/a-universal-pendant-could-elucidate-the-interface-to-industrial-robot-manipulators
tags: ros ros-i ros-industrial ros-i-consortium mitch-pryor ut-austin-nrg ut-austin-nuclear-and-applied-robotics-lab
---

A guest post by Dr. Mitch Pryor, [UT Austin Nuclear and Applied Robotics Group](http://robotics.me.utexas.edu/)

The ROS-Industrial Consortium Americas held its 2014 members meeting at SwRI in San Antonio, Texas on March 6th. One of the primary activities of the Consortium is to establish the technical vision and requirements for ROS-Industrial. This is done through a series of requirements gathering and analysis activities known as roadmapping. This blog provides a useful forum for sharing ideas on the proposed ROS-I roadmap and gives members a chance to succinctly present thoughts on particular topics and receive feedback from all stake holders via constructive comments. The [roadmap development approach](http://prod.sandia.gov/techlib/access-control.cgi/1997/970665.pdf) presented by Clay Flannigan (and [Steve Jobs](https://www.youtube.com/watch?v=1SIeTmORl0E)) starts with the end-user's needs (i.e. applications). Once identified, as many were at the ROS-I spring meeting, the roadmap then pinpoints the technical gaps and puts forward an implementation plan to develop the envisioned technologies.

I want to start a discussion on what "commands" hardware must reliably execute to follow the desired trajectories and/or apply proscribed forces for a given application. In the traditional paradigm, such commands are communicated via a *teach pendant* or *offline programming*.

A teach pendant is a handheld controller that provides the primary conduit for moving the robot and recording the position locations. Traditionally, it is used to sequentially teach the EEF locations associated with a given task. This instruction method is insufficient for ROS-I to extend the **advanced** (i.e. advancing the autonomy or flexibility of a system) capabilities of ROS to **new** industrial applications.Offline programming offers more flexibility but there is no standard language or set of capabilities offered among hardware vendors. What is needed is a**universal Application Program Interface (or universal API)**with as much of the functionality as possible accessible via a**Universal Pendant.**

![Traditional Dedicated Industrial Robot Teach Pendant. Source: SwRI 2011](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1396394069065-LK21UIYTXA7369C3ZFFN/Pendant.png)

Figure: *Traditional Dedicated Industrial Robot Teach Pendant. Source: SwRI 2011*

[![Mobile HMI: Notional Universal (i.e. interoperable) Pendant. Source link.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1396394187210-0710UHBQNRWLKVVHVVMG/MobileHMI.jpg)](http://www.automation.siemens.com/mcms/human-machine-interface/en/operator-interfaces/mobile-panel/series-270/simatic-mobile-panel-277-iwlan/pages/default.aspx)
Figure: *Mobile HMI: Notional Universal (i.e. interoperable) Pendant. Source [link](http://www.automation.siemens.com/mcms/human-machine-interface/en/operator-interfaces/mobile-panel/series-270/simatic-mobile-panel-277-iwlan/pages/default.aspx).*

The notion of a universal pendant is not new. Toyota developed an internal [unified teach pendant](http://www.toyota-global.com/company/history_of_toyota/75years/data/automotive_business/production/production_engineering/vehicles/welding/index.html) in 2000. Its development did more than reduce the training time for Toyota operators, it helped Toyota define the underlying capabilities that robotic vendors must provide. The Toyota unified pendant currently does not provide access to all of the capabilities envisioned by ROS-I members. If the ROS-I Consortium was to develop a similar, but more advanced device, it would help clarify and illustrate many of the API capabilities that are needed by industry. Its development would help clarify API ambiguities and hopefully reduce the barrier to entry to much of the API functionality in an industrial setting.

What would such a teach pendant look like? What core functionality should it have? As developers, the second question is more important to answer. It certainly must provide access to the internal state of the robot (i.e. tool location, current position, current motor currents, operational status, etc.) It should be possible to modify individual joint positions as well as command joint velocities. Many advanced technologies would require access to joint torques and/or joint currents. Another useful feature would be to directly prompt a given robotic system for its mass, inertial and/or compliance parameters that are necessary in many advanced control algorithms. Remote systems should provide battery life information which is necessary to plan extended tasks. Another interesting option would be access to any internal, extensible wiring harness. One could even envision a universal messaging service for commanding hardware via existing proprietary languages. As the ROS-I Consortium develops new capabilities, such a service may become obsolete, but the universal API should not negate existing system capabilities.

Once the API is defined, it may not be possible to expose all functionality in a traditional pendant. Innovative ideas may be necessary if the full API is to be exposed. Even then certain functionality may still require writing code. The definition and scope of such an API is not trivial. All parties (end-users, integrators, vendors, researchers, etc.) need to assist in its creation. Once developed, hardware vendors must have the right to only partially implement the proposed functionality. But **our goal must be to develop an API that enables all the technologies proposed in the roadmap** and make as much of the API as possible accessible to traditional (i.e. no command line!) end-users. A universal pendant would help address this and provide a mechanism for precisely illustrating and resolving ambiguities in the proposed API.


