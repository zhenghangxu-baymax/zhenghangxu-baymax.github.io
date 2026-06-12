---
title: "Papers"
permalink: /papers/
---

## Research Interests

My research lies at the intersection of **operations management**, **causal inference**, and **machine learning**, with a focus on developing data-driven methods for decision-making in uncertain service environments.

<style>
  .paper-list {
    line-height: 1.42;
  }

  .paper-entry {
    margin-bottom: 0.9rem;
  }

  .paper-entry p {
    margin-bottom: 0.25rem;
  }

  .paper-entry p:first-child {
    margin: 0;
    line-height: 0;
  }

  .paper-entry ul {
    margin-top: 0.15rem;
    margin-bottom: 0;
  }

  .paper-entry li {
    margin-bottom: 0.1rem;
  }

  .paper-entry li p {
    margin-bottom: 0;
  }
</style>

## Submitted & Working Papers

<div class="paper-list" markdown="1">
{% assign paper_number = 0 %}
{% assign submitted_papers = site.data.papers | where: "section", "submitted" %}
{% for paper in submitted_papers %}
{% assign paper_number = paper_number | plus: 1 %}
<div class="paper-entry" markdown="1">
<a id="{{ paper.id }}"></a>

**[{{ paper_number }}] {% if paper.url %}[{{ paper.title }}]({{ paper.url }}){% else %}{{ paper.title }}{% endif %}**  
(with {{ paper.authors }})  
{{ paper.status | markdownify | remove: '<p>' | remove: '</p>' }}
{% if paper.notes %}
{% for note in paper.notes %}
- {{ note }}
{% endfor %}
{% endif %}

</div>
{% endfor %}
</div>

## Publications

<div class="paper-list" markdown="1">
{% assign published_papers = site.data.papers | where: "section", "published" %}
{% for paper in published_papers %}
{% assign paper_number = paper_number | plus: 1 %}
<div class="paper-entry" markdown="1">
<a id="{{ paper.id }}"></a>

**[{{ paper_number }}] {% if paper.url %}[{{ paper.title }}]({{ paper.url }}){% else %}{{ paper.title }}{% endif %}**  
(with {{ paper.authors }})  
{{ paper.status | markdownify | remove: '<p>' | remove: '</p>' }}
{% if paper.notes %}
{% for note in paper.notes %}
- {{ note }}
{% endfor %}
{% endif %}

</div>
{% endfor %}
</div>
