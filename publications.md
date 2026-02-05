---
layout: page
title: Events & Publications
subtitle: Events and publication records.
---

This page is the landing page for the `publications` collection.

## Entries
{% assign publication_entries = site.publications | sort: "title" %}
{% if publication_entries.size > 0 %}
{% for item in publication_entries %}
- **[{{ item.title }}]({{ item.url | relative_url }})**
{% endfor %}
{% else %}
- No publication entries yet. Add files in `_publications/`.
{% endif %}
