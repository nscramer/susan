---
layout: page
title: Photos
permalink: /photos/
---

<!-- <div class="container container--lg">
<ul class="photos">
  {% assign sorted_photos = site.photos | sort: 'rating', 'last' %}
  {% for photo in sorted_photos %}
    <li>
      <img src="/assets/images/{{ photo.image }}" alt="{{ photo.title }}" />
    </li>
  {% endfor %}
</ul>
</div> -->

<div class="container conatiner--lg photos">
  {% if page.title %}
    <hgroup>
      <h1>{{ page.title }}</h1>
      {% if page.subtitle %}
        <h2>{{ page.subtitle }}</h2>
      {% endif %}
    </hgroup>
  {% endif %}

  {% for image in site.static_files %}
      {% if image.path contains 'images' %}
          <img src="{{ site.baseurl }}{{ image.path }}" alt="image" />
      {% endif %}
  {% endfor %}
</div>
