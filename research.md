---
layout: default
title: Research
permalink: /research/
---

<style>

  /* ── Hero Banner ── */
  .research-hero {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 60%, #ff4b2b 100%);
    border-radius: 18px;
    padding: 50px 40px;
    color: white;
    margin-bottom: 45px;
    position: relative;
    overflow: hidden;
  }
  .research-hero::before {
    content: "∑ ∫ ∂ π";
    position: absolute;
    top: 10px;
    right: 30px;
    font-size: 5rem;
    opacity: 0.08;
    font-family: serif;
    letter-spacing: 20px;
  }
  .research-hero h1 {
    font-size: 2.4rem;
    font-weight: 800;
    margin: 0 0 12px 0;
    color: white;
  }
  .research-hero p {
    font-size: 1.1rem;
    opacity: 0.92;
    max-width: 680px;
    line-height: 1.7;
    margin: 0;
  }
  .research-hero .hero-badge {
    display: inline-block;
    background: rgba(255,255,255,0.2);
    border: 1px solid rgba(255,255,255,0.35);
    border-radius: 20px;
    padding: 5px 16px;
    font-size: 0.82rem;
    font-weight: 600;
    margin-bottom: 18px;
    letter-spacing: 0.5px;
  }

  /* ── Section Title ── */
  .section-title {
    font-size: 1.45rem;
    font-weight: 800;
    color: #1e3c72;
    margin: 45px 0 22px 0;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 2px;
    background: linear-gradient(to right, #1e3c72, transparent);
    border-radius: 2px;
  }

  /* ── Research Area Cards ── */
  .area-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 22px;
    margin-bottom: 10px;
  }
  .area-card {
    background: white;
    border-radius: 16px;
    padding: 28px 24px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.07);
    transition: all 0.3s ease;
    border-top: 5px solid transparent;
    position: relative;
    overflow: hidden;
  }
  .area-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 3px;
    opacity: 0;
    transition: opacity 0.3s;
  }
  .area-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 30px rgba(0,0,0,0.12);
  }
  .area-card.blue  { border-top-color: #1e3c72; }
  .area-card.red   { border-top-color: #ff4b2b; }
  .area-card.green { border-top-color: #00b894; }
  .area-card.gold  { border-top-color: #f0b429; }

  .area-icon {
    width: 52px;
    height: 52px;
    border-radius: 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    margin-bottom: 16px;
  }
  .area-card.blue  .area-icon { background: #e8eeff; color: #1e3c72; }
  .area-card.red   .area-icon { background: #fff0ed; color: #ff4b2b; }
  .area-card.green .area-icon { background: #e6faf5; color: #00b894; }
  .area-card.gold  .area-icon { background: #fff8e1; color: #f0b429; }

  .area-card h3 {
    font-size: 1.05rem;
    font-weight: 700;
    color: #1a1a2e;
    margin: 0 0 10px 0;
  }
  .area-card p {
    font-size: 0.9rem;
    color: #666;
    line-height: 1.65;
    margin: 0;
  }

  /* ── Algorithm Pills ── */
  .algo-section {
    background: linear-gradient(135deg, #f8f9fc, #eef2ff);
    border-radius: 16px;
    padding: 32px;
    margin-bottom: 35px;
    border: 1px solid #e0e7ff;
  }
  .algo-section h2 {
    font-size: 1.2rem;
    font-weight: 700;
    color: #1e3c72;
    margin: 0 0 20px 0;
    border: none;
    padding: 0;
  }
  .algo-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }
  .algo-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: white;
    border: 2px solid #e0e7ff;
    border-radius: 30px;
    padding: 9px 18px;
    font-size: 0.88rem;
    font-weight: 600;
    color: #1e3c72;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    transition: all 0.2s;
  }
  .algo-pill:hover {
    background: #1e3c72;
    color: white;
    border-color: #1e3c72;
    transform: translateY(-2px);
  }
  .algo-pill i {
    font-size: 0.9rem;
    color: #ff4b2b;
    transition: color 0.2s;
  }
  .algo-pill:hover i { color: white; }

  /* ── Tools & Skills ── */
  .tools-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 14px;
    margin-bottom: 35px;
  }
  .tool-card {
    background: white;
    border-radius: 12px;
    padding: 18px 14px;
    text-align: center;
    box-shadow: 0 2px 10px rgba(0,0,0,0.06);
    transition: all 0.25s;
    border-bottom: 3px solid #e0e7ff;
  }
  .tool-card:hover {
    transform: translateY(-5px);
    border-bottom-color: #ff4b2b;
    box-shadow: 0 8px 20px rgba(0,0,0,0.1);
  }
  .tool-card i {
    font-size: 1.6rem;
    color: #1e3c72;
    margin-bottom: 8px;
    display: block;
  }
  .tool-card span {
    font-size: 0.82rem;
    font-weight: 600;
    color: #444;
  }

  /* ── Impact Numbers ── */
  .impact-strip {
    background: linear-gradient(135deg, #1e3c72, #2a5298);
    border-radius: 16px;
    padding: 30px 35px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    gap: 20px;
    margin-bottom: 35px;
    color: white;
    text-align: center;
  }
  .impact-item .num {
    font-size: 2.2rem;
    font-weight: 800;
    display: block;
    line-height: 1;
  }
  .impact-item .lbl {
    font-size: 0.78rem;
    opacity: 0.8;
    margin-top: 5px;
    display: block;
    letter-spacing: 0.5px;
    text-transform: uppercase;
  }

  /* ── Collaboration Box ── */
  .collab-box {
    background: #fff8f6;
    border: 2px dashed #ff4b2b;
    border-radius: 14px;
    padding: 28px 30px;
    text-align: center;
    margin-top: 10px;
  }
  .collab-box i {
    font-size: 2rem;
    color: #ff4b2b;
    margin-bottom: 10px;
    display: block;
  }
  .collab-box h3 {
    color: #1e3c72;
    font-size: 1.1rem;
    margin: 0 0 8px 0;
  }
  .collab-box p {
    color: #666;
    font-size: 0.92rem;
    margin: 0 0 16px 0;
  }
  .collab-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: #ff4b2b;
    color: white;
    text-decoration: none;
    padding: 10px 24px;
    border-radius: 30px;
    font-weight: 600;
    font-size: 0.9rem;
    transition: all 0.2s;
  }
  .collab-btn:hover {
    background: #1e3c72;
    transform: translateY(-2px);
  }

  @media (max-width: 768px) {
    .research-hero { padding: 35px 22px; }
    .research-hero h1 { font-size: 1.8rem; }
    .impact-strip { flex-direction: column; align-items: center; }
  }
</style>

<!-- Hero Banner -->
<div class="research-hero">
  <div class="hero-badge">🔬 Academic Research</div>
  <h1>Research Overview</h1>
  <p>My research bridges <strong>pure mathematics</strong> and <strong>real-world decision problems</strong> — developing intelligent inventory and supply chain models powered by nature-inspired optimization algorithms.</p>
</div>

<!-- Impact Numbers -->
<div class="impact-strip">
  <div class="impact-item"><span class="num">9</span><span class="lbl">Publications</span></div>
  <div class="impact-item"><span class="num">3+</span><span class="lbl">Algorithms Used</span></div>
  <div class="impact-item"><span class="num">4</span><span class="lbl">Research Areas</span></div>
  <div class="impact-item"><span class="num">2022–25</span><span class="lbl">Active Years</span></div>
</div>

<!-- Research Areas -->
<div class="section-title"><i class="fas fa-layer-group"></i> Core Research Areas</div>

<div class="area-grid">

  <div class="area-card blue">
    <div class="area-icon"><i class="fas fa-boxes"></i></div>
    <h3>Inventory Control</h3>
    <p>Development of mathematical models for deteriorating items incorporating pricing policies, preservation investment, advance payments, and memory-sensitive demand under real-world constraints.</p>
  </div>

  <div class="area-card red">
    <div class="area-icon"><i class="fas fa-truck-loading"></i></div>
    <h3>Supply Chain Management</h3>
    <p>Optimization of integrated production-distribution systems using mathematical modeling, fractional calculus, and computational intelligence for complex multi-echelon supply chains.</p>
  </div>

  <div class="area-card green">
    <div class="area-icon"><i class="fas fa-leaf"></i></div>
    <h3>Sustainability</h3>
    <p>Integration of environmental and economic sustainability into supply chain models — minimizing carbon footprint while maximizing profit through green inventory optimization strategies.</p>
  </div>

  <div class="area-card gold">
    <div class="area-icon"><i class="fas fa-industry"></i></div>
    <h3>Imperfect Production</h3>
    <p>Modeling realistic manufacturing environments with defective items, rework processes, inspection policies, and random quality variations to minimize total production-inventory costs.</p>
  </div>

</div>

<!-- Metaheuristic Algorithms -->
<div class="section-title"><i class="fas fa-brain"></i> Nature-Inspired Algorithms</div>

<div class="algo-section">
  <h2>Optimization techniques applied in research:</h2>
  <div class="algo-grid">
    <span class="algo-pill"><i class="fas fa-dna"></i> Differential Evolution (DE)</span>
    <span class="algo-pill"><i class="fas fa-dove"></i> Bat Algorithm (BA)</span>
    <span class="algo-pill"><i class="fas fa-random"></i> Hybrid Optimization Methods</span>
    <span class="algo-pill"><i class="fas fa-project-diagram"></i> Nature-Inspired Heuristics</span>
    <span class="algo-pill"><i class="fas fa-calculator"></i> Fractional Calculus Models</span>
    <span class="algo-pill"><i class="fas fa-chart-line"></i> Metaheuristic Techniques</span>
  </div>
</div>

<!-- Computational Tools -->
<div class="section-title"><i class="fas fa-tools"></i> Computational Tools</div>

<div class="tools-grid">
  <div class="tool-card">
    <i class="fab fa-python"></i>
    <span>Python</span>
  </div>
  <div class="tool-card">
    <i class="fas fa-superscript"></i>
    <span>MATLAB / Scilab</span>
  </div>
  <div class="tool-card">
    <i class="fas fa-file-code"></i>
    <span>LaTeX</span>
  </div>
  <div class="tool-card">
    <i class="fas fa-infinity"></i>
    <span>Manim</span>
  </div>
  <div class="tool-card">
    <i class="fas fa-chart-bar"></i>
    <span>Data Analysis</span>
  </div>
  <div class="tool-card">
    <i class="fas fa-code-branch"></i>
    <span>Optimization</span>
  </div>
</div>

<!-- Collaboration CTA -->
<div class="collab-box">
  <i class="fas fa-handshake"></i>
  <h3>Open to Research Collaboration</h3>
  <p>Interested in joint research on inventory optimization, supply chain modeling, or metaheuristic applications? Feel free to reach out.</p>
  <a href="/contact/" class="collab-btn"><i class="fas fa-envelope"></i> Get in Touch</a>
</div>
