---
layout: page
title: Projects
description: Products, commercial collaborations, and personal development work.
permalink: /projects/
---
{% assign commercial = site.data.projects | where: "type", "Commercial" %}
{% assign personal = site.data.projects | where: "type", "Personal" %}
{% assign technical = site.data.projects | where: "type", "Technical Case Study" %}

{% include section-title.html title="Commercial projects" subtitle="Products built with companies and external teams." %}
<div class="grid grid-2">
  {% for project in commercial %}
  {% include project-card.html %}
  {% endfor %}
</div>

{% include section-title.html title="Personal projects" subtitle="Independent prototypes and long-term development tracks." %}
<div class="grid grid-2">
  {% for project in personal %}
  {% include project-card.html %}
  {% endfor %}
</div>

{% include section-title.html title="Technical case studies" subtitle="Systems and implementation deep dives." %}
<div class="grid grid-2">
  {% for project in technical %}
  {% include project-card.html %}
  {% endfor %}
</div>

