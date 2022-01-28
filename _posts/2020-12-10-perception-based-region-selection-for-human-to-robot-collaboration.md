---
author: Jorge Nicho (SwRI)
comments: false
date: '2020-12-10 18:11:50+00:00'
slug: 2020-12-10-perception-based-region-selection-for-human-to-robot-collaboration
title: Perception-Based Region Selection for Human to Robot Collaboration
media_type: None
description: The need for robotic systems that can collaborate with humans on the
  factory floor is in demand by the manufacturing community, but collaborative ...
layout: post
old_sp_link: https://rosindustrial.org/news/2020/12/10/perception-based-region-selection-for-human-to-robot-collaboration
---

Background
----------

The need for robotic systems that can collaborate with humans on the factory floor is in demand by the manufacturing community, but collaborative robotic solutions are still lacking in many respects. One such problem appears in quality control of subtractive manufacturing applications, such as sanding, grinding, and deburring, where material from a part is removed using an abrasive tool until a desired surface condition is obtained. In such scenario, the quality of the finish can be assessed by an expert human operator and therefore it would be very advantageous to leverage this expertise so as to guide semi-automated robotic systems to work on the regions that need further work until the desired quality is achieved.
Given this challenge, this research focused on enhanced human-robot collaboration, by producing a capability that allows a human operator to guide the process by physically drawing a closed selection region on the part itself. This region will then be sensed by a vision system coupled with an algorithmic solution to crop out sections of the nominal process toolpaths that fall outside the confines of this region.

Approach
--------

Initially, a small dataset of hand-drawn closed-region images was produced in order to aid the initial development of the 2D contour detection method and projection into 3D. These images were made with a dark marker on white paper laying on a flat surface and imaged with the Framos d435 camera. The 2D contour method that resulted from this dataset was implemented with the OpenCV open-source library and comprised the following filters/method: grayscaling, thresholding, dilation, canny edge detection and contour finding. The output of this operation was the 2D pixel coordinates of the detected contours (Figures 1.a and 1.b).

![Figure 1a. amoeba 2d detection](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607620986688-X2FOAZMZ4HTVHA45IYWT/Figure+1.a+-+Amoeba+2D+detection.png.jpg)

*Figure 1a. amoeba 2d detection*

![Figure 1B. Box 2D Detection](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607621007889-YN9NKDD553AYFAKHEMD6/Figure+1.b+-+Box+2D+detection.png.jpg)

*Figure 1B. Box 2D Detection*

The following stage used the 2D pixel coordinates and located the corresponding 3D points from the point cloud associated with the image; this was possible because both the 2D image and point cloud were of the same size. Following that, some additional filters were applied, and adjacent lines were merged in order to form larger segments. In the final steps, the segments were classified as open open and closed contours and then normal vectors were estimated. Results are shown in Figures 2.a and 2.b.
Additional datasets were collected with varying conditions such as thicker, thinner lines, curved surfaces and multiple images containing parts of the same closed contour. These datasets allowed refining the method and addressed corner cases that emerged under more challenging conditions such as regions spanning multiple images (Figures 3.a, 3.b, 3.c).

![Figure 2a. trianble region detection](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607621076662-IGALVKPNWTX5K79OZ4WG/Figure+2.a+-+Triangle+Region+Detected.png.jpg)

*Figure 2a. trianble region detection*

![figure 2b. amoeba region detection](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607621115802-21BSOC4H98CNUFTUGYX5/Figure+2.b+-+Amoeba+Region+Detected.png.jpg)

*figure 2b. amoeba region detection*

![Figure 3a. Box Multi-image 2d contour](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607621165673-QJUA5ZY8GB3MPNI1SH1M/Figure+3.a+-+Box+Multi-Image+2D+Contour.png.jpg)

*Figure 3a. Box Multi-image 2d contour*

![figure 3b. Box multi-image 2d contour](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607621191419-6DM3C6RSI7SSYI5IK84P/Figure+3.b+-+Box+Multi-Image+2D+Contour.png.jpg)

*figure 3b. Box multi-image 2d contour*

![Figure 3c. Box Multi-image region detection](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1607621212971-7ICCB7MY7M5BBB5PFETC/Figure+3.c+-+Box+Multi-Image+Region+Detected.png.jpg)

*Figure 3c. Box Multi-image region detection*

Accomplishments
---------------

This research lead to the creation of an open-source C++ library that can be used to detect regions that have a similar need for human-robot collaboration. The repository can be found here <https://github.com/swri-robotics/Region-Detection>.

Furthermore, the work was featured as part of a recently ARM Insitute Project, with Spirit AeroSystems as prime investigator called Collaborative Robotic Sanding. An excerpt of that demonstration video highlighting the region detecion is included in the excerpt below.


