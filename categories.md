---
layout: page
title: Categories
permalink: /categories/
---

<div id="category-list">
  <ul>
    {% for category in site.categories %}
      {% capture category_name %}{{ category | first }}{% endcapture %}
      <li>
        <a href="#{{ category_name | slugify }}">
          {{ category_name }} <span class="badge">{{ category | last | size }}</span>
        </a>
      </li>
    {% endfor %}
  </ul>
</div>

<hr>

{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  
  <h2 id="{{ category_name | slugify }}">{{ category_name }}</h2>
  
  <ul>
    {% for post in category | last %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-date">- {{ post.date | date: "%B %-d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}