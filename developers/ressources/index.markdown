---
layout: page
slug: developers/ressources
title: Ressources
---
<p style="margin-bottom: 50px;">This site contains links to useful slides, repositories and videos.</p>

<h3 style="margin-top: 50px;"> Developer Material </h3>
<div class="row align-items-stretch">
    <div class="col-4 d-flex align-items-stretch">
        <div class="card" >
        <img src="../../assets/images/application.png" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">3D Camera Survey </h5>
            <p class="card-text">
            A comprehensive list of 3D cameras including their characteristics, that can be used with ROS.
            </p>
            <a class="button" href="#">Link</a>
        </div>
        </div>
    </div>
        <div class="col-4 d-flex align-items-stretch">
        <div class="card" >
        <img src="../../assets/images/application.png" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">Training Material</h5>
            <p class="card-text">
            The complete materials of the ROS-Industrial Consortium America's Training.
            </p>
            <a class="button" href="https://industrial-training-master.readthedocs.io/en/foxy/">Link</a>
        </div>
        </div>
    </div>
</div>

<h3 style="margin-top: 50px;"> Event Material </h3>
<div class="row" style="margin-bottom: 100px;">
  <div class="col-sm-12 col-lg-12 p-12 align-items-stretch">
    <div class="row">
      <div class="col-1" style="margin-top: auto; margin-bottom:auto"> 
      <h5> Type </h5>
      </div>
      <div class="col-2" style="margin-top: auto; margin-bottom:auto"> 
      <h5> Date </h5>
      </div>
      <div class="col-6" style="margin-top: auto; margin-bottom:auto">
        <h5>
          Title
        </h5>
      </div>
      <div class="col-3" style="margin-top: auto; margin-bottom:auto">
        <h5> Link </h5>
    </div>
  {% for ressource in site.ressources reversed %}
  <div class="col-sm-12 col-lg-12 p-12 align-items-stretch">
    <div class="row">
      <div class="col-1" style="margin-top: auto; margin-bottom:auto"> 
      {% if ressource.type == "slides" %}
        <img src="../../assets/icons/Icon_Slides.png"/>
      {% elsif ressource.type == "videos" %}
        <img src="../../assets/icons/Icon_Videos.png"/>
      {% endif %}
      </div>
      <div class="col-2" style="margin-top: auto; margin-bottom:auto"> 
      <h5>{{ ressource.date | date: "%Y-%m-%d" }}</h5>
      </div>
      <div class="col-6" style="margin-top: auto; margin-bottom:auto">
        <h5>
          {{ ressource.title }}
        </h5>
      </div>
      <div class="col-3" style="margin-top: auto; margin-bottom:auto">
        <a class="button" href="{{ ressource.link }}">Link</a>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
