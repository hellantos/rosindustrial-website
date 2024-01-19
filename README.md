# ROS-Industrial Website



## Installing local dependencies
Follow these [instructions](https://jekyllrb.com/docs/installation/ubuntu/).

## Building locally
In file `_config.yaml` comment the prefix line and save.
First time after repo download probably do:
```
bundle install
```

Then use jekyll to build:

```
bundle exec jekyll serve
```

## Adding a contributer

Add a .md file with the following contents under `_people/` and add a mugshot under `assets/mugshots`. Files should be named as the contributer with dashes as separators. 

```
---
name: [Contributer name]
position: [Contributer position]
image: /assets/mugshots/[mugshot file]
---
short cv
```

## Adding a package
Add a .md file with the following contents under `_packages/`. Files should be named as the package with dashes as separators. 

```
---
name: [package name - should be easy to understand]
description: [description]
category: [Driver| Automation Tool| Motion Tool | Development Tool]
repo: [link to reop]
ros1: [y|n]
ros2: [y|n]
level: [2 - Consortium & Vendor | 1 - Vendor | 0 - Community]
---
```

## Adding a member
Add a .md file with the following contents under `_members/` and a logo under /assets/member-logos/. .md Files should be named as the package with dashes as separators. 

```
---
name: [Organisation]
type: [Type]
logo: /assets/member-logos/logo_[Organisation].png
---
[Description]
```

## Adding a training
Add a .md file with the following contents under `_trainings/` and an image under /assets/images/. Files should be named as the package with dashes as separators. 

```
---
title: [title]
organiser: [Organiser]
image: /assets/images/[image]
description: [description]
contact: [contact]
mail: [mail]
---
```

## Adding an event
Add a .md file with the following contents under `_events/` and an image under /assets/images/. Files should be named as the event with date as suffix with dashes as separators. 

```
---
organiser: [Organiser]
comments: false
start_date: [e.g. 2022-06-06 09:00:00+00:00]
end_date: [e.g. 2022-06-06 09:00:00+00:00]
location: [location]
slug: [slug]
title: [title]
description: [short description]
media_type: [image|video]
media_link: [where image is stored | youtube link ]
layout: event
---

[Long description]
```

## Adding an blog post
Add a .md file with the following contents under `_posts_/` and an image under /assets/images/. Files should be named as the event with date as prefix with dashes as separators. 

```
---
author: [author]
comments: false
date: [date e.g. 2013-05-06 08:15:12+00:00]
slug: [slug]
title: [title]
media_type: [video|image]
media_link: [link]
description: [short description]
layout: post
---
[post in markdown or html]
```