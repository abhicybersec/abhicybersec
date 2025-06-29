---
layout: default
title: Home
---

# 📚 My Reference Portal

Welcome to a curated library of blog posts and articles that have helped me grow in web development, content strategy, and tech writing. Each post has a short summary, original link, and helpful tags so you can explore them at your own pace.

<hr>

<div class="references-list">

  {% for post in site.posts %}
  <article class="reference-card">

    {% if post.featured_image %}
    <img src="{{ post.featured_image }}" alt="Thumbnail for {{ post.title }}" class="thumbnail" />
    {% endif %}

    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

    {% if post.summary %}
    <p class="summary"><em>{{ post.summary }}</em></p>
    {% endif %}

    <ul class="metadata">
      {% if post.author %}<li>👤 <strong>Author:</strong> {{ post.author }}</li>{% endif %}
      {% if post.date %}<li>📅 <strong>Published:</strong> {{ post.date | date: "%B %d, %Y" }}</li>{% endif %}
      {% if post.platform %}<li>🌐 <strong>Platform:</strong> {{ post.platform }}</li>{% endif %}
      {% if post.reading_time %}<li>⏱️ <strong>Duration:</strong> {{ post.reading_time }}</li>{% endif %}
      {% if post.difficulty %}<li>📊 <strong>Level:</strong> {{ post.difficulty }}</li>{% endif %}
      {% if post.language %}<li>🌎 <strong>Language:</strong> {{ post.language }}</li>{% endif %}
      {% if post.categories %}<li>📂 <strong>Categories:</strong> {{ post.categories | join: ", " }}</li>{% endif %}
      {% if post.tags %}<li>🏷️ <strong>Tags:</strong> {{ post.tags | join: ", " }}</li>{% endif %}
    </ul>

    {% if post.external_url %}
    <a href="{{ post.external_url }}" class="external-link" target="_blank" rel="noopener">🔗 Read Original Article</a>
    {% endif %}

  </article>
  {% endfor %}

</div>
