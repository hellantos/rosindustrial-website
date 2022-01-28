---
author: Guest User
comments: false
date: '2016-07-29 22:16:39+00:00'
slug: 2016-7-29-packml-initiative-for-ros-i
title: PackML Initiative for ROS-I
media_type: None
description: 'Submitted by: Lex Tinker-Sackett, Mfg Technology Specialist, 3M'
layout: post
old_sp_link: https://rosindustrial.org/news/2016/7/29/packml-initiative-for-ros-i
---

Submitted by: Lex Tinker-Sackett, Mfg Technology Specialist, 3M

![PackML State Model (from the PackML Implementation Guide)](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1469829875799-H96CGQOTDX852Z01N2V8/image-asset.jpeg)

Figure: *PackML State Model (from the PackML Implementation Guide)*

ROS-Industrial is a foundational technology abstracting robot applications for industry. ROS-I runs on PC hardware (currently Linux based), which makes complete sense to the roboticist. To the manufacturing plant, however, the automation systems tend toward Programmable Logic Controller (PLC) hardware. Rockwell, Siemens, Mitsubishi and many other industrial vendors supply PLCs to factories all over the world. One challenge with PLC automation is developing complex manufacturing solutions for multiple vendors.

Bringing together hardware from multiple vendors using different technologies (heterogeneous machines) with a standard programming paradigm would simplify the problem. Fortunately, the ISA-88 standard includes a subset called PackML, which provides PLC programmers with a state machine (see Figure above) and messaging protocol that allows disparate machines to work together. As more and more robots are integrated into manufacturing environments, it makes sense to extend the PackML standard into the ROS-I world. 

ROS-I and PackML are a natural fit for each other. Both create a new way to solve old problems. Under the ROS-I Consortium, a group is forming to create an open source C++ library (think Boost) to implement the PackML state machine abstraction for use in ROS-I. Integration of robots into complex manufacturing environments will be made simpler with the new ROS-I/PackML library.

To join future discussions about the PackML project for ROS-I, please email the ROS-I developer email list with your interest: swri-ros-pkg-dev [at sign] googlegroups.com

Not already subscribed to the list? [Please use this link to subscribe.](https://groups.google.com/forum/?fromgroups#!forum/swri-ros-pkg-dev)


