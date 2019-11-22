---
layout: page
title: Tags
permalink: /tags/
---

<ul class="tags">
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

<span id="{{t | downcase | replace:" ","-" }}">
<b>{{t | downcase | replace:" ","-" }}</b> has {{ posts | size }} posts</span>
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}
</ul>
