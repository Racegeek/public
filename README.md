---
layout: page
title: support
---
{% assign h = "" %}
{% for p in site.faq %}

{% assign cat = p.path | split: "/" %}

{% if cat[1] contains '.md' %}
* {{ p.title }}
{% else %}

{% if cat[1] != h %}
* {{ cat[1] }}
{% endif %}
  - {{ p.title }}

{% endif %}

{% endfor %}
