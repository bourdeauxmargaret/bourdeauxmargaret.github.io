---
layout: page
title: Blog
permalink: /blog/
---

<p class="blog-intro">Analysis, commentary, and announcements related to health security policy and practice.</p>

{% if site.posts.size > 0 %}
<ul class="blog-list">
  {% for post in site.posts %}
  <li class="blog-item">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="blog-meta">{{ post.date | date: "%B %-d, %Y" }}{% if post.author %} · {{ post.author }}{% endif %}</p>
    <p class="blog-excerpt">{{ post.excerpt | strip_html | truncate: 220 }}</p>
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="muted">No posts yet. Add files in `_posts/`.</p>
{% endif %}
