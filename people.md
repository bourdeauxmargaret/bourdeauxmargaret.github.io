---
layout: page
title: People
subtitle: Leadership, collaborators, and partners.
---

This page introduces the team behind HSPA and links to full profile pages.

## People
{% assign people_entries = site.people | sort: "title" %}
{% if people_entries.size > 0 %}
{% for person in people_entries %}
- **[{{ person.title }}]({{ person.url | relative_url }})**
{% endfor %}
{% else %}
- No people entries yet. Add files in `_people/`.
{% endif %}
