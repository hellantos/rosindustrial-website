---
layout: people
slug: about/people
title: People
---


<div class="row justify-content-between g-2 ">
{% for person in site.people %}
    <div class="col-6">
        <div class="background-card" style="height: 100%;">
        <div class="row" style="height: 100%; background-color: lightgrey; margin: 0">
            <div class="col-5" style="padding-left: 0;" >
                <img class="mugshot" src="/rosindustrial-website/{{person.image}}" alt="mugshot">
            </div>
            <div class="col-7" style="margin-top: 20px;">
                <h2>{{person.name}}</h2>
                <p style="font-weight: bold;">{{person.position}}</p>
                <p>{{person.content}}</p>
            </div>
            </div>
        </div>
    </div>
    {% endfor %}
</div>