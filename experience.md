---
layout: page
title: 💼 Professional Experience
permalink: /experience/
---

<div class="exp-gallery">
{%- assign sorted_experiences = site.experiences | sort: "order" -%}
{%- for exp in sorted_experiences -%}
<a class="exp-card" href="{{ exp.url | relative_url }}">
  <p class="exp-card-dates">{{ exp.start_date }} – {{ exp.end_date }}</p>
  <h3 class="exp-card-title">{{ exp.title }}</h3>
  <p class="exp-card-company">{{ exp.company }} &mdash; {{ exp.location }}</p>
  <ul class="exp-card-highlights">
    {%- for h in exp.highlights -%}
    <li>{{ h }}</li>
    {%- endfor -%}
  </ul>
  <span class="exp-card-more">Learn more &rarr;</span>
</a>
{%- endfor -%}
</div>
