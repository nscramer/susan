---
layout: page
title: Photos
permalink: /photos/
---

<div class="container container--lg">
<ul>
  {% assign sorted_photos = site.photos | sort: 'rating', 'last' %}
  {% for photo in sorted_photos %}
    <li>
      <a href="{{ photo.url | prepend: site.baseurl }}">
        <img src="/assets/images/{{ photo.image }}" alt="{{ photo.title }}" />
      </a>
    </li>
  {% endfor %}
</ul>
</div>