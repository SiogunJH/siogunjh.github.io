---
layout: page
title: Code Snippets
description: Some of the reusable code snippets of mine. 
permalink: /gists/
---
{% include section-title.html title="Gists" subtitle="Each entry includes context so the snippet is understandable outside the original project." %}
<div class="grid">
  {% for gist in site.data.gists %}
  {% include gist-card.html %}
  {% endfor %}
</div>
