---
title: Projects
layout: default
abstract: Open source projects
keywords: oss,software,programming
---

{% for project in site.data.projects %}

### [{{ project.name }}](/projects/{{ project.id }})

{{ project.description }}

{% endfor %}