---
layout: page
title: Gists
description: Reusable code snippets and technical references with context.
permalink: /gists/
---
{% include section-title.html title="Code gists" subtitle="Each entry includes context so the snippet is understandable outside the original project." %}
<div class="grid grid-2">
  {% for gist in site.data.gists %}
  {% include gist-card.html %}
  {% endfor %}
</div>

<div class="card">
  <h3>How to add a new gist</h3>
  <ol>
    <li>Create a new gist and copy its URL.</li>
    <li>Add an item in <code>_data/gists.yml</code>.</li>
    <li>Set <code>gist_url</code> and update the description, language, and tags.</li>
  </ol>
</div>

