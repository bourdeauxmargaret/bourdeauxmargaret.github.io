---
layout: page
title: Videos
subtitle: Curated clips published via the HSPA blog.
---

{% assign video_posts = site.posts | where_exp: "post", "post.video_id" %}
{% for post in video_posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})**  
  <span class="muted">{{ post.date | date: "%B %-d, %Y" }}</span>
  {% if post.video_note %} — <span class="muted">{{ post.video_note }}</span>{% endif %}
{% endfor %}
