---
layout: default
title: Portfolio
description: Unity developer portfolio with projects, skills, and technical case studies.
---
{% assign profile = site.data.profile %}
{% include hero.html
  kicker="Portfolio"
  title=profile.name
  summary=profile.summary[0]
  links=profile.links
%}

<section class="container">
  {% include section-title.html title="About me" subtitle=profile.headline %}
  <div class="card">
    <p><strong>Location:</strong> {{ profile.location }}</p>
    <p><strong>Contact:</strong> <a href="mailto:{{ profile.email }}">{{ profile.email }}</a> / <a href="tel:{{ profile.phone | replace: ' ', '' }}">{{ profile.phone }}</a></p>
    {% for paragraph in profile.summary %}
    <p>{{ paragraph }}</p>
    {% endfor %}
  </div>
</section>

<section class="container">
  {% include section-title.html title="Featured products" subtitle="Commercial and personal work from the CV." %}
  <div class="grid grid-2">
    {% for project in site.data.projects limit:4 %}
    {% include project-card.html %}
    {% endfor %}
  </div>
</section>

<section class="container">
  {% include section-title.html title="Core expertise" subtitle="Selected strengths and tools." %}
  <div class="grid grid-3">
    {% for group in site.data.skills %}
    <article class="card">
      <h3>{{ group.category }}</h3>
      <ul class="skill-list">
        {% for skill in group.items limit:4 %}
        {% include skill-chip.html %}
        {% endfor %}
      </ul>
    </article>
    {% endfor %}
  </div>
</section>

