---
permalink: /
title: "Zhenghang Xu"
author_profile: true
excerpt: "Postdoctoral Research Fellow at Rotman School of Management, University of Toronto. AI for Queueing Discovery and Control."
redirect_from:
  - /about/
  - /about.html
---

<!-- <p class="current-appointment"><span lang="zh">徐正航</span><br>
<strong>Postdoctoral Research Fellow</strong><br>
<a href="https://www.rotman.utoronto.ca/">Rotman School of Management</a>, University of Toronto</p>

<nav class="intro-links" aria-label="Profile resources">
  <a href="{{ '/papers/' | relative_url }}">Research</a>
  <a href="{{ '/files/Resume.pdf' | relative_url }}">CV (PDF)</a>
  <a href="mailto:zhenghang.xu@rotman.utoronto.ca">Email</a>
</nav> -->

<!-- ## Biography -->

Welcome to my page!

I am Zhenghang Xu (徐正航), a Postdoctoral Research Fellow at [Rotman School of Management](https://www.rotman.utoronto.ca/), University of Toronto. I have the pleasure of working with Prof. [Nasser Barjesteh](https://www-2.rotman.utoronto.ca/nasser.barjesteh/), Prof. [Sheng Liu](https://sites.google.com/site/thushengliu/), and Prof. [Vahid Roshanaei](https://www.rotman.utoronto.ca/the-rotman-experience/our-community/people/roshanaei-vahid/), continuing my academic journey with the Rotman community.

I received my PhD in [Operations Management and Statistics](https://www.rotman.utoronto.ca/faculty-and-research/academic-areas/operations-management-and-statistics/) from the University of Toronto in 2026. It was my great honor and pleasure to be advised by Prof. [Opher Baron](https://discover.research.utoronto.ca/10004-opher-baron), Prof. [Dmitry Krass](https://discover.research.utoronto.ca/7243-dmitry-krass), and Prof. [Philipp Afèche](https://discover.research.utoronto.ca/15099-philipp-afeche). Prior to my PhD, I received my bachelor's degree in Statistical Science from [The Chinese University of Hong Kong, Shenzhen (CUHKSZ)](https://www.cuhk.edu.cn/en) in 2021.

My research brings together causal inference, machine learning, stochastic modeling, and control to understand operational systems and support decision-making. I am particularly interested in what we can learn about queueing dynamics from data, how that understanding informs capacity decisions, and how to learn and adapt pricing decisions over time. These interests form the research program described below.

## AI for Queueing Discovery and Control

{% include research-introduction.html %}

{% include research-pipeline.html %}

<div class="research-directions">
{% assign featured = site.data.papers | where: "section", "featured" %}
{% for paper in featured %}
  <section class="research-direction" aria-labelledby="direction-{{ paper.id }}">
    <h3 id="direction-{{ paper.id }}"><a href="{{ '/papers/' | relative_url }}#{{ paper.id }}">{{ paper.direction }}</a></h3>
    <p>{{ paper.direction_summary }}</p>
    <p class="direction-paper">{% if paper.id == 'paper-mri-capacity' %}Featured project{% else %}Featured paper{% endif %}: {% include paper-ref.html id=paper.id label=paper.featured_label %}.</p>
{% if paper.related_id %}
    <p class="direction-paper">Inventory extension: {% include paper-ref.html id=paper.related_id label="SCIM (ongoing research)" %}.</p>
{% endif %}
  </section>
{% endfor %}
</div>

## Seminar and Contact

I co-organize the [Rotman Young Scholar Seminar series](https://sites.google.com/view/rotmanyoungscholarseminar/home). Please feel free to contact me about the seminar or potential research connections.

Contact: [zhenghang.xu@rotman.utoronto.ca](mailto:zhenghang.xu@rotman.utoronto.ca)

{% include mapmyvisitors.html %}
