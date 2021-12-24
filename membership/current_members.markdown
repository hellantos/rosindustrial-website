---
layout: members
slug: membership/current_members
title: Current Members
---


{% assign counter = 0 %}
{% for member in site.members %}
{% assign counter = counter | plus: 1 %}
{% endfor %}
<h2 style="text-align: center;">Members: {{counter}} </h2>
<div class="row justify-content-between">
    {% for member in site.members %}
    <div class="col-xs-12 col-lg-6 col-sm-12" style="padding:0px;">
        <div class="background-card p-2" style="height: 100%;">
        <div class="row" style="height: 100%;  margin: 0">
            <div class="col-xs-12 col-lg-4 col-sm-12" style="padding-left: 0; margin: auto auto">
                <img class="member-logo" src="{{site.prefix}}{{member.logo}}" alt="member-logo">
            </div>
            <div class="col-xs-12 col-lg-8 col-sm-12" style="margin-top: 20px;">
                <h2>{{member.name}}</h2>
                <p style="font-weight: bold;">{{member.type}}</p>
                <p>{{member.content}}</p>
            </div>
            </div>
        </div>
    </div>
    {% endfor %}
</div>
