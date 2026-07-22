---
title: "Papers"
permalink: /papers/
---

## Research Interests

My research lies at the intersection of **operations management**, **causal inference**, and **machine learning**, with a focus on developing data-driven methods for decision-making in uncertain service environments.

## Submitted & Working Papers

<div class="cv-list paper-list">
{% assign paper_number = 0 %}
{% assign submitted_papers = site.data.papers | where: "section", "submitted" %}
{% for paper in submitted_papers %}
{% assign paper_number = paper_number | plus: 1 %}
<section class="cv-entry paper-entry" id="{{ paper.id }}">
  <h3 class="cv-entry-title"><span class="cv-entry-index">[{{ paper_number }}]</span> {% if paper.url %}<a href="{{ paper.url }}">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</h3>
  <p class="cv-entry-authors">(with {{ paper.authors }})</p>
  <p class="cv-entry-status">{{ paper.status | markdownify | remove: '<p>' | remove: '</p>' | strip }}</p>
{% if paper.notes %}
  <ul class="cv-entry-notes">
{% for note in paper.notes %}
    <li>{{ note | markdownify | remove: '<p>' | remove: '</p>' | strip }}</li>
{% endfor %}
  </ul>
{% endif %}
</section>
{% endfor %}
</div>

## Publications

<div class="cv-list paper-list">
{% assign published_papers = site.data.papers | where: "section", "published" %}
{% for paper in published_papers %}
{% assign paper_number = paper_number | plus: 1 %}
<section class="cv-entry paper-entry" id="{{ paper.id }}">
  <h3 class="cv-entry-title"><span class="cv-entry-index">[{{ paper_number }}]</span> {% if paper.url %}<a href="{{ paper.url }}">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</h3>
  <p class="cv-entry-authors">(with {{ paper.authors }})</p>
  <p class="cv-entry-status">{{ paper.status | markdownify | remove: '<p>' | remove: '</p>' | strip }}</p>
{% if paper.notes %}
  <ul class="cv-entry-notes">
{% for note in paper.notes %}
    <li>{{ note | markdownify | remove: '<p>' | remove: '</p>' | strip }}</li>
{% endfor %}
  </ul>
{% endif %}
</section>
{% endfor %}
</div>
