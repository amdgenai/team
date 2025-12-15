---
layout: default
title: "Blogs"
permalink: /blogs/
---

<link rel="stylesheet" href="{{ site.baseurl }}/assets/css/custom.css">

<div class="section-header section-header--centered">All Blogs</div>

<div class="blog-list">
{% assign blogs = site.data.blogs %}
{% for blog in blogs %}
<div class="blog-card" style="background-image: url('{{ site.baseurl }}{{ blog.background_image }}')">
  <a href="{{ blog.url }}" class="blog-item" target="_blank">
    <div class="blog-title">{{ blog.title }}</div>
    <div class="blog-meta">{{ blog.date }}</div>
    <div class="blog-excerpt">{{ blog.excerpt }}</div>
  </a>
</div>
{% endfor %}
</div>
