---
layout: page
title: Topics
---

Welcome to my blog! Here are the different topics I write about:

<ul>
  {% for p in site.pages %}
    {% if p.layout == 'category' %}
      <li>
        <a href="{{ site.baseurl }}{{ p.url }}">
          {{ p.title }}
        </a>
      </li>
    {% endif %}
  {% endfor %}
</ul>