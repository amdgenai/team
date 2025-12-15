---
layout: default
permalink: /models/
title: "Models"
---

<link rel="stylesheet" href="{{ site.baseurl }}/assets/css/custom.css">

<div class="section-header section-header--centered">Models</div>
<p class="hf-subtitle">Open-source models from AMD GenAI on Hugging Face</p>

<div class="hf-grid">
{% for model in site.data.models %}
<a href="{{ model.url }}" target="_blank" class="hf-card">
  <div class="hf-card__header">
    <svg class="hf-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
      <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
    </svg>
    <span class="hf-card__name">{{ model.name }}</span>
  </div>
  <p class="hf-card__desc">{{ model.description }}</p>
  <div class="hf-card__tags">
    {% for tag in model.tags %}
    <span class="hf-tag">{{ tag }}</span>
    {% endfor %}
  </div>
  <div class="hf-card__footer">
    <span class="hf-source">
      <svg width="14" height="14" viewBox="0 0 95 88" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
        <path d="M47.2 0C26.5 0 9.6 16.9 9.6 37.6c0 2.7.3 5.4.8 8-8.2 3.7-13.9 12-13.9 21.6 0 13.1 10.6 23.7 23.7 23.7 7.8 0 14.7-3.8 19-9.6 2.3.4 4.7.6 7.2.6 20.7 0 37.6-16.9 37.6-37.6S68 4.7 47.2 4.7"/>
      </svg>
      Hugging Face
    </span>
    <span class="hf-arrow">→</span>
  </div>
</a>
{% endfor %}
</div>


