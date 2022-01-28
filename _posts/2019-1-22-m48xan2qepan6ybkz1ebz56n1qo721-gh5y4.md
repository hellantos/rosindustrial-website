---
author: Thilo Zimmermann (Fraunhofer IPA)
comments: false
date: '2019-02-01 10:48:46+00:00'
slug: 2019-1-22-m48xan2qepan6ybkz1ebz56n1qo721-gh5y4
title: 'ROS Industrial Conference #RICEU2018 (Session 3)'
media_type: None
description: From public funding opportunities to the latest technologies in software
  and system integration, the combination of robotics and IT to hardware ...
layout: post
old_sp_link: https://rosindustrial.org/news/2019/1/22/m48xan2qepan6ybkz1ebz56n1qo721-gh5y4
tags: ros ros-industrial ros-industrial-consortium europe ros-industrial-conference
  fraunhofer-ipa stuttgart germany open-source-software robotics robot robot-operatin-system
---

From public funding opportunities to the latest technologies in software and system integration, the combination of robotics and IT to hardware and application highlights: [ROS-Industrial Conference 2018](https://rosindustrial.org/events/2018/12/11/ros-industrial-conference-2018) offered a varied and top-class programme to more than 150 attendees. For the sixth time already, Fraunhofer IPA organized a ROS event in Stuttgart to present the status of ROS in Europe and to discuss existing challenges.

This is the **third** instalment of a series of four consecutive blog posts, presenting content and discussions according to the sessions:

1. EU ROS Updates (watch all talks in this [YouTube playlist](https://www.youtube.com/playlist?list=PLXUpEXjGC63xRrb7IGPRnKPhKc-IkjFEC))
2. Software and system integration (watch all talks in this [YouTube playlist](https://www.youtube.com/playlist?list=PLXUpEXjGC63z7Zhe0gyk2tCkZvoEsADpg))
3. Robotics meets IT (watch all but 1 talks in this [YouTube playlist](https://www.youtube.com/playlist?list=PLXUpEXjGC63yahlg5Lu8gU2hMtsFplwOs))
4. Hardware and application highlights

Day 2 - Session "Robotics meets IT"
-----------------------------------

![Henrik Christensen (UC San Diego) at ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1549015968060-VUMYPSGGYXZX850UBKEX/IMG_3975-bearbeitet.JPG)

Figure: *Henrik Christensen (UC San Diego) at ROS-Industrial Conference 2018*

The third session testified the growing importance of ROS to support the development and deployment of robotic solutions from companies outside the traditional boundaries of this industry. Predominantly software players such as Amazon or Google now offer platforms leveraging ROS, which they described during the session.

Henrik Christensen, from [UC San Diego](https://ucsd.edu/) and [ROBO Global](https://www.roboglobal.com/), gave a very inspiring keynote speech on why robotics is increasingly using cloud technologies and how it will benefit from them. He outlined three factors as current business drivers for this development: the increasing demand for flexibility in production, the aging world population and the associated increasing demand for service robots at home, and finally the trend that more and more people live in cities, posing great challenges for logistics. All robot solutions must be cost-efficient and robust at the same time in order to offer the required reliability. If computer performance always had to be on board, the hardware would often be inadequate (e.g. for slim service robots for private use) or the costs for suitable hardware would be too high (e.g. for autonomous cars).

Technologies from or in the cloud can be a solution for this. Christensen presented the value of these ecosystems using extensive market examples and explained how they differ in agility and size. Many successful companies, primarily in the USA and Asia, have shifted their business model from owning things or technologies to orchestrating them and offering services. For robotics, ROS 2.0 can be a decisive door opener here, offering the standardization required for platforms.

![Milad Geravand (Bosch Engineering) at ROS-Industrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1549016332413-F0B5FMZS7EAC2QBEANCR/2018-12-ROS-Industrial-Konferenz-25.JPG)

Figure: *Milad Geravand (Bosch Engineering) at ROS-Industrial Conference 2018*

The next presentations in the session took up these and similar ideas and presented existing solutions. Milad Geravand from [Bosch Engineering](https://www.bosch-engineering.de/en/de/home/startpage.html) presented a modular software platform for mobile systems such as cleaning, off-road and intralogistics robots and how they can be developed more efficiently. In his experience, the difficulties in the development process are similar in many companies: The applications are usually very different, the software is becoming increasingly complex, a structured deployment and integration process is lacking. ROS is not yet ready for the products and the leap from prototype to series production is still too big. With the software platform presented, which is based on ROS, Bosch would therefore like to address precisely these challenges and enable uses cases to be developed quickly and reliably.

Eric Jensen, working for [Canonical](https://www.canonical.com/), the company well known for the [Ubuntu Linux distribution](https://www.ubuntu.com/), presented the advantages of Ubuntu Core especially with regard to security that is still an open issue for ROS. The mentioned advantages are: A minimal, transactional Ubuntu for appliances, safe and reliable updates with tests and rollbacks, app containment and isolation with managed access to resources, a unique development environment familiar for Linux developers and the possibility to easily create app stores for all devices needed. Furthermore, Ubuntu has one of the biggest developer communities in the world and is backed by Canonical itself, an important plus for security. Last but not least, the system offers automatic security warnings for the „snaps", the special package format in Ubuntu, system audits through package verification and compliance management – all are important features for an improved security.

![Roger Barga (Amazon AWS) at ROS-Inudstrial Conference 2018](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1549016544151-K57L06Y0JDXBDEY3Q4QL/2018-12-ROS-Industrial-Konferenz-34.JPG)

Figure: *Roger Barga (Amazon AWS) at ROS-Inudstrial Conference 2018*

Only a few weeks before the ROS-Industrial-Conference, Amazon, for a long time far more than an e-commerce store, had introduced its new platform [AWS RoboMaker](https://aws.amazon.com/robomaker/?nc1=h_ls), which caused a sensation beyond the ROS-Community. Roger Barga, General Manager at AWS Robotics & Autonomous Services, kindly presented this novel development at the conference. Amazon's commitment to robotics is based on discussions with around 100 companies, during which they were able to identify two main problems in robot development. On the one hand, this is a very high demand for automation solutions with simultaneous difficulties with ROS such as security or performance. On the other hand, the development process is usually very inefficient.

The RoboMaker platform addresses these requirements with its four main components. It offers a browser-based development environment, which in turn has integrated cloud extensions for ROS as well as a simulation environment. The cloud extensions range from machine learning tools to monitoring and analytics. Concrete capabilities for robots include speech recognition and output, video streaming, image and video analysis, as well as logging and monitoring with Amazon CloudWatch. The simulation environment allows thousands of simulations to be run in parallel. The fourth component is fleet management, so that robot applications can be deployed over the air. The presentation ended with a short introduction to the learning environment of RoboMaker, with which Amazon applies reinforcement learning to robots. The robots then learn according to the principle "trial and error". By merging all errors within a fleet in the cloud, a large knowledge base is quickly available and not every single robot has to make a specific error to learn from, but it benefits from the learning experiences of other robots in the fleet.

The topic of robotics in the cloud was also the focus of the lecture by Christian Henkel from [Fraunhofer IPA](https://www.ipa.fraunhofer.de/en.html). In his experience, the deployment of ROS-based applications on distributed systems such as mobile robots is still too great a challenge, which he would like to address in his work with docker containers ([dockeROS](http://wiki.ros.org/dockeros)). With his solution, it is possible to simply run ros nodes in docker containers on remote robots.

![Martin Hägele (Fraunhofer IPA) moderates a panel discussion with Henrik Christensen (UC San Diego), Oliver Goetz (SAP), Michael Grupp (magazino), Niels Jul Jacobsen (MiR) and Damon Kohler (Google).](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1549016893444-6371L293UMPN40TN3G7Q/IMG_3993-bearbeitet.JPG)

Figure: *Martin Hägele (Fraunhofer IPA) moderates a panel discussion with Henrik Christensen (UC San Diego), Oliver Goetz (SAP), Michael Grupp (magazino), Niels Jul Jacobsen (MiR) and Damon Kohler (Google).*

With Damon Kohler, [Google Robotics](https://www.youtube.com/watch?v=eo8MzGIYGzs) and its recently presented cloud solution were also represented at the conference. In his introductory remarks, Kohler mentioned several challenges related to cloud robotics, including security, connectivity and latency, and distributing work, e.g. partitioning problems. In contrast, he sees advantages such as scalability, collaborative perception and behaviour and a robust change management and monitoring. He sees cloud robotics as a further development of the well-known principle "sense -> plan -> act" around the component "sense -> share -> plan -> act" and as an interplay of edge and cloud processing. 

The aims of cloud robotics are an increased launch cadence, more data and more users and a better resource utilization. This shall be reached by infrastructure as a service, design for small and decoupled components as well as tools for automation and orchestration. The ROS nodes correspond to the Google micro-services: They are stateless and replicable, which means horizontally scalable. The container orchestration engine Kubernetes helps to deploy and release these micro-services. Several mature and robust logging and monitoring tools like Stackdriver help managing the system. The heart of the whole is the Cloud Robotics Core, being available from beginning of 2019 that enables to integrate Kubernetes on robots. Overall, Google's vision is an open platform and a thriving ecosystem where integrators, developers, hardware developers and operators can collaborate with customers efficiently. 

The second day of the conference ended with a panel discussion. The panellists were Henrik Christensen (UC San Diego), Oliver Goetz (SAP), Michael Grupp (magazino), Niels Jul Jacobsen (MiR) and Damon Kohler (Google). Moderated by Martin Hägele (Fraunhofer IPA), they summed up some advantages from their respective company perspectives, but also existing challenges of ROS and the role of open source software and robotics for their corporate strategy.


