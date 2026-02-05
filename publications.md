---
layout: page
title: Events & Publications
subtitle: Events and publication records.
---

This page is the landing page for the `event-publications` collection.

## Entries
{% assign event_publication_entries = site["event-publications"] | sort: "title" %}
{% if event_publication_entries.size > 0 %}
{% for item in event_publication_entries %}
- **[{{ item.title }}]({{ item.url | relative_url }})**
{% endfor %}
{% else %}
- No event/publication entries yet. Add files in `_event-publications/`.
{% endif %}
