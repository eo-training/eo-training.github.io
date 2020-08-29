---
layout: page
title: "Slides Summary"
---

<ul>
  <li>page.dir: {{page.dir}}</li>
  <li>page.url: {{page.url}}</li>
  <li>page.path: {{page.path}}</li>
  <li></li>
  <li></li>
</ul>


<div>

  {% for page in site.2020-06-new-chief %}
  <div class="slide-summary">

      <div class="slide-image">
        <a href="{{ page.url | relative_url }}">
            <img src="./{{ page.slug }}.png">
        </a>
    </div>
    <div class="slide-notes">
        
        <p><strong>{{ page.slug }}. {{ page.title }}</strong></p>

        {{ page.content }}

    </div>

</div>

{% endfor %}

</div>