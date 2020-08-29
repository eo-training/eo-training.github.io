---
layout: page
title: "Test"
permalink: "/test/"
---

<div>

  {% for page in site.test %}
  <div class="slide-summary">

      <div class="slide-image">
        <a href="{{ page.url | relative_url }}">
            <img src="../slides/{{ page.slug }}.png">
        </a>
    </div>
    <div class="slide-notes">
        
        <p><strong>{{ page.slug }}. {{ page.title }}</strong></p>

        {{ page.content }}

    </div>

</div>

{% endfor %}

</div>