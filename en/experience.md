---
layout: page
title: 💼 Professional Experience
permalink: /en/experience/
lang: en
ref: experience
---

<div class="exp-gallery">
{%- assign sorted_experiences = site.experiences_en | sort: "order" -%}
{%- for exp in sorted_experiences -%}
<div class="exp-card">
  <p class="exp-card-dates">{{ exp.start_date }} – {{ exp.end_date }}</p>
  <h3 class="exp-card-title"><a class="exp-card-link" href="{{ exp.url | relative_url }}">{{ exp.title }}</a></h3>
  <p class="exp-card-company">{{ exp.company }} &mdash; {{ exp.location }}</p>
  <ul class="exp-card-highlights">
    {%- for h in exp.highlights -%}
    <li>{{ h }}</li>
    {%- endfor -%}
  </ul>
  <span class="exp-card-more">Learn more &rarr;</span>
</div>
{%- endfor -%}
</div>
