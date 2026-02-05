---
layout: page
title: Projects
subtitle: Active workstreams and methods development.
---

This page highlights active workstreams and links to detailed project pages.

## Projects
{% assign project_entries = site.projects | sort: "title" %}
{% if project_entries.size > 0 %}
{% for project in project_entries %}
- **[{{ project.title }}]({{ project.url | relative_url }})**
{% endfor %}
{% else %}
- No project entries yet. Add files in `_projects/`.
{% endif %}
