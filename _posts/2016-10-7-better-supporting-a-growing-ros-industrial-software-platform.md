---
author: Guest User
comments: false
date: '2016-10-07 15:48:28+00:00'
slug: 2016-10-7-better-supporting-a-growing-ros-industrial-software-platform
title: Better supporting the growing ROS-Industrial software platform
media_type: None
description: As ROS-Industrial approaches its fifth anniversary, we wanted to share
  some reflections on how the initiative is evolving and on some adjustments ...
layout: post
old_sp_link: https://rosindustrial.org/news/2016/10/7/better-supporting-a-growing-ros-industrial-software-platform
---

As ROS-Industrial approaches its fifth anniversary, we wanted to share some reflections on how the initiative is evolving and on some adjustments in policy to maintain it on a healthy, sustainable growth path.

The first demo showcasing the advantages of ROS on industrial hardware, [a pick-and-place application performed on a Motoman SIA10D](https://www.youtube.com/watch?v=qd76wAywZos), was developed in the [fall of 2011](http://www.ros.org/news/2011/09/swri-and-yaskawa-team-up-to-use-ros-with-motoman.html) by Shaun Edwards. From this early effort we have come a long way both in terms of Consortia and Community building and of further development of the software platform. With the recent addition of the Asia Pacific region we now have more than 40 organizations supporting the ROS-Industrial Consortia worldwide. On the software side, ROS-Industrial is growing in terms of more supported hardware and of more, and more advanced, capabilities that it offers to industrial users.

In parallel to the effort of expanding the Consortia and to keep the "voice of business" in the loop, the software development community is growing under the technical leadership of Shaun Edwards and Gijs van der Hoorn. We have been hosting online developer meetings since last fall: now held monthly, they provide a venue for contributors to become more involved with the rest of the community and eventually join it on a stable basis. In addition to growing the codebase, we are gradually enforcing best practices in the development process to ensure a better overall software quality. These include an improved review process for PRs; unit and system test coverage; continuous integration tests.

While the expansion of the development community brings on-board very welcome contributors, the commitment required to maintain and support a fast expanding software platform is calling for a more structured approach than we had so far. This in order for us to be able to more effectively and more fairly commit development resources, and for our users to get a better understanding of the support level that they can expect.

A more effective and fair allocation of resources means standing behind the code which supports the activities of Consortia members. These are the organizations making the initiative possible, as they provide financial support and public advocacy for the adoption of open-source software in industrial robotics. A better understanding of support level means helping our users to set their expectations to an appropriate level when evaluating the adoption of specific packages. For instance, a manufacturer actively supporting the driver for its equipment, directly or through its regional ROS-Industrial Consortium, makes for a much different situation than having to rely solely on community support. 

As a first step towards this direction, we announce the following levels of support for packages in the ros-industrial github organization:

* consortium / vendor: for packages supporting the activities of a Consortium member, which ideally also contributes with in-house technical support (e.g., robot drivers); for core ROS-I packages developed and maintained by the technical leads;
* vendor: for packages directly supported by the vendor's technical staff;
* community: support is community-based, and as such it is best-effort and based upon the work of volunteers.

![support badges for ROS-I packages](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1475856061379-F1U6LQ7WKJYW6X143EP4/badges.png)

Figure: *support badges for ROS-I packages*

We are currently rolling out this scheme by gradually assigning "badges" corresponding to the appropriate support level to the various ROS-Industrial packages. We also want to provide soon users with means to "ping the OEM" behind a specific piece of hardware which is currently at community-level support, and we are currently looking for the most effective means to do so.


