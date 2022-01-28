---
author: Joseph Schornak (SwRI)
comments: false
date: '2019-05-13 19:26:11+00:00'
slug: 2019-5-10-field-notes-from-automate-2019-and-why-were-bullish-on-ros2
title: Field notes from Automate 2019, and why we're bullish on ROS2
media_type: None
description: What makes a good industrial automation demonstration? When we started
  preparing
layout: post
old_sp_link: https://rosindustrial.org/news/2019/5/10/field-notes-from-automate-2019-and-why-were-bullish-on-ros2
tags: automate ros2 ros-i ros-industrial ros-bridge yak path-planning ros
---

What makes a good industrial automation demonstration? When we started preparing
for Automate 2019 back in January, a few key points came to mind. Our specialty
in SwRI's Manufacturing and Robotics Technology Department is advanced robotic
perception and planning, so we decided that the robot should perform an
authentic dynamic scan-and-plan process on a previously-unseen scene – as far
away as we could get from a "canned" demo. We also wanted the demo to be an
interactive experience to help drive discussion with visitors and entertain
onlookers. These goals led us to the tube threading concept: a human would bend
a piece of shiny metal tubing into a novel shape, and the robot would perceive
it and plan a path to sweep a ring along it.

![Michael Ripperger &amp; Joseph Schornak on location at Automate 2019](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557775023839-60QKUT04W2R4904BVGL7/IMG_13221.jpg)

Figure: *Michael Ripperger & Joseph Schornak on location at Automate 2019*

Developing a demo system presents an opportunity to explore new ideas in a low-risk environment because the schedule and deliverables are primarily internally-motivated. Since my group had limited previous exposure to ROS2, we decided that our Automate demo should use ROS2 to the greatest possible extent. The original vision was that the system would be entirely composed of ROS2 nodes. However, due to the practical requirements of getting everything working before the ship date, we decided to use a joint ROS/ROS2 environment, with ROS motion planning and the GUI nodes communicating with the ROS2 perception nodes across the ROS-to-ROS2 bridge

**ROS2 Strengths and Challenges**

