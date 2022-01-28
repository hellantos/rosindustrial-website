---
author: Guest User
comments: false
date: '2016-11-09 21:03:17+00:00'
slug: 2016-11-9-series-on-ros-industrial-development-process-code-review
title: Continuation of Series on ROS-Industrial Development Process - Code Review
media_type: None
description: This is the continuation of a multiple-post series detailing the ROS-Industrial
  software development process. The [first ...
layout: post
old_sp_link: https://rosindustrial.org/news/2016/11/9/series-on-ros-industrial-development-process-code-review
---



![](https://images.squarespace-cdn.com/content/v1/51df34b1e4b08840dcfd2841/1478725152486-S55SITFE0022J3HZR68V/image-asset.png)

This is the continuation of a multiple-post series detailing the ROS-Industrial software development process. The [first post](http://rosindustrial.org/news/2016/8/26/ros-industrial-development-process-contribution) in the series described the process of contributing code to the project (steps 1-3 in the figure above). This post is focused on the steps involved in reviewing code up to the point where is can be submitted for release as a ROS package. Note that the starred numbers in the outline correspond to steps in the software development process illustrated above.

4. When a Pull Request (PR) is issued there is the Travis Continuous Integrations (CI) step (step 4) which happens automatically in the background. The Travis CI performs several operations and if any of the steps below fail, then the PR is marked accordingly for the maintainer. Travis:

4. Installs a barebones ROS distribution on a fresh Ubuntu virtual machine.

8. Creates a catkin workspace and puts the repository in it.

12. Uses *wstool* to check out any from-source dependencies (i.e. other repositories).

16. Resolves package dependencies using *rosdep* (i.e. install packages using *apt-get*).

20. Compiles the catkin workspace

24. Runs all available unit tests

12. If the PR passes Travis CI and one of the maintainers is satisfied with the changes they post a +1 as a comment on the PR (step 5). The +1 signifies that the PR is ready to be merged all PR require at least one +1 and pass Travis CI before it can be merged.

16. The next step (step 6) is for the PR to be merged into the main branch. This is done through the GitHub web interface by selecting the "Merge pull request" button. After the PR is merged, all status badges are updated automatically.

20. Periodically the maintainer will release the package (step 7), which then gets sent to the ROS build farm for Debian creation (more on this next time).

Stay tuned for our final post in the series on steps 8-10 about Debian creation.
