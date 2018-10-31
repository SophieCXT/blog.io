---
layout: page
title: "Archive"
description: "Articles sorting by year"
header-img: "img/orange.jpg"
---


<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator" style="color:#00868B; font-size:x-large; font-weight: bold;" type="square">{{ y }}</li>
  {% endif %}
  <li class="listing-item" style="font-size:large">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>