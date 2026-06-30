---
layout: page
title: About
description: Profile, experience, education, and contact links.
permalink: /about/
---
{% assign profile = site.data.profile %}

{% include section-title.html title="Profile" subtitle=profile.headline %}
<div class="card">
  <p><strong>Name:</strong> {{ profile.name }}</p>
  <p><strong>Location:</strong> {{ profile.location }}</p>
  <p><strong>Email:</strong> <a href="mailto:{{ profile.email }}">{{ profile.email }}</a></p>
  <p><strong>Phone:</strong> <a href="tel:{{ profile.phone | replace: ' ', '' }}">{{ profile.phone }}</a></p>
  {% for paragraph in profile.summary %}
  <p>{{ paragraph }}</p>
  {% endfor %}
  <p class="muted">{{ profile.availability_note }}</p>
</div>

{% include section-title.html title="Experience" subtitle="Commercial background and responsibilities." %}
<div class="grid">
  {% for item in site.data.experience %}
  {% include timeline-item.html %}
  {% endfor %}
</div>

{% include section-title.html title="Education" subtitle="Academic background and specialization." %}
<div class="grid">
  {% for item in site.data.education %}
  {% include timeline-item.html %}
  {% endfor %}
</div>

{% include section-title.html title="Links" subtitle="Public profiles and contact points." %}
<div class="card">
  <ul>
    {% for link in profile.links %}
    <li><a href="{{ link.url }}" target="_blank" rel="noopener noreferrer">{{ link.label }}</a></li>
    {% endfor %}
  </ul>
</div>

