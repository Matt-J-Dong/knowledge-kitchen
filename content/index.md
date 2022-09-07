---
title: Pages & Posts
permalink: /
---

{% for cat in site.page-categories %}

### {{ cat }}

<ul>
  {% for page in site.pages %}
    {% for pc in page.categories %}
      {% if pc == cat %}
        <li><a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>
      {% endif %}   <!-- cat-match-p -->
    {% endfor %}  <!-- page-category -->
  {% endfor %}  <!-- page -->
</ul>

{% endfor %} <!-- cat -->
