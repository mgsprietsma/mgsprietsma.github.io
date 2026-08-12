---
layout: default
title: Research
permalink: /research/
description: Papers, preprints, and ongoing work.
---

<section class="page-head">
  <h1>Research</h1>
  <p class="lede">Selected papers and ongoing work. Preprints and code are linked where available. To add or edit entries, edit <code>_data/publications.yml</code> — you don't need to touch this page.</p>
</section>

<div class="paper-grid">
  {% for paper in site.data.publications %}
  <article class="paper-card">
    <div class="paper-meta">
      <span class="paper-venue">{{ paper.venue }}</span>
      {% if paper.year %}<span class="paper-year">{{ paper.year }}</span>{% endif %}
    </div>
    <h2 class="paper-title">{{ paper.title }}</h2>
    <p class="paper-authors">{{ paper.authors }}</p>
    {% if paper.summary %}<p class="paper-summary">{{ paper.summary }}</p>{% endif %}
    {% if paper.links %}
    <div class="paper-links">
      {% for link in paper.links %}
      <a class="chip" href="{{ link.url }}"{% unless link.url contains 'mailto' %} target="_blank" rel="noopener"{% endunless %}>{{ link.label }}</a>
      {% endfor %}
    </div>
    {% endif %}
  </article>
  {% endfor %}
</div>
