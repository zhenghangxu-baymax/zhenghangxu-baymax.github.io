---
title: "Papers"
permalink: /papers/
---

## Research Interests

My research lies at the intersection of **operations management**, **causal inference**, and **machine learning**, with a focus on developing data-driven methods for decision-making in uncertain service environments.

## Submitted & Working Papers

{% assign paper_number = 0 %}
{% assign submitted_papers = site.data.papers | where: "section", "submitted" %}
{% for paper in submitted_papers %}
{% assign paper_number = paper_number | plus: 1 %}
<a id="{{ paper.id }}"></a>

**[{{ paper_number }}] {% if paper.url %}[{{ paper.title }}]({{ paper.url }}){% else %}{{ paper.title }}{% endif %}**  
(with {{ paper.authors }})  
{{ paper.status | markdownify | remove: '<p>' | remove: '</p>' }}
{% if paper.notes %}
{% for note in paper.notes %}
- {{ note }}
{% endfor %}
{% endif %}

{% endfor %}

## Publications

{% assign published_papers = site.data.papers | where: "section", "published" %}
{% for paper in published_papers %}
{% assign paper_number = paper_number | plus: 1 %}
<a id="{{ paper.id }}"></a>

**[{{ paper_number }}] {% if paper.url %}[{{ paper.title }}]({{ paper.url }}){% else %}{{ paper.title }}{% endif %}**  
(with {{ paper.authors }})  
{{ paper.status | markdownify | remove: '<p>' | remove: '</p>' }}
{% if paper.notes %}
{% for note in paper.notes %}
- {{ note }}
{% endfor %}
{% endif %}

{% endfor %}
