---
author: admin
comments: false
date: 2013-12-08 23:55:02+00:00
layout: events
slug: events
title: Events
---
<div class="container-event">
<div class="row">
  {% for event in site.events %}
  {% capture buildtime %}{{'now' | date: '%s'}}{% endcapture %}
  {% capture event_time %}{{event.start_date | date: '%s'}}{% endcapture %}
  {% if event_time > buildtime %}
  <div class="col-sm-6 col-lg-4 p-4 align-items-stretch">
    <div class="media-wrapper">
      <div class="blog-image-wrapper">
          {% if event.media_type == 'video' %}
            <iframe
                    style="width:100%;"
                    height="315"
                    src="{{ event.media_link }}"
                    frameborder="0"
                    allowfullscreen
            ></iframe>
          {% elsif event.media_type == 'image' %}
            <div class="blog-image-wrapper">
              <img src="../{{ event.media_link }}" alt="image"/>
            </div>
          {%- else -%} 
            <div class="blog-image-wrapper">
              <img src="../assets/ric_logo.png" alt="image"/>
            </div>
          {% endif %}  
      </div>
      <div class="blog-text-wrapper">
        <h3>
          {{ event.title }}
        </h3>
        <p class="event-date">
          {{ event.start_date | date: "%B %d, %Y" }} - {{ event.end_date | date: "%B %d, %Y" }}<br/>
          {{event.location}}
        </p>
        <a class="button" href="{{ event.url }}">Info</a>
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
  <div class="col-sm-6 col-lg-4 p-4 align-items-stretch" >
    <div class="media-wrapper">
      <div class="blog-image-wrapper">
          {% if event.media_type == 'video' %}
            <iframe
                    style="width:100%;"
                    height="315"
                    src="{{ event.media_link }}"
                    frameborder="0"
                    allowfullscreen
            ></iframe>
          {% elsif event.media_type == 'image' %}
            <div class="blog-image-wrapper">
              <img src="../{{ event.media_link }}" alt="image"/>
            </div>
          {%- else -%} 
            <div class="blog-image-wrapper">
              <img src="../assets/ric_logo.png" alt="image"/>
            </div>
          {% endif %}  
      </div>
      <div class="blog-text-wrapper" style="padding-top: 20px;">
        <h3>
          {{ event.title }}
        </h3>
        <p class="event-date">
          {{ event.start_date | date: "%B %d, %Y" }} - {{ event.end_date | date: "%B %d, %Y" }}<br/>
          {{event.location}}
        </p>
        <p class="event-description">{{ event.description | truncatewords: 10, "..."}}</p>
      </div>
    </div>
  </div>
  {% endif %}  
  {% endfor %}
</div>
</div>