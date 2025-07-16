---
layout: default
title: "Blogs"
permalink: /blogs/
---
<div class="section-header">All Blogs</div>

<div class="blog-list">
{% assign blogs = site.data.blogs %}
{% for blog in blogs %}
<div class="blog-card" style="background-image: url('{{ site.baseurl }}{{ blog.background_image }}')">
    <a href="{{ blog.url }}" class="blog-item" target="_blank">
    <div class="blog-title">{{ blog.title }}</div>
    <div class="blog-meta">{{ blog.date }}</div>
    <div class="blog-excerpt">{{ blog.excerpt }}</div></a>
</div>
{% endfor %}
</div>

<style>
    .section-header {
    font-size: 1.8rem;
    font-weight: bold;
    margin: 2rem 0 1rem 0; /* 上下留白 */
    text-align: center; /* 如果想居中可以加 */
    }

    .blog-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin: 2rem auto;            /* 上下 2rem，左右自动居中 */
    padding: 0 1rem;              /* 左右留白 */
    max-width: 1200px;            /* 最大宽度控制 */
    justify-content: center;     /* 居中对齐 */
    }
      
    .blog-item {
    display: block;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 1rem;
    text-decoration: none;
    color: inherit;
    transition: box-shadow 0.2s ease;
    }
    
    .blog-item:hover {
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    
    .blog-title {
    font-size: 1.1rem;
    font-weight: bold;
    }
    
    .blog-meta {
    font-size: 0.85rem;
    color: #888;
    margin-top: 0.2rem;
    }
    
    .blog-excerpt {
    font-size: 0.95rem;
    color: #555;
    margin-top: 0.5rem;
    }

    .blog-card {
    background-size: cover;
    background-position: center;
    color: #fff;
    padding: 1rem;
    border-radius: 6px;
    margin-bottom: 1rem;
    position: relative;
    z-index: 1;
    }
      
    .blog-card::before {
    content: '';
    position: absolute;
    inset: 0;
    background: rgba(0, 0, 0, 0.4); /* 调暗或透明遮罩 */
    z-index: 0;
    }
      
    .blog-card > * {
    position: relative;
    z-index: 1;
    }

    .blog-item {
    text-decoration-color: #000 !important;
    color: #000 !important;
    }
    
    .blog-item:hover {
    text-decoration-color: #666;
    color: #666;
    }
    
</style>