---
author: Josh Langs (SwRI)
comments: false
date: '2020-09-11 18:58:42+00:00'
slug: 2020-9-11-ros-industrial-training-focused-on-ros2-and-virtual-in-the-americas
title: First Virtual ROS-Industrial Training focused on ROS2 in the Americas
media_type: None
description: SwRI recently hosted a training session for ROS-Industrial Americas consortium
  members, led by instructors Josh Langsfeld, David Merz, and Randall ...
layout: post
old_sp_link: https://rosindustrial.org/news/2020/9/11/ros-industrial-training-focused-on-ros2-and-virtual-in-the-americas
---

SwRI recently hosted a training session for ROS-Industrial Americas consortium members, led by instructors Josh Langsfeld, David Merz, and Randall Kliman. As it was held in the middle of the COVID19 pandemic, the traditional in-person format was replaced with a brand new virtual training method, using videoconferencing and virtual machines running in the cloud instead of students' own laptops. The overall schedule was similar to previous training sessions, with two days focused on exercises designed to teach the basics of ROS and ROS-Industrial, followed by a more free-form lab day where the students could work on longer exercise. The class was held in a Zoom meeting that ran all day long, enabling easy interaction between the instructors and students during both the presentation and the exercise times.

![Training live on the Zoom feed, while development exercises took place on AWS EC2](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1599850685662-JV2FPSC5F8DSGIGHRICS/training.jpg)

Figure: *Training live on the Zoom feed, while development exercises took place on AWS EC2*

To provide students with an Ubuntu environment, we opted for a new approach where we set up virtual machines using Amazon's Elastic Compute Cloud (EC2) service and asked the students to log in using a remote desktop protocol. We were pleased to work with Amazon in setting up this arrangement and they helped by preparing an Ubuntu 18.04 base image with ROS Melodic preinstalled. This let us start up a whole set of virtual machine instances, one for each student, ready to go for training. These instances were made accessible to the public internet and so all students were able to directly log in using only an IP address and a provided key file. This approach turned out to be quite robust and no one had any issues accessing the cloud instances. The use of EC2 virtual machines also enabled easy instructor-student interactions, as the instructors could also log into the same instances and see exactly what the student was seeing. We used this to great effect along with Zoom breakout rooms to engage in one-on-one troubleshooting with the students, both guiding the students with next steps to take and even controlling their machine to help with more complicated problems. Overall, the virtual training experience was quite smooth and it is likely we will keep it as an option going forward, even when in-person trainings are able to resume.

And if attempting virtual training for the first time was not enough, this training also marked a milestone in the ongoing adoption of ROS2, as the basic material and exercises taught on the first day were updated to use ROS2, without assuming prior knowledge of ROS1. This first day covers the fundamental concepts of ROS packages, messages, topics, services, and parameters, all of which are fully functional and easily demonstrated in ROS2. As ROS-Industrial is in the middle of the transition, however, the full training is not yet available in ROS2. Instead, the second day, which teaches the basic concepts specific to ROS-Industrial, including URDFs, TF, and motion planning with MoveIt were done in ROS1. We expect this transition to continue and soon all of this material will be available in ROS2 as well, especially now that MoveIt2 is out and ready for use. Check back on the training website over the next few months to keep an eye out for the updates! We'll be looking forward to additional training sessions and expanding what we can do with both ROS2 and the virtual training format.


