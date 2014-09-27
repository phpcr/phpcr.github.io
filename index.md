---
layout: default
title: PHP Content Repository
overview: true
---

## Welcome

Welcome to the PHPCR website. See the [About](/about) page to find out what PHPCR is and when
to use it.

## News

{% for post in site.posts %}
- {{ post.date | date_to_string }} [{{ post.title }}]({{ post.url }})
{% endfor %}
