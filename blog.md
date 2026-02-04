---
layout: page
title: Blog
subtitle: Short posts, briefs, and field notes.
---

{% for post in site.posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})**  
  <span class="muted">{{ post.date | date: "%B %-d, %Y" }}</span>
{% endfor %}
