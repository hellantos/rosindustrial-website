---
author: Guest User
comments: false
date: '2019-10-02 20:43:09+00:00'
slug: 2019-10-1-an-experience-in-working-with-industrial-hardware-drivers-for-ros
title: Documentation updates improve ROS utilization and functionality
media_type: None
description: Lessons from UR driver updates reinforce importance of documentation
layout: post
old_sp_link: https://rosindustrial.org/news/2019/10/1/an-experience-in-working-with-industrial-hardware-drivers-for-ros
tags: ur ros ros2 modern-driver ros-i ros-industrial
---

*Lessons from UR driver updates reinforce importance of documentation*

A key strength of the open-source community is the capacity to build on the
knowledge of other developers who enable future advancements. Documentation
plays a critical role in advancing understanding, which improves ROS utilization
globally. This will be increasingly important as we move from ROS to ROS2 and
document the various steps, including driver updates, necessary to execute
projects.

Recent driver updates for a Universal Robots project helped demonstrate the
importance of documentation to our team. In July 2019, Universal Robots updated
their software for e-series and CB-series to 5.4 and 3.10. We were using the 5.4
software on UR 10e robots for a few different projects, and the
ur\_modern\_driver [1] for ROS kinetic and melodic was no longer compatible due to
this update. I updated the driver by investigating the release notes for
5.4.x.x [2] and the client\_interface document [3]. 

View fullsize

![UR10 E-series in the SwRI collaborative lab](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1570048913926-H15G9TRE94EKT7NFE330/20191002_153716.jpg)

Figure: *UR10 E-series in the SwRI collaborative lab*

To update the ROS driver for compatibility with software updates, I first
identified what changes occurred and located appropriate software documentation
for the hardware. The software documentation defined modules and variable types
for the changes, which allowed for comparison with equivalent variables and
modules in the current driver code. Without proper documentation from Universal
Robots this would have been a much more difficult endeavor. 

The ur\_modern\_driver specifically interacts with the client interface. Two
variables were added to the 5.4 software client interface: a reserved byte in
the Masterboard data sub package of Robot State Message to be used for internal
UR use and a safety status value to the real time interface. The client
interface document gave the types and sizes of these variables along with
variables used in previous software versions.

The client interface for 5.3 and earlier had an internal UR int in Robot Mode
Data I could compare to, and the safety status value could be compared to any of
the other double variables in the previous driver's RealTime interface. I used
the search feature in QTCreator to find instances of these variables and added
equivalent lines for the new ones. Then I used QTCreator's debugger to track
where new if statements and functions needed to be added to allow the driver to
detect the new software version being used and access these new variables. 

Working on this upgrade reinforced the necessity of good documentation. In
general, the ur\_modern\_driver had more detailed documentation than many other
ROS repos; however, it could still be improved. The README had no mention of the
purpose of the use\_lowbandwidth\_trajectory\_follower parameter in the launch
files or the urXXe\_bringup\_joint\_limited.launch file; both of these are useful
when simulations are being overenthusiastic in their trajectory planning. I
added documentation to the README to help others use these features to
troubleshoot. 

To update drivers, you will need to know what has been changed in the software,
and you will ideally have access to a previous version of the driver. Because
industrial hardware is intended to be reliable and accessible for multiple
clients, there is often plenty of useful documentation if you can search with
the correct terminology. Using the known changes and the documentation to
compare with the previous driver code allowed me to update the driver fairly
quickly so projects could move forward. 

1[https://github.com/ros-industrial/ur\_modern\_driver](https://urldefense.proofpoint.com/v2/url?u=https-3A__github.com_ros-2Dindustrial_ur-5Fmodern-5Fdriver&d=DwMFaQ&c=l_IU86Q8JTGnHn9K9kRmRlrLmhfeE6S9tCyr6T8mzvM&r=g82jlXpkAlQYZr3pjAgOObx2RJeTG-QNqBpd-DWgPGY&m=TKY-FwzvmP4tze9GkY4a0MX0qYBwNnil8vi3c55akpA&s=oDANreG5C6r0as0-EZtuVQ--BPswItYJJXuALpcI29s&e=)

2[https://www.universal-robots.com/how-tos-and-faqs/faq/ur-faq/release-note-software-version-54xx/](https://urldefense.proofpoint.com/v2/url?u=https-3A__www.universal-2Drobots.com_how-2Dtos-2Dand-2Dfaqs_faq_ur-2Dfaq_release-2Dnote-2Dsoftware-2Dversion-2D54xx_&d=DwMFaQ&c=l_IU86Q8JTGnHn9K9kRmRlrLmhfeE6S9tCyr6T8mzvM&r=g82jlXpkAlQYZr3pjAgOObx2RJeTG-QNqBpd-DWgPGY&m=TKY-FwzvmP4tze9GkY4a0MX0qYBwNnil8vi3c55akpA&s=GoNbsAp8ejvnI3eaOC-WTKF4sNFb9TTNLVkjIFyDDek&e=) 

3[https://www.universal-robots.com/how-tos-and-faqs/how-to/ur-how-tos/remote-control-via-tcpip-16496/](https://urldefense.proofpoint.com/v2/url?u=https-3A__www.universal-2Drobots.com_how-2Dtos-2Dand-2Dfaqs_how-2Dto_ur-2Dhow-2Dtos_remote-2Dcontrol-2Dvia-2Dtcpip-2D16496_&d=DwMFaQ&c=l_IU86Q8JTGnHn9K9kRmRlrLmhfeE6S9tCyr6T8mzvM&r=g82jlXpkAlQYZr3pjAgOObx2RJeTG-QNqBpd-DWgPGY&m=TKY-FwzvmP4tze9GkY4a0MX0qYBwNnil8vi3c55akpA&s=ruVEPiQsTaCBVGYyeTvzvNqEM4CumXh88kcbmqqh-pM&e=)


