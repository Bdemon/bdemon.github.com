---
layout: page
title: Bdemon
tagline: Pain is inevitable,suffering is optional.
---
{% include JB/setup %}

##Recently Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

##To-do

###1. 阅读《番茄工作法图解》

###2. 阅读《拖延心理学》