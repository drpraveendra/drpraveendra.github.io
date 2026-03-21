---
layout: post
title: "Introduction to Point Set Topology in ℝ – Basic Concepts"
date: 2026-02-01
category: maths
lang: en
lang_pair: "/blog/introduction-to-point-set-topology-hindi/"
permalink: /blog/introduction-to-point-set-topology/
description: "A beginner-friendly introduction to Point Set Topology in ℝ — covering the real number system, absolute value, neighbourhoods, and supremum."
---

<style>
  .math-post { font-family: Georgia, serif; font-size: 1.05rem; line-height: 1.85; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 60%, #7c3aed 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "ℝ"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
  .post-hero h1 { font-size: 1.85rem; font-weight: 800; color: white; margin: 0 0 10px; line-height: 1.3; }
  .post-hero p { font-size: 1rem; opacity: 0.9; margin: 0; }
  .stats-strip { background: linear-gradient(135deg, #1e3c72, #7c3aed); border-radius: 14px; padding: 22px 28px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 16px; margin-bottom: 35px; text-align: center; color: white; }
  .stat-item .num { font-size: 1.9rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.7rem; opacity: 0.8; margin-top: 4px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }
  .section-title { display: flex; align-items: center; gap: 12px; font-size: 1.4rem; font-weight: 800; color: #1e3c72; margin: 42px 0 20px; padding-bottom: 10px; border-bottom: 3px solid transparent; border-image: linear-gradient(to right, #1e3c72, #7c3aed, #ff4b2b, transparent) 1; }
  .sec-icon { width: 38px; height: 38px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .sub-title { font-size: 1.1rem; font-weight: 700; color: #2a5298; margin: 26px 0 12px; display: flex; align-items: center; gap: 8px; }
  .sub-title::before { content: ''; width: 4px; height: 18px; background: linear-gradient(to bottom, #ff4b2b, #fbbf24); border-radius: 2px; flex-shrink: 0; }
  .info-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-left: 5px solid #1e3c72; }
  .info-card.gold   { border-left-color: #d97706; background: #fffbeb; }
  .info-card.purple { border-left-color: #7c3aed; background: #f5f3ff; }
  .info-card.green  { border-left-color: #059669; background: #ecfdf5; }
  .info-card.red    { border-left-color: #dc2626; background: #fff5f5; }
  .info-card-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px; color: #1e3a5f; }
  .info-card.gold   .info-card-header { color: #92400e; }
  .info-card.purple .info-card-header { color: #5b21b6; }
  .info-card.green  .info-card-header { color: #065f46; }
  .info-card.red    .info-card-header { color: #991b1b; }
  .example-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-top: 5px solid #1e3c72; transition: transform 0.2s; }
  .example-card:hover { transform: translateY(-3px); }
  .example-card:nth-child(2) { border-top-color: #7c3aed; }
  .example-card:nth-child(3) { border-top-color: #d97706; }
  .example-card:nth-child(4) { border-top-color: #dc2626; }
  .example-num { display: inline-flex; align-items: center; justify-content: center; width: 32px; height: 32px; background: linear-gradient(135deg, #1e3c72, #7c3aed); color: white; border-radius: 50%; font-size: 0.85rem; font-weight: 800; margin-bottom: 10px; }
  .example-label { font-size: 0.7rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; color: #888; margin-bottom: 6px; }
  .tip-box { background: linear-gradient(135deg, #fffbeb, #fef3c7); border-left: 5px solid #d97706; border-radius: 0 12px 12px 0; padding: 20px 24px; margin: 20px 0; }
  .tip-box-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.6px; color: #92400e; margin-bottom: 12px; }
  .tip-box ul { margin: 0; padding-left: 18px; color: #78350f; }
  .tip-box ul li { margin-bottom: 7px; font-size: 0.95rem; }
  .warning-box { background: #fff5f5; border-left: 5px solid #dc2626; border-radius: 0 12px 12px 0; padding: 20px 24px; margin: 20px 0; }
  .warning-box-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.6px; color: #991b1b; margin-bottom: 12px; }
  .warning-box ul { margin: 0; padding-left: 18px; color: #7f1d1d; }
  .warning-box ul li { margin-bottom: 7px; font-size: 0.95rem; }
  .app-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(185px, 1fr)); gap: 14px; margin: 18px 0; }
  .app-card { background: white; border-radius: 12px; padding: 18px 16px; box-shadow: 0 3px 10px rgba(0,0,0,0.06); border-top: 4px solid #1e3c72; text-align: center; transition: transform 0.2s; }
  .app-card:hover { transform: translateY(-4px); }
  .app-card:nth-child(2) { border-top-color: #7c3aed; }
  .app-card:nth-child(3) { border-top-color: #d97706; }
  .app-card:nth-child(4) { border-top-color: #059669; }
  .app-card .app-icon { font-size: 1.7rem; margin-bottom: 8px; }
  .app-card strong { color: #1e3c72; display: block; margin-bottom: 4px; font-size: 0.9rem; }
  .app-card p { font-size: 0.82rem; color: #555; margin: 0; line-height: 1.45; }
  .summary-table { width: 100%; border-collapse: collapse; margin: 18px 0; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 14px rgba(0,0,0,0.07); font-size: 0.88rem; }
  .summary-table th { background: linear-gradient(135deg, #1e3c72, #2a5298); color: white; padding: 13px 16px; text-align: left; }
  .summary-table td { padding: 11px 16px; color: #333; border-bottom: 1px solid #e5e7eb; }
  .summary-table tr:nth-child(even) td { background: #f8faff; }
  .summary-table tr:last-child td { border-bottom: none; }
  .summary-table td:first-child { font-weight: 700; color: #1e3c72; }
  @media (max-width: 640px) { .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.5rem; } .stats-strip { flex-direction: column; align-items: center; } }
</style>

<div class="math-post">

<div class="post-hero">
  <h1>Introduction to Point Set Topology in ℝ</h1>
  <p><strong>Point Set Topology</strong> is the study of the structure of subsets of ℝ using openness, closedness, limits, and continuity. It forms the rigorous foundation of all real analysis.</p>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">ℝ</span><span class="lbl">Real Line</span></div>
  <div class="stat-item"><span class="num">ε</span><span class="lbl">Neighbourhood</span></div>
  <div class="stat-item"><span class="num">★★★</span><span class="lbl">CSIR NET Priority</span></div>
  <div class="stat-item"><span class="num">sup</span><span class="lbl">Completeness</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-infinity"></i></span> The Real Line ℝ</h2>

<p>The set of all real numbers $\mathbb{R}$ is a <strong>complete ordered field</strong>. Its three key properties are:</p>

<div class="info-card">
  <div class="info-card-header"><i class="fas fa-list"></i> Three Fundamental Properties</div>
  <ul>
    <li><strong>Ordered:</strong> For any $a, b \in \mathbb{R}$, exactly one of $a &lt; b$, $a = b$, $a &gt; b$ holds.</li>
    <li><strong>Field:</strong> Addition and multiplication are well-defined with inverses.</li>
    <li><strong>Complete:</strong> Every non-empty subset bounded above has a <strong>least upper bound</strong> (supremum) in $\mathbb{R}$.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-ruler"></i></span> Absolute Value and Distance</h2>

<p>The <strong>absolute value</strong> of $x \in \mathbb{R}$ is:</p>

$$|x| = \begin{cases} x & \text{if } x \geq 0 \\ -x & \text{if } x < 0 \end{cases}$$

<p>The <strong>distance</strong> between two real numbers $a$ and $b$ is $d(a, b) = |a - b|$.</p>

<div class="sub-title">Properties of Absolute Value</div>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-check-circle"></i> Four Key Properties</div>
  <ol style="margin:0;padding-left:20px;color:#4c1d95;">
    <li style="margin-bottom:6px;">$\lvert a\rvert \geq 0$, and $\lvert a\rvert = 0 \iff a = 0$</li>
    <li style="margin-bottom:6px;">$\lvert ab\rvert = \lvert a\rvert\lvert b\rvert$</li>
    <li style="margin-bottom:6px;"><strong>Triangle Inequality:</strong> $\lvert a + b\rvert \leq \lvert a\rvert + \lvert b\rvert$</li>
    <li style="margin-bottom:6px;"><strong>Reverse Triangle Inequality:</strong> $\big\lvert\lvert a\rvert - \lvert b\rvert\big\rvert \leq \lvert a - b\rvert$</li>
  </ol>
</div>

<div class="sub-title">Proof of Triangle Inequality</div>

<p>Since $-\lvert a\rvert \leq a \leq \lvert a\rvert$ and $-\lvert b\rvert \leq b \leq \lvert b\rvert$, adding both inequalities:</p>

$$-(\lvert a\rvert+\lvert b\rvert) \leq a+b \leq \lvert a\rvert+\lvert b\rvert \implies \lvert a+b\rvert \leq \lvert a\rvert + \lvert b\rvert \quad \checkmark$$

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-circle"></i></span> The ε-Neighbourhood</h2>

<div class="info-card green">
  <div class="info-card-header"><i class="fas fa-book"></i> Definition</div>
  The <strong>ε-neighbourhood</strong> of a point $a \in \mathbb{R}$ is:
  $$N_\varepsilon(a) = (a - \varepsilon,\, a + \varepsilon) = \{x \in \mathbb{R} : \lvert x - a\rvert < \varepsilon\}$$
  This is the <strong>open ball</strong> of radius $\varepsilon$ centred at $a$.
</div>

<p><strong>Example:</strong> $N_{0.5}(3) = (2.5, 3.5)$ — all points within distance $0.5$ of $3$.</p>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-pencil-alt"></i></span> Solved Examples</h2>

<div class="example-card">
  <div class="example-label">Example 1 — Easy</div>
  <div class="example-num">1</div>
  <p><strong>Find all $x \in \mathbb{R}$ satisfying $\lvert x - 3\rvert < 2$.</strong></p>
  <p><strong>Solution:</strong> $\lvert x-3\rvert &lt; 2 \iff -2 &lt; x-3 &lt; 2 \iff 1 &lt; x &lt; 5$.</p>
  <p>So the solution set is the open interval $(1, 5) = N_2(3)$. ✓</p>
</div>

<div class="example-card">
  <div class="example-label">Example 2 — Easy-Medium</div>
  <div class="example-num">2</div>
  <p><strong>Let $S = \{1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots\}$. Find $\sup S$ and $\inf S$.</strong></p>
  <p><strong>Solution:</strong></p>
  <ul>
    <li>$\sup S = 1$ — the maximum element is $1$, and it belongs to $S$. ✓</li>
    <li>$\inf S = 0$ — every term $\frac{1}{n} &gt; 0$, but for any $\varepsilon &gt; 0$, $\frac{1}{n} &lt; \varepsilon$ for large enough $n$, so $0$ is the greatest lower bound.</li>
    <li>Note: $0 \notin S$ — the infimum need NOT belong to the set. ✓</li>
  </ul>
</div>

<div class="example-card">
  <div class="example-label">Example 3 — Medium</div>
  <div class="example-num">3</div>
  <p><strong>Prove: $\lvert a - b\rvert \geq \big\lvert \lvert a\rvert - \lvert b\rvert \big\rvert$ for all $a, b \in \mathbb{R}$.</strong></p>
  <p><strong>Solution:</strong> By the Triangle Inequality:</p>
  $$\lvert a\rvert = \lvert (a-b)+b\rvert \leq \lvert a-b\rvert + \lvert b\rvert \implies \lvert a\rvert - \lvert b\rvert \leq \lvert a-b\rvert$$
  <p>Similarly $\lvert b\rvert - \lvert a\rvert \leq \lvert a-b\rvert$. Therefore $\big\lvert\lvert a\rvert - \lvert b\rvert\big\rvert \leq \lvert a-b\rvert$. $\blacksquare$</p>
</div>

<div class="example-card">
  <div class="example-label">Example 4 — Exam Level</div>
  <div class="example-num">4</div>
  <p><strong>Let $A = \{x \in \mathbb{R} : x^2 &lt; 3\}$. Find $\sup A$ and verify it using the definition of supremum.</strong></p>
  <p><strong>Solution:</strong> $A = (-\sqrt{3}, \sqrt{3})$. Claim: $\sup A = \sqrt{3}$.</p>
  <ul>
    <li><strong>Upper bound:</strong> Every $x \in A$ satisfies $x &lt; \sqrt{3}$. ✓</li>
    <li><strong>Least upper bound:</strong> For any $\varepsilon &gt; 0$, $\sqrt{3} - \varepsilon \in A$ (since $(\sqrt{3}-\varepsilon)^2 &lt; 3$ for small $\varepsilon$), so no number smaller than $\sqrt{3}$ is an upper bound. ✓</li>
  </ul>
  <p>Therefore $\sup A = \sqrt{3} \notin A$ — the supremum need not belong to the set. $\blacksquare$</p>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> CSIR NET / GATE / IIT JAM Tips</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> Exam Strategies</div>
  <ul>
    <li><strong>Triangle Inequality is used in almost every analysis proof</strong> — memorise it and its reverse form completely.</li>
    <li><strong>Supremum vs Maximum:</strong> $\sup S$ always exists for bounded sets (completeness), but $\max S$ exists only if $\sup S \in S$.</li>
    <li><strong>ε-neighbourhood questions:</strong> $\lvert x - a\rvert &lt; \varepsilon$ is equivalent to $x \in (a-\varepsilon, a+\varepsilon)$ — always translate between these forms.</li>
    <li><strong>Archimedean Property:</strong> For any $\varepsilon &gt; 0$, $\exists\, n \in \mathbb{N}$ with $\frac{1}{n} &lt; \varepsilon$ — used constantly in proofs.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> Common Mistakes</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> Avoid These Errors</div>
  <ul>
    <li><strong>Confusing sup and max:</strong> $\sup S$ always exists (completeness), but $\max S$ exists only when $\sup S \in S$. For $S = (0,1)$: $\sup S = 1$ but $\max S$ does not exist.</li>
    <li><strong>Incorrect Triangle Inequality direction:</strong> The inequality is $\lvert a+b\rvert \leq \lvert a\rvert + \lvert b\rvert$ — not equality in general.</li>
    <li><strong>Forgetting ε-neighbourhood is open:</strong> $N_\varepsilon(a)$ is an open interval — it does NOT include the endpoints $a \pm \varepsilon$.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> Real-World Applications</h2>

<div class="app-grid">
  <div class="app-card"><div class="app-icon">📡</div><strong>Signal Processing</strong><p>ε-neighbourhoods model tolerance bands around signal values in digital filters.</p></div>
  <div class="app-card"><div class="app-icon">💻</div><strong>Numerical Analysis</strong><p>Supremum and infimum are used to bound errors in numerical approximations.</p></div>
  <div class="app-card"><div class="app-icon">⚡</div><strong>Control Theory</strong><p>Completeness of ℝ guarantees stability of feedback control systems converge.</p></div>
  <div class="app-card"><div class="app-icon">📐</div><strong>Geometry</strong><p>The concept of distance generalises to metric spaces used in computer graphics.</p></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> Intervals in ℝ — Summary</h2>

<table class="summary-table">
  <thead><tr><th>Notation</th><th>Name</th><th>Definition</th></tr></thead>
  <tbody>
    <tr><td>$(a,b)$</td><td>Open interval</td><td>$\{x : a &lt; x &lt; b\}$</td></tr>
    <tr><td>$[a,b]$</td><td>Closed interval</td><td>$\{x : a \leq x \leq b\}$</td></tr>
    <tr><td>$[a,b)$</td><td>Half-open</td><td>$\{x : a \leq x &lt; b\}$</td></tr>
    <tr><td>$(a,\infty)$</td><td>Unbounded open</td><td>$\{x : x &gt; a\}$</td></tr>
    <tr><td>$(-\infty,\infty)$</td><td>Entire real line</td><td>$\mathbb{R}$</td></tr>
  </tbody>
</table>

</div>
