---
author: Shaun Edwards (SwRI)
comments: false
date: '2016-08-26 22:30:28+00:00'
slug: 2016-8-26-ros-industrial-development-process-contribution
title: Series on ROS-Industrial Development Process - Contribution
media_type: None
description: We often receive questions from those unfamiliar with open-source development
  about what process we follow to ensure the quality of the ROS- ...
layout: post
old_sp_link: https://rosindustrial.org/news/2016/8/26/ros-industrial-development-process-contribution
---



![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1478726651499-GMNZ4FVVKA2JCRDWHJ9Y/image-asset.png)

Overview
========

We often receive questions from those unfamiliar with open-source development about what process we follow to ensure the quality of the ROS-Industrial software. The process we utilize (see figure above) is probably not that different from any large software project. The main differences being that the team is made up of many different stakeholder (for lack of a better term) and any stackeholder is welcome to contribute. With this open model, one might assume we have more checks in place to intercept "bad" contributions, but in practice that's not required. We utilize the same checks for our open source projects as we would for any project. Specifically, all code is verified at multiple steps in the process. Contributions from trusted sources as well as unknown sources are given the same level of scrutiny. This is the beginning a multiple-post series detailing the ROS-Industrial process, with our first post focusing on contributing software changes and fixes.

Contributing
============

ROS-Industrial is a community project. We welcome contributions from any source, from those who are extremely active to casual users. The following sections outline the steps on how to contribute to ROS-Industrial. It assumes there is an existing repository to which one would like to contribute (item 1 in the figure above) and one is familiar with the git "Fork and Branch" workflow, detailed [here](http://blog.scottlowe.org/2015/01/27/using-fork-branch-git-workflow/). 

1. Before any development is undertaken, a contributor would communicate a need and/or issue to the ROS-Industrial community. This can be done by submitting a bug to the appropriate github repo, the [issues repo](https://github.com/ros-industrial/ros_industrial_issues), or by emailing the [users group](mailto://swri-ros-pkg-dev@googlegroups.com). Doing so may save you time if similar development is underway and ensure that whatever approach you take is acceptable to the community of reviewers once it is submitted.
2. The second step (item 2 in the figure above) is to implement your change. If you are working on a code contribution, we highly recommend you utilize the [ROS Qt-Creator plugin](http://rosindustrial.org/news/2016/6/9/ros-qt-ide-plugin). Verify your change successfully builds and passes all tests.
3. Next, push your changes to a "feature" branch in your personal fork of the repo and issue a pull request (PR)(item 3). The PR allows maintainers to review the submitted code. Before the PR can be accepted, the maintainer and contributor must agree that the contribution is implemented appropriately. This process can take several back and forth steps (see [example](https://github.com/ros-industrial/motoman/pull/89)). Contributors should expect to spend as much time reviewing/changing the code as on the initial implementation. This time can be minimized by communicating with the ROS-Industrial community before any contribution is made.

Next week we will continue the series on the topic of ROS-I Maintainers…


