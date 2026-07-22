---
title: "Talks"
permalink: /talks/
---

<div class="cv-list talk-list">
{% for talk in site.data.talks %}
<section class="cv-entry talk-entry" id="{{ talk.id }}">
  <h3 class="cv-entry-title">{{ talk.title }}</h3>
{% if talk.note %}
  <p class="cv-entry-note"><small>{{ talk.note }}</small></p>
{% endif %}
{% for group in talk.groups %}
  <div class="cv-entry-group">
    <p class="cv-entry-group-title">{{ group.name }}</p>
    <ul class="cv-entry-items">
{% for item in group.items %}
      <li>{{ item.venue }}{% if item.joint %}*{% endif %} &mdash; <em>{{ item.date }}</em></li>
{% endfor %}
    </ul>
  </div>
{% endfor %}
</section>
{% endfor %}
</div>
