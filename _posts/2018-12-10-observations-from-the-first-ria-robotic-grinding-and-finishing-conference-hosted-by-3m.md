---
author: Matt Robinson (SwRI)
comments: false
date: '2018-12-10 22:35:42+00:00'
slug: 2018-12-10-observations-from-the-first-ria-robotic-grinding-and-finishing-conference-hosted-by-3m
title: Observations from the first RIA Robotic Grinding and Finishing Conference hosted
  by 3M
media_type: None
description: A recent conference brought together end-users, solution providers, OEMs
  and researchers to discuss the latest in robotic applications around ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/12/10/observations-from-the-first-ria-robotic-grinding-and-finishing-conference-hosted-by-3m
---

A recent conference brought together end-users, solution providers, OEMs and researchers to discuss the latest in robotic applications around grinding and surface finishing (<https://www.robotics.org/robotic-grinding-and-finishing-conference>). It was an eye opening event and the first of its kind to focus on automation for these types of processes. While there are many conferences on automation, the topics of surface grinding and finishing are rarely at the top of the topic areas. This event also underscored how there are few specialists in this area.

Day 1
-----

The first panel of note discussed whether to automate these operations and how to understand if there was benefit in attacking what is typically considered manual work. There were a number of assumptions that went into the approach, but we learned quickly there was a lot of interest as this was an audience that has historically struggled with legacy approaches and hardware in automating such operations and processes. 

![Charles Gales of Weldon Solutions Presents on Automating of Complimentary Processes as a means to introduce surface finishing to your operations.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1544480685729-NO8ZRV6OM568H3ZEWNB4/20181128_134258.jpg)

Figure: *Charles Gales of Weldon Solutions Presents on Automating of Complimentary Processes as a means to introduce surface finishing to your operations.*

The sessions' two main points were: automate as you can, such as complimentary processes (capture more work with that automation investment), understand your process and burden, and be cognizant of the fact of how you do it a certain way manually today doesn't mean that will be the most optimal way to execute your process robotically.

Force control was the next panel that gained a lot of attention. Obviously, force/torque sensing in a number of areas has become an area of active robotic interest in traditional automation applications and of course applicable in surface processing. There were introductory conversations about the types of force control, such as the pros and cons of passive versus active. A number of compelling applications leveraging active force control were featured. ATI, PushCorp and FerRobotics all offer approaches to meet a wide array of client needs and applications.

![ATI, PushCorp, and Fer Robotics participate on a panel discussing force control in surface finishing and grinding applications.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1544480867079-JL94YBGC1USEBTBXBF6B/20181128_150957.jpg)

Figure: *ATI, PushCorp, and Fer Robotics participate on a panel discussing force control in surface finishing and grinding applications.*

Near the end of the day was an additional panel around DIY Integration, which was incredibly eye opening and generated a lot of conversation. The panelists – Brandon Berth, from Kohler, Matt Morrison, from Marshalltown, and Scott Harms, from MetalQuest – shared interesting stories about making progress on their automation journey through trial and error and developing their own in-house skills to manage deployments. These were stories that relied on a commitment and a process; starting small, developing the skills and gradually moving to more complex applications. 

Day 2
-----

The second day started off with Kuka presenting on enabling small and medium enterprises to take on grinding application development. The key tool they demonstrated was the ability in their simulation ecosystem to empirically model the sanding process and highlight the path and planned surface contact and subsequent material removal. This provided a very compelling visual assessment for the grinding process as it is being developed in their off-line environment. 

The next two presentations were very interesting as they showcased two competent integrators in the space. What was evident, even though their core expertise varied, was that they relied heavily on the teach pendant and skilled online programmers to really bring the process over the finish line. Much like the prior presentations, or the presentations by the DIY'ers, here again we were relying on skilled technicians and industrial robot programmers to complete the implementation of the automation. The level of variation management is limited due to the nature of the deployments. Also, for some of these applications, it may not be realistic to enable too much flexibility as the broad array of complex surface finishing applications was impressive.

I had the opportunity to talk about ROS-Industrial and the work that has been going on in surface finishing using perception and advanced path planning and process planning techniques. This space has talked about path planners ([Trajopt!](https://rosindustrial.org/news/2018/7/5/optimization-motion-planning-with-tesseract-and-trajopt-for-industrial-applications)) and applications ([Robotic Blending](https://rosindustrial.org/news/2017/9/7/robotic-blending-milestone-4-technology-demonstration-at-wolf-robotics), [A5](https://www.wpafb.af.mil/News/Article-Display/Article/1516400/afrl-demos-advanced-robotics-for-aerospace-manufacturing/) and [undergrads using these tools](https://youtu.be/VsaFB4GLaZM)), so I won't get into those details here, but two thing are evident. There is a need to change how we approach these processes if we want to truly attack these types of applications. We can't rely on skilled robot techs to have a teach pendant in-hand. Not every company can grow that expertise in-house over years. Even if they do, how do they scale beyond their core facilities?

![Panel on advances in surface finishing moderated by Jay Douglass of the ARM Institute](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1544481231595-DI2DTSXSCRVFUSUW72B7/IMG_20181129_123546.jpg)

Figure: *Panel on advances in surface finishing moderated by Jay Douglass of the ARM Institute*

I was asked about the capabilities in the blending and A5 videos and how ready they are to go into anyone's plant. That is a great question, and I would be asking that, too, if I was in that seat, as I did when I was on the industry side. We are working on that, hence we were there with the ARM Institute and all the interest in the surface finishing topic calls, and continued development of A5, and an additional milestone upcoming for Robotic Blending. That is why there is a ROS-I Consortium and a [ROSIN](http://rosin-project.eu/) initiative in the EU. We will continue to make the modules more robust and build out application examples that can be leveraged and molded into end-user capability. In the meantime we hope to entice integrator and solution providers to embrace a ROS-based software approach along with our OEM partners. If we work together we can build out reusable components that meet this need, in this greatly underserved area. The exciting part is there is a lot we can do, and it doesn't have to that far away! It was great to see 3M, our hosts, showcase a ROS-based demonstration and do their part to introduce the concepts and how they could lend a hand in solution development. We are excited to have 3M as such an engaged partner and hope together we can keep growing the open-source tool revolution! #GoROS


