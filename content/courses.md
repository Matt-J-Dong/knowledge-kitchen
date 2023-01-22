---
title: Knowledge Kitchen
permalink: /courses/
---

{% assign featured_categories = "courses" | split: ", "  %}
{% assign featured_collections = "" | split: ", "  %}

{% for cat in featured_categories %}<!-- use site.page-categories instead for all categories defined in config -->

### {{ cat }}

<ul>
  {% for page in site.pages %}
    {% for pc in page.categories %}
    
      {% if pc == cat and page.name != "index.md" %}
      
        {% if page.path contains "index.md" %}
          <!-- ignore landing pages -->
        {% else %}

        <li><a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>
        {% endif %}

      {% endif %}   <!-- cat-match-p -->

    {% endfor %}  <!-- page-category -->

{% endfor %} <!-- page -->

</ul>

{% endfor %} <!-- cat -->

{% for col in site.collections %}

    {% if featured_collections contains col.label %}

### {{ col.label }}

<ul>

      {% for page in site[col.label] %}
        {% if page.path contains "index.md" %}
          <!-- ignore landing pages -->
        {% else %}

  <li>{{ page.name }} <a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>
        {% endif %}
      {% endfor %}

</ul>
    {% endif %}

{% endfor %} <!-- col -->

... <a href='{{ "/" | prepend:site.baseurl  }}'>main</a> stuff
