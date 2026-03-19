---
layout: default
title: "Digital Library"
permalink: /resources/digital-library/
---

<style>
  .sub-hero {
    background: linear-gradient(135deg, #1e3c72, #2a5298);
    border-radius: 16px; padding: 40px 35px; color: white; margin-bottom: 40px;
  }
  .sub-hero h1 { font-size: 2rem; font-weight: 800; color: white; margin: 0 0 10px; }
  .sub-hero p  { opacity: 0.88; margin: 0; font-size: 0.95rem; max-width: 650px; line-height: 1.7; }
  .breadcrumb  { font-size: 0.82rem; opacity: 0.75; margin-bottom: 12px; }
  .breadcrumb a { color: white; text-decoration: none; }
  .breadcrumb a:hover { text-decoration: underline; }

  .lib-section { margin-bottom: 45px; }
  .section-title {
    font-size: 1.25rem; font-weight: 800; color: #1e3c72;
    margin: 0 0 20px; display: flex; align-items: center; gap: 12px;
    padding-bottom: 10px;
    border-bottom: 3px solid transparent;
    border-image: linear-gradient(to right, #1e3c72, transparent) 1;
  }
  .lib-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 18px;
  }
  .lib-card {
    background: white; border-radius: 14px; padding: 22px 22px 18px;
    box-shadow: 0 4px 14px rgba(0,0,0,0.07);
    transition: all 0.25s; text-decoration: none; color: inherit;
    display: flex; flex-direction: column;
    border-top: 4px solid #1e3c72;
  }
  .lib-card:nth-child(2) { border-top-color: #ff4b2b; }
  .lib-card:nth-child(3) { border-top-color: #059669; }
  .lib-card:nth-child(4) { border-top-color: #d97706; }
  .lib-card:nth-child(5) { border-top-color: #7c3aed; }
  .lib-card:nth-child(6) { border-top-color: #0891b2; }
  .lib-card:hover { transform: translateY(-5px); box-shadow: 0 10px 28px rgba(0,0,0,0.12); text-decoration: none; }
  .lib-card-header { display: flex; align-items: center; gap: 12px; margin-bottom: 10px; }
  .lib-card-icon { font-size: 1.6rem; }
  .lib-card h3 { font-size: 1rem; font-weight: 800; color: #1e3c72; margin: 0; }
  .lib-card .lib-type { font-size: 0.7rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; color: #888; }
  .lib-card p  { font-size: 0.85rem; color: #555; line-height: 1.65; margin: 0 0 14px; flex: 1; }
  .lib-card-footer { display: flex; justify-content: space-between; align-items: center; }
  .lib-visit {
    display: inline-flex; align-items: center; gap: 6px;
    font-size: 0.8rem; font-weight: 700; color: #1e3c72;
    text-decoration: none; transition: gap 0.2s;
  }
  .lib-visit:hover { gap: 10px; color: #ff4b2b; text-decoration: none; }
  .lib-tag {
    font-size: 0.68rem; font-weight: 700;
    background: #f1f5f9; color: #475569;
    padding: 3px 9px; border-radius: 10px;
  }
  .back-link {
    display: inline-flex; align-items: center; gap: 8px;
    color: #1e3c72; text-decoration: none; font-size: 0.88rem; font-weight: 600;
    margin-top: 10px; padding: 8px 18px; border-radius: 30px;
    background: #eff6ff; border: 1px solid #bfdbfe; transition: all 0.2s;
  }
  .back-link:hover { background: #1e3c72; color: white; text-decoration: none; }
</style>

<div class="sub-hero">
  <p class="breadcrumb"><a href="/resources/">← Resources Hub</a> / Digital Library</p>
  <h1><i class="fas fa-globe"></i> Digital Library</h1>
  <p>Free, publicly accessible mathematics resources from top institutions worldwide — textbooks, video lectures, research papers, and open-access learning platforms.</p>
</div>

<!-- Video Lecture Platforms -->
<div class="lib-section">
  <div class="section-title"><i class="fas fa-video" style="color:#ff0000;"></i> Video Lecture Platforms</div>
  <div class="lib-grid">

    <a class="lib-card" href="https://nptel.ac.in/courses" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">🇮🇳</span>
        <div><h3>NPTEL Mathematics</h3><span class="lib-type">Video Lectures</span></div>
      </div>
      <p>Free IIT and IISc professor lectures on Real Analysis, Linear Algebra, Differential Equations, Topology, and more. Official Government of India platform.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Visit NPTEL <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free</span>
      </div>
    </a>

    <a class="lib-card" href="https://ocw.mit.edu/courses/mathematics/" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">🎓</span>
        <div><h3>MIT OpenCourseWare</h3><span class="lib-type">Courses & Notes</span></div>
      </div>
      <p>Full lecture notes, assignments, and exams from MIT mathematics courses — including Real Analysis, Algebra, Probability, and Topology. World-class content, completely free.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Visit MIT OCW <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free</span>
      </div>
    </a>

    <a class="lib-card" href="https://www.youtube.com/@FractalFrontierMaths" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">📺</span>
        <div><h3>Fractal Frontier Maths</h3><span class="lib-type">YouTube Channel</span></div>
      </div>
      <p>Our own YouTube channel with animated mathematics lectures in Hindi — covering Real Analysis, Linear Algebra, ODE, and exam-focused content for CSIR NET and GATE.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Watch Now <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Hindi</span>
      </div>
    </a>

  </div>
</div>

<!-- Free Textbooks -->
<div class="lib-section">
  <div class="section-title"><i class="fas fa-book-open" style="color:#059669;"></i> Free Textbooks & Open Books</div>
  <div class="lib-grid">

    <a class="lib-card" href="https://math.libretexts.org/" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">📖</span>
        <div><h3>LibreTexts Mathematics</h3><span class="lib-type">Open Textbooks</span></div>
      </div>
      <p>Thousands of free, openly licensed mathematics textbooks covering undergraduate and graduate topics. Searchable, readable online, and downloadable as PDF.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Browse Books <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free PDF</span>
      </div>
    </a>

    <a class="lib-card" href="https://archive.org/search?query=mathematics+textbook&mediatype=texts" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">🗄️</span>
        <div><h3>Internet Archive</h3><span class="lib-type">Classic Books</span></div>
      </div>
      <p>Millions of free books including classic mathematics textbooks by Rudin, Apostol, Royden, Herstein, and many more. Borrow or download in PDF format.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Search Archive <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free</span>
      </div>
    </a>

    <a class="lib-card" href="https://www.gutenberg.org/ebooks/bookshelf/672" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">📜</span>
        <div><h3>Project Gutenberg</h3><span class="lib-type">Classic Texts</span></div>
      </div>
      <p>Public domain mathematics books — including works by Euler, Gauss, and other historical mathematicians. Free to download in multiple formats.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Visit Gutenberg <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Public Domain</span>
      </div>
    </a>

  </div>
</div>

<!-- Research & Preprints -->
<div class="lib-section">
  <div class="section-title"><i class="fas fa-flask" style="color:#7c3aed;"></i> Research Papers & Preprints</div>
  <div class="lib-grid">

    <a class="lib-card" href="https://arxiv.org/archive/math" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">📄</span>
        <div><h3>arXiv Mathematics</h3><span class="lib-type">Preprints</span></div>
      </div>
      <p>Free preprints of mathematics research papers — the world's largest open-access mathematics archive. Browse by subject area including Analysis, Algebra, and Topology.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Browse arXiv <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free</span>
      </div>
    </a>

    <a class="lib-card" href="https://scholar.google.com/" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">🔍</span>
        <div><h3>Google Scholar</h3><span class="lib-type">Research Search</span></div>
      </div>
      <p>Search millions of research papers, theses, and books. Many papers have free PDF links. Essential for finding references for M.Sc. projects and research.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">Search Papers <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free</span>
      </div>
    </a>

    <a class="lib-card" href="https://www.ams.org/open-math-notes" target="_blank" rel="noopener">
      <div class="lib-card-header">
        <span class="lib-card-icon">🏛️</span>
        <div><h3>AMS Open Math Notes</h3><span class="lib-type">Lecture Notes</span></div>
      </div>
      <p>Free lecture notes from professors around the world — contributed to the American Mathematical Society's open repository. Graduate-level coverage.</p>
      <div class="lib-card-footer">
        <span class="lib-visit">View Notes <i class="fas fa-arrow-right"></i></span>
        <span class="lib-tag">Free PDF</span>
      </div>
    </a>

  </div>
</div>

<a href="/resources/" class="back-link"><i class="fas fa-arrow-left"></i> Back to Resources Hub</a>
