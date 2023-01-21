---
title: Amos Bloomberg's Web Site
permalink: /
---

{% for col in site.collections %}

    {% if col.label != 'posts' %}

### {{ col.label }}

<ul>

        {% for page in site[col.label] %}

  <li><a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>
        {% endfor %}

</ul>
    {% endif %}

{% endfor %}

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
