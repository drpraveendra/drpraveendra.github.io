---
layout: post
title: "Fourier Series — Introduction, Coefficients & Solved Examples"
date: 2026-03-20
category: maths
lang: en
lang_pair: "/blog/fourier-series-hindi/"
permalink: /blog/fourier-series-english/
description: "A complete introduction to Fourier Series — Euler's formulas, Dirichlet conditions, even/odd functions, and step-by-step solved examples including the Basel Problem."
---

<style>
  .math-post { font-family: Georgia, serif; font-size: 1.05rem; line-height: 1.85; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 50%, #059669 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "∫"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
  .post-hero h1 { font-size: 1.85rem; font-weight: 800; color: white; margin: 0 0 10px; line-height: 1.3; }
  .post-hero p { font-size: 1rem; opacity: 0.9; margin: 0; }
  .stats-strip { background: linear-gradient(135deg, #1e3c72, #059669); border-radius: 14px; padding: 22px 28px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 16px; margin-bottom: 35px; text-align: center; color: white; }
  .stat-item .num { font-size: 1.9rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.7rem; opacity: 0.8; margin-top: 4px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }
  .section-title { display: flex; align-items: center; gap: 12px; font-size: 1.4rem; font-weight: 800; color: #1e3c72; margin: 42px 0 20px; padding-bottom: 10px; border-bottom: 3px solid transparent; border-image: linear-gradient(to right, #1e3c72, #059669, #ff4b2b, transparent) 1; }
  .sec-icon { width: 38px; height: 38px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .sub-title { font-size: 1.1rem; font-weight: 700; color: #2a5298; margin: 26px 0 12px; display: flex; align-items: center; gap: 8px; }
  .sub-title::before { content: ''; width: 4px; height: 18px; background: linear-gradient(to bottom, #059669, #fbbf24); border-radius: 2px; flex-shrink: 0; }
  .compare-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 20px 0; }
  .compare-card { border-radius: 12px; padding: 20px; }
  .compare-card.blue  { background: #eff6ff; border: 2px solid #93c5fd; }
  .compare-card.green { background: #ecfdf5; border: 2px solid #6ee7b7; }
  .compare-card h4 { margin: 0 0 10px; font-size: 1rem; font-weight: 700; }
  .compare-card.blue h4  { color: #1e40af; }
  .compare-card.green h4 { color: #065f46; }
  .compare-card ul { margin: 0; padding-left: 18px; font-size: 0.9rem; color: #444; }
  .compare-card ul li { margin-bottom: 5px; }
  .info-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-left: 5px solid #1e3c72; }
  .info-card.gold   { border-left-color: #d97706; background: #fffbeb; }
  .info-card.green  { border-left-color: #059669; background: #ecfdf5; }
  .info-card.purple { border-left-color: #7c3aed; background: #f5f3ff; }
  .info-card-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px; color: #1e3a5f; }
  .info-card.gold   .info-card-header { color: #92400e; }
  .info-card.green  .info-card-header { color: #065f46; }
  .info-card.purple .info-card-header { color: #5b21b6; }
  .example-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-top: 5px solid #059669; transition: transform 0.2s; }
  .example-card:hover { transform: translateY(-3px); }
  .example-card:nth-child(2) { border-top-color: #7c3aed; }
  .example-card:nth-child(3) { border-top-color: #d97706; }
  .example-card:nth-child(4) { border-top-color: #dc2626; }
  .example-num { display: inline-flex; align-items: center; justify-content: center; width: 32px; height: 32px; background: linear-gradient(135deg, #059669, #1e3c72); color: white; border-radius: 50%; font-size: 0.85rem; font-weight: 800; margin-bottom: 10px; }
  .example-label { font-size: 0.7rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; color: #888; margin-bottom: 6px; }
  .formula-strip { background: linear-gradient(135deg, #0f172a, #1e3c72); border-radius: 14px; padding: 24px 28px; margin: 18px 0; text-align: center; overflow-x: auto; }
  .tip-box { background: linear-gradient(135deg, #fffbeb, #fef3c7); border-left: 5px solid #d97706; border-radius: 0 12px 12px 0; padding: 20px 24px; margin: 20px 0; }
  .tip-box-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.6px; color: #92400e; margin-bottom: 12px; }
  .tip-box ul { margin: 0; padding-left: 18px; color: #78350f; }
  .tip-box ul li { margin-bottom: 7px; font-size: 0.95rem; }
  .warning-box { background: #fff5f5; border-left: 5px solid #dc2626; border-radius: 0 12px 12px 0; padding: 20px 24px; margin: 20px 0; }
  .warning-box-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.6px; color: #991b1b; margin-bottom: 12px; }
  .warning-box ul { margin: 0; padding-left: 18px; color: #7f1d1d; }
  .warning-box ul li { margin-bottom: 7px; font-size: 0.95rem; }
  .app-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(185px, 1fr)); gap: 14px; margin: 18px 0; }
  .app-card { background: white; border-radius: 12px; padding: 18px 16px; box-shadow: 0 3px 10px rgba(0,0,0,0.06); border-top: 4px solid #059669; text-align: center; transition: transform 0.2s; }
  .app-card:hover { transform: translateY(-4px); }
  .app-card:nth-child(2) { border-top-color: #7c3aed; }
  .app-card:nth-child(3) { border-top-color: #d97706; }
  .app-card:nth-child(4) { border-top-color: #1e3c72; }
  .app-card .app-icon { font-size: 1.7rem; margin-bottom: 8px; }
  .app-card strong { color: #065f46; display: block; margin-bottom: 4px; font-size: 0.9rem; }
  .app-card p { font-size: 0.82rem; color: #555; margin: 0; line-height: 1.45; }
  .summary-table { width: 100%; border-collapse: collapse; margin: 18px 0; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 14px rgba(0,0,0,0.07); font-size: 0.88rem; }
  .summary-table th { background: linear-gradient(135deg, #1e3c72, #059669); color: white; padding: 13px 16px; text-align: left; }
  .summary-table td { padding: 11px 16px; color: #333; border-bottom: 1px solid #e5e7eb; }
  .summary-table tr:nth-child(even) td { background: #f0fdf4; }
  .summary-table tr:last-child td { border-bottom: none; }
  .summary-table td:first-child { font-weight: 700; color: #065f46; }
  .highlight-result { background: linear-gradient(135deg, #ecfdf5, #d1fae5); border: 2px solid #059669; border-radius: 12px; padding: 20px 24px; margin: 18px 0; text-align: center; }
  @media (max-width: 640px) { .compare-grid { grid-template-columns: 1fr; } .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.5rem; } .stats-strip { flex-direction: column; align-items: center; } }
</style>

<div class="math-post">

<div class="post-hero">
  <h1>Fourier Series — Introduction, Coefficients &amp; Solved Examples</h1>
  <p><strong>Fourier Series</strong> represents a periodic function as an infinite sum of sines and cosines. It is one of the most powerful tools in mathematics, physics, and engineering — and a core CSIR NET and GATE topic.</p>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">3</span><span class="lbl">Coefficient Formulas</span></div>
  <div class="stat-item"><span class="num">4</span><span class="lbl">Solved Examples</span></div>
  <div class="stat-item"><span class="num">★★★</span><span class="lbl">CSIR NET Priority</span></div>
  <div class="stat-item"><span class="num">π²/6</span><span class="lbl">Basel Problem</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-book-open"></i></span> Definition</h2>

<p>Let $f(x)$ be a periodic function with period $2\pi$. Its <strong>Fourier series</strong> is:</p>

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty}\left(a_n\cos nx + b_n\sin nx\right)$$

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-calculator"></i></span> Euler's Formulas for Coefficients</h2>

<div class="info-card green">
  <div class="info-card-header"><i class="fas fa-function"></i> The Three Euler Formulas</div>
  $$a_0 = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\,dx$$
  $$a_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\cos(nx)\,dx, \quad n = 1, 2, 3, \ldots$$
  $$b_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\sin(nx)\,dx, \quad n = 1, 2, 3, \ldots$$
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-exchange-alt"></i></span> Even and Odd Functions</h2>

<div class="compare-grid">
  <div class="compare-card blue">
    <h4><i class="fas fa-mirror"></i> Even Function: $f(-x) = f(x)$</h4>
    <ul>
      <li>$b_n = 0$ (no sine terms)</li>
      <li>$a_0 = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} f(x)\,dx$</li>
      <li>$a_n = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} f(x)\cos(nx)\,dx$</li>
    </ul>
    $$f(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty} a_n\cos nx$$
  </div>
  <div class="compare-card green">
    <h4><i class="fas fa-sort-alt"></i> Odd Function: $f(-x) = -f(x)$</h4>
    <ul>
      <li>$a_0 = a_n = 0$ (no cosine terms)</li>
      <li>$b_n = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} f(x)\sin(nx)\,dx$</li>
    </ul>
    $$f(x) = \sum_{n=1}^{\infty} b_n\sin nx$$
  </div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-check-square"></i></span> Dirichlet's Conditions for Convergence</h2>

<div class="info-card">
  <div class="info-card-header"><i class="fas fa-list-check"></i> The Fourier series of $f(x)$ converges to $f(x)$ if:</div>
  <ol style="margin:0;padding-left:20px;color:#333;">
    <li style="margin-bottom:6px;">$f(x)$ is <strong>periodic</strong></li>
    <li style="margin-bottom:6px;">$f(x)$ is <strong>piecewise continuous</strong> on $[-\pi,\pi]$</li>
    <li style="margin-bottom:6px;">$f(x)$ has a <strong>finite number of maxima and minima</strong> in one period</li>
    <li style="margin-bottom:6px;">$f(x)$ has a <strong>finite number of discontinuities</strong> in one period</li>
  </ol>
  <p style="margin-top:12px;"><strong>At a discontinuity</strong> $x = c$:</p>
  $$\text{Fourier series} = \frac{f(c^+) + f(c^-)}{2}$$
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-pencil-alt"></i></span> Solved Examples</h2>

<div class="example-card">
  <div class="example-label">Example 1 — Easy (Square Wave)</div>
  <div class="example-num">1</div>
  <p><strong>Find the Fourier series of:</strong></p>
  $$f(x) = \begin{cases} -1 & -\pi &lt; x &lt; 0 \\ 1 & 0 &lt; x &lt; \pi \end{cases}$$
  <p><strong>Step 1:</strong> $f(x)$ is an <strong>odd function</strong> → $a_0 = 0$, $a_n = 0$.</p>
  <p><strong>Step 2:</strong> Compute $b_n$:</p>
  $$b_n = \frac{2}{\pi}\int_0^{\pi}\sin(nx)\,dx = \frac{2}{\pi}\left[-\frac{\cos(nx)}{n}\right]_0^{\pi} = \frac{2}{\pi}\cdot\frac{1-\cos(n\pi)}{n} = \frac{2(1-(-1)^n)}{n\pi}$$
  <p><strong>Step 3:</strong> For even $n$: $b_n = 0$. For odd $n$: $b_n = \dfrac{4}{n\pi}$.</p>
  $$\boxed{f(x) = \frac{4}{\pi}\left(\sin x + \frac{\sin 3x}{3} + \frac{\sin 5x}{5} + \cdots\right)}$$
</div>

<div class="example-card">
  <div class="example-label">Example 2 — Medium (Basel Problem via Fourier)</div>
  <div class="example-num">2</div>
  <p><strong>Find the Fourier series of $f(x) = x^2$ on $[-\pi,\pi]$ and hence find $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^2}$.</strong></p>
  <p><strong>Step 1:</strong> $f(x) = x^2$ is <strong>even</strong> → $b_n = 0$.</p>
  <p><strong>Step 2:</strong> $a_0 = \dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} x^2\,dx = \dfrac{2\pi^2}{3}$.</p>
  <p><strong>Step 3:</strong> $a_n = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} x^2\cos(nx)\,dx = \dfrac{4(-1)^n}{n^2}$ (by integration by parts twice).</p>
  <p><strong>Step 4:</strong> Fourier series:</p>
  $$x^2 = \frac{\pi^2}{3} + 4\sum_{n=1}^{\infty}\frac{(-1)^n}{n^2}\cos(nx)$$
  <p><strong>Step 5:</strong> Put $x = \pi$ (Dirichlet conditions satisfied — $f$ continuous at $\pi$):</p>
  $$\pi^2 = \frac{\pi^2}{3} + 4\sum_{n=1}^{\infty}\frac{(-1)^n}{n^2}(-1)^n = \frac{\pi^2}{3} + 4\sum_{n=1}^{\infty}\frac{1}{n^2}$$
  <div class="highlight-result">
    $$\sum_{n=1}^{\infty}\frac{1}{n^2} = \frac{\pi^2}{6}$$
    <p style="margin:8px 0 0;font-size:0.88rem;color:#065f46;"><strong>The famous Basel Problem — solved by Euler in 1734!</strong></p>
  </div>
</div>

<div class="example-card">
  <div class="example-label">Example 3 — Medium-Hard (Discontinuous Function)</div>
  <div class="example-num">3</div>
  <p><strong>Find the Fourier series of:</strong> $f(x) = x$ on $(-\pi, \pi)$.</p>
  <p><strong>Step 1:</strong> $f(x) = x$ is <strong>odd</strong> → $a_0 = 0$, $a_n = 0$.</p>
  <p><strong>Step 2:</strong></p>
  $$b_n = \frac{2}{\pi}\int_0^{\pi} x\sin(nx)\,dx$$
  <p>Integrating by parts: $= \dfrac{2}{\pi}\left[-\dfrac{x\cos(nx)}{n} + \dfrac{\sin(nx)}{n^2}\right]_0^{\pi} = \dfrac{2(-1)^{n+1}}{n}$</p>
  $$\boxed{f(x) = x = 2\left(\sin x - \frac{\sin 2x}{2} + \frac{\sin 3x}{3} - \cdots\right), \quad x \in (-\pi, \pi)}$$
  <p><em>At $x = \pm\pi$ (discontinuity):</em> Fourier series converges to $\dfrac{\pi + (-\pi)}{2} = 0$. ✓</p>
</div>

<div class="example-card">
  <div class="example-label">Example 4 — Exam Level (Parseval's Theorem)</div>
  <div class="example-num">4</div>
  <p><strong>Using the Fourier series of $f(x) = x$ on $(-\pi,\pi)$, find $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^2}$.</strong></p>
  <p><strong>Step 1:</strong> Parseval's Theorem:</p>
  $$\frac{1}{\pi}\int_{-\pi}^{\pi}[f(x)]^2\,dx = \frac{a_0^2}{2} + \sum_{n=1}^{\infty}(a_n^2 + b_n^2)$$
  <p><strong>Step 2:</strong> Left side: $\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} x^2\,dx = \dfrac{2\pi^2}{3}$.</p>
  <p><strong>Step 3:</strong> Right side (from Example 3, $a_n = 0$, $b_n = \dfrac{2(-1)^{n+1}}{n}$):</p>
  $$\sum_{n=1}^{\infty} b_n^2 = \sum_{n=1}^{\infty}\frac{4}{n^2}$$
  <p><strong>Step 4:</strong> Equating:</p>
  $$\frac{2\pi^2}{3} = 4\sum_{n=1}^{\infty}\frac{1}{n^2} \implies \sum_{n=1}^{\infty}\frac{1}{n^2} = \frac{\pi^2}{6}\ ✓$$
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-infinity"></i></span> Parseval's Theorem</h2>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-wave-square"></i> Statement</div>
  For the Fourier series of $f(x)$ on $[-\pi,\pi]$:
  $$\frac{1}{\pi}\int_{-\pi}^{\pi}[f(x)]^2\,dx = \frac{a_0^2}{2} + \sum_{n=1}^{\infty}(a_n^2 + b_n^2)$$
  This connects the <strong>energy of a function</strong> to its Fourier coefficients — fundamental in signal processing.
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> CSIR NET / GATE / IIT JAM Exam Tips</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> Exam Strategies</div>
  <ul>
    <li><strong>Odd/Even shortcut saves huge time:</strong> Always check symmetry first. Odd → only $b_n$, Even → only $a_n$. This halves your computation.</li>
    <li><strong>Dirichlet conditions MCQ trick:</strong> If $f$ satisfies Dirichlet conditions and is continuous at $x_0$, the series converges to $f(x_0)$ exactly.</li>
    <li><strong>Discontinuity formula is frequently tested:</strong> At $x = c$, series converges to $\dfrac{f(c^+)+f(c^-)}{2}$. Memorise this.</li>
    <li><strong>Basel-type sums always come from $f(x) = x^2$:</strong> Setting $x = 0$ gives $\sum \dfrac{(-1)^{n+1}}{n^2} = \dfrac{\pi^2}{12}$; setting $x = \pi$ gives $\sum \dfrac{1}{n^2} = \dfrac{\pi^2}{6}$.</li>
    <li><strong>Parseval's Theorem</strong> is the fastest tool for computing $\sum \dfrac{1}{n^4}$, $\sum \dfrac{1}{n^2}$, etc.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> Common Mistakes</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> Avoid These Errors</div>
  <ul>
    <li><strong>Wrong coefficient formula:</strong> Note $a_0 = \dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\,dx$ but the series uses $\dfrac{a_0}{2}$. This factor of 2 is a classic exam trap.</li>
    <li><strong>Forgetting to check Dirichlet conditions:</strong> Always verify conditions before claiming the series converges to $f(x)$.</li>
    <li><strong>Integration by parts errors:</strong> Fourier coefficient integrals typically need integration by parts. Set $u = f(x)$ and $dv = \cos(nx)\,dx$ or $\sin(nx)\,dx$.</li>
    <li><strong>Using Parseval without the factor $\frac{1}{\pi}$:</strong> The left side is $\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi}[f(x)]^2\,dx$, not $\displaystyle\int_{-\pi}^{\pi}[f(x)]^2\,dx$.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> Real-World Applications</h2>

<div class="app-grid">
  <div class="app-card"><div class="app-icon">📡</div><strong>Signal Processing</strong><p>Every digital signal is decomposed into frequency components using the Fourier series — fundamental to audio, video, and telecommunications.</p></div>
  <div class="app-card"><div class="app-icon">🌡️</div><strong>Heat Conduction</strong><p>Fourier himself developed this theory to solve the heat equation — modelling temperature distribution in materials.</p></div>
  <div class="app-card"><div class="app-icon">🎵</div><strong>Music &amp; Acoustics</strong><p>Musical timbre is determined by the relative amplitudes of Fourier harmonics — the mathematics behind why instruments sound different.</p></div>
  <div class="app-card"><div class="app-icon">🏗️</div><strong>Structural Engineering</strong><p>Vibration analysis of bridges and buildings uses Fourier series to identify resonant frequencies and prevent structural failure.</p></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> Summary Table</h2>

<table class="summary-table">
  <thead><tr><th>Quantity</th><th>Formula</th><th>Condition</th></tr></thead>
  <tbody>
    <tr><td>$a_0$</td><td>$\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\,dx$</td><td>Always</td></tr>
    <tr><td>$a_n$</td><td>$\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\cos(nx)\,dx$</td><td>$n \geq 1$</td></tr>
    <tr><td>$b_n$</td><td>$\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\sin(nx)\,dx$</td><td>$n \geq 1$</td></tr>
    <tr><td>$b_n = 0$</td><td>—</td><td>$f$ is even</td></tr>
    <tr><td>$a_0 = a_n = 0$</td><td>—</td><td>$f$ is odd</td></tr>
    <tr><td>At discontinuity</td><td>$\dfrac{f(c^+)+f(c^-)}{2}$</td><td>Dirichlet conditions hold</td></tr>
  </tbody>
</table>

</div>
