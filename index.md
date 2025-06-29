---
layout: default
title: Home
---

# Welcome to My Reference Portal

Browse curated references to blogs and LinkedIn articles.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.external_url | default: post.url }}">{{ post.title }}</a>
      {% if post.author %}by {{ post.author }}{% endif %}
      <small> - {{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
