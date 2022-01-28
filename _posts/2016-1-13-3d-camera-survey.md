---
author: Guest User
comments: false
date: '2016-01-18 20:43:12+00:00'
slug: 2016-1-13-3d-camera-survey
title: 3D Camera Survey
media_type: None
description: Due to the activity and interest on this topic, an [updated permanent
  page](https://rosindustrial.org/3d-camera-survey/) has been created under ...
layout: post
old_sp_link: https://rosindustrial.org/news/2016/1/13/3d-camera-survey
---

Due to the activity and interest on this topic, an [updated permanent page](https://rosindustrial.org/3d-camera-survey/) has been created under the developer heading in the banner!

The recent availability of affordable ROS-compatible 3D
sensors has been one of the fortunate coincidences that
has accelerated the spread of ROS. Since the popular the
ASUS Xtion Pro Live has been intermittently stocked, check out the field of ROS-compatible 3D sensors to review the contenders.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1452893038763-AEUOZGNT1MQBDMZYDQDR/image-asset.jpeg)

ASUS® XtionPro™ Live
--------------------

**Type:** Structured light  

**Depth Range:** 0.8 to 3.5 m  

**3D Resolution:** 640 x 480  

**RGB Resolution:** 1280 x 1024  

**Frame Rate:** 30 fps  

**Latency:** ~1.5 frames  

**FOV:** 58° H, 45° V  

**Physical dims:** ~180x40x25 mm (head)  

**Interface:** USB 2.0  

[Link to ROS Driver](http://structure.io/openni)  

**Notes:** Similar internals to the Xbox Kinect 1.0.
Intermittent availability for purchase.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1452895033752-A7YPJJPKZ5TX7AUJGU14/image-asset.jpeg)

Microsoft® Kinect™ 2.0
----------------------

**Type:** Time of flight  

**Depth Range:** 0.5 to 4.5 m  

**3D Resolution:** 512 x 424  

**RGB Resolution:** 1920 x 1080  

**Frame Rate:** 30 fps  

**Latency:** 20 ms minimum  

**FOV:** 70° H, 60° V  

**Physical dims:** ~250x70x45 mm (head)  

**Interface:** USB 3.0  

[Link to ROS Driver](https://github.com/code-iai/iai_kinect2)  

**Notes:** Latency with ROS is multiple frames.  

Active cooling.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1453132259456-VY5E0J2BY5JIMEQPHFIC/image-asset.png)

[Intel RealSense R200](https://software.intel.com/en-us/articles/realsense-r200-camera)
---------------------------------------------------------------------------------------

**Type:** Stereo with pattern projector  

**Depth Range:** 0.6 – 3.5 m  

**3D Resolution:** 640 x 480  

**RGB Resolution:** 1920 x 1080  

**Frame Rate:** 60 fps (3D), 30 fps (RGB)  

**Latency:** 1 frame  

**FOV:** 59° H, 46° V  

**Physical dims:** 102x9.5x7 mm  

**Interface:** USB 3.0  

[Link to ROS Driver](https://github.com/PercATI/RealSense_ROS)  

**Notes: Outdoors capable.**

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1453132702061-G9MGEY6UY6IZKDGN0RYP/image-asset.png)

[IFM® Efector™ O3D303](http://www.ifm.com/products/us/ds/O3D303.htm)
--------------------------------------------------------------------

**Type:** Time of flight  

**3D Resolution:** 176 x 132  

**RGB Resolution:** N/A  

**Depth Range:** 0.3 to 8 m  

**Frame Rate:** 25 fps  

**Latency:** 1 frame  

**FOV:** 60° V, 45° H  

**Physical Dims:** 120x95x76 mm  

**Interface:** Ethernet  

[Link to ROS Driver](https://github.com/lovepark/o3d3xx-ros)  

**Notes:** Accuracy +/-4 mm. IP65/67 industrial enclosure.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1453144040529-2J2UO3HUCST5Y2GYMAYC/image-asset.jpeg)

[Stereolabs® ZED™](https://www.stereolabs.com/zed/specs/)
---------------------------------------------------------

**Type:** Embedded stereo  

**3D Resolution:** 2208 x 1242 max  

**RGB:** 2208 x 1242 max  

**Depth Range:** 1.5 to 20 m  

**Frame Rate:** 15 fps at max res., 120 fps at VGA res.  

**Latency:** 1 frame  

**FOV:** 96° H, 54° V  

**Physical Dims:** 175x30x33 mm  

**Interface:** USB 3.0  

[Link to ROS Driver](https://github.com/stereolabs/zed-ros-wrapper)  

**Notes:** Latency not confirmed.

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1453145149616-XOB1M693VGGYDUI5SQLO/image-asset.jpeg)

[Carnegie Robotics® MultiSense™ S7](http://files.carnegierobotics.com/products/MultiSense_S7/MultiSense_Stereo_brochure.pdf)
----------------------------------------------------------------------------------------------------------------------------

**Type:** Embedded stereo  

**3D Resolution:** 2048 x 1088  

**RGB Resolution:** 2048 x 1088 max (7.5 fps)  

**Depth Range:** 0.4 m to infinity  

**Frame Rate:** 15 fps at 2048 x 544  

**Latency:** 1 frame  

**FOV:** 80° H, 45° V  

**Physical Dims:** 130x130x65 mm  

**Interface:** Ethernet  

[Link to ROS Driver](https://bitbucket.org/crl/multisense_ros)  

**Notes:** IP68 enclosure.  

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1453145129935-T0LKOZ2AOO4RRH29VY9T/image-asset.png)

[Ensenso® N35-606-16-BL](http://www.ensenso.com/support/modellisting/?id=N35-606-16-BL)
---------------------------------------------------------------------------------------

**Type:** Structured light  

**3D Resolution:** 1280 x 1024  

**RGB:** 1280 x 1024  

**Frame Rate:** 10 fps  

**Latency:** 1 frame  

**FOV:** 58° H, 52° V  

**Physical Dims:** 175x50x52 mm  

**Interface:** Ethernet  

[Link to PCL/ROS Driver](https://github.com/PointCloudLibrary/pcl/blob/a654fe4188382416c99322cafbd9319c59a7355c/io/src/ensenso_grabber.cpp)  

**Notes:** Many other resolutions and FOVs available. IP65/67 enclosure available.  

![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1453149133620-9E2F7A2WPTQ6EPDIRJDO/image-asset.png)

[SICK® Visionary-T™](https://sick-virginia.data.continum.net/media/dox/3/33/433/Product_information_3vistor_T_3D_Snapshot_For_versatile_use_indoors_en_IM0062433.PDF)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Type:** Time of flight  

**3D Resolution:** 144 x 176  

**RGB:** N/A  

**Frame Rate:** 30 fps  

**Latency:** 66 msec  

**FOV:** 69° H, 56° V  

**Physical Dims:** 162x93x78 mm  

**Interface:** Ethernet  

[Link to ROS Driver](http://wiki.ros.org/sick_visionary_t_driver)  

**Notes:** IP67 enclosure  

![Tara-Stereo-Vision-USB3-Camera.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1479593100039-2TIB47VWMZO4WZEWWV0Q/Tara-Stereo-Vision-USB3-Camera.jpg)

[e-Con Systems Tara Stereo Camera](https://www.e-consystems.com/3D-USB-stereo-camera.asp)
-----------------------------------------------------------------------------------------

**Type:** Embedded Stereo Camera  

**3D Resolution:** 752 x 480  

**RGB:** N/A  

**Frame Rate:** 60 fps  

**Latency:** 1 Frame  

**FOV:** 60° H  

**Physical Dims:** 100x30x35 mm  

**Interface:** USB 3.0  

[Link to ROS Driver](https://github.com/dilipkumar25/see3cam)  

**Notes:** Inbuilt IMU  

![karmin-front.jpg](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1479593852801-ZQLCNNDL67Y1F4ZO0BZ3/karmin-front.jpg)

[Narian SPI](https://nerian.com/products/sp1-stereo-vision/)
------------------------------------------------------------

**Type:** FPGA Stereo Camera  

**3D Resolution:** 640 x 480  

**RGB:** N/A  

**Frame Rate:** 30 fps  

**Latency:** 1 Frame  

**FOV:** Variable  

**Physical Dims:** 105x76x36 mm  

**Interface:** USB 2.0 to cameras, Gigabit Ethernet to Host  

[Link to ROS Driver](http://wiki.ros.org/nerian_sp1)  

**Notes:** Resolution up to 1440 x 1072  


