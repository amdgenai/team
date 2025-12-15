---
layout: default
permalink: /datasets/
title: "Datasets"
---

<link rel="stylesheet" href="{{ site.baseurl }}/assets/css/custom.css">

<div class="section-header section-header--centered">Datasets</div>
<p class="hf-subtitle">Open-source datasets from AMD GenAI on Hugging Face</p>

<div class="hf-grid">
{% for item in site.data.datasets %}
<a href="{{ item.url }}" target="_blank" class="hf-card hf-card--dataset">
  <div class="hf-card__header">
    <svg class="hf-icon hf-icon--dataset" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
      <path d="M20 6h-8l-2-2H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V8c0-1.1-.9-2-2-2zm-6 10H6v-2h8v2zm4-4H6v-2h12v2z"/>
    </svg>
    <span class="hf-card__name">{{ item.name }}</span>
  </div>
  <p class="hf-card__desc">{{ item.description }}</p>
  <div class="hf-card__tags">
    {% for tag in item.tags %}
    <span class="hf-tag hf-tag--dataset">{{ tag }}</span>
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

