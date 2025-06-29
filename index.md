---
layout: default
title: Home
---

# 📚 My Reference Portal

Welcome to a curated library of blog posts and articles that have helped me grow in web development, content strategy, and tech writing. Each post has a short summary, original link, and helpful tags so you can explore them at your own pace.

---

{% for post in site.posts %}
<div style="border: 1px solid #ddd; border-radius: 8px; padding: 1rem; margin-bottom: 2rem; background-color: #fafafa;">
  
  {% if post.featured_image %}
  <img src="{{ post.featured_image }}" alt="Thumbnail for {{ post.title }}" style="max-width: 100%; height: auto; border-radius: 6px; margin-bottom: 10px;">
  {% endif %}

  ## 🔖 [{{ post.title }}]({{ post.url }})

  {% if post.summary %}
  > _{{ post.summary }}_
  {% endif %}

  **👤 Author:** {{ post.author }}  
  **📅 Published:** {{ post.date | date: "%B %d, %Y" }}  
  {% if post.platform %}**🌐 Platform:** {{ post.platform }}{% endif %}  
  {% if post.reading_time %}**⏱️ Duration:** {{ post.reading_time }}{% endif %}  
  {% if post.difficulty %}**📊 Level:** {{ post.difficulty }}{% endif %}  
  {% if post.language %}**🌎 Language:** {{ post.language }}{% endif %}  
  {% if post.categories %}**📂 Categories:** {{ post.categories | join: ", " }}{% endif %}  
  {% if post.tags %}**🏷️ Tags:** {{ post.tags | join: ", " }}{% endif %}

  {% if post.external_url %}
  <div style="margin-top: 10px;">
    🔗 <a href="{{ post.external_url }}" target="_blank" rel="noopener" style="font-weight: bold;">Read Original Article</a>
  </div>
  {% endif %}

</div>
{% endfor %}
