---
title: "Talks"
permalink: /talks/
page_class: talks-page
excerpt: "Invited seminars and conference presentations on queueing causal models, MRI capacity allocation, and online pricing."
---

<div class="cv-list talk-list">
{% for talk in site.data.talks %}
{% assign paper = site.data.papers | where: "id", talk.paper_id | first %}
<section class="cv-entry talk-entry" id="{{ talk.id }}">
{% for alias in talk.aliases %}
  <span class="anchor-alias" id="{{ alias }}" aria-hidden="true"></span>
{% endfor %}
  <h3 class="cv-entry-title"><a href="{{ '/papers/' | relative_url }}#{{ paper.id }}">{{ paper.title }}</a></h3>
{% for group in talk.groups %}
{% unless group.published == false %}
  <div class="cv-entry-group">
    <p class="cv-entry-group-title">{{ group.name }}</p>
    <ul class="cv-entry-items">
{% for item in group.items %}
      <li class="talk-row"><span class="talk-venue">{{ item.venue }}{% if item.role == 'Joint presentation' %}<sup aria-label="Joint presentation">*</sup>{% endif %}</span><span class="talk-date">&mdash; <em>{{ item.date }}</em></span></li>
{% endfor %}
    </ul>
  </div>
{% endunless %}
{% endfor %}
</section>
{% endfor %}
</div>

<p class="talk-footnote"><small>* Joint presentations.</small></p>
