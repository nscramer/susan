---
layout: page
title: Portfolio
permalink: /portfolio/
---

<div class="container">
  <ul>
  {% for node in site.portfolio %}
    <li>
      <a href="{{ node.url }}">{{ node.title }}</a>
    </li>
  {% endfor %}
  </ul>
</div>