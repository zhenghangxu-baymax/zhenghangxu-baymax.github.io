---
title: "Research"
permalink: /papers/
excerpt: "AI for Queueing Discovery and Control: queueing causal models, MRI capacity allocation, online pricing, and ongoing inventory research."
redirect_from:
  - /publications/
---

<span id="research-interests" class="anchor-alias" aria-hidden="true"></span>

## AI for Queueing Discovery and Control

{% include research-introduction.html %}

{% include research-pipeline.html %}

<nav class="research-jump-links" aria-label="Research directions">
{% assign featured = site.data.papers | where: "section", "featured" %}
{% for paper in featured %}
  <a href="#{{ paper.id }}">{{ paper.direction }}</a>
{% endfor %}
  <a href="#paper-structural-causal-inventory-models">Inventory research</a>
</nav>

## Featured Research

<span id="submitted--working-papers" class="anchor-alias" aria-hidden="true"></span>
<div class="cv-list paper-list">
{% for paper in featured %}
  {% include paper-entry.html paper=paper %}
{% endfor %}
</div>

## Other Publications

<span id="publications" class="anchor-alias" aria-hidden="true"></span>
<div class="cv-list paper-list">
{% assign other = site.data.papers | where: "section", "other" %}
{% for paper in other %}
  {% include paper-entry.html paper=paper %}
{% endfor %}
</div>

## Ongoing Research

<div class="cv-list paper-list">
{% assign ongoing = site.data.papers | where: "section", "ongoing" %}
{% for paper in ongoing %}
  {% include paper-entry.html paper=paper %}
{% endfor %}
</div>
