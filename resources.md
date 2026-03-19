---
layout: default
title: "Student Resources Hub"
permalink: /resources/
---

<style>
  .resources-hero {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 55%, #059669 100%);
    border-radius: 18px; padding: 50px 40px; color: white;
    margin-bottom: 45px; position: relative; overflow: hidden;
  }
  .resources-hero::before {
    content: "📚";
    position: absolute; right: 40px; top: 20px;
    font-size: 7rem; opacity: 0.1;
  }
  .resources-hero h1 { font-size: 2.4rem; font-weight: 800; color: white; margin: 0 0 12px; }
  .resources-hero p  { font-size: 1.05rem; opacity: 0.92; max-width: 680px; line-height: 1.7; margin: 0; }
  .hero-badge {
    display: inline-block;
    background: rgba(255,255,255,0.2); border: 1px solid rgba(255,255,255,0.35);
    border-radius: 20px; padding: 5px 16px;
    font-size: 0.82rem; font-weight: 600; margin-bottom: 18px;
  }

  .resources-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
    gap: 26px; margin-bottom: 50px;
  }
  .resource-card {
    background: white; border-radius: 18px;
    box-shadow: 0 6px 20px rgba(0,0,0,0.08);
    overflow: hidden; transition: all 0.3s;
    text-decoration: none; color: inherit;
    display: flex; flex-direction: column;
    border: 1px solid #f0f4ff;
  }
  .resource-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 16px 40px rgba(0,0,0,0.14);
    text-decoration: none; color: inherit;
  }
  .card-banner {
    height: 10px;
  }
  .card-banner.blue   { background: linear-gradient(90deg, #1e3c72, #2a5298); }
  .card-banner.green  { background: linear-gradient(90deg, #059669, #10b981); }
  .card-banner.gold   { background: linear-gradient(90deg, #d97706, #fbbf24); }
  .card-banner.purple { background: linear-gradient(90deg, #7c3aed, #a855f7); }

  .card-body { padding: 28px 26px; flex: 1; }
  .card-icon-wrap {
    width: 58px; height: 58px; border-radius: 16px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.6rem; margin-bottom: 18px;
  }
  .icon-blue   { background: #eff6ff; color: #1e3c72; }
  .icon-green  { background: #ecfdf5; color: #059669; }
  .icon-gold   { background: #fffbeb; color: #d97706; }
  .icon-purple { background: #f5f3ff; color: #7c3aed; }

  .card-body h2 {
    font-size: 1.2rem; font-weight: 800; color: #1e3c72;
    margin: 0 0 10px; border: none; padding: 0;
  }
  .card-body p {
    font-size: 0.88rem; color: #666; line-height: 1.7; margin: 0 0 18px;
  }
  .card-items { list-style: none; padding: 0; margin: 0 0 20px; }
  .card-items li {
    font-size: 0.83rem; color: #555; padding: 5px 0;
    display: flex; align-items: center; gap: 8px;
    border-bottom: 1px solid #f1f5f9;
  }
  .card-items li:last-child { border-bottom: none; }
  .card-items li i { font-size: 0.75rem; flex-shrink: 0; }

  .card-footer {
    padding: 16px 26px;
    border-top: 1px solid #f1f5f9;
    background: #fafbff;
  }
  .card-link {
    display: inline-flex; align-items: center; gap: 8px;
    font-size: 0.85rem; font-weight: 700;
    text-decoration: none; transition: all 0.2s;
    padding: 8px 20px; border-radius: 30px;
  }
  .card-link.blue   { background: #eff6ff; color: #1e3c72; }
  .card-link.green  { background: #ecfdf5; color: #059669; }
  .card-link.gold   { background: #fffbeb; color: #d97706; }
  .card-link.purple { background: #f5f3ff; color: #7c3aed; }
  .card-link:hover  { filter: brightness(0.92); transform: translateX(3px); text-decoration: none; }

  .coming-soon-badge {
    display: inline-flex; align-items: center; gap: 5px;
    background: #fef3c7; color: #92400e;
    border: 1px solid #fde68a; border-radius: 12px;
    padding: 3px 10px; font-size: 0.72rem; font-weight: 700;
    margin-left: 8px; vertical-align: middle;
  }

  .section-title {
    font-size: 1.3rem; font-weight: 800; color: #1e3c72;
    margin: 40px 0 20px;
    display: flex; align-items: center; gap: 12px;
  }
  .section-title::after {
    content: ''; flex: 1; height: 2px;
    background: linear-gradient(to right, #1e3c72, transparent);
  }

  .quick-links-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 14px; margin-bottom: 40px;
  }
  .quick-link-card {
    background: white; border-radius: 12px; padding: 18px 16px;
    text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    text-decoration: none; color: #1e3c72; font-weight: 600;
    font-size: 0.88rem; transition: all 0.25s;
    border: 1px solid #e0e7ff;
    display: flex; flex-direction: column; align-items: center; gap: 10px;
  }
  .quick-link-card i { font-size: 1.5rem; }
  .quick-link-card:hover {
    background: #1e3c72; color: white; transform: translateY(-4px);
    box-shadow: 0 8px 20px rgba(30,60,114,0.25); text-decoration: none;
  }

  @media (max-width: 768px) {
    .resources-hero { padding: 35px 22px; }
    .resources-hero h1 { font-size: 1.8rem; }
  }
</style>

<!-- Hero -->
<div class="resources-hero">
  <div class="hero-badge">📚 Student Resources</div>
  <h1>Mathematics Resource Hub</h1>
  <p>Everything you need for B.Sc., M.Sc., CSIR NET, GATE and IIT JAM preparation — free digital books, lecture notes, past papers, and official syllabi — all in one place.</p>
</div>

<!-- 4 Resource Cards -->
<div class="resources-grid">

  <!-- Digital Library -->
  <a class="resource-card" href="/resources/digital-library/">
    <div class="card-banner blue"></div>
    <div class="card-body">
      <div class="card-icon-wrap icon-blue"><i class="fas fa-globe"></i></div>
      <h2>Digital Library</h2>
      <p>Free public digital content — textbooks, lecture series, video courses, and open-access mathematics resources from top institutions worldwide.</p>
      <ul class="card-items">
        <li><i class="fas fa-check-circle" style="color:#1e3c72;"></i> NPTEL Video Lectures</li>
        <li><i class="fas fa-check-circle" style="color:#1e3c72;"></i> MIT OpenCourseWare</li>
        <li><i class="fas fa-check-circle" style="color:#1e3c72;"></i> Internet Archive & LibreTexts</li>
        <li><i class="fas fa-check-circle" style="color:#1e3c72;"></i> arXiv & Open Textbooks</li>
      </ul>
    </div>
    <div class="card-footer">
      <span class="card-link blue"><i class="fas fa-arrow-right"></i> Browse Library</span>
    </div>
  </a>

  <!-- Lecture Notes -->
  <a class="resource-card" href="/resources/lecture-notes/">
    <div class="card-banner green"></div>
    <div class="card-body">
      <div class="card-icon-wrap icon-green"><i class="fas fa-file-alt"></i></div>
      <h2>Lecture Notes</h2>
      <p>My own handwritten and typed lecture notes — structured topic-by-topic, aligned with university syllabi and competitive exam requirements.</p>
      <ul class="card-items">
        <li><i class="fas fa-check-circle" style="color:#059669;"></i> Real Analysis</li>
        <li><i class="fas fa-check-circle" style="color:#059669;"></i> Linear Algebra</li>
        <li><i class="fas fa-check-circle" style="color:#059669;"></i> Differential Equations</li>
        <li><i class="fas fa-check-circle" style="color:#059669;"></i> More topics coming soon</li>
      </ul>
    </div>
    <div class="card-footer">
      <span class="card-link green"><i class="fas fa-arrow-right"></i> View Notes</span>
    </div>
  </a>

  <!-- Previous Year Papers -->
  <a class="resource-card" href="/resources/previous-papers/">
    <div class="card-banner gold"></div>
    <div class="card-body">
      <div class="card-icon-wrap icon-gold"><i class="fas fa-file-alt"></i></div>
      <h2>Previous Year Papers</h2>
      <p>Past question papers with detailed solutions for CSIR NET, GATE, and IIT JAM — the most effective way to prepare for competitive examinations.</p>
      <ul class="card-items">
        <li><i class="fas fa-check-circle" style="color:#d97706;"></i> CSIR NET Mathematical Sciences</li>
        <li><i class="fas fa-check-circle" style="color:#d97706;"></i> GATE Mathematics (MA)</li>
        <li><i class="fas fa-check-circle" style="color:#d97706;"></i> IIT JAM Mathematics</li>
        <li><i class="fas fa-check-circle" style="color:#d97706;"></i> Solutions & Answer Keys</li>
      </ul>
    </div>
    <div class="card-footer">
      <span class="card-link gold"><i class="fas fa-arrow-right"></i> View Papers</span>
    </div>
  </a>

  <!-- Syllabi -->
  <a class="resource-card" href="/resources/syllabus/">
    <div class="card-banner purple"></div>
    <div class="card-body">
      <div class="card-icon-wrap icon-purple"><i class="fas fa-list-alt"></i></div>
      <h2>Exam Syllabi</h2>
      <p>Official and detailed syllabi for major competitive mathematics examinations — know exactly what to study and plan your preparation effectively.</p>
      <ul class="card-items">
        <li><i class="fas fa-check-circle" style="color:#7c3aed;"></i> CSIR NET Syllabus</li>
        <li><i class="fas fa-check-circle" style="color:#7c3aed;"></i> GATE MA Syllabus</li>
        <li><i class="fas fa-check-circle" style="color:#7c3aed;"></i> IIT JAM Syllabus</li>
        <li><i class="fas fa-check-circle" style="color:#7c3aed;"></i> University B.Sc. / M.Sc. Syllabi</li>
      </ul>
    </div>
    <div class="card-footer">
      <span class="card-link purple"><i class="fas fa-arrow-right"></i> View Syllabi</span>
    </div>
  </a>

</div>

<!-- Other Quick Links -->
<div class="section-title"><i class="fas fa-link"></i> More Resources</div>

<div class="quick-links-grid">
  <a href="/blog/" class="quick-link-card">
    <i class="fas fa-pen-nib" style="color:#ff4b2b;"></i>
    Mathematics Blog
  </a>
  <a href="/videos/" class="quick-link-card">
    <i class="fab fa-youtube" style="color:#ff0000;"></i>
    Video Lectures
  </a>
  <a href="/recommended-books/" class="quick-link-card">
    <i class="fas fa-book-open" style="color:#1e3c72;"></i>
    Recommended Books
  </a>
  <a href="https://t.me/fractalfrontiermaths" class="quick-link-card" target="_blank" rel="noopener">
    <i class="fab fa-telegram" style="color:#0088cc;"></i>
    Telegram Community
  </a>
</div>
