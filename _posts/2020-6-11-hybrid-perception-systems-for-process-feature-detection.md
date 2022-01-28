---
author: Guest User
comments: false
date: '2020-06-11 17:16:21+00:00'
slug: 2020-6-11-hybrid-perception-systems-for-process-feature-detection
title: Hybrid Perception Systems for Process Feature Detection
media_type: None
description: In the past years, Southwest Research Institute has used ROS Industrial
  tools to
layout: post
old_sp_link: https://rosindustrial.org/news/2020/6/11/hybrid-perception-systems-for-process-feature-detection
---

In the past years, Southwest Research Institute has used ROS Industrial tools to
integrate numerous Scan-N-Plan surface finishing applications. A typical
application involves reconstructing the environment, generating raster paths on
some unwieldy curved surface, and then executing that path using an industrial
manipulator carrying some process tool like a sander or spray nozzle. Automating
these tasks is often hugely value-added as they can often be difficult and
dangerous for humans to perform.

However, generalizing this concept a bit more beyond rasters on curved surfaces,
industrial applications abound where some generic process is applied to some
feature. Examples include grinding flashing from a steel casting, applying
sealant to a seam, or smoothing a wrinkle in a composite layup. While each of
these applications involve numerous complications, the first step is the same.
Some feature must be detected in 3D space.

![Example of a flashing removal application where only part of the surface requires grinding](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1591887527323-GQGQIPISHS1IIR83ONDA/flash.png)

Figure: ***Example of a flashing removal application where only part of the surface requires grinding***

When thinking about how to detect these features, machine learning is often considered. While machine learning sometimes poses a potential solution to these problems, this can be plagued by a few issues. First, machine learning is progressing quickly. An algorithm developed in Caffe, Torch, or Theano only a few years ago may be difficult to maintain or deploy today and need to be ported to Tensorflow or PyTorch. Thus, any robotics system that uses these approaches should be flexible enough to use any of these frameworks. Second, while semantic segmentation for 2D images is a relatively mature field, performing these operations in 3D space is much newer, requiring more computationally expensive algorithms and annotation of 3D data. While these challenges are certainly known to the machine learning community, they have limited adoption in industrial applications where dataset availability is limited and robotics integrators have day jobs that don't involve AI research.

![Experimental Lab Setup for high mix welding application](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1591887606957-QF0VQTC8XRBJE3E70YAL/cell.jpg)

Figure: *Experimental Lab Setup for high mix welding application*

To address these challenges, the ROS Industrial team at Southwest Research Institute proposes a hybrid approach to 3D perception systems wherein mature 2D detectors are integrated into a ROS 3D perception pipeline to detect process features and enable the flexibility to upgrade the detector without any modifications to the rest of the system.

The principal is simple. Often in industrial applications 3D perception data (i.e. point clouds) comes from 3D depth cameras that provide not only depth information but also a 2D video stream (<https://rosindustrial.org/3d-camera-survey>). By using open source ROS tools, we can use the 2D video stream to detect the features we want and project them back to the 3D data. We can then aggregate those detected features over the course of a scan in order to get a semantically labelled 3D mesh. This allows toolpaths to then be generated on the mesh that are informed by the detected process features. In order to evaluate such an approach, an example high-mix fillet welding application was developed where each part was a set of tack welded aluminum plates, but their exact size and location was unknown.

![Left column shows 2D image and detected weld seam. Right column shows 3D mesh and aggregate 3D detected weld seam. Notice that the 2D detector was trained to avoid welding additional brackets and clamps.](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1591888229719-VHY6INY4YTKO48L00PEF/Output+Composite.JPG)

Figure: *Left column shows 2D image and detected weld seam. Right column shows 3D mesh and aggregate 3D detected weld seam. Notice that the 2D detector was trained to avoid welding additional brackets and clamps.*

The system makes use of open source ROS tools and proceeds as follows. First, the camera driver provides a colorized point cloud to the TSDF Node (from yak\_ros, <https://github.com/ros-industrial/yak_ros>) which reconstructs the environmental geometry. Simultaneously, point cloud annotating node (<https://github.com/swri-robotics/point_cloud_segmentation>) extracts a pixel aligned 2D image from the point cloud and sends it across a ROS service to the arbitrary 2D detector (in this case FCN8) which returns a mask with a label for each pixel in the image. These labels are then used to annotate the point cloud by re-colorizing it. By doing so, these results can be aggregated using the open source octomap\_server (<http://wiki.ros.org/octomap_server>). At the end of the scan, YAK provides a 3D mesh of the environment and octomap provides an octomap colorized with the semantic labels. Tesseract (<https://github.com/ros-industrial-consortium/tesseract>) collision checking interfaces can then be used to detect the voxels associated with each mesh triangle, allowing the geometric mesh to be annotated with semantic data. In this case, the areas non marked as "weldable" were removed and a region of interest mesh was passed to the tool path planning application. The final architecture diagram is shown below.

![Architecture Diagram of the components of the system](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1591888053332-HL030CDLHTNG7OAED06G/node.png)

Figure: *Architecture Diagram of the components of the system*

The result can be seen in the video below. While this approach has its limitations, overall it performed well. We look forward to deploying systems like this in the future to further explore its capabilities. 

Currently the point cloud segmentation library is still under development, but we believed there was value in making the industrial open-source community aware now to provide additioanl insight and feedback. In the future we anticipate this migrating to the ROS-Industrial family of repositories.


