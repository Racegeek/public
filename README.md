---
layout: page
title: support
---
{% assign h = "" %}
{% for p in site.faq %}

	{% assign cat = p.path | split: "/" %}
	{% if cat[1] != h %}
	{% if cat[1] contains '.md' %}
	{% else %}
## {{ cat[1] }}
	{% endif %}
	{% endif %}

{{ p.title }}

{% endfor %}
