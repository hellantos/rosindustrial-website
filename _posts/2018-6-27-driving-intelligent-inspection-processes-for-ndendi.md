---
author: Matt Robinson (SwRI)
comments: false
date: '2018-06-27 21:28:58+00:00'
slug: 2018-6-27-driving-intelligent-inspection-processes-for-ndendi
title: Driving Intelligent Inspection Processes for NDE/NDI
media_type: None
description: Nondestructive evaluation (NDE) techniques for parts and structures that
  are created from either forming processes or additively manufactured ...
layout: post
old_sp_link: https://rosindustrial.org/news/2018/6/27/driving-intelligent-inspection-processes-for-ndendi
---

Nondestructive evaluation (NDE) techniques for parts and structures that are created from either forming processes or additively manufactured processes typically have had to be manually performed. Recent advances in scanning technologies and intelligent path planning tools, such as those available within ROS -Industrial, present a platform capable of performing multiple NDE processes in an intelligent fashion leveraging the Scan-N-Plan framework.

[The Sensors Systems & Nondestructive Evaluation team](https://www.swri.org/industries/sensors-systems-nondestructive-evaluation-nde) within Southwest Research®, along with ROS-Industrial developers have conceived of a concept to enable a Scan-N-Plan approach to Nondestructive Inspection (NDI) thereby reducing the amount of inspection time by only performing detailed surface or volumetric inspections where mandated by an initial higher level screening.

The Sensors Systems & Nondestructive Evaluation team has developed a unique technology within their portfolio that performs full volumetric inspection using a guided wave technique that leverages an omni-directional probe. The concept would be to perform a macro-level scan leveraging the [MsT360 Guided Wave Sensor](https://www.swri.org/sites/default/files/brochures/mst360-guided-wave-omnidirectional.pdf), analyzing the output and for indications, or areas of interest, drive low level inspection. A sample output from this stationary sensor can be seen below. This output can then be leveraged to generate process paths for follow on inspections such as Eddy Current (EC) or Ultrasonic Testing (UT), only in the areas of interest. This provides the full volumetric inspection output, but reduces the time spent doing a 100 percent surface scan with higher resolution traditional UT. This improves solution velocity as well as reduces post-processing clean up. 

Based on experience with the MsT360 follow-on low level inspection techniques can be selected based on the characterized potential defect. The system would then Plan trajectories based on this scan for each process, including the stand-off or contact forces and trajectories mandated by the process. A map could be visualized and colored to aid the operator in understanding which regions will be inspected by which NDE process. In the below example for instance, a process would be planned for the area identified with the 35% wall area, or where weld 1 and 2 are located, as opposed to UT or EC of the entire volume or surface respectively.

![Scan output.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530134558303-WG34FVATNEQXWNK5L66I/Scan+output.JPG)

Sample output from MsT360

A sample workflow for this type of operation would be as such:
• Assembly or Piece within a robotic system is ready for NDE Assessment
• Locate MsT360 Guided Wave Sensor (Manually or Robotically)
• Perform macro volumetric inspection
• Analyze output
• For areas of concern plan trajectories for each process type (EC or UT) and execute inspection in the areas of interest
• Tool Change
• Perform inspection
• Tool Change if required
• Clean
• Generate Report; either unload or launch a repair process

The flexibility inherent to this design and the capability included enable processing of piece-parts, such as forms, as well as fabricated structures. The macro scan and detailed path planning approach is more efficient for when it is not inherently value added to inspect an entire volume or surface area. 

![Planned Region.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530134578111-C6DO0FVYE0ZNA386O5HA/Planned+Region.JPG)

As can be seen in the above image, specific regions can be highlighted based on an output such as described earlier, or these can be user adjusted based on a response from a developed GUI. These trajectories can be planned for all the processes of interest, in this case UT and EC, with their requirements relative to process execution included. 
Leveraging the flexibility of the Scan-N-Plan framework it is easy to see how NDE processes can either be included into a multi-process cell, or just automated in a manner that effectively applies them where required, or where that detailed scrutiny is most beneficial. Furthermore, this can be augmented with visual imaging to allow for assessment of human readable details , or human generated markings to drive further process planning and inspection. For future consideration as well are several visual NDE techniques for surface inspection that could be incorporated, such as dye penetrant, magnetic particle, pulsed thermography, etc.

![Human Markings.JPG](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1530134635694-AZCHK4CF8FWPXTWSBJRE/Human+Markings.JPG)

Example of Identification and Tool Path Plans for a Human Generated Indication

As advances in both inspection technologies and automation move forward there lie the opportunities to more tightly couple these processes, and optimize their effectiveness in the areas of greatest need. This enables more efficient utilization while optimizing cost and throughput, as well as reducing non-value-added steps that currently come with many of the NDE techniques. Moving forward we hope to see more opportunities for integrated quality evaluation within automation applications, enabling further optimization of manufacturing value streams. For more information about SwRI's NDE solutions please visit: <https://www.swri.org/industries/sensors-systems-nondestructive-evaluation-nde>