In contrast to virtually every other robotics project I've worked on, the demo system's perception pipeline worked consistently and reliably. Intel maintains a ROS2 driver for Realsense RGB-D cameras, which allowed us to use the D435 camera without any customization or extra development. Our [YAK surface reconstruction](https://www.swri.org/press-release/robotic-machine-vision-shiny-objects-ros2?utm_source=ROSblog-Automate2019&utm_medium=Blog&utm_campaign=Automate2019) library based on the Truncated Signed Distance Field algorithm helped us avoid the interreflection issues that would usually plague perception of shiny surfaces. After a couple afternoons spent learning how to use new-to-me VTK libraries, the mesh-to-waypoint postprocessor could consistently convert tube scans into trajectory waypoints. More information about this software is available from the SwRI [press release](https://www.swri.org/press-release/robotic-machine-vision-shiny-objects-ros2?utm_source=ROSblog-Automate2019&utm_medium=Blog&utm_campaign=Automate2019) or the writeup in [Manufacturing Automation](https://www.swri.org/press-release/robotic-machine-vision-shiny-objects-ros2?utm_source=ROSblog-Automate2019&utm_medium=Blog&utm_campaign=Automate2019).

![Block Diagram of SwRI ROS-I Automate 2019 Demonstration](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557845272979-FHZ77U5MH1Q0NZZW6AY9/Block+Diagram1.png)

Figure: *Block Diagram of SwRI ROS-I Automate 2019 Demonstration*

Motion planning turned out to be a particularly challenging problem. Compared to a traditional robot motion task like pick-and-place, which involves planning unconstrained paths through open space, the kinematic constraints of the tube threading problem are rather bizarre. While the ring tool is axially underconstrained and can be rotated freely to the most convenient orientation, it is critical that it remain aligned with the axis of the tube to avoid collision. It's impossible to flip the ring once it's over the tube, so if the chosen ring orientation causes the robot to encounter a joint limit halfway down the tube, tough luck! Additionally, the robot must avoid collision between the tube and robot hardware during motion. Our initial solution used [Trajopt](https://rosindustrial.org/news/2018/7/5/optimization-motion-planning-with-tesseract-and-trajopt-for-industrial-applications) by itself, but it would sometimes introduce unallowable joint flips since it tried to optimize every path waypoint at once without a globally-optimal perspective on how best to transition between those waypoints. We added the Descartes sampling algorithm, which addressed these issues by populating Trajopt's seed trajectory with an approximate globally-optimal path that satisfied these kinematic and collision constraints. Planning still failed occasionally: even with a kinematically-redundant Kuka iiwa7 arm, solving paths for certain tube configurations simply wasn't feasible[^1].

![TrajOpt Path Planning Implementation &amp; Testing](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557775197196-5W36X2P3AN4ZTU9RRR5R/Plan+Simulation+on+Noodle.gif)

Figure: *TrajOpt Path Planning Implementation & Testing*

[^1]: The extent of solvable tube configurations could be greatly increased by
including the turntable as a controllable motion axis. Given the constraints of
the iiwa7's ROS driver, we decided that this would be, in technical software
terms, a whole other can of worms.

We shipped the robot hardware about a week in advance of the exhibit setup
deadline. Our reliance on ROS meant we could switch to simulation with minimal
hassle, but there were some lingering issues with the controller-side software
that had to wait until we were reunited with the robot the Saturday before the
show[^2]. This contributed to moderate anxiety on Sunday evening as we worked to
debug the system using real-world data. We had to cut some fun peripherals due
to time constraints, such as the handheld ring wand that would let visitors race
the robot. By Tuesday morning the robot was running consistently, provided we
didn't ask it to solve paths for too-complicated tubes. This freed up some time
for me to walk the halls away from our booth and talk to other exhibitors and
visitors.

[^2]: Our lunch upon arrival was Chicago-style deep dish pizza, which
conveniently doubled as dinner that evening.

**More Collaborative Robots**

There were collaborative robots of all shapes and sizes on display from many
manufacturers. I may have seen nearly the same number of collaborative robots as
traditional ones! A handful were programmed to interact with visitors, offering
lanyards and other branded largesse to passersby. Most of them were doing
"normal robot things," albeit intermingled with crowds of visitors without any
cages of barriers, and generally at a much more sedate pace compared to the
traditional robots. Some of the non-collaborative robots were demonstrating
safety sensors that let them slow down and stop as visitors approached them -- I
usually discovered these by triggering them accidentally.

I was surprised by the number of autonomous forklifts and pallet transporters.
I'm told that there were more in 2019 than at previous shows, so I'm curious
about what recent developments drove growth in this space.

I learned that ROS-Industrial has significant brand recognition. I got pulled
into several conversations solely because I was wearing a ROS-I polo! Many of
these discussions turned to ROS2, which produced some interesting insights. Your
average roboticist-on-the-street is aware of ROS2 (no doubt having read about it
on this very blog), but their understanding of its capabilities and current
condition might be rather fuzzy. Many weren't sure how to describe the key
differences between ROS and ROS2, and a few weren't even aware that ROS2 has
been out in the wild for three versions! I'll unscientifically hypothesize that
a key challenge blocking wider ROS2 adoption is the lack of demonstrated success
on high-visibility projects. Our demo drove some good conversation to alleviate
these concerns: I could show a publicly-visible robotic system heavily reliant
on ROS2 and point to the open-source native ROS2 device drivers that let it
function.

**Showcasing Perception and Planning Potential**

In terms of demo reception, people who visited our booth were impressed that we
were scanning and running trajectories on previously-unseen parts. I usually had
to provide additional context to show how our perception and planning pipeline
could be extended to other kinds of industrial applications. There's a tricky
balance at play here – an overly abstract demo requires some imagination on the
part of the viewer to connect it to an industrial use case, but a highly
application-specific demo isn't easily generalized beyond the task at hand.
Since our group specializes in application-generic robot perception and
planning, I think that a demo tending towards the abstract better showcases our
areas of proficiency. This is a drastically different focus from other exhibits
at the show, which generally advertised a specific automation process or turnkey
product. I feel like we successfully reached our target audience of people with
difficult automation tasks not addressed by off-the-shelf solutions.

![Development of the Industrial YAK reconstruction for the Automate Demo in ROS2](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1557775537743-B0DTG114LYDFOTH7DOBA/20190405_131610.jpg)

Figure: *Development of the Industrial YAK reconstruction for the Automate Demo in ROS2*

While it certainly would have been easier to adapt an already-polished system to
serve as a show demo, developing a completely new one from scratch was way more
fun. Improvements made to our perception and planning software were pushed back
upstream and rolled into other ongoing projects. We're now much more comfortable
with ROS2, to the extent that we've decided that from here on out new robotics
projects will be developed using ROS2. The show was a lot of fun, a great time
was had by all, and I hope to see you at Automate 2021!


