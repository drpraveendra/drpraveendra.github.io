---
layout: default
title: "📝 Blog"
permalink: /blog/
---

<style>
  .blog-header {
    margin-bottom: 30px;
  }
  .blog-header h1 {
    font-size: 2rem;
    color: #1e3c72;
    margin-bottom: 8px;
  }
  .blog-header p {
    color: #666;
    font-size: 1rem;
  }
  .post-card {
    background: white;
    border-radius: 12px;
    padding: 25px 30px;
    margin-bottom: 20px;
    border-left: 5px solid #1e3c72;
    box-shadow: 0 3px 12px rgba(0,0,0,0.06);
    transition: all 0.3s ease;
  }
  .post-card:hover {
    transform: translateX(6px);
    box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    border-left-color: #ff4b2b;
  }
  .post-card h2 {
    margin: 0 0 8px 0;
    font-size: 1.3rem;
    border: none;
    padding: 0;
  }
  .post-card h2 a {
    color: #1e3c72;
    text-decoration: none;
  }
  .post-card h2 a:hover {
    color: #ff4b2b;
  }
  .post-meta {
    font-size: 0.85rem;
    color: #999;
    margin-bottom: 10px;
  }
  .post-meta i {
    margin-right: 5px;
  }
  .post-description {
    color: #555;
    font-size: 0.95rem;
    line-height: 1.6;
    margin-bottom: 12px;
  }
  .read-more {
    font-size: 0.88rem;
    font-weight: 600;
    color: #1e3c72;
    text-decoration: none;
  }
  .read-more:hover {
    color: #ff4b2b;
  }
  .no-posts {
    text-align: center;
    padding: 60px 20px;
    color: #999;
    font-size: 1rem;
  }
</style>

<div class="blog-header">
  <h1>📝 Mathematics Blog</h1>
  <p>Theorems, solved problems, and concepts explained clearly — for B.Sc., M.Sc., CSIR NET, GATE & IIT JAM students.</p>
</div>

{% if site.posts.size > 0 %}
  {% for post in site.posts %}
  <div class="post-card">
    <div class="post-meta">
      <i class="fas fa-calendar-alt"></i> {{ post.date | date: "%B %d, %Y" }}
    </div>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    {% if post.description %}
    <p class="post-description">{{ post.description }}</p>
    {% endif %}
    <a class="read-more" href="{{ post.url }}">Read More →</a>
  </div>
  {% endfor %}
{% else %}
  <div class="no-posts">
    <i class="fas fa-pen" style="font-size:2rem; margin-bottom:15px; display:block;"></i>
    New posts coming soon. Stay tuned!
  </div>
{% endif %}
