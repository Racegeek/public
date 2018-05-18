---
layout: page
title: support
---
{% assign h = "" %}
{% for p in site.faq %}

{{ p.path }}

{% assign cat = p.path | split: "/" %}
{% if cat[1] contains '.md' %}
* {{ p.title }}
{% else %}
{% if cat[1] != h %}
* {{ cat[1] }}
{% else %}
  - {{ p.title }}
{% endif %}
{% endif %}

{% endfor %}
