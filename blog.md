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

  /* ── Tab Bar ── */
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
  .tab-btn:hover         { border-color: #1e3c72; color: #1e3c72; }
  .tab-btn.active-all    { background: #1e3c72; color: white; border-color: #1e3c72; }
  .tab-btn.active-maths  { background: #1e3c72; color: white; border-color: #1e3c72; }
  .tab-btn.active-hist   { background: #d4820a; color: white; border-color: #d4820a; }
  .tab-btn.active-gen    { background: #059669; color: white; border-color: #059669; }
  .tab-btn.active-hindi  { background: #e65100; color: white; border-color: #e65100; }
  .tab-btn.active-eng    { background: #1565c0; color: white; border-color: #1565c0; }

  .tab-count {
    background: rgba(255,255,255,0.25);
    border-radius: 10px;
    padding: 1px 7px;
    font-size: 0.72rem;
  }

  /* ── Tab Group Divider ── */
  .tab-divider {
    width: 1px;
    height: 30px;
    background: #e0e7ff;
    align-self: center;
    margin: 0 4px;
  }

  /* ── Post Cards ── */
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
  .post-card.cat-general { border-left-color: #059669; }
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
  .post-cat-icon.general { background: #e6faf5; color: #059669; }

  .post-card-body { flex: 1; }

  /* ── Badges row ── */
  .badges-row {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 8px;
    align-items: center;
  }

  .post-badge {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 0.7rem; font-weight: 700; text-transform: uppercase;
    letter-spacing: 0.5px; padding: 2px 10px; border-radius: 10px;
  }
  .badge-maths   { background: #e8eeff; color: #1e3c72; }
  .badge-history { background: #fff8e1; color: #d4820a; }
  .badge-general { background: #e6faf5; color: #059669; }

  /* ── Language Badge ── */
  .lang-badge {
    display: inline-flex; align-items: center; gap: 4px;
    font-size: 0.7rem; font-weight: 700;
    padding: 2px 9px; border-radius: 10px;
  }
  .lang-hi { background: #fff3e0; color: #e65100; border: 1px solid #ffcc80; }
  .lang-en { background: #e3f2fd; color: #1565c0; border: 1px solid #90caf9; }

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
    .tab-divider { display: none; }
  }
</style>

<div class="blog-hero">
  <h1>📝 Mathematics Blog</h1>
  <p>Concepts, theorems, solved problems, and the fascinating history of mathematics — available in both English and Hindi, for B.Sc., M.Sc., CSIR NET, GATE &amp; IIT JAM students.</p>
</div>

<!-- ══════════════════════════════════════════════════ -->
<!-- TAB BAR — Category + Language filters              -->
<!-- ══════════════════════════════════════════════════ -->
<div class="tab-bar">

  <!-- Category Filters -->
  <button class="tab-btn active-all" onclick="filterPosts('all', this, 'cat')">
    <i class="fas fa-border-all"></i> All Posts
    <span class="tab-count" id="count-all">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('maths', this, 'cat')">
    <i class="fas fa-square-root-alt"></i> Mathematics
    <span class="tab-count" id="count-maths">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('history', this, 'cat')">
    <i class="fas fa-scroll"></i> History
    <span class="tab-count" id="count-history">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('general', this, 'cat')">
    <i class="fas fa-pen"></i> General
    <span class="tab-count" id="count-general">0</span>
  </button>

  <!-- Divider -->
  <div class="tab-divider"></div>

  <!-- Language Filters -->
  <button class="tab-btn" onclick="filterPosts('hi', this, 'lang')">
    🇮🇳 हिंदी
    <span class="tab-count" id="count-hi">0</span>
  </button>
  <button class="tab-btn" onclick="filterPosts('en', this, 'lang')">
    🇬🇧 English
    <span class="tab-count" id="count-en">0</span>
  </button>

</div>

<!-- ══════════════════════════════════════════════════ -->
<!-- POST GRID                                          -->
<!-- ══════════════════════════════════════════════════ -->
<div class="post-grid" id="post-grid">

  {% for post in site.posts %}

  {% assign cat  = post.category | default: "maths" %}
  {% assign lang = post.lang     | default: "" %}

  <div class="post-card cat-{{ cat }}"
       data-cat="{{ cat }}"
       data-lang="{{ lang }}">

    <!-- Category Icon -->
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

      <!-- Badges Row: Category + Language -->
      <div class="badges-row">

        <span class="post-badge badge-{{ cat }}">
          {% if cat == "history" %}
            <i class="fas fa-scroll"></i> History of Mathematics
          {% elsif cat == "general" %}
            <i class="fas fa-pen"></i> General
          {% else %}
            <i class="fas fa-square-root-alt"></i> Mathematics
          {% endif %}
        </span>

        {% if lang == "hi" %}
          <span class="lang-badge lang-hi">🇮🇳 हिंदी</span>
        {% elsif lang == "en" %}
          <span class="lang-badge lang-en">🇬🇧 English</span>
        {% endif %}

      </div>

      <!-- Title -->
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>

      <!-- Meta -->
      <div class="post-meta">
        <span><i class="fas fa-calendar-alt"></i> {{ post.date | date: "%B %d, %Y" }}</span>
        <span><i class="fas fa-user"></i> Dr. Praveendra Singh</span>
      </div>

      <!-- Description -->
      {% if post.description %}
      <p class="post-desc">{{ post.description }}</p>
      {% endif %}

      <!-- Read More + Language pair link -->
      <div style="display:flex; align-items:center; gap:16px; flex-wrap:wrap;">
        <a class="read-more" href="{{ post.url }}">Read More <i class="fas fa-arrow-right"></i></a>
        {% if post.lang_pair %}
          {% if post.lang == "hi" %}
            <a href="{{ post.lang_pair }}"
               style="font-size:0.78rem; color:#1565c0; text-decoration:none; font-weight:600; display:inline-flex; align-items:center; gap:4px;">
              <i class="fas fa-language"></i> Read in English
            </a>
          {% elsif post.lang == "en" %}
            <a href="{{ post.lang_pair }}"
               style="font-size:0.78rem; color:#e65100; text-decoration:none; font-weight:600; display:inline-flex; align-items:center; gap:4px;">
              <i class="fas fa-language"></i> हिंदी में पढ़ें
            </a>
          {% endif %}
        {% endif %}
      </div>

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
  var activeFilter = { cat: 'all', lang: 'all' };

  function countPosts() {
    const cards = document.querySelectorAll('.post-card');
    const counts = { all: cards.length, maths: 0, history: 0, general: 0, hi: 0, en: 0 };
    cards.forEach(c => {
      const cat  = c.dataset.cat  || 'maths';
      const lang = c.dataset.lang || '';
      if (counts[cat]  !== undefined) counts[cat]++;
      if (lang === 'hi') counts.hi++;
      if (lang === 'en') counts.en++;
    });
    Object.keys(counts).forEach(k => {
      const el = document.getElementById('count-' + k);
      if (el) el.textContent = counts[k];
    });
  }

  function filterPosts(value, btn, type) {
    // Update active state for clicked button group
    if (type === 'cat') {
      activeFilter.cat = value;
      // Reset all cat buttons
      document.querySelectorAll('.tab-btn').forEach(b => {
        if (['all','maths','history','general'].some(v =>
          b.getAttribute('onclick') && b.getAttribute('onclick').includes("'" + v + "'"))) {
          b.className = 'tab-btn';
        }
      });
      if (value === 'all')     btn.className = 'tab-btn active-all';
      else if (value === 'maths')   btn.className = 'tab-btn active-maths';
      else if (value === 'history') btn.className = 'tab-btn active-hist';
      else if (value === 'general') btn.className = 'tab-btn active-gen';

    } else if (type === 'lang') {
      // Toggle: click again to deselect
      if (activeFilter.lang === value) {
        activeFilter.lang = 'all';
        btn.className = 'tab-btn';
      } else {
        activeFilter.lang = value;
        // Reset other lang buttons
        document.querySelectorAll('.tab-btn').forEach(b => {
          if (b.getAttribute('onclick') &&
              (b.getAttribute('onclick').includes("'hi'") ||
               b.getAttribute('onclick').includes("'en'"))) {
            b.className = 'tab-btn';
          }
        });
        if (value === 'hi') btn.className = 'tab-btn active-hindi';
        else                btn.className = 'tab-btn active-eng';
      }
    }

    // Apply filters
    document.querySelectorAll('.post-card').forEach(card => {
      const cardCat  = card.dataset.cat  || 'maths';
      const cardLang = card.dataset.lang || '';

      const catOk  = activeFilter.cat  === 'all' || cardCat  === activeFilter.cat;
      const langOk = activeFilter.lang === 'all' || cardLang === activeFilter.lang;

      card.style.display = (catOk && langOk) ? 'flex' : 'none';
    });
  }

  document.addEventListener('DOMContentLoaded', countPosts);
</script>
