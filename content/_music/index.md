---
title: "Music"
permalink: /music/
---

I studied classical guitar for many years, first with private instruction from a professor from the [Manhattan School of Music](https://www.msmnyc.edu/) and then at the [Eastman School of Music](https://www.esm.rochester.edu/), where I would spend hours in practice rooms and in the library listening to obscure records. Years ago, I used to occasionally release experimental concept albums, including [Normal Music For Strange People]({{site.url}}{{ site.baseurl }}/music/normal-music-for-strange-people/) and [The Complete Dance Party]({{site.url}}{{ site.baseurl }}/music/the-complete-dance-party/).

{% for page in site[page.collection] %}

{% if page.path contains "index.md" %}<!-- ignore landing pages -->

{% else %}

  <li><a href="{{ page.url | prepend:site.baseurl  }}">{{ page.title }}</a></li>

{% endif %}

{% endfor %}
