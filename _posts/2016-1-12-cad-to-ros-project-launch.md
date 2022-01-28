---
author: Guest User
comments: false
date: '2016-01-14 00:32:51+00:00'
slug: 2016-1-12-cad-to-ros-project-launch
title: CAD to ROS Project Launch
media_type: None
description: A longstanding need, which will improve the efficiency of
layout: post
old_sp_link: https://rosindustrial.org/news/2016/1/12/cad-to-ros-project-launch
---

A longstanding need, which will improve the efficiency of
setting up a ROS project, is the ability to import model and
process data from various CAD systems. In collaboration with
TU Delft last year, we proposed a ROS-I Consortium Focused Technical Project to develop a CAD data importer for ROS that could automatically convert from common CAD files to URDFs and SRDFs. While the initiative was met with great interest, the lengthy duration and fixed-price
milestone contract arrangement were not sufficiently attractive
to garner the investment required to launch the
project. However, a strong showing by the developer community
led us to believe that much of the software development
work would be contributed by collaborating consortium members,
if technical leadership was provided to guide and curate the
development. Furthermore, we wished to expand the future
vision of CAD to ROS by building it into a 3D workbench
framework. This will provide a common user experience for
importing and configuring sensors, Cartesian process plans,
motion plans, and point cloud data in the future.
To assure incremental progress, we restructured the CAD
to ROS project, reorganizing it into five milestones, each
approximately four months:

1. URDF GUI Editor
2. Process Planning
3. Work Cell Planning
4. Sensor Configuration and Calibration Setup
5. 3D Point Cloud Importer

We also restructured the business model. There are now four
types of contributors to the project:

* **Technical Overseer:** TU Delft will set the software
architecture design goals and will review pull requests from
developers.
* **Sponsor:** In December 2015, one of the ROS-I Consortium members pledged their support for TU Delft's efforts.
* **Developers:** In exchange for helping to write the code,
Consortium members will have access to the private project repository.
* **Consortium Administrator:** SwRI and Fraunhofer IPA will
recruit developers from amongst the Consortium membership to help with coding.

For this particular Consortium project, we are implementing a business model in which only contributors from the Consortium have access to the URDF editor tool. This is an opportunity to see how productive the community can be when motivated by a little self-interest.

We need the help of ROS-I Consortium member software developers! Please contact paul.hvass@swri.org, or mirko.bordignon@ipa.fraunhofer.de to gain access to the project and to help complete Milestone 1!

![CAD to ROS Milestone 1: URDF Editor. Thanks to Levi Armstrong from SwRI for contributing his QT GUI as a head start for the project!](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1452719059476-4LJCLC5BNYBZ94XGTCSC/ROS_URDF_Editor)

Figure: *CAD to ROS Milestone 1: URDF Editor. Thanks to Levi Armstrong from SwRI for contributing his QT GUI as a head start for the project!*


