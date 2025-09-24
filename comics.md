---
layout: default
title: Comics
---

# 🎨 The Codelores Comic Gallery

Welcome to the **comic archive**!  
Here you’ll find all published strips in one place. New comics get added automatically as we go. 🚀

---

{% for comic in site.static_files %}
  {% if comic.path contains 'comics/' and comic.extname == '.png' %}
  <div align="center" style="margin: 20px 0;">
    <img src="{{ comic.path }}" alt="{{ comic.name }}" width="600"/>
    <p><em>{{ comic.name | replace: '-', ' ' | replace: '.png', '' | capitalize }}</em></p>
    <hr/>
  </div>
  {% endif %}
{% endfor %}
