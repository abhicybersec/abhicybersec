---
layout: default
title: Home
---

# 📚 My Reference Portal

Browse my curated list of blog posts and LinkedIn articles. Each entry includes summary, platform, tags, and more.

---

<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 2rem;">

      {% if post.featured_image %}
        <img src="{{ post.featured_image }}" alt="Thumbnail for {{ post.title }}" style="max-width:150px; margin-bottom: 10px;">
      {% endif %}

      <strong><a href="{{ post.url }}">{{ post.title }}</a></strong><br>

      {% if post.summary %}
        📝 <em>{{ post.summary }}</em><br>
      {% endif %}

      {% if post.author %}👤 <strong>Author:</strong> {{ post.author }}<br>{% endif %}
      {% if post.date %}📅 <strong>Date:</strong> {{ post.date | date: "%B %d, %Y" }}<br>{% endif %}
      {% if post.platform %}🌐 <strong>Platform:</strong> {{ post.platform }}<br>{% endif %}
      {% if post.language %}🌎 <strong>Language:</strong> {{ post.language }}<br>{% endif %}
      {% if post.reading_time %}⏱️ <strong>Reading Time:</strong> {{ post.reading_time }}<br>{% endif %}
      {% if post.difficulty %}📊 <strong>Difficulty:</strong> {{ post.difficulty }}<br>{% endif %}
      {% if post.categories %}📂 <strong>Categories:</strong> {{ post.categories | join: ", " }}<br>{% endif %}
      {% if post.tags %}🏷️ <strong>Tags:</strong> {{ post.tags | join: ", " }}<br>{% endif %}

      {% if post.external_url %}
        🔗 <a href="{{ post.external_url }}" target="_blank" rel="noopener">Read Original Article</a>
      {% endif %}
    </li>
    <hr>
  {% endfor %}
</ul>
