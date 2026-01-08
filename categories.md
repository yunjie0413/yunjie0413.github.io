---
layout: page
title: Categories
permalink: /categories/
---

<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <h3 id="{{ category_name | slugify }}">{{ category_name }}</h3>
    
    <ul>
      {% for post in category[1] %}
        <li>
          <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
          <span class="post-date"> - {{ post.date | date: "%B %-d, %Y" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>
  <hr>
{% endfor %}
</div>