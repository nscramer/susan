---
layout: page
title: Journal
permalink: /journal/
---

<div class="container container--lg journal">
  {% if page.title %}
    <hgroup>
      <h1>{{ page.title }}</h1>
      {% if page.subtitle %}
        <h2>{{ page.subtitle }}</h2>
      {% endif %}
    </hgroup>
  {% endif %} 
  
  
  <ul class="postList">
  {% for post in site.posts %}
    <li class="postList__item">
      <a href="{{ post.url }}">
        <div class="postList__item__thumbWrap">
          <div class="postList__item__thumb">
           {% assign foundImage = 0 %}
              {% assign images = post.content | split:"<img " %}
              {% for image in images %}
                {% if image contains 'src' %}
                  {% if foundImage == 0 %}
                    {% assign html = image | split:"/>" | first %}
                    {% assign tags = html | split:" " %}
                    {% for tag in tags %}
                      {% if tag contains 'src' %}
                        <img {{ tag }} />
                      {% endif %}
                    {% endfor %}
                    {% assign foundImage = 1 %}
                  {% endif %}
                {% endif %}
              {% endfor %}
            </div>
          </div>
        <h3 class="postList__item__title">{{ post.title }}</h3>
      </a>
    </li>
  {% endfor %}
  </ul>
</div>
