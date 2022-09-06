---
title: Foo
---

# {{ page.title }}

{% assign post_count=site.posts | size %}
{% if post_count > 0 %}

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | prepend:site.baseurl }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endif %}
