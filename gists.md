---
layout: page
title: Gists
description: Reusable code snippets and technical references with context.
permalink: /gists/
---
{% include section-title.html title="Code gists" subtitle="Each entry includes context so the snippet is understandable outside the original project." %}
<div class="grid">
  {% for gist in site.data.gists %}
  {% include gist-card.html %}
  {% endfor %}
</div>
