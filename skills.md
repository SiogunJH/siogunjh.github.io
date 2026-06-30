---
layout: page
title: Skills
description: Expertise and tools used across development, optimization, and release workflows.
permalink: /skills/
---
{% include section-title.html title="Expertise map" subtitle="Grouped skills for quick review." %}
<div class="grid grid-2">
  {% for group in site.data.skills %}
  <article class="card">
    <header class="card-header">
      <h3>{{ group.category }}</h3>
      <span class="badge">{{ group.items.size }} items</span>
    </header>
    <ul class="skill-list">
      {% for skill in group.items %}
      {% include skill-chip.html %}
      {% endfor %}
    </ul>
  </article>
  {% endfor %}
</div>
