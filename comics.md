---
layout: default
title: Comics
---

# 🎨 The CodeLores Comic Gallery

Welcome to the **comic archive**!  
All published strips are here, automatically updated as new ones are added.

---

{% for comic in site.static_files %}
{% if comic.path contains 'comics/' and comic.extname == '.png' %}
<div align="center">
  <img src="{{ comic.path }}" alt="{{ comic.name }}" width="600"/>
  <p><em>{{ comic.name | replace: '-', ' ' | replace: '.png', '' | capitalize }}</em></p>
  <hr/>
</div>
{% endif %}
{% endfor %}
