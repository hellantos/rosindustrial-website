---
layout: page
slug: about
title: History
---


Here you find some key events that have helped shaping the ROS-Industrial Consortium.
<div class="" style="height: 50px;"></div>
<div class="row g-2">
        {% assign counter = 0 %}
        {% for item in site.history %}
        <div class="col-0">
        </div>
        <div class="col-1" style="vertical-align: middle;">
            <div class="vertline" style="margin: auto auto; background-color:darkblue; height: 20px; width: 20px; vertical-align: middle;">
            </div>
            <div class="vertline" style="margin: 10% auto 0 auto; background-color:lightgrey; width: 5px; height: 90%">
            </div>
        </div>
        <div class="col-11">
            <p>{{item.date | date: "%B, %Y"}}</p>
            <h3>{{item.title}}</h3>
            <p>{{item.description}}</p>
        </div>
        <div class="col-0">
        </div>
        {% endfor %}
</div>