---
author: Matt Robinson (SwRI)
comments: false
date: '2018-09-28 16:59:20+00:00'
slug: 2018-9-28-imts-2018-leveraging-open-standards-and-technologies-to-re-imagine-interoperability-within-factories
title: IMTS 2018 – Leveraging Open Standards and Technologies to Re-Imagine Interoperability
  within Factories
media_type: None
description: The International Manufacturing Technology Show ([IMTS](https://www.imts.com/))
  held in Chicago brings
layout: post
old_sp_link: https://rosindustrial.org/news/2018/9/28/imts-2018-leveraging-open-standards-and-technologies-to-re-imagine-interoperability-within-factories
---

The International Manufacturing Technology Show ([IMTS](https://www.imts.com/)) held in Chicago brings
together technology solution providers, innovators, thought leaders and
interested parties seeking to leverage innovations, and improved capabilities to
impact their operations and bottom line. The IMTS 2018 Emerging Technology
Center (ETC), hosted by the Association for Manufacturing Technology ([AMT](http://www.amtonline.org/)), a
team consisting of [Southwest Research Institute](https://www.swri.org/industries/manufacturing-technologies), AMT, and [Vimana](https://govimana.com/) presented a
practical demonstration showing a NIST grant-funded initiative leveraging open
technologies to [facilitate interoperability between manufacturing equipment team
members](https://rosindustrial.org/news/2017/12/18/nist-grant-helping-enhance-ros-industrial-interoperability-with-mtconnect). The demonstration was supported by [Hurco Companies](http://www.hurco.com/pages/default.aspx), [Hexagon
Manufacturing Intelligence](https://www.hexagonmi.com/en-US), and [Universal Robots](https://www.universal-robots.com/). The intent was to show how a
new version of the [previously developed ROS-to-MTConnect bridge](https://youtu.be/IWXMMjI2LtI) can be extended
along with an extended MTConnect architecture, to enable a many-to-many
interoperability that seeks to enable more intelligent interoperability.

![Figure 1. Demo at the ETC at IMTS](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1538153098755-N2FJOQ8DV2QZN2JSIMQI/ca4255090df89cf67b538915f3f8c649.jpgFigure)

*Figure 1. Demo at the ETC at IMTS*

[MTConnect](https://www.mtconnect.org/) is an open, royalty-free standard intended to foster greater
interoperability between controls, devices and software applications, by
publishing structured data over networks, using the TPC/IP. The initial project,
mentioned above, demonstrated the ability to implement ROS-Industrial to enable
the execution of robot paths and use the MTConnect protocol for communications
between the robot and a CNC machine tool. Similar to the previous effort, this
new solution is primarily software based and leveraged the open standard
application level protocol, MTConnect, and the open source Robot Operating
System (ROS) Industrial to enable facility-level interoperability between robot
teams and machine-cell devices.

The expansion of the previous ROS/MTConnect solution, further enhances the
viability of using industry supported open source software for smart
manufacturing applications. Open source software permits a continuation of free
development, over a very large development workspace that ultimately solves
complex problems where the solution is free to the end user. The output from
this project is intended to enable industry-wide adoption of open source
technologies, by providing a use-case and testbed showcasing lower cost
solutions for comprehensive factory floor integration for the small- and
medium-sized manufacturer. In parallel, it is anticipated that this work will
foster and/or inspire other solution providers to incorporate this approach to
leverage and incentivize both the leverage of open standards/open source as well
as further refine their capabilities to align with the vision further moving the
ball forward, enabling a future state where dynamic agile execution may be
realized.

At IMTS
-------

demonstration at IMTS was intended to show the type of operation or
intelligence that may be deployed by leveraging this new approach to
interoperability. As seen in Figure 2, the intent is to enable a robot,
leveraging ROS/ROS-Industrial, to communicate with other types of manufacturing
equipment that already take advantage of the MTConnect standard, as far as
communicating what they are doing.

![Figure 2. Robot able to "understand" what the other team members need and/or are doing.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1538153193555-H9PKYOKKOEC1YOI7EFE8/b4b41fdb4b288b9b0be545e17fb90dc3.png)

*Figure 2. Robot able to "understand" what the other team members need and/or are doing.*

We are also demonstrating the ability of a robot to perform more than material
handling tasks. The robot can also tend the machines' need for a replacement
tool or a coolant change. The MTConnect standard is providing the language to
allow the equipment to express its needs, from the movement of material to the
maintenance tasks required to keep the cell at top performance. The architecture
for device orchestration and collaboration provides the framework for allowing
multiple manufacturing processes to coordinate their activities to complete a
task. The task-based models and the coordinator models can be seen in Figure 2.
This architecture enables the ROS-I platform to provide the ability for the
robot to find optimal ways to dynamically move material and other assets where
they need to be.

This framework is inherently extensible. For instance, industrial AI will be an
essential addition to future capability, enabling the notion of autonomous,
continuous improvement or dynamic optimization through learning. Plans can be
previewed as conditions change and subject matter experts that choose to
intervene to ensure consistency in value stream performance can also be
additional input into this Industrial AI capability.

![Figure 3. State Model Architecture](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1538153250871-TFXRQN324TLTESEMU9QW/663c497dbf691712433e182a599b6e03.jpg)

*Figure 3. State Model Architecture*

Along with this software and supporting architecture will be a simulation test
environment. This will enable testing of various scenarios. Within the scope of
the current project is testing the scalability of the current developed state
that was developed at IMTS 2018. This will include multi-robot scenarios to
ensure the software and architecture support these use cases and of course
support future iterations as we seek to extend the capability beyond one robot
servicing to, say, one or two fixed assets.

![Figure 4. Simulation Environment](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1538153297286-IJBCZ3K1BDFEJ3TGON54/57e5680041160a7baf500d5f9abe7e27.png)

*Figure 4. Simulation Environment*

Both the software and the virtual test environment will be made fully open
source with documentation. In parallel, the team is excited to see test beds
assembled to enable further testing with hardware in the loop supported by
additional research, non-profit, and even for-profit entities. The goal is to
enable a future state where dynamism may be managed on-the-fly by enabling
intelligent devices to effectively share information and act on it, both
leveraging information from order to deliver systems, best practice rules, along
with developments around industrial AI noted above. As we move forward towards
smart, agile manufacturing, and we reduce the risk of inventory and static
supply chains. Our ability to rapidly deploy equipment and repurpose it will be
vital to expanding our industry and allowing for more customization and
productivity.

![Figure 5. Multi-robot agility and self-optimization and organization](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1538153343052-MTM1AIKXNQQOIO7RQ9JT/3461ff9a491f555e2bfb0ba65095ee25.jpg)

*Figure 5. Multi-robot agility and self-optimization and organization*

What was the reception at IMTS 2018?
------------------------------------

Overall, there were a lot of questions regarding the scope of the work: what it means, when is it available, and how do average end-users take advantage?

The ETC was covered by team members from all organizations that contributed, and each brought a different perspective to what may be realized, what we would like to see next, and what specifically they heard from those they spoke with at the ETC.

Shaurabh Singh of AMT provided his insights:

*> "The ETC cell was received very well. Many were appreciative of the non PLC distributed cell concept. A couple of them had a centralized master control in their cells and were stuck as their engineer who configured it had left. The peer-to-peer network-based interaction between different cell equipment was an attractive solution to them. For a lot of them it was about getting aware of different capabilities of MTConnect and ROS. Engineers asked a lot of technical questions including about MTConnect Interfaces Pub-Sub implementation, flexible collaboration models and edge computing/intelligence. On one hand, people were interested in the machine intelligence and task priority abstraction; on the other hand, they asked questions about low-level ROS dynamic path planning. Most of them were interested in where the project was headed and when it would get into the market. A lot of discussions were also on the ERP-machine level integration, process planning, part specifications and machine capabilities which are already ongoing parallel development in the MTConnect Standard Committee."*

![Figure 6. Crowd Visiting the ETC demonstration](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1538154000054-S7NG2YLY8BOT617MW0N7/1964b6558d625850982ebd4c9b646c3f.jpg)

*Figure 6. Crowd Visiting the ETC demonstration*

![](https://github.com/mtconnect/ros_mtconnect_2_demo)

Josh Langsfeld of SwRI, Lead ROS Software Developer:

*> "I thought the response to the project and the technology was quite positive. It was interesting to see the widely varying perspectives different people had when seeing our demo. Some were just interested in the idea of a robot doing machine tending at all while others were more interested in how the CMM could automatically get its output to change the CNC program. People who were aware of MTConnect and had used it before were excited about its potential for defining tasks between multiple devices. I think the idea of having mobile robots servicing and tending to a whole factory floor of various machines on demand was an especially compelling vision for how this technology can be put to practical use. We have a long way to go before reaching that, especially on the robot side since we'll have to really make use of and scale up some of the advanced planning and sensing capabilities of ROS-I. The potential is definitely there though, and I'm excited to see how this work continues to develop in the future."*

Matthew Powelson of SwRI, ROS Developer and Integration/Debug:

*> "I think the reception on the whole was good. Several people were excited about it, and said things like "can you help me do this?" or "my customers really want this." People really seemed to like this idea of doing cool demos like they saw in the Fanuc booth, but doing it without having to buy all yellow robots because we are using open standards and open code. However, there were some outliers that I think are important. First, I remember one representative from a robot OEM say that this kind of open code would commoditize machine tools, and that was their biggest fear. Another man didn't like the idea of decentralized intelligence. He described some of the projects he had worked on over his 25-year career and just said that "one centralized controller isn't really that bad." Shaurabh Singh, of AMT, make a good point about how this manufacturing space is going through the same sort of transformation that the IT space did 10 years ago, where you see established companies like Microsoft now releasing code open source because it actually makes things*> more *> accessible and safe – not less. Open software and open standards have obvious advantages to the end user, but we still need to keep making the case to the OEMs."*

I think the team's insights are interesting and my interactions with those that came by the ETC were very similar. It was exciting to interact with such a diverse audience, in the context of what their business is, what they sell or are looking to buy, and/or where they operate or are based. This diversity is part of the challenge when we talk about simpler interoperability, the simple "plug it in and it works". I believe this is a simple, compelling, yet "lot to do" vision, and I hope you will stay engaged as this work moves forward.

We will seek to have all the software open source by the end of October 2018 in the MTConnect GitHub repository. There are plans to have a physical test bed established so that both industry interested parties as well as NIST and other research organizations can continue to further the capability. Please let us know if you have any questions, or would like to learn more. A detailed final report as well as follow-on presentations will be upcoming, and we will announce those via our typical communication vehicles. In the meantime, please keep the dialog going. We always look forward to questions and feedback!

UPDATE!

The software and the demonstration simulation are now available over at:

* Source Code: <https://github.com/mtconnect/ros_mtconnect_2>
* The Demo: <https://github.com/mtconnect/ros_mtconnect_2_demo>

