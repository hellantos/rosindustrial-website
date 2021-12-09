---
layout: page
slug: developers/ressources
title: Ressources
---
<p style="margin-bottom: 100px;">This site contains links to useful slides, repositories and videos.</p>


<h3> Slides </h3>
<div class="row" style="margin-bottom: 100px;">
  {% for ressource in site.ressources %}
  {% if ressource.type == "slides" %}
  <div class="col-sm-12 col-lg-12 p-12 align-items-stretch">
    <div class="row">
      <div class="col-1" style="margin-top: auto; margin-bottom:auto"> 
      <img src="../../assets/icons/Icon_Slides.png"/>
      </div>
      <div class="col-8" style="margin-top: auto; margin-bottom:auto">
        <h5>
          {{ ressource.title }}
        </h5>
      </div>
      <div class="col-3" style="margin-top: auto; margin-bottom:auto">
        <a class="button" href="{{ ressource.link }}">Link</a>
      </div>
    </div>
  </div>
  {% endif %}
  {% endfor %}
</div>

<h3> Videos </h3>
<div class="row" style="margin-bottom: 100px;">
  {% for ressource in site.ressources %}
  {% if ressource.type == "videos" %}
  <div class="col-sm-12 col-lg-12 p-12 align-items-stretch">
    <div class="row">
      <div class="col-1" style="margin-top: auto; margin-bottom:auto"> 
      <img src="../../assets/icons/Icon_Videos.png"/>
      </div>
      <div class="col-8" style="margin-top: auto; margin-bottom:auto">
        <h5>
          {{ ressource.title }}
        </h5>
      </div>
      <div class="col-3" style="margin-top: auto; margin-bottom:auto">
        <a class="button" href="{{ ressource.link }}">Link</a>
      </div>
    </div>
  </div>
  {% endif %}
  {% endfor %}
</div>

<h3> Repositories </h3>
<div class="row">
  {% for ressource in site.ressources %}
  {% if ressource.type == "repo" %}
  <div class="col-sm-12 col-lg-12 p-12 align-items-stretch">
    <div class="row">
      <div class="col-1" style="margin-top: auto; margin-bottom:auto"> 
      <img src="../../assets/icons/Icon_Repo.png"/>
      </div>
      <div class="col-8" style="margin-top: auto; margin-bottom:auto">
        <h5>
          {{ ressource.title }}
        </h5>
      </div>
      <div class="col-3" style="margin-top: auto; margin-bottom:auto">
        <a class="button" href="{{ ressource.link }}">Link</a>
      </div>
    </div>
  </div>
  {% endif %}
  {% endfor %}
</div>