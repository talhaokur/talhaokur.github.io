---
layout: page
title: Projects
permalink: /projects/
---

{% if site.data.research.publications %}
## Publications

<ul class="listing">
{% for pub in site.data.research.publications %}
<li>
<b>{{ pub.title }}</b> <br>
<i>{{ pub.journal }} {%if pub.note %} ({{ pub.note }}) {% endif %} {{ pub.year }} {% if pub.url %} [<a href="{{ pub.url }}">URL</a>] {% endif %} {% if pub.doi %} [<a href="{{ pub.doi }}">DOI</a>] {% endif %} </i>
</li>
{% endfor %}
</ul>
{% endif %}

{% if site.data.research.projects %}
## Projects
<ul class="listing">
{% for project in site.data.research.projects %}
<li>
<b>{{ project.title }}</b><br>
<small><i>{{ project.contributors }}</i></small><br>
{{ project.description }}
{% if project.url %}[<a href="{{ project.url }}">URL</a>]{% endif %}
</li>
{% endfor %}
</ul>
{% endif %}

{% if site.data.research.softwares %}
## Software
<ul class="listing">
{% for software in site.data.research.softwares %}
<li>
<b>{{ software.title }}</b> <br>
<small><i>{{ software.contributors }}</i></small><br>
{{ software.description }} <br>
[<a href="{{ software.url }}">URL</a>]
</li>
{% endfor %}
</ul>
{% endif %}
