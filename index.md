---
title: Home
category: "meta"

pagetitle: notebook
---

This is a sort of digital notebook for me to store technical notes about various topics that I learn about, or work on.

## Index

{% assign notes = site.pages | where: "category", "note" | sort: "nid" %}

{% for pg in notes %}

> [**{{ pg.nid }} - {{ pg.title }}**]({{ pg.url }})\
  {{ pg.description }}\
  *{{ pg.date }}*

{% endfor %}
