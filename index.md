---
layout: home
title: ""
---

<p align="center">
  <img src="assets/logo1.png" width="600" alt="The Codelores Banner"/>
</p>

# 🚀 The CodeLores – Where Code Meets Stories

**The CodeLores** is a comic series that explains coding, debugging, algorithms, and developer life through storytelling and visuals.  
Instead of long docs or dry explanations, think of this as **short, fun strips** that bring tech to life.

---

## 🌟 Featured Comic (Latest)

{% assign latest_comic = site.static_files | where: "extname", ".png" | where_exp: "f", "f.path contains 'comics/'" | sort: "modified_time" | last %}
{% if latest_comic %}
<div align="center">
  <a href="{{ site.baseurl }}{{ latest_comic.path }}">
    <img src="{{ site.baseurl }}{{ latest_comic.path }}" alt="{{ latest_comic.name }}" width="600"/>
  </a>

  {% assign folder = latest_comic.path | split: '/' | slice: -2, 1 %}
  <p><em>{{ folder | replace: '-', ' ' | capitalize }}</em></p>
</div>
{% endif %}


---

## 🌟 Why The Codelores?
- Make complex concepts simple and engaging  
- Learn through relatable stories and humor  
- Show that tech doesn’t have to be intimidating — it can be creative and fun  

---

## 📚 What You'll Find Here
- 🎨 **Comic strips** (PNG/JPG)  
- 📝 **Behind-the-scenes notes**  
- 🔗 Links to posts on [LinkedIn](https://www.linkedin.com/in/aisha-karigar/)  
- 💡 **Community contributions & ideas**  

---

## 📢 Latest Comics

| Title | Link |
|-------|------|
{% for comic in site.static_files %}
{% if comic.path contains 'comics/' and comic.extname == '.png' %}
| {{ comic.name | replace: '-', ' ' | replace: '.png', '' | capitalize }} | [View]({{ comic.path }}) |
{% endif %}
{% endfor %}

---

## 🤝 How to Contribute
Got a funny dev story, bug, or coding struggle that deserves a strip? 👉 See our [Contributing Guidelines](CONTRIBUTING.md).  

---

## 📜 License
Maintained by **[@aishakarigar](https://github.com/aishakarigar)**.  
- Licensed under **CC BY-NC 4.0**  
- Share, remix, and adapt with credit ✅  
- Not for commercial use ❌  

---

## 👩‍💻 Contributors
- [@aishakarigar](https://github.com/aishakarigar) — Creator  
- [@classmate123](https://github.com/classmate123) — Collaboration: *Debugging Nightmares*  

---

## ✨ Stay Tuned
This is just the beginning — more strips will be added regularly!  
Follow along, share with your dev friends, and let’s make tech fun 🚀  
