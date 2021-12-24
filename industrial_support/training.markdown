---
layout: page
slug: industrial_support/training
title: Training
---

The ROS-Industrial Consortium provides training courses around using ROS in industrial applications and organisations. 

<div class="row align-items-stretch gy-4">
    {%- for training in site.trainings -%}
    <div class="col-xs-12 col-lg-4 col-sm-12 d-flex align-items-stretch">
    <div class="card" style="width:100%;">
        <img src="../../{{ training.image }}" class="card-img-top" alt="..."/>
        <div class="card-body">
            <h5 class="card-title">{{ training.title }}</h5>
            <p class="card-text">
            {{ training.description }}<br><br>
            <b>Contact Information:</b><br>
            {{ training.contact }}<br>
            {{ training.mail }}<br>
            </p>
        </div>
    </div>
    </div>
    {%- endfor -%}
</div>

Note that ROS-I Consortium membership comes with limited lnumber of free training seats.