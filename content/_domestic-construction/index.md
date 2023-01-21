---
title: "Domestic Construction"
permalink: /domestic-construction/
---

{% for page in site[page.collection] %}

{% if page.path contains "index.md" %}<!-- ignore landing pages -->
{% else %}<li><a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>{% endif %}

{% endfor %}
