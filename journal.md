---
layout: page
title: Journal
permalink: /journal/
---

<div class="container">
  <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
  </ul>
</div>