---
author: Matt Robinson (SwRI)
comments: false
date: '2018-03-12 16:31:25+00:00'
slug: 2018-3-12-human-performance-researchers-pair-ros-i-with-markerless-mocap
title: Human Performance Researchers Pair ROS-I with Markerless Mocap
media_type: None
description: The ROS-Industrial team recently collaborated with Southwest Research
  Institute's Human Performance Initiative to develop a demonstration robot ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/3/12/human-performance-researchers-pair-ros-i-with-markerless-mocap
---

The ROS-Industrial team recently collaborated with Southwest Research Institute's Human Performance Initiative to develop a demonstration robot for an exhibit at Arizona State University. The idea was to leverage work around their Markerless Motion Capture technology, which enables precise, 3-D capture of biomechanical movement, and merge it with the path-planning capability inherent to open-source ROS/ROS-Industrial. The demonstration would recognize a hand, and a specific open gesture of a user and this would then queue the robotic system to retrieve a part from the hand. Though this first iteration only relied on recognizing the object, the training for hand recognition is still of interest and not far off.

![Set Up and Final Demonstration Testing at Arizona State University](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1520871325892-BSW8PN2KUII32V3VCYDF/setup2.jpg)

Figure: *Set Up and Final Demonstration Testing at Arizona State University*

The Human Performance Initiative (HPI) is advancing the motion capture space by improving the performance of motion capture without the need to wear cumbersome suits with the well-known "ping pong balls" attached, and a complex array of cameras. The latest developments by the HPI team involve leveraging expertise in neural networks, sensor fusion, and biomechanics to realize markerless motion capture that can be leveraged, essentially on the fly focusing initially on biomedical, sports science, and animation applications.

In the manufacturing research space, there has been broad interest around understanding what people are doing in the work space. This is mostly in the context of: effective use of space, optimizing ergonomics, recording traffic patterns, predicting or enabling improved safety by understanding people movement, and quantifying the interaction between value stream efficiency and human interaction and movement.

The long-term vision here would be to combine richer, dynamic biomechanical monitoring to enable gesture recognition. In this context, a robot can understand when to interact, and possibly respond based on gesture or human queue. An open palm means "take" or "place" next tool for instance, or a hybrid of verbal and physical combined on the fly by the system. This type of collaboration today is not possible due to limitations in the perception technologies in the context of human-to-human variation, both in structure (size and shape) and how humans specifically execute a gesture, such as indicating they are ready for a robotic hand to take something from them, and the anticipation of what the human may do next. 

In another future state you can imagine the optimal coordination of both mobile robots and humans in a complex orchestration in a high-mix manufacturing environment. Adjusting the process and the tasking of the robots even based on perceived fatigue of the human team members. Continuous value stream, or whole plant optimization combined with this type of human performance monitoring and feedback from the automated partners enable a new paradigm for true manufacturing optimization. There are many pieces coming to maturity to enable this vision, but they need to be brought together to see what is possible.

![Markerless Motion Capture recognizing "Open Hand" &amp; launching path planning to retrieve part from recent 2018 ROS-I Consortium Americas Annual Meeting.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1520871893559-FMEUUE4MGHW1FQ0MAH87/20180307_133623.jpg)

Figure: *Markerless Motion Capture recognizing "Open Hand" & launching path planning to retrieve part from recent 2018 ROS-I Consortium Americas Annual Meeting.*

The idea of a "robot assistant" that can be an active participant in helping a worker to complete a task is still a long way off, but demonstrations such as these offer a meaningful proof-of-concept test bed, to help aid in the roadmap to realize some incremental improvement. Cross-disciplinary collaborations such as ROS-Industrial and the Human Performance Initiative can enable the ability to see what can be done by leveraging the work from each team, each with their own discrete objectives, to realize an entirely new capability set. Here at ROS-Industrial we welcome and advocate for these proof-of-concept type evaluations, and seek to provide the means to enable them.

Visit the [Human Performance Solutions](https://www.swri.org/biomechanics-human-performance-sensing-perception/human-performance-solutions?utm_source=ROSIsite&utm_medium=blog&utm_campaign=ASUdemoblog) web page for more on that team's capabilities and offerings, and follow them on Twitter [@SwRIHP](https://twitter.com/swrihpi).


