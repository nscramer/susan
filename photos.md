---
layout: page
title: Photos
permalink: /photos/
---

<div class="container container--lg">
<ul class="photos">
  {% assign sorted_photos = site.photos | sort: 'rating', 'last' %}
  {% for photo in sorted_photos %}
    <li>
      <img src="/assets/images/{{ photo.image }}" alt="{{ photo.title }}" />
    </li>
  {% endfor %}
</ul>
</div>