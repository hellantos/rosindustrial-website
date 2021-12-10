---
author: admin
comments: false
layout: blog
slug: blog
title: Blog
---

<div class="row" >
  {% for post in site.posts limit: 1 %}
  <div class="col-sm-12 col-lg-12 p-2">
    <div class="row blog-image-wrapper">
      <div class="col-8 blog-image-wrapper">
        {% if post.media_type == 'video' %}
          <iframe
            style="width:100%;"
            height="315"
            src="{{ post.media_link }}"
            frameborder="0"
            allowfullscreen
          ></iframe>
        {% elsif post.media_type == 'image' %}
        <div class="blog-image-wrapper">
          <img src="{{site.prefix}}{{post.media_link}}" alt="iamge"/>
        </div>
        {%- else -%} 
        <div class="blog-image-wrapper">
        <img src="{{site.prefix}}/assets/ric_logo.png" alt="image"/>
        </div>
        {% endif %}  
      </div>
      <div class="col-4">
        <a href="{{site.prefix}}/{{ post.url }}">
          <div class="blog-text-wrapper">
            <span class="blog-date">
              {{ post.date | date: "%B %d, %Y" }}
            </span>
            <h3 class="dark-text">
              {{ post.title }}
            </h3>
            <p class="dark-text">{{ post.description }}</p>
          </div>
        </a>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

<div class="row">
  {% for post in site.posts offset: 1 %}
  <div class="col-sm-6 col-lg-4 p-2" style="height: 100%; padding: 0 0;">
    <div class="media-wrapper" style="height:100%;  margin: 0;">
    {% if post.media_type == 'video' %}
      <iframe
        style="width:100%;"
        height="315"
        src="{{ post.media_link }}"
        frameborder="0"
        allowfullscreen
      ></iframe>
    {% elsif post.media_type == 'image' %}
      <div class="blog-image-wrapper">
        <img src="{{post.media_link}}" alt="iamge"/>
      </div>
    {%- else -%} 
      <div class="blog-image-wrapper">
      <img style="padding: 5px;" src="{{site.prefix}}/assets/ric_logo.png" alt="image"/>
      </div>
    {% endif %}  
      <a href="{{site.prefix}}/{{ post.url }}">
        <div class="blog-text-wrapper">
          <span class="blog-date">
            {{ post.date | date: "%B %d, %Y" }}
          </span>
          <h5>
            {{ post.title }}
          </h5>
          <p class="dark-text">{{ post.description }}</p>
        </div>
      </a>
    </div>
  </div>
  {% endfor %}
</div>