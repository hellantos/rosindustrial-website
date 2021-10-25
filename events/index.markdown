---
author: admin
comments: false
date: 2013-12-08 23:55:02+00:00
layout: events
slug: events
title: Events
---

<div class="row">
  {% for event in site.events %}
  {% capture buildtime %}{{'now' | date: '%s'}}{% endcapture %}
  {% capture event_time %}{{event.start_date | date: '%s'}}{% endcapture %}
  {% if event_time > buildtime %}
  <div class="col-sm-6 col-lg-4 p-2" style="height: 100%; padding: 0 0;">
    <div class="media-wrapper" style="height:100%;  margin: 0;">
      <div class="blog-text-wrapper">
        <h3>
          {{ event.title }}
        </h3>
        <p class="event-date">
          {{ event.start_date | date: "%B %d, %Y" }} - {{ event.end_date | date: "%B %d, %Y" }}<br/>
          {{event.location}}
        </p>
        <p class="event-description">{{ event.description }}</p>
        <a class="button" href="/rosindustrial-website/install">Register</a>
      </div>
    </div>
  </div>
  {% endif %}  
  {% endfor %}
</div>
<div class="line"></div>
<div class="row">
  {% for event in site.events %}
  {% capture buildtime %}{{'now' | date: '%s'}}{% endcapture %}
  {% capture event_time %}{{event.start_date | date: '%s'}}{% endcapture %}
  {% if event_time < buildtime %}
  <div class="col-sm-6 col-lg-4 p-2" style="height: 100%; padding: 0 0;">
    <div class="media-wrapper" style="height:100%;  margin: 0;">
      <div class="blog-text-wrapper">
        <h3>
          {{ event.title }}
        </h3>
        <p class="event-date">
          {{ event.start_date | date: "%B %d, %Y" }} - {{ event.end_date | date: "%B %d, %Y" }}<br/>
          {{event.location}}
        </p>
        <p class="event-description">{{ event.description }}</p>
      </div>
    </div>
  </div>
  {% endif %}  
  {% endfor %}
</div>