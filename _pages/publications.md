---
layout: default
permalink: /publications/
title: "Publications"
---

<link rel="stylesheet" href="{{ site.baseurl }}/assets/css/custom.css">

<div class="section-header section-header--centered">All Publications</div>

<div class="pub-grid">
{% assign pubs = site.data.publications %}
{% for pub in pubs %}
<div class="pub-card">
  <img src="{{ site.baseurl }}{{ pub.image }}" alt="{{ pub.title }}">
  <div class="pub-content">
    <span class="pub-tag">Publication</span>
    <div class="pub-year">{{ pub.year }}</div>
    <div class="pub-title">{{ pub.title }}</div>
    <div class="pub-desc">{{ pub.description }}</div>
    <a href="{{ pub.url }}" target="_blank" class="btn btn--primary">Read more</a>
  </div>
</div>
{% endfor %}
</div>
