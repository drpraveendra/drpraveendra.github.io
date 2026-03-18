---
layout: default
title: "📝 Blog"
permalink: /blog/
---

<style>
  .blog-hero {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 60%, #ff4b2b 100%);
    border-radius: 16px;
    padding: 40px 35px;
    color: white;
    margin-bottom: 35px;
  }
  .blog-hero h1 { font-size: 2rem; font-weight: 800; margin: 0 0 10px; color: white; }
  .blog-hero p  { font-size: 1rem; opacity: 0.9; margin: 0; line-height: 1.6; }
  .tab-bar {
    display: flex;
    gap: 10px;
    margin-bottom: 30px;
    flex-wrap: wrap;
  }
  .tab-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 22px;
    border-radius: 30px;
    font-size: 0.9rem;
    font-weight: 700;
    cursor: pointer;
    border: 2px solid #e0e7ff;
    background: white;
    color: #555;
    transition: all 0.2s;
  }
  .tab-btn:hover        { border-color: #1e3c72; color: #1e3c72; }
  .tab-btn.active-all   { background: #1e3c72; color: white; border-color: #1e3c72; }
  .tab-btn.active-maths { background: #1e3c72; color: white; border-color: #1e3c72; }
  .tab-btn.active-hist  { background: #d4820a; color: white; border-color: #d4820a; }
  .tab-count {
    background: rgba(255,255,255,0.25);
    border-radius: 10px;
    padding: 1px 7px;
    font-size: 0.72rem;
  }
  .post-grid { display: flex; flex-direction: column; gap: 16px; }
  .post-card {
    background: white;
    border-radius: 14px;
    padding: 22px 26px;
    box-shadow: 0 3px 14px rgba(0,0,0,0.06);
    border-left: 5px solid #1e3c72;
    transition: all 0.25s ease;
    display: flex;
    gap: 18px;
    align-items: flex-start;
  }
  .post-card.cat-history { border-left-color: #d4820a; }
  .post-card.cat-general { border-left-color: #00b894; }
  .post-card:hover {
    transform: translateX(6px);
    box-shadow: 0 6px 22px rgba(0,0,0,0.1);
  }
  .post-cat-icon {
    width: 44px; height: 44px; border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem; flex-shrink: 0; margin-top: 2px;
  }
  .post-cat-icon.maths   { background: #e8eeff; color: #1e3c72; }
  .post-cat-icon.history { background: #fff8e1; color: #d4820a; }
  .post-cat-icon.general { background: #e6faf5; color: #00b894; }
  .post-card-body { flex: 1; }
  .post-badge {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 0.7rem; font-weight: 700; text-transform: uppercase;
    letter-spacing: 0.5px; padding: 2px 10px; border-radius: 10px;
    margin-bottom: 8px;
  }
  .badge-maths   { background: #e8eeff; color: #1e3c72; }
  .badge-history { background: #fff8e1; color: #d4820a; }
  .badge-general { background: #e6faf5; color: #00b894; }
  .post-card h3 {
    font-size: 1rem; font-weight: 700;
    color: #1a1a2e; margin: 0 0 6px; line-height: 1.4;
  }
  .post-card h3 a { text-decoration: none; color: inherit; }
  .post-card h3 a:hover { color: #ff4b2b; }
  .post-meta {
    font-size: 0.8rem; color: #999;
    display: flex; gap: 14px; margin-bottom: 8px; flex-wrap: wrap;
  }
  .post-meta span { display: flex; align-items: center; gap: 5px; }
  .post-desc { font-size: 0.88rem; color: #666; line-height: 1.55; margin-bottom: 12px; }
  .read-more {
    font-size: 0.82rem; font-weight: 700;
    color: #1e3c72; text-decoration: none;
    display: inline-flex; align-items: center; gap: 5px;
  }
  .read-more:hover { color: #ff4b2b; }
  .no-posts { text-align: center; padding: 60px 20px; color: #aaa; }
  @media (max-width: 600px) {
    .post-card { flex-direction: column; gap: 10px; }
    .post-cat-icon { display: none; }
  }
</style>

<div class="blog-hero">
  <h1>📝 Mathematics Blog</h1>
  <p>Concepts, theorems, solved problems, and the fascinating history of mathematics — for B.Sc., M.Sc., CSIR NET, GATE & IIT JAM students.</p>
</div>

<div class="tab-bar">
  <button class="tab-btn active-all" onclick="filterPosts('all', this)">
    <i class="fas fa-border-all"></i> All Posts
    <span class="tab-count" id="count-all">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('maths', this)">
    <i class="fas fa-square-root-alt"></i> Mathematics
    <span class="tab-count" id="count-maths">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('history', this)">
    <i class="fas fa-scroll"></i> History of Maths
    <span class="tab-count" id="count-history">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('general', this)">
    <i class="fas fa-pen"></i> General
    <span class="tab-count" id="count-general">0</span>
  </button>
</div>

<div class="post-grid" id="post-grid">

  {% for post in site.posts %}
  {% assign cat = post.category | default: "maths" %}

  <div class="post-card cat-{{ cat }}" data-cat="{{ cat }}">
    <div class="post-cat-icon {{ cat }}">
      {% if cat == "history" %}
        <i class="fas fa-scroll"></i>
      {% elsif cat == "general" %}
        <i class="fas fa-pen"></i>
      {% else %}
        <i class="fas fa-square-root-alt"></i>
      {% endif %}
    </div>
    <div class="post-card-body">
      <span class="post-badge badge-{{ cat }}">
        {% if cat == "history" %}
          <i class="fas fa-scroll"></i> History of Mathematics
        {% elsif cat == "general" %}
          <i class="fas fa-pen"></i> General
        {% else %}
          <i class="fas fa-square-root-alt"></i> Mathematics
        {% endif %}
      </span>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div class="post-meta">
        <span><i class="fas fa-calendar-alt"></i> {{ post.date | date: "%B %d, %Y" }}</span>
        <span><i class="fas fa-user"></i> Dr. Praveendra Singh</span>
      </div>
      {% if post.description %}
      <p class="post-desc">{{ post.description }}</p>
      {% endif %}
      <a class="read-more" href="{{ post.url }}">Read More <i class="fas fa-arrow-right"></i></a>
    </div>
  </div>

  {% endfor %}

  {% if site.posts.size == 0 %}
  <div class="no-posts">
    <i class="fas fa-pen" style="font-size:2rem; margin-bottom:15px; display:block;"></i>
    New posts coming soon. Stay tuned!
  </div>
  {% endif %}

</div>

<script>
  function countPosts() {
    const cards = document.querySelectorAll('.post-card');
    const counts = { all: cards.length, maths: 0, history: 0, general: 0 };
    cards.forEach(c => {
      const cat = c.dataset.cat || 'maths';
      if (counts[cat] !== undefined) counts[cat]++;
    });
    Object.keys(counts).forEach(k => {
      const el = document.getElementById('count-' + k);
      if (el) el.textContent = counts[k];
    });
  }
  function filterPosts(cat, btn) {
    document.querySelectorAll('.tab-btn').forEach(b => { b.className = 'tab-btn'; });
    if (cat === 'all')          btn.className = 'tab-btn active-all';
    else if (cat === 'maths')   btn.className = 'tab-btn active-maths';
    else if (cat === 'history') btn.className = 'tab-btn active-hist';
    else                        btn.className = 'tab-btn active-all';
    document.querySelectorAll('.post-card').forEach(card => {
      card.style.display = (cat === 'all' || card.dataset.cat === cat) ? 'flex' : 'none';
    });
  }
  document.addEventListener('DOMContentLoaded', countPosts);
</script>
