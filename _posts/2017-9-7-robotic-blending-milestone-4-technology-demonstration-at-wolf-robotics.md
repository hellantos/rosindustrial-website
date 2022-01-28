---
author: Matt Robinson (SwRI)
comments: false
date: '2017-09-07 17:04:21+00:00'
slug: 2017-9-7-robotic-blending-milestone-4-technology-demonstration-at-wolf-robotics
title: Robotic Blending Milestone 4 Technology Demonstration at Wolf Robotics
media_type: None
description: The Robotic Blending project is the first open source instantiation of
  what will become a general Scan-N-PlanTM framework (Figure 1). The project ...
layout: post
old_sp_link: https://rosindustrial.org/news/2017/9/7/robotic-blending-milestone-4-technology-demonstration-at-wolf-robotics
tags: ros-industrial ros-industrial-consortium ros
---

The Robotic Blending project is the first open source instantiation of what will become a general Scan-N-PlanTM framework (Figure 1). The project has been making steady progress over the past two and a half years.

![Figure 1. Execution of surface blending of a complex contour part on Wolf Robotics Demonstration Hardware in Fort Collins, CO.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504802835113-43TUD446L6PDN5U24Y0K/20170811_130651.jpg)

*Figure 1. Execution of surface blending of a complex contour part on Wolf Robotics Demonstration Hardware in Fort Collins, CO.*

Starting in earnest at the beginning of 2017, Milestone 4 (M4) sought to further the functionality of the technology to incorporate functionality that was of interest to the participating members. These members, 3M, Caterpillar, GKN Aerospace, Wolf Robotics, and the SwRI development team set forth to realize a set of objectives:

* Closed-loop inspection and retouch: Integrating the process planning and quality assurance steps so that parts are finished with a closed, sensor-driven loop.
* More Robust Surface Segmentation: Improving the surface segmentation and planning algorithms to accommodate more complex surfaces found on real parts (continuous surfaces with radius of curvature above a 50 mm threshold, as seen in Figure 1 above)
* Blending Process Refinement: Improving the quality of the blending process to produce surface finishes that meet engineering requirements.
* Edge Processing: Processing/chamfering simple 2.5D edges that occur where two surfaces meet.
* Technology Transfer: Meetings, demonstrations, and sponsor sites to support knowledge sharing among project participants and performers.
* Integration and Testing: Demonstration support.

The intent of the demonstration was to review the capability as-developed relative to the processing of provided Caterpillar production parts. Performance was tracked to a provided success criteria that tied to performance metrics that were relevant to the target application.

All parts presented were able to be perceived, meshed, and discrete parts for processing selected. There were difficulties with GUI interaction relative to selection, but these were considered minor.

Paths were generated for every part presented that included blending surface paths as well as the edge paths. Every path that was generated was simulated without issue.

Execution of the blending paths was performed on 100% of presented parts, and a subset of parts for edge processing. There were observed challenges due to the scale of the tools and media relative to the edge and execution of the paths without having issues with either collision or losing contact with the part. This is simply a need for finer calibration techniques for these particular hardware configurations.

Quality assurance (QA) paths were generated and simulated in all cases. False positives were prevalent and related to scatter/reflectivity, particularly for aggressive media combined with edges/corners on the parts. This is a common issue for laser-based sensors and spectral (shiny) surfaces, particularly along edges. Root cause was identified in detailed views of the scan data showing the scatter that exceeds the acceptance criteria of 0.5 mm.

For cases where slag was present to be identified the QA algorithm identified the slag and subsequent path plans were generated, displayed, and able to be simulated and executed, see Figure 2. In cases where there was no remaining slag and the finish was not high spectral the QA passed the part.

![Figure 2. Processed Part and Resultant QA that highlights non-compliant regions for re-processing](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504802742257-VHTG0NUIYL4XRDEAK3AF/QA+in+Process.jpg)

*Figure 2. Processed Part and Resultant QA that highlights non-compliant regions for re-processing*

Overall, the demonstration was considered a success, and follow on work is in the proposal development phase. The next steps for the team: First, consider establishing two test-sites where follow on development and testing can be performed. Second, evaluate functionality around these elements: work flow, path planning relative to perceived and characterized anomaly or feature, human mark/indication and plan, process refinement considering PushCorp functionality and 3M media, and finally Digital Twin elements to enable consistent performance between the two sites.

