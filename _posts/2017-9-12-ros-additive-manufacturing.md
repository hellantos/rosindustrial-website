---
author: Matt Robinson (SwRI)
comments: false
date: '2017-09-12 16:48:51+00:00'
slug: 2017-9-12-ros-additive-manufacturing
title: ROS Additive Manufacturing
media_type: None
description: The ROS Additive Manufacturing (RAM) project is a set of ROS packages
  that enables automatic generation of trajectories for additive ...
layout: post
old_sp_link: https://rosindustrial.org/news/2017/9/12/ros-additive-manufacturing
---

The ROS Additive Manufacturing (RAM) project is a set of ROS packages that enables automatic generation of trajectories for additive manufacturing. It has been designed for metallic additive manufacturing with industrial robots. This project is open-source and under the BSD license.

Starting with a YAML file representing a 2D polygon or a 3D mesh, the goal is to obtain a trajectory and construct a 3D part with a robot. The user provides input files and some parameters, then generate the trajectory. The user is then able to modify the trajectory within a GUI if needed. Finally the user can obtain a robot program (specific to a brand) via a post processor (the post processor is not included in the project).

**MOTIVE**

There are many software products available to generate trajectories for 3-D printing. Most of them are designed for plastic and resin 3-D printing (FDM, SLS etc.) with Cartesian machines. The algorithms usually have an "infill" parameter that allows the user to choose how much material should be put inside of the "shells" (the exterior of the 3D volume). This is very handy to produce lightweight parts, but when set to 100%, the parts are not completely filled and some holes (porosities) remain.

With 3-D metallic printing, parts are very often expected to be fully filled with material and the tolerance for porosities is very low. This constraint does not allow us to use conventional 3-D printing software and led us to create our own solution. Depending on the process (powder projection, wire) there can be other requirements. For example processes using wire are not simple to stop and start, having a continuous trajectory becomes mandatory to ensure deposition quality.

This is why we decided to create a very flexible software solution, providing a clean and modern approach to 3-D printing.

**SOFTWARE ARCHITECTURE**

The project is split in modules, each of them has a specific functionality, the main modules are:

* Path planning: Automatically generates a trajectory given an input file and some parameters (layer height, etc.)
* Display: Publishes the trajectory in RViz so that it can be visualized and features different visualization modes
* Modify trajectory: Allows for trajectory modification by selecting poses and tweaking them (geometry, parameters)

This modular approach easily allows for adding, removing or modifying functionalities inside the software. The software can be used through a Qt GUI based on RViz and is designed to be easy to use for a non programmer.

![Star.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1505233049782-0A3GCJ05EQA7FU025GCH/Star.jpg)

**CURRENT STATE**

The application is working and easy to compile, code quality is ensured by Continuous Integration including Unit Tests.

There are some missing functionalities, for example:

* Entry/exit trajectories (will be added before the end of September)
* Trajectory simulation (will be added soon)
* Post processor (most likely won't be included in the project because it is too robot specific)
* Ability to generate trajectories with process stop/start: sometimes the part cannot be constructed without stopping and starting the process again
* Allow to generate trajectories with diagonal layers

The software is already able to generate complex trajectories:

![Complex Stack.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1505232479993-67EAX33P2A3407H7QHDP/Complex+Stack.jpg)

![trivet.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1505232516430-KBX1CLSZN3EBVFPMP45M/trivet.jpg)

**FUTURE DEVELOPMENTS**

In the future, we would like to be able to generate trajectories for 3D printing when the initial surface is not flat. This implies creating a specific algorithm.  

We also need to write some documentation and a user guide for the software.

**CONCLUSION**

You can find more information on the official [ROS Additive manufacturing]([http://wiki.ros.org/ros\_additive\_manufacturing](https://urldefense.proofpoint.com/v2/url?u=http-3A__wiki.ros.org_ros-5Fadditive-5Fmanufacturing&d=DwMCaQ&c=l_IU86Q8JTGnHn9K9kRmRlrLmhfeE6S9tCyr6T8mzvM&r=g82jlXpkAlQYZr3pjAgOObx2RJeTG-QNqBpd-DWgPGY&m=EA-1Ie-IkI_RMSOkSwwKO2jkSLtAbZJmr00BWdfjiB4&s=9gP82KRa3igxnQSzCng76W4KwfA0h663Kj6CSUjddiM&e=)) wiki webpage.  
Digests of the advancement are frequently posted on [the SwRI mailing list]([https://groups.google.com/forum/#!searchin/swri-ros-pkg-dev/additive%7Csort:relevance/swri-ros-pkg-dev/Bd7weRLIrpU/Wk-aCsGiAQAJ](https://urldefense.proofpoint.com/v2/url?u=https-3A__groups.google.com_forum_-23-21searchin_swri-2Dros-2Dpkg-2Ddev_additive-257Csort-3Arelevance_swri-2Dros-2Dpkg-2Ddev_Bd7weRLIrpU_Wk-2DaCsGiAQAJ&d=DwMCaQ&c=l_IU86Q8JTGnHn9K9kRmRlrLmhfeE6S9tCyr6T8mzvM&r=g82jlXpkAlQYZr3pjAgOObx2RJeTG-QNqBpd-DWgPGY&m=EA-1Ie-IkI_RMSOkSwwKO2jkSLtAbZJmr00BWdfjiB4&s=FXRhQtTdH8DCvU4lPGNNqRBwKXPVNkiPMWr7U9pqlPg&e=)); please post your questions about the project here!  

You can contribute to this project by reporting issues, writing documentation or opening merge request to fix bugs, improve/add functionalities.

Authored by Victor Lamoine, Institut Maupertuis, France, on GitHub at [https://gitlab.com/InstitutMaupertuis/](https://urldefense.proofpoint.com/v2/url?u=https-3A__gitlab.com_InstitutMaupertuis_&d=DwMCaQ&c=l_IU86Q8JTGnHn9K9kRmRlrLmhfeE6S9tCyr6T8mzvM&r=g82jlXpkAlQYZr3pjAgOObx2RJeTG-QNqBpd-DWgPGY&m=cwJFOaQmsBpTJpZzgOb2fuKUvCA8PMHCj6VhyxLA48Y&s=kff3RYCQHGs5zlrkb4SVE5lFjizvzqScmTAekyv-ISM&e=)


