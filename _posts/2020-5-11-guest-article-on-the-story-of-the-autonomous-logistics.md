---
author: Thilo Zimmermann (Fraunhofer IPA)
comments: false
date: '2020-05-15 14:40:05+00:00'
slug: 2020-5-11-guest-article-on-the-story-of-the-autonomous-logistics
title: 'Guest article: A Story of Autonomous Logistics'
media_type: None
description: From rapid robot prototyping to pre-series robot production
layout: post
old_sp_link: https://rosindustrial.org/news/2020/5/11/guest-article-on-the-story-of-the-autonomous-logistics
---

From rapid robot prototyping to pre-series robot production
-----------------------------------------------------------

a guest article by [Deparment of Autonomous Logisitics of StreetScooter](https://github.com/Autonomous-Logistics)

![The robotic delivery arm of Eva was self-constructed at StreetScooter](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229259441-OZRKI3ZDA7QSP6QAXF9L/Pic+1.png)

Figure: **The robotic delivery arm of Eva was self-constructed at StreetScooter**

The vision of a generic toolbox to solve automated delivery challenges was born in the Department of Autonomous Logistics in 2016. ROS was chosen as the framework because it was quite popular among students in robotics and many suitable open source modules were already identified. At the same time, a ROS-based software stack for urban autonomous driving called [Autoware](https://www.autoware.ai/) was released open source. This was a blessing for the young robotic team since multiple components could later be adapted for Eva's Follow Me Delivery function. The fresh robotic engineers could learn from the experiences made with this stack, without having a senior robotic expert in the team. With the test track next to the developers' office, a short iteration cycle was introduced to gather the knowledge needed.

Eva, Adam and Alfi for Follow Me and Autonomous Parcel Delivery
---------------------------------------------------------------

The first prototype was not Adam but Eva, constructed in partnership with TAS (Institute for Autonomous Systems Technology of the Bundeswehr University) [[1](https://www.researchgate.net/publication/323105001_Prototyping_an_autonomous_delivery_vehicle)], PEM (Production Engineering of E-Mobility Components) of RWTH Aachen and Beckhoff Automation. Eva was constructed to demonstrate the autonomous parcel delivery.

After showing the first promising in-house developments in software and hardware design, two realistic use-cases for applying robotic technology to logistics were identified in 2017:

1. Follow Me Delivery
2. Autonomous Yard Logistic

Both developments were chosen based on the agile mindset to deliver benefits as early as possible to the customer. A maximum speed of 10 km/h was a promising entry point since an emergency stop was possible under all circumstances. In the meantime, the usage of open source technology for robotics prototyping increased since this showed strong acceleration in the development. The re-usage of components between both use cases and vehicle types was given by the modularity of the ROS Framework [[2](https://www.missinglinkelectronics.com/www/images/LandingPage/FPGA4ADAS_2/9_Augspurger_StreetScooter_Open-Source-System-Prototyping-in-Autonomous-Logistics.pdf)] Two StreetScooter Work vehicles, Adam and Alfi, have been equipped with the Follow Me Delivery system (Adam for rapid prototyping and Alfi to show the next steps in system design and focus on industrialization).

![Most systems have been integrated into the roof top of Alfi. In this way the integration of the Follow Me Delivery System into a series StreetScooter Work M vehicle was possible.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229403736-MXHJ6TKA9WD3UTUJ2P51/Pic+2.JPG)

Figure: **Most systems have been integrated into the roof top of Alfi. In this way the integration of the Follow Me Delivery System into a series StreetScooter Work M vehicle was possible.**

Adam and the Demonstration of Follow Me Delivery
------------------------------------------------

Nvidia invited StreetScooter to [demonstrate](http://www.youtube.com/watch?v=PWhm4gtEfB4) the Follow Me Delivery function on a test track next to the NVIDIA GTC conference at Munich in 2017 [[3](https://nvidianews.nvidia.com/news/deutsche-post-dhl-group-selects-nvidia-drive-px-for-autonomous-delivery-truck-fleet)]. The new cooperation announcement on the conference and the immense press feedback reveal the potential of Follow Me Delivery. The software itself was a combination of multiple open source ROS modules integrated into the basic [move\_base](https://wiki.ros.org/move_base) navigation framework of ROS. The team showed that, by combining and adapting multiple ROS modules like [depth\_clustering](https://github.com/PRBonn/depth_clustering) or [osm\_cartography](http://wiki.ros.org/osm_cartography) of different organizations, the development of an autonomous vehicle is possible. Safety was given by the low-level controller that supervised the controllability of the system in combination with a trained safety driver.

![The ground was quite uneven. This led to false-positive obstacles detected in the ground.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229509238-RKFI2B007CLIDC524ZCV/Pic+3.png)

Figure: **The ground was quite uneven. This led to false-positive obstacles detected in the ground.**

Obelix for Prototyping in Autonomous Yard Logistics
---------------------------------------------------

In 2018, the first prototype system for the autonomous yard logistics was equipped on an electric Wiesel truck from KAMAG. At this time, the vehicle base itself was also a prototype. The first step was to automate the steering to reduce safety risks of the heavy truck with a maximum weight of about 26 tons. That way, the acceleration of the vehicle was still in control of the safety driver. This level of automation generated lots of interest at DHL since the safety concept is much simpler and the system costs are lower in comparison to a fully autonomous system.

Many benefits like lower material wear, less noise and simpler vehicle handling were still given. This worldwide unique concept was named [Assisted Maneuvering and Positioning System](https://www.streetscooter.com/en/amps/) (AMPS). Field-tested software and hardware solutions from Alfi have been adapted to the new vehicle Obelix. Based on the experiences made from the open source packages of Follow Me Delivery, a new in-house development has been started. Some powerful packages like [robot\_localization](https://github.com/cra-ros-pkg/robot_localization) or Google's [carthograpther](https://google-cartographer-ros.readthedocs.io/en/latest/) are still used in our software stacks today. Because of a planned in-field test at a DHL parcel center in cologne in 2019, much more requirements and quality management had to be introduced. LiDAR was chosen as the main sensor system because a high precision in localization and detection with an error margin smaller than 3 centimeters is demanded in changing and demanding outdoor conditions.

![Obelix at his daily mission on the test track of Avantis.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229644189-PDDGSMO103T8TUXNYK53/Pic+4.png)

Figure: **Obelix at his daily mission on the test track of Avantis.**

![Snow tracks on Avanits in the LiDAR measurement. Even under those conditions, the system needed to adhere to its requirements.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229702524-QQPWKTL6LKU6DRSB4JDR/Pic+5.png)

Figure: **Snow tracks on Avanits in the LiDAR measurement. Even under those conditions, the system needed to adhere to its requirements.**

Asterix at the parcel centers of Cologne and Hanover
----------------------------------------------------

In 2019, Asterix and the AMPS system were deployed to the parcel center Eifeltor next to Cologne. The operation of the new electric Wiesel vehicle from KAMAG in combination with AMPS was possible after smaller adoptions. The container loading worked right from the start, but the loading dock approach was not precise enough under all circumstances. Goal poses of the docks were defined only by mapped GNSS measurements. Even with a high-end localization system, metal objects and walls around Asterix disturbed the radio signals of the satellites. These experiences led to the development of an active loading dock detection that is fused with the global goal pose. After 3 months of daily operation, Asterix and the AMPS system received very positive feedback from evaluation with multiple DHL test drivers. The fenced area of the parcel center was an ideal use case to gather first experiences in mixed traffic with robotic transportation system. Afterward, Asterix was also successfully tested at the freight section of DHL on a newly constructed parcel center without any adaptations of the system or environment [[3](https://www.sueddeutsche.de/wirtschaft/dienstleistungen-langenhagen-dhl-eroeffnet-neues-frachtzentrum-mit-290-beschaeftigten-dpa.urn-newsml-dpa-com-20090101-190913-99-862135)]. The open source package [Marv Robotics](https://gitlab.com/ternaris/marv-robotics) supported us in the creation of a bagfile database.

![﻿Datasets from the parcel center operation tests were crucial for further development of AMPS and higher levels of autonomy.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229887356-AQ62IGHFS3Q83ZOVEKIL/Pic+6.png)

Figure: **Datasets from the parcel center operation tests were crucial for further development of AMPS and higher levels of autonomy.**

![﻿LiDAR data of multiple containers and loading docks on the parcel center. Loading docks and containers can be detected with sufficient accuracy without artificial landmarks.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229932226-Q0YKEY281XV7WXGLQCQP/Pic+7.png)

Figure: **LiDAR data of multiple containers and loading docks on the parcel center. Loading docks and containers can be detected with sufficient accuracy without artificial landmarks.**

Simba, Asterix and Columbus for Industrialization of AMPS
---------------------------------------------------------

Based on customer feedback, data analysis methods and advanced robotic components test benches, a pre-series version of AMPS is in development. The design is focused to increase adaptability. Therefore, multiple vehicle types can be supported. Drivers of the DHL parcel centers will evaluate the system in daily operation. They will be supported by developers on demand, when the driver activates the remote access to the AMPS system. A precise absolute and relative localization is demanded for the precise maneuvering of the vehicle. The GNSS and IMU systems that have been used in the prototyping phase were too expensive and nontransparent. That's why in-house hardware and software designs have been done based on state-of-the-art electronic components. The system is called [Columbus](https://www.streetscooter.com/wp-content/uploads/2020/03/columbus_localisation_system.pdf). 

Simba, the virtual vehicle, got quite popular since most developers work remotely during the COVID-19 pandemic. The continuous integration testing framework runs multiple scenarios on a virtual parcel center. Since the LiDAR sensors can be simulated in the Gazebo simulation, the complete software stack is been tested closed-loop. Most errors in the software development can be detected, therefore, in this stage before deploying to the vehicle. In that way the validation of the software components is done in an automated and reproducible way with every new release.

![Vehicle, parcel center, LiDAR and Containers are simulated in detail for the test bench.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589229995244-BVW42EZ9VHISK61PS36Z/Pic+8.png)

Figure: *Vehicle, parcel center, LiDAR and Containers are simulated in detail for the test bench.*

Idefix, our Hardware-in-the-Loop test bench, is gone be refactored with industrial graded hardware. Software and hardware integration aspects like networking can be analyzed before working directly in the car. In combination with our virtual vehicle we created a virtual driver seat to drive AMPS inside the simulation on the actual hardware. Asterix is also been used to evaluate ROS2, industrial graded middlewares and operation systems. Challenges at the integration of new software frameworks on the target hardware are identified in an early development phase.

![Idefix gets new dresses. Mock-up designs in the simulation allows us in an early stage to evaluate new functionality with our customer.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1589230054916-WL1WZ2NEJZGGTX1TVYWF/Pic+9.jpg)

Figure: **Idefix gets new dresses. Mock-up designs in the simulation allows us in an early stage to evaluate new functionality with our customer.**

References:

[[1](https://github.com/Autonomous-Logistics)] 

<https://www.researchgate.net/publication/323105001_Prototyping_an_autonomous_delivery_vehicle>

[[2](https://www.missinglinkelectronics.com/www/images/LandingPage/FPGA4ADAS_2/9_Augspurger_StreetScooter_Open-Source-System-Prototyping-in-Autonomous-Logistics.pdf)] 

<https://www.missinglinkelectronics.com/www/images/LandingPage/FPGA4ADAS_2/9_Augspurger_StreetScooter_Open-Source-System-Prototyping-in-Autonomous-Logistics.pdf>

[[3](https://gitlab.com/ternaris/marv-robotics)] 

<https://gitlab.com/ternaris/marv-robotics>

+++

This was a guest article by [Deparment of Autonomous Logisitics of StreetScooter](https://github.com/Autonomous-Logistics)

(slightly updated - Text added - on May 18, 2020)


