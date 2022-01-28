---
author: Shaun Edwards (SwRI)
comments: false
date: '2015-08-07 20:57:03+00:00'
slug: 2015-7-27-announcing-profinet-support
title: Announcing PROFINET Support
media_type: None
description: Hardware interfaces are particularly important for any future integration
  of ROS-Industrial with production systems. With already existing ...
layout: post
old_sp_link: https://rosindustrial.org/news/2015/7/27/announcing-profinet-support
---



Hardware interfaces are particularly important for any future integration of ROS-Industrial with production systems. With already existing [EtherCat](http://wiki.ros.org/soem) (maintained by [Intermodalics](http://www.intermodalics.eu/)) and [CanOpen](http://wiki.ros.org/ros_canopen) (maintainted by [Fraunhofer IPA](http://www.ipa.fraunhofer.de/)) networks, we are happy to announce support for [PROFINET](http://www.profibus.com/technology/profinet/), as one of the most widely used fieldbuses in automation world.

PROFINET, an open automation standard and part of IEC 61158 is not only fully compatible with all the features of standard Ethernet, but it is also capable of real-time performance. It enables high-speed data exchange for the entire range of automation applications. PROFINET uses three communication services (Standard TCP/IP, Real Time, Isochronous Real Time), which can be used simultaneously, allowing transfers of both input/output data within submilisecond cycle times. To access all the features of PROFINET, use of specialized hardware is necessary. There are various PROFINET PCI cards on the market. We decided on the communication processor [CP1616](http://w3.siemens.com/mcms/industrial-communication/en/ie/system-interfacing/system-interfacing-pg-pc/cp1616/pages/cp1616.aspx) from Siemens, since it provides not only Linux compatible drivers, but support for IO Controller/IO Device modes. This allows ROS-Industrial to work as both - a master or a slave on PROFINET network.

The goal of current development is to define a ROS-PROFINET abstraction layer and provide a specific implementation for the CP1616. The package release date is targeted for September.

Special thanks to the [Google Summer of Code](http://www.google-melange.com/gsoc/homepage/google/gsoc2015) program for supporting this effort. Additional thanks to Siemens for technical support. Software development is ongoing and can be found in the ROS-Industrial Siemens experimental [repo.](https://github.com/ros-industrial/siemens_experimental)


