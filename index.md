---
layout: page
title: Topics
---

<p> Welcome to my blogs! Here are different topics I write about:</p>
<ul>
  {% for category in site.categories %}
    <li>
      <a href="{{ site.baseurl }}/categories/#{{ category[0] | slugify }}">
        {{ category[0] }}
      </a>
    </li>
  {% endfor %}
</ul>

---