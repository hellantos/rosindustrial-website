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

Add a file with the following contents under `_people/` and add a mugshot under `assets/mugshots` with the contributers full name as file name. 

```
---
name: [Contributer name]
position: [Contributer position]
image: /assets/mugshots/[mugshot file]
---
short cv
```

