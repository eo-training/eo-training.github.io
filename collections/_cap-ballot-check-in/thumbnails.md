---
layout: page
title: "Slide Thumbnails"
---

<div>

{% for page in site.2020-06-new-chief %}

<a href="{{ page.url | relative_url }}">

  <img class="slide-thumbnail" src="./{{ page.slug }}.png">

</a>

{% endfor %}

</div>