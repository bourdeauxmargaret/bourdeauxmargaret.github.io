---
layout: page
title: Blog
subtitle: Short posts, briefs, and curated video clips.
---

{% for post in site.posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})**
  {% if post.video_id %} <span class="muted">· Video</span>{% endif %}  
  <span class="muted">{{ post.date | date: "%B %-d, %Y" }}</span>
  {% if post.video_note %} — <span class="muted">{{ post.video_note }}</span>{% endif %}
{% endfor %}
