---
layout: default
title: The Codelores
---

<p align="center">
  <img src="assets/logo1.png" width="600" alt="The Codelores Banner"/>
</p>

# 🚀 The Codelores – Where Code Meets Stories

**The Codelores** is a comic series that explains coding, debugging, algorithms, and developer life through storytelling and visuals.  
Instead of long docs or dry explanations, think of this as **short, fun strips** that bring tech to life.

---

## 🌟 Featured Comic (Latest)

{% assign latest_comic = site.static_files | where: "extname", ".png" | sort: "modified_time" | last %}
{% if latest_comic %}
<div align="center" style="margin: 20px 0;">
  <img src="{{ latest_comic.path }}" width="600" alt="{{ latest_comic.name }}" />
  <p><em>{{ latest_comic.name | replace: '-', ' ' | replace: '.png', '' | capitalize }}</em></p>
</div>
{% endif %}

---

## 🌟 Why The Codelores?
- Make complex concepts simple and engaging  
- Learn through relatable stories and humor  
- Show that tech doesn’t have to be intimidating — it can be creative and fun  

---

## 📚 What You'll Find Here
- 🎨 **Comic strips** (PNG/JPG format)  
- 📝 **Behind-the-scenes notes** on how each strip was made  
- 🔗 Links to posts on [LinkedIn](https://www.linkedin.com/in/aisha-karigar/) and other platforms  
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
Got a funny dev story, bug, or coding struggle that deserves a strip? We’d love your input!  

👉 See our [Contributing Guidelines](CONTRIBUTING.md) to get started.  

---

## 📜 Ownership & License
This repository is maintained by **[@aishakarigar](https://github.com/aishakarigar)**, the original creator of *The Codelores*.  

- All content is licensed under **CC BY-NC 4.0**  
- You can share, remix, and adapt with credit ✅  
- Not for commercial use without permission ❌  

---

## 👩‍💻 Contributors
- [@aishakarigar](https://github.com/aishakarigar) — Creator  
- [@classmate123](https://github.com/classmate123) — Collaboration: *Debugging Nightmares*  

---

## ✨ Stay Tuned
This is just the beginning — more strips will be added regularly!  
Follow along, share with your dev friends, and let’s make tech fun together 🚀  

🔗 Hashtag: `#TheCodelores`
