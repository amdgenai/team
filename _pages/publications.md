---
layout: default
permalink: /publications/
title: "Publications"
---

<div class="section-header">All Publications</div>

<div class="pub-grid">
{% assign pubs = site.data.publications %}
{% for pub in pubs %}
    <div class="pub-card">
    <img src="{{ pub.image }}" alt="{{ pub.title }}">
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

<style>
    .section-header {
    font-size: 1.8rem;
    font-weight: bold;
    margin: 2rem 0 1rem 0; /* 上下留白 */
    text-align: center; /* 如果想居中可以加 */
    }

    .pub-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin: 2rem auto;            /* 上下 2rem，左右自动居中 */
    padding: 0 1rem;              /* 左右留白 */
    max-width: 1200px;            /* 最大宽度控制 */
    justify-content: center;     /* 居中对齐 */
    }

    .pub-card {
    flex: 1 1 calc(33% - 1rem);
    max-width: 380px;            /* 限制每个卡片最大宽度 */
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    }
    
    .pub-card img {
    width: 100%;
    height: 160px;
    }
    
    .pub-content {
    padding: 1rem;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    flex-grow: 1; /* 让它填充剩余高度 */
    }

    .pub-content > .btn {
    margin-top: auto; /* 挤到最底下 */
    }
    
    .pub-tag {
    font-size: 0.75rem;
    background: #eee;
    color: #333;
    padding: 0.2rem 0.5rem;
    border-radius: 4px;
    display: inline-block;
    }
    
    .pub-year {
    font-size: 0.9rem;
    color: #555;
    }
    
    .pub-title {
    font-weight: bold;
    }
    
    .pub-desc {
    font-size: 0.85rem;
    color: #666;
    }
</style>
