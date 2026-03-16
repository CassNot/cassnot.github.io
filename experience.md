---
layout: page
title: 💼 Professional Experience
permalink: /experience/
---

<div class="exp-gallery">
{%- assign sorted_experiences = site.experiences | sort: "order" -%}
{%- for exp in sorted_experiences -%}
<a class="exp-card" href="{{ exp.url | relative_url }}">
  <div class="exp-card-inner">
  {%- if exp.image -%}
  <div class="exp-card-img-wrap{% if exp.image_dark_bg %} exp-card-img-wrap--dark{% endif %}">
    <img src="{{ exp.image }}" alt="{{ exp.company }}">
  </div>
  {%- endif -%}
  <div class="exp-card-body">
    <p class="exp-card-dates">{{ exp.start_date }} – {{ exp.end_date }}</p>
    <h3 class="exp-card-title">{{ exp.title }}</h3>
    <p class="exp-card-company">{{ exp.company }} &mdash; {{ exp.location }}</p>
    <ul class="exp-card-highlights">
      {%- for h in exp.highlights -%}
      <li>{{ h }}</li>
      {%- endfor -%}
    </ul>
    <span class="exp-card-more">Learn more &rarr;</span>
  </div>
  </div>
</a>
{%- endfor -%}
</div>
