---
layout: page
title: Blog
subtitle: Updates, briefs, and commentary.
permalink: /blog/
---

This page is the archive for blog posts published by HSPA.

## Latest posts
{% if site.posts.size > 0 %}
{% for post in site.posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})**
  <span class="muted">{{ post.date | date: "%B %-d, %Y" }}</span>
{% endfor %}
{% else %}
- No posts yet. Add files in `_posts/`.
{% endif %}