Additional information and videos highlighting the current capability will be available soon!

Latest updates to the packages can be found here:https://github.com/ros-industrial-consortium

Special thanks to the Robotic Blending M4 team members:

Schoen Schuknecht – 3M

JD Haas – 3M

Leon Adcock – Caterpillar

Prem Chidambaram – Caterpillar

Wajahat Afsar - Caterpillar

Chris Allison – GKN Aerospace

Richard Cheng – GKN Aerospace

Mike McMillen – PushCorp

Jonathan Meyer – SwRI

Austin Deric - SwRI

Alex Goins - SwRI

Lance Guyman – Wolf Robotics

Jason Flamm – Wolf Robotics

Zach Bennett – Wolf Robotics

Nephan Dawson – Wolf Robotics

![20170810_112452.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803475579-S17H2APDZQYVPAP1XM39/20170810_112452.jpg)

![DSC00150.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803613223-9UO706FBL6EPCMDF73H7/DSC00150.JPG)

![20170810_133709.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803492086-VW4Q4N13L4CPQ3KO8TU3/20170810_133709.jpg)

![20170810_142507.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803491369-RBNJ6CQ0EZX2NA25KLRK/20170810_142507.jpg)

![20170810_142515.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803507015-C5JML88D5RCGY62EQZHO/20170810_142515.jpg)

![20170810_153714.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803507272-7O0TMF6E86VRAYPSX40P/20170810_153714.jpg)

![20170810_155032.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803525357-BJH0DZI4DU5Z1GFPSWE8/20170810_155032.jpg)

![20170810_155338.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803527625-2LCSVLHX38LUER1UYZSJ/20170810_155338.jpg)

![20170811_092218.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803537847-7X3S09BPCVNSDKXX6VGJ/20170811_092218.jpg)

![20170811_104915.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803540956-WZ983KAEQ12KETYC6COP/20170811_104915.jpg)

![20170811_104927.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803554899-31KHPPTBWNRCBV6UXBKN/20170811_104927.jpg)

![20170811_105037.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803554753-MWC01Q8A2G5139HUHKDV/20170811_105037.jpg)

![20170811_105042.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803567101-WRQKQKN3MBDCTCN4KKYF/20170811_105042.jpg)

![20170811_105145.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803567143-7VLP1V3CKRJ318M0MYRO/20170811_105145.jpg)

![20170811_105508.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803572652-1X34ZN92N7F70UTA7HQ7/20170811_105508.jpg)

![20170810_112452.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803475579-S17H2APDZQYVPAP1XM39/20170810_112452.jpg)
![DSC00150.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803613223-9UO706FBL6EPCMDF73H7/DSC00150.JPG)
![20170810_133709.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803492086-VW4Q4N13L4CPQ3KO8TU3/20170810_133709.jpg)
![20170810_142507.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803491369-RBNJ6CQ0EZX2NA25KLRK/20170810_142507.jpg)
![20170810_142515.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803507015-C5JML88D5RCGY62EQZHO/20170810_142515.jpg)
![20170810_153714.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803507272-7O0TMF6E86VRAYPSX40P/20170810_153714.jpg)
![20170810_155032.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803525357-BJH0DZI4DU5Z1GFPSWE8/20170810_155032.jpg)
![20170810_155338.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803527625-2LCSVLHX38LUER1UYZSJ/20170810_155338.jpg)
![20170811_092218.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803537847-7X3S09BPCVNSDKXX6VGJ/20170811_092218.jpg)
![20170811_104915.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803540956-WZ983KAEQ12KETYC6COP/20170811_104915.jpg)
![20170811_104927.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803554899-31KHPPTBWNRCBV6UXBKN/20170811_104927.jpg)
![20170811_105037.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803554753-MWC01Q8A2G5139HUHKDV/20170811_105037.jpg)
![20170811_105042.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803567101-WRQKQKN3MBDCTCN4KKYF/20170811_105042.jpg)
![20170811_105145.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803567143-7VLP1V3CKRJ318M0MYRO/20170811_105145.jpg)
![20170811_105508.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1504803572652-1X34ZN92N7F70UTA7HQ7/20170811_105508.jpg)

