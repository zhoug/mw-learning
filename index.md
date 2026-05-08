---
layout: home
title: 首页
order: 0
---

<div class="home-hero">
  <div class="brand">知 庚</div>
  <div class="tagline">认 知 · 记 录 · 创 造</div>
  <div class="subtitle">
    一个党务工作者的 AI 深度使用记录。<br>
    既是经验簿，也是成长日志。
  </div>
  <div class="hero-date">从 2026 年 05 月 的某个下午开始</div>
</div>

<div class="stats-dashboard">
  <div class="stat-item">
    <span class="stat-number">{{ site.posts | size }} <small>篇</small></span>
    <span class="stat-label">文章累计</span>
  </div>
  <div class="stat-item">
    <span class="stat-number">0 <small>字</small></span>
    <span class="stat-label">累计沉淀</span>
  </div>
  <div class="stat-item">
    <span class="stat-number">0</span>
    <span class="stat-label">收藏数</span>
  </div>
</div>

<div class="home-layout">
  <div class="home-main">

    <div class="section-header">
      <h2>📝 最近更新</h2>
    </div>

    {% for post in site.posts limit:5 %}
    <article class="article-card">
      <a href="{{ post.url | relative_url }}" class="card-img">
        {% if post.image %}
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" loading="lazy">
        {% else %}
          <div class="card-img-placeholder" style="background: linear-gradient(135deg, {{ post.color_start | default: '#1a1a2e' }}, {{ post.color_end | default: '#2d3436' }});">
            <span>{{ post.emoji | default: "📖" }}</span>
          </div>
        {% endif %}
      </a>
      <div class="card-text">
        <div class="card-meta-top">
          <span class="card-category">{{ post.category }}</span>
          <span class="card-date">{{ post.date | date: "%Y 年 %-m 月 %-d 日" }}</span>
        </div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | truncate: 100 }}</p>
      </div>
    </article>
    {% endfor %}

  </div>

  <aside class="home-sidebar">
    <div class="sidebar-card">
      <h3>📬 近期更新</h3>
      {% for post in site.posts limit:8 %}
      <div class="ru-item">
        <span class="ru-date">{{ post.date | date: "%m/%d" }}</span>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </div>
      {% endfor %}
    </div>

    <div class="sidebar-card sidebar-about">
      <h3>🙋 关于我</h3>
      <p>AI 学习庚，一个党务工作者的 AI 探索日志。</p>
      <p>坚信 AI 不是程序员的专利，每个人都能找到自己的 AI 之路。</p>
    </div>
  </aside>
</div>
