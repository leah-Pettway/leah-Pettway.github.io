---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% assign research_projects = site.projects | where_exp: "item", "item.categories contains 'research'" %}
{% assign applied_projects = site.projects | where_exp: "item", "item.categories contains 'applied'" %}

## Research Projects
{% for post in research_projects %}
  {% include archive-single.html type="grid" %}
{% endfor %}

## Applied / Technical Projects
{% for post in applied_projects %}
  {% include archive-single.html type="grid" %}
{% endfor %}
