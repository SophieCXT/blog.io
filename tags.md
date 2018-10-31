---
layout: page
title: "Tags"
description: "Hah！You found my article gene library~"  
header-img: "img/semantic.jpg"  
---
## 基因列表 List of Tags

<div id='tag_cloud'>
{% for tag in site.tags %}
<p style="color:#00868B; font-size:x-large; font-weight: bold;"> {{ tag[0] }}</p>
{% endfor %}
</div>

## 目录 Contents
<ul class="listing" >
{% for tag in site.tags %}
  <li class="listing-seperator" id="{{ tag[0] }}" style="color:#00868B; font-size:x-large; font-weight: bold;" type="square">{{ tag[0] }}</li>
  
{% for post in tag[1] %}
  <li class="listing-item" style="font-size:large">
  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
  <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
{% endfor %}
</ul>