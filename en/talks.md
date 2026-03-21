---
layout: page
title: 🎤 Talks & Presentations
permalink: /en/talks/
lang: en
ref: talks
---

<div class="talk-list">
{%- assign sorted_talks = site.talks | sort: "date" | reverse -%}
{%- for talk in sorted_talks -%}
<div class="talk-card">
  <p class="talk-date">{{ talk.date_label }}</p>
  <h3 class="talk-event">{{ talk.event }}</h3>
  {%- if talk.venue -%}
  <p class="talk-venue">{{ talk.venue }}</p>
  {%- endif -%}
  <p class="talk-desc">{{ talk.description }}</p>
  {%- if talk.contributor == false -%}
  <p class="talk-note">Presenter — not a project contributor</p>
  {%- endif -%}
  {%- if talk.topics -%}
  <div class="talk-topics">
    {%- for topic in talk.topics -%}
    <span class="talk-topic-badge">{{ topic }}</span>
    {%- endfor -%}
  </div>
  {%- endif -%}
  {%- if talk.links -%}
  <div class="talk-links">
    {%- for link in talk.links -%}
    <a href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a>
    {%- endfor -%}
  </div>
  {%- endif -%}
</div>
{%- endfor -%}
</div>
