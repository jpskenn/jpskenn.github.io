---
layout: default
title: 特集
---
<!-- Feature -->
<h1>{{ page.title }}</h1>

<ul>
{% for feature in site.feature %}
   {% unless feature.title == "feature" %}
  <li><a href="{{ site.url }}{{ feature.url }}">{{ feature.title }}</a></li>
  {% endunless %}
{% endfor %}
</ul>
