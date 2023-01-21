---
title: "Musings"
permalink: /musings/
---

{% for page in site[page.collection] %}

{% if page.path contains "index.md" %}<!-- ignore landing pages -->
{% else %}<li><a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>{% endif %}

{% endfor %}
