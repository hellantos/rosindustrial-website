---
author: Ryan Howard (SwRI)
comments: false
date: '2018-04-13 13:55:56+00:00'
slug: 2018-4-13-leveraging-scan-n-plan-for-additive-manufacturing
title: Leveraging Scan-N-Plan for Additive Manufacturing
media_type: None
description: Implementing Additive Manufacturing (AM) principles with a collaborative
  twist is still an unexplored area of manufacturing. Traditional AM ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/4/13/leveraging-scan-n-plan-for-additive-manufacturing
---

Implementing Additive Manufacturing (AM) principles with a collaborative twist is still an unexplored area of manufacturing. Traditional AM typically involves step motors moving a printing head, or a laser bonding a material to itself. More advanced solutions have even gone to mounting print heads as robotic end effectors to gain a larger print volume. [A ROS framework](http://wiki.ros.org/ros_additive_manufacturing) has already been developed in this space, though additional features are always of interest.

Often when a part is damaged it is either thrown out or repaired with direct labor. What if there was a way for autonomous blending part repair with AM? Assuming a known CAD model, a [Scan-N-Plan](https://rosindustrial.org/scan-n-plan/) AM solution could bring new life to previously scrapped parts. The method proposed here involves bringing in a damaged part, doing a laser scan and determine which elements of the part need repair.

Laser scans produce good resolution of parts and is largely insensitive to material and surface quality though some cases may require several scans to achieve high resolution. A pre-scan process can easily assume this role to reduce print downtime. The scan in the image below was done on a FARO arm. As can be seen, in the image below, the quality is excellent. The file exports a point cloud that can be imported into the ROS framework. Similarly, a non-contact structured light sensor could provide the output as seen below, whereby subsequent process planning could be driven.

![Crack.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1523630299502-YT2IEWM14S9Q90YQP4BF/Crack.jpg)

Once the file is scanned, the part is then checked against a master CAD file. The deviation of the point clouds indicates where the flaw exists. The point cloud is then converted to a YAML file and the path is generated. Locating the part between scan and print head is done using 3 known touch off points or a non-contact form of localization. The material deposition process is then free to take place. For cases such as the above example where prep-work is required to enable material deposition, a cutting or grinding tool can be process planned and executed as well to create a suitable prepared region for material deposition to occur.

![Additive Value Stream Reman.png](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1523636479632-WNK67C4YCDVDVVM4FI5X/Additive+Value+Stream+Reman.png)

In [remanufacturing use cases](http://www.westeconline.com/wp-content/uploads/2015/09/Li-Bingbing-Laser-Additive-Manufacturing.pdf), specifically where the variation is high due to the unknown state of the provided material, a more efficient workflow with higher return and repurposing of field return material is possible. The leverage of a ROS-based framework in a distributed manner could enable common intelligence being applied over a range of assets residing at multiple sites, making process control more uniform wherever the operation takes place. Furthermore, as in the case in remanufacturing, as opposed to additive processing (building up) a complete part, leveraging the Scan-N-Plan framework enables optimization of applying only where the additive process delivers the most value in the broader context of the value stream and cost of both incoming materials and the processing itself. An example of this would be the replacement of a linkage forging on a structure with an additive deposit, where the remaining structure is fabricated plate material, the additive can be optimized to both manage load (print direction and properties), while optimizing costs where commodities do the job and are readily available at favorable costs.

Issues that could arise with this process include interference with the print head with the part (oddly shaped flange interfering with a robot wrist independent of the print head) and cable management for certain types of deposition processes. Though material waste is minimal with advances in additive near-net processing, there is the cost and maintenance of the media and encompassing all of the tools that need to be accessible to the manipulator, from the QA assessment, material prep/finish/surface treatments, and of course the AM process itself. Underside printing would be a second print unless an auxiliary positioner is implemented, such as in some of the more recent hybrid additive/subtractive platforms.

Physical attributes of a repair part are untested based on metallurgical properties. Part repair is still a fledging industry of research, though there have been recent advances in aerospace remanufacturing. [Cohen](http://danlcohen.com/wp-content/uploads/2010/09/Cohen-Biofabrication-In-Situ-Bone-Repair.pdf) has done some work with tissue engineering and still uses a 3-axis step motor . Great advances still stand to be made in this research area, however a number of tools exist to create an agile process leveraging the benefits of additive and approaches like Scan-N-Plan.


