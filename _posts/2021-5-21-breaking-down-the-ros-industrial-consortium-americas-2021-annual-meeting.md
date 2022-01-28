---
author: Matt Robinson (SwRI)
comments: false
date: '2021-05-21 17:55:45+00:00'
slug: 2021-5-21-breaking-down-the-ros-industrial-consortium-americas-2021-annual-meeting
title: Breaking Down the ROS-Industrial Consortium Americas 2021 Annual Meeting
media_type: None
description: The ROS-Industrial Consortium Americas (RIC Americas) gathered virtually
  on April 13-15 for the 2021 Annual Meeting. The event was a great ...
layout: post
old_sp_link: https://rosindustrial.org/news/2021/5/21/breaking-down-the-ros-industrial-consortium-americas-2021-annual-meeting
---

The ROS-Industrial Consortium Americas (RIC Americas) gathered virtually on April 13-15 for the 2021 Annual Meeting. The event was a great opportunity for the diverse ROS community to discuss challenges and progress while laying out new initiatives and fostering relationships. The event demonstrated several ways RIC Americas members and the open-source community are furthering ROS for industry through global consortia initiatives, tech and software company projects, and collaboration among researchers and industry organizations. All the presentations and videos for the public day and the demonstrations may be found over at the [event page](https://rosindustrial.org/events/2020/ros-industrial-consortium-americas-2021-annual-meeting), or over at the ROS-Industrial YouTube channel [playlists page](https://www.youtube.com/channel/UCXyGVRiCwUMc1gav-G7z2ew/playlists)!

**Day 1** 

The first day was open to the public and kicked off with a summary of 2020 RIC Americas activities relative to ROS-Industrial. The topic of training centered on the migration from ROS to ROS2,the move from preconfigured virtual machines to a cloud-based training environment, and the delivery of the training virtually. Overall feedback was positive; however, there are quite a few areas for improvement:

* Some exercises have still required reaching back to ROS1 to complete.
* There could be more explanation about how things are done and why.
* Labs need to be optimized for ROS2 and to be more meaningful in the virtual format.

![Zoom Training-1021.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1621609983464-MFAJYZOWAHKWXOHBFB7D/Zoom+Training-1021.JPG)

Tech updates that have been contributed include collision checking improvements, parallel process planners using Taskflow as well as discrete capability improvements such as the addition of kinematic calibration added to [robot\_cal\_tools](https://github.com/Jmeyer1292/robot) and heat raster-based tool path planning on meshes within the [toolpath\_offline\_planner](https://github.com/swrirobotics/toolpath_offline_planning).

Darryl Lee of the ROS-Industrial Consortium Asia-Pacific (RIC Asia-Pacific) shared Focused Technical Project (FTP) developments around Interoperable Robotics with RMF. The Robotics Middleware Framework (RMF) has been a successful program funded by the Singapore government that has sought to implement a unified IoT infrastructure, based on ROS, for the healthcare industry. This new FTP initiative seeks to extend this work to commercialization for the manufacturing industry.

RIC Asia-Pacific also launched ROS2 training but also included training on their own developed [Easy\_Perception\_Deployment](https://github.com/ros-industrial/easy_perception_deployment) (EPD) and [Easy\_Manipulation\_Deployment](https://github.com/ros-industrial/easy_manipulation_deployment) (EMD). Of interest via feedback from their training events have been use cases around mobile manipulators, depalletizing, and easy pick-and-place configuration set up. The talk by RIC Asia-Pacific concluded with Glenn Tan going into the development of their EPD and EMD implementations, where to find them, and how they came to be. 

Christoph Hellmann Santos of the ROS-Industrial Consortium European Union (RIC EU) shared the developments in collaboration with Fraunhofer IPA, including the recent advancements as the ROSIN project concludes and the current work and near-term roadmap for the Cognitive Robotics and AI Innovation Center seeks to advance ROS2 capability for industry, with an initial focus on hybrid model-driven engineering and diagnostics and monitoring framework for ROS and ROS-based systems. 

![ipa model base.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1621614277239-QMFLHLA7F2Q5BQGBRI76/ipa+model+base.JPG)

RIC EU shared their launch of ROS2 training and application development examples, focused on an easy programming for welding robots that include seam detection, collision free motion planning and execution, optimized path planning, work piece pose detection, with easy set up and integration into the UR caps ecosystem. 

Following the ROS-Industrial updates, a collaboration between MathWorks and Delft University of Technology was presented on Automated Code Generation of Simulink Models as ros\_control Controllers which showcased the process for moving Simulink developed controllers and implementing them into the ros\_control framework. 

From here partner organizations provided introductions and updates to what has been taking place within their organizations. NIST has been a champion for ease of interoperability and moving to unifying standards to foster more efficient innovation for all users of robotics. NIST's Craig Schlenoff focused on the move towards agility and all the activities related around facilitating agility in robotics. Georgia Tech Research Institute's Stephen Balakirsky shared their organizations leverage of ROS to facilitate advanced capability, how they have realized robot teams to work together on tasks. ARM Institute CTO Arnie Kravitz shared both the impact of ROS on the development within the ARM Institute technology project portfolio and how the technology project portfolio becomes a proving ground for capability within the ROS ecosystem. 

Spirit Aerosystems wrapped up the morning by reviewing the outcomes from the ARM Institute supported Collaborative Robotic Sanding project. This project featured a ROS2 software backbone, but also included ROS-based training, woven in with a gap assessment for Spirit and partner Wichita State's National Institute for Aviation Research. While the technical outcomes for the project were of note, and it was interesting to build a fully functional ROS2 system, for ROS to gain real traction in industry a more thorough educational infrastructure is required to support all facets of the industrial teams that create, deploy and sustain these future systems on the factory floor.

The afternoon provided a number of advances from the tech company side of the ROS-Industrial Consortium, starting with the case for migrating to ROS2 by Open Robotics. There are now several utilities to assist with migration, and a handy cheat sheet if someone is interested in considering ROS2 migration, with more utilities on the horizon.

PickNik's Andy Zelenak shared the recent collaboration with Universal Robots and FZI Research to realize a ROS2 Driver, which is now available for all UR models. Intel's Atul Hatalkar shared the vision around ROS++ where a ROS++ exists to support industrial autonomy including non-programmer utilities, active bridges to facilitate autonomous interoperability, and security and data reliability.

Microsoft shared a good portion of their recent work around the Mixed Reality Toolkit and how they are working to enable richer AR/VR applications in ROS2. Canonical's Sid Faber updated the group on the latest efforts around security, particularly security for legacy ROS implementations via their ESM service and shared their work on the CIS ROS Melodic Benchmark. 
AWS' Jack Reilly introduced AWS' goals around their EDU program seeking to "democratize robotics, support the ROS Community, and create features and resources to support learners and educators." This is a toolset focused on educational content, including accessible cloud-based content, development environment utilities, and even physical implementations to support educational objectives. 

Wrapping up the day, Michael Jaentsch of Siemens and Robert Burridge of TRACLabs shared work that seeks to leverage interoperability to facilitate improved collaboration between disparate devices. Siemens, with funding from the ARM Institute, built on the prior work funded by NIST extending MTConnect to ROS to support many-to-many functionality and brought in RTI's DDS Connext to create an OPC-UA to DDS bridge. TRACLabs demonstrated using their two tools, PRIDE and CRAFTSMAN to facilitate dynamic tasking between disparate types of hardware, in a NASA-based application. 

**Day 2**

Day two brought together the ROS-Industrial Consortium membership, focused on the Americas, but open to global members. Here the focus was on members sharing some of their experiences, learning from each other and providing feedback on how the Consortium, as an organization, should leverage its shared resources to advance open source for industry. The panel focused on getting ramped up into ROS development, and decisions you make before deciding to go in that direction. There were insights around talent development and how to engage in open source, with a great challenge by PlusOne's Shaun Edwards to think beyond simply pushing fixes to leveraged repos.

![Summary of the Training Flows Need to Support ROS for Industry](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1621615038185-8M6NOM9SXWVKFSMGQMRQ/education+and+ROS.JPG)

Figure: *Summary of the Training Flows Need to Support ROS for Industry*

From there, inputs for influence of the roadmap were next. To date, the member feedback has evolved the focus of the Consortium into four main themes:

* Ease of Use
* Advanced Capability
* Interoperability
* Human Interface and Reaction

Feedback from the 2020 workshop indicated additional focus on resources for members and the broader community were of great interest. This includes write ups, simple explainers, more complete and up-to-date wikis, to help bridge the gap between traditional industry decision makers and application builders to the open source developer community. Feedback from the 2021 workshop centered on educational resources, field service "How Tos," status dashboard templates, functional safety, ROS2 porting guidance, and security resources. There was significant interest in terms of capability around machining/CAM style path planning and execution to support processes such as additive manufacturing, as well as additional PLC tools for controlling external devices.

The member speaking portion of Day 2 was highlighted by David Poweleit of Steel Founders' Society of America (SFSA) sharing the needs of their membership, and how they align with the objectives of ROS-Industrial, relative to driving high-mix intelligent processing, in a way that is easy for end-user/operator interaction. 

Boeing, represented by Martin Szarski and William Ko, followed up with their success story around open-source implementation of their navigation implementation as they worked toward robust factory mobility. This was definitely an interesting talk from the technical development and implementation of their navigation solution, to the journey to be able to open source this resource for the broader community.

The day wrapped with a workshop on project brainstorming. Here the membership offered up collaborative topics, that could be projects, or working groups to address challenges relative to industrial leverage of open source. A couple key topics:

1. Hardware Reference Implementation Working Group – The goal of this working group would be to leverage existing standards, but factor in a way that is understandable for the industrial community. Initial starting point would be manipulators, ideally speaking ROS2 out of the box, and consistent across OEMs with a focus on target or desired behavior.
2. Scan-N-Plan Implementation Generalized for High-Mix Processing – Demonstrated on an SFSA use case, this would be a high-mix surface finishing where the output would be a generalized implementation of Scan-N-Plan that could be adopted by solution providers for various high-mix end user customers.
3. ROS Workbench – Provide model-driven and GUI-driven utilities to lower the barrier to entry for manufacturing engineers, or those with more traditional industrial automation experience to set up and do preliminary configuration of a ROS-based application.
4. Calibration – Revisit the calibration toolset and create one toolset with resources to enable all the various forms of calibration, intrinsic, extrinsic, and kinematic, to enable high performance ROS-based applications.
5. Planning for Additive or Machining – The interest in doing more with manipulators in one system is appealing, but currently there are no easily incorporated tool planning utilities to support additive or subtractive processes as seen in Additive or CNC type machining applications.

The next day, Demo Day!, was a great share of what a number of the different members and community participants are doing with regards to making open source happen in the real world, and the hardware to make interesting applications happen. We encourage you to check out the [event page](https://rosindustrial.org/events/2020/ros-industrial-consortium-americas-2021-annual-meeting) for the full Demo Day! list, which inludes the link to the video. Special thanks to all the participants in Demo Day! for sharing their contributions and recent developments.

Now the ball is in the court of the community and the membership that expressed interest in working together to address gaps and move these various topics forward. We are excited about what the next year has to offer and look forward to sharing more outcomes, collaboration opportunities, and resources for the community and industry to continue making open source software a reality on production floors around the world. 


