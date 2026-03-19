---
layout: default
title: "Lecture Notes"
permalink: /resources/lecture-notes/
---

<style>
  .sub-hero {
    background: linear-gradient(135deg, #059669, #10b981);
    border-radius: 16px; padding: 40px 35px; color: white; margin-bottom: 40px;
  }
  .sub-hero h1 { font-size: 2rem; font-weight: 800; color: white; margin: 0 0 10px; }
  .sub-hero p  { opacity: 0.9; margin: 0; font-size: 0.95rem; max-width: 650px; line-height: 1.7; }
  .breadcrumb  { font-size: 0.82rem; opacity: 0.8; margin-bottom: 12px; }
  .breadcrumb a { color: white; text-decoration: none; }
  .breadcrumb a:hover { text-decoration: underline; }

  .section-title {
    font-size: 1.25rem; font-weight: 800; color: #1e3c72;
    margin: 40px 0 20px; display: flex; align-items: center; gap: 12px;
    padding-bottom: 10px;
    border-bottom: 3px solid transparent;
    border-image: linear-gradient(to right, #059669, transparent) 1;
  }
  .notes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
    gap: 18px; margin-bottom: 30px;
  }
  .note-card {
    background: white; border-radius: 14px; padding: 22px;
    box-shadow: 0 4px 14px rgba(0,0,0,0.07);
    border-left: 5px solid #059669; transition: all 0.25s;
  }
  .note-card:hover { transform: translateY(-4px); box-shadow: 0 10px 28px rgba(0,0,0,0.12); }
  .note-card-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 10px; }
  .note-card h3 { font-size: 1rem; font-weight: 800; color: #1e3c72; margin: 0; }
  .note-badge {
    font-size: 0.68rem; font-weight: 700; padding: 3px 10px; border-radius: 12px;
    white-space: nowrap; flex-shrink: 0; margin-left: 8px;
  }
  .badge-available { background: #ecfdf5; color: #059669; border: 1px solid #a7f3d0; }
  .badge-soon      { background: #fef3c7; color: #92400e; border: 1px solid #fde68a; }
  .badge-blog      { background: #eff6ff; color: #1e3c72; border: 1px solid #bfdbfe; }
  .note-card p  { font-size: 0.85rem; color: #555; line-height: 1.65; margin: 0 0 14px; }
  .note-topics  { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 16px; }
  .note-topic   { font-size: 0.72rem; background: #f0fdf4; color: #166534; padding: 3px 9px; border-radius: 10px; font-weight: 600; }
  .note-links   { display: flex; gap: 10px; flex-wrap: wrap; }
  .note-link {
    display: inline-flex; align-items: center; gap: 6px;
    font-size: 0.8rem; font-weight: 700; padding: 7px 16px;
    border-radius: 20px; text-decoration: none; transition: all 0.2s;
  }
  .link-blog   { background: #eff6ff; color: #1e3c72; }
  .link-blog:hover { background: #1e3c72; color: white; text-decoration: none; }
  .link-pdf    { background: #ecfdf5; color: #059669; }
  .link-pdf:hover  { background: #059669; color: white; text-decoration: none; }
  .link-coming { background: #f1f5f9; color: #94a3b8; cursor: not-allowed; }

  .contribute-box {
    background: linear-gradient(135deg, #ecfdf5, #d1fae5);
    border: 2px dashed #059669; border-radius: 14px;
    padding: 28px 30px; margin-top: 20px; text-align: center;
  }
  .contribute-box h3 { color: #065f46; margin: 0 0 8px; }
  .contribute-box p  { color: #047857; font-size: 0.9rem; margin: 0 0 16px; }
  .contribute-btn {
    display: inline-flex; align-items: center; gap: 8px;
    background: #059669; color: white; text-decoration: none;
    padding: 10px 24px; border-radius: 30px;
    font-weight: 700; font-size: 0.9rem; transition: all 0.2s;
  }
  .contribute-btn:hover { background: #047857; transform: translateY(-2px); color: white; text-decoration: none; }

  .back-link {
    display: inline-flex; align-items: center; gap: 8px;
    color: #059669; text-decoration: none; font-size: 0.88rem; font-weight: 600;
    margin-top: 30px; padding: 8px 18px; border-radius: 30px;
    background: #ecfdf5; border: 1px solid #a7f3d0; transition: all 0.2s;
  }
  .back-link:hover { background: #059669; color: white; text-decoration: none; }
</style>

<div class="sub-hero">
  <p class="breadcrumb"><a href="/resources/">← Resources Hub</a> / Lecture Notes</p>
  <h1><i class="fas fa-file-alt"></i> Lecture Notes</h1>
  <p>My own lecture notes — carefully structured for B.Sc., M.Sc. students and CSIR NET / GATE / IIT JAM aspirants. Notes are continuously updated.</p>
</div>

<!-- Real Analysis -->
<div class="section-title"><i class="fas fa-infinity" style="color:#059669;"></i> Real Analysis</div>

<div class="notes-grid">

  <div class="note-card">
    <div class="note-card-header">
      <h3>Sequences & Series</h3>
      <span class="note-badge badge-blog">Blog</span>
    </div>
    <p>Convergence of sequences, Cauchy sequences, series convergence tests — Ratio, Root, Raabe's, Alternating Series, Weierstrass M-Test.</p>
    <div class="note-topics">
      <span class="note-topic">Convergence Tests</span>
      <span class="note-topic">Uniform Convergence</span>
      <span class="note-topic">Fourier Series</span>
    </div>
    <div class="note-links">
      <a href="/blog/" class="note-link link-blog"><i class="fas fa-pen"></i> Read on Blog</a>
    </div>
  </div>

  <div class="note-card">
    <div class="note-card-header">
      <h3>Point Set Topology</h3>
      <span class="note-badge badge-blog">Blog</span>
    </div>
    <p>Open and closed sets, limit points, interior/exterior/boundary, compact sets, Heine-Borel theorem, connected sets, dense and nowhere dense sets.</p>
    <div class="note-topics">
      <span class="note-topic">Metric Spaces</span>
      <span class="note-topic">Compactness</span>
      <span class="note-topic">Connectedness</span>
    </div>
    <div class="note-links">
      <a href="/blog/" class="note-link link-blog"><i class="fas fa-pen"></i> Read on Blog</a>
    </div>
  </div>

  <div class="note-card">
    <div class="note-card-header">
      <h3>Differentiation & Integration</h3>
      <span class="note-badge badge-soon">Coming Soon</span>
    </div>
    <p>Riemann integration, fundamental theorem of calculus, uniform continuity, differentiability, mean value theorems, and Taylor series.</p>
    <div class="note-topics">
      <span class="note-topic">Riemann Integral</span>
      <span class="note-topic">MVT</span>
      <span class="note-topic">Taylor Series</span>
    </div>
    <div class="note-links">
      <span class="note-link link-coming"><i class="fas fa-clock"></i> Coming Soon</span>
    </div>
  </div>

</div>

<!-- Linear Algebra -->
<div class="section-title"><i class="fas fa-th" style="color:#1e3c72;"></i> Linear Algebra</div>

<div class="notes-grid">
  <div class="note-card" style="border-left-color:#1e3c72;">
    <div class="note-card-header">
      <h3>Matrices & Determinants</h3>
      <span class="note-badge badge-soon">Coming Soon</span>
    </div>
    <p>Matrix operations, rank, determinants, systems of linear equations, eigenvalues, eigenvectors, diagonalization.</p>
    <div class="note-topics">
      <span class="note-topic">Eigenvalues</span>
      <span class="note-topic">Rank</span>
      <span class="note-topic">Diagonalization</span>
    </div>
    <div class="note-links">
      <span class="note-link link-coming"><i class="fas fa-clock"></i> Coming Soon</span>
    </div>
  </div>

  <div class="note-card" style="border-left-color:#1e3c72;">
    <div class="note-card-header">
      <h3>Vector Spaces</h3>
      <span class="note-badge badge-soon">Coming Soon</span>
    </div>
    <p>Subspaces, basis, dimension, linear transformations, null space, range, inner product spaces, orthogonality.</p>
    <div class="note-topics">
      <span class="note-topic">Basis & Dimension</span>
      <span class="note-topic">Linear Maps</span>
      <span class="note-topic">Inner Product</span>
    </div>
    <div class="note-links">
      <span class="note-link link-coming"><i class="fas fa-clock"></i> Coming Soon</span>
    </div>
  </div>
</div>

<!-- Differential Equations -->
<div class="section-title"><i class="fas fa-wave-square" style="color:#7c3aed;"></i> Differential Equations</div>

<div class="notes-grid">
  <div class="note-card" style="border-left-color:#7c3aed;">
    <div class="note-card-header">
      <h3>Ordinary Differential Equations</h3>
      <span class="note-badge badge-soon">Coming Soon</span>
    </div>
    <p>First and second order ODEs, series solutions, Laplace transforms, systems of ODEs, existence and uniqueness theorems.</p>
    <div class="note-topics">
      <span class="note-topic">First Order</span>
      <span class="note-topic">Laplace Transform</span>
      <span class="note-topic">Series Solutions</span>
    </div>
    <div class="note-links">
      <span class="note-link link-coming"><i class="fas fa-clock"></i> Coming Soon</span>
    </div>
  </div>
</div>

<!-- Request -->
<div class="contribute-box">
  <h3><i class="fas fa-hand-paper"></i> Request Notes on a Specific Topic</h3>
  <p>Can't find notes on a topic you need? Send a request and I will prioritise it for the next update.</p>
  <a href="https://t.me/fractalfrontiermaths" target="_blank" rel="noopener" class="contribute-btn">
    <i class="fab fa-telegram"></i> Request on Telegram
  </a>
</div>

<a href="/resources/" class="back-link"><i class="fas fa-arrow-left"></i> Back to Resources Hub</a>
