---
layout: home
title: Comics
---

# 🎨 The CodeLores Comic Gallery

Welcome to the **comic archive**!  
All published strips are here, automatically updated as new ones are added.

---
{% for comic in site.static_files %}
{% if comic.path contains 'comics/' and comic.extname == '.png' %}
<div align="center">
  <a href="{{ site.baseurl }}{{ comic.path }}">
    <img src="{{ site.baseurl }}{{ comic.path }}" alt="{{ comic.name }}" width="600"/>
  </a>

  {% assign folder = comic.path | split: '/' | slice: -2, 1 %}
  <p>
    <em>
      <a href="{{ site.baseurl }}/comics/{{ folder }}/">
        {{ folder | replace: '-', ' ' | capitalize }}
      </a>
    </em>
  </p>
  <hr/>
</div>
{% endif %}
{% endfor %}

