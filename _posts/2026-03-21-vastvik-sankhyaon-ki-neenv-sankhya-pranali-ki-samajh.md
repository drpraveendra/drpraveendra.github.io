---
layout: post
title: "वास्तविक संख्याओं की नींव: संख्या प्रणाली की समझ"
date: 2026-03-21
category: maths
lang: hi
lang_pair: "/blog/foundations-of-real-numbers-understanding-the-number-system/"
permalink: /blog/vastvik-sankhyaon-ki-neenv-sankhya-pranali-ki-samajh/
listed: false
description: "वास्तविक संख्याओं की नींव — संख्या प्रणाली का क्रम ℕ⊂ℤ⊂ℚ⊂ℝ, Axioms और गुणधर्म।"
---

<style>
  .math-post-hi{font-family:'Hind','Noto Sans Devanagari',sans-serif;line-height:1.9;font-size:1.05rem;line-height:1.85;color:#2d2d2d;max-width:860px;margin:0 auto}
  .post-hero{background:linear-gradient(135deg,#1e3c72 0%,#2a5298 60%,#ff4b2b 100%);border-radius:16px;padding:38px 35px;color:white;margin-bottom:35px;position:relative;overflow:hidden}
  .post-hero h1{font-size:1.85rem;font-weight:800;color:white;margin:0 0 10px;line-height:1.3}
  .post-hero p{font-size:1rem;opacity:.9;margin:0}
  .post-hero .hindi-subtitle{font-family:'Hind',sans-serif;font-size:1.1rem;color:#fbbf24;margin-top:8px}
  .stats-strip{background:linear-gradient(135deg,#1e3c72,#7c3aed);border-radius:14px;padding:22px 28px;display:flex;flex-wrap:wrap;justify-content:space-around;gap:16px;margin-bottom:35px;text-align:center;color:white}
  .stat-item .num{font-size:1.9rem;font-weight:900;display:block;line-height:1}
  .stat-item .lbl{font-size:.7rem;opacity:.8;margin-top:4px;display:block;text-transform:uppercase;letter-spacing:.5px}
  .section-title{display:flex;align-items:center;gap:12px;font-size:1.4rem;font-weight:800;color:#1e3c72;margin:42px 0 20px;padding-bottom:10px;border-bottom:3px solid transparent;border-image:linear-gradient(to right,#1e3c72,#7c3aed,#ff4b2b,transparent) 1}
  .sec-icon{width:38px;height:38px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:1rem;flex-shrink:0}
  .sub-title{font-size:1.1rem;font-weight:700;color:#2a5298;margin:26px 0 12px;display:flex;align-items:center;gap:8px}
  .sub-title::before{content:'';width:4px;height:18px;background:linear-gradient(to bottom,#ff4b2b,#fbbf24);border-radius:2px;flex-shrink:0}
  .info-card{background:white;border-radius:13px;padding:22px 26px;margin:18px 0;box-shadow:0 4px 14px rgba(0,0,0,.07);border-left:5px solid #1e3c72}
  .info-card.gold{border-left-color:#d97706;background:#fffbeb}
  .info-card.hindi{border-left-color:#d97706;background:#fffbeb;font-family:'Hind','Noto Sans Devanagari',sans-serif;font-size:1rem;line-height:1.9}
  .info-card-header{display:flex;align-items:center;gap:8px;font-size:.75rem;font-weight:700;text-transform:uppercase;letter-spacing:.8px;margin-bottom:10px;color:#1e3a5f}
  .info-card.gold .info-card-header,.info-card.hindi .info-card-header{color:#92400e}
  .example-card{background:white;border-radius:13px;padding:22px 26px;margin:18px 0;box-shadow:0 4px 14px rgba(0,0,0,.07);border-top:5px solid #1e3c72;transition:transform .2s}
  .example-card:hover{transform:translateY(-3px)}
  .example-card:nth-child(2){border-top-color:#7c3aed}
  .example-card:nth-child(3){border-top-color:#d97706}
  .example-card:nth-child(4){border-top-color:#dc2626}
  .example-num{display:inline-flex;align-items:center;justify-content:center;width:32px;height:32px;background:linear-gradient(135deg,#1e3c72,#7c3aed);color:white;border-radius:50%;font-size:.85rem;font-weight:800;margin-bottom:10px}
  .example-label{font-size:.7rem;font-weight:700;text-transform:uppercase;letter-spacing:.5px;color:#888;margin-bottom:6px}
  .solution-box{background:#f0fdf4;border-left:4px solid #059669;border-radius:0 8px 8px 0;padding:14px 18px;margin-top:12px}
  .tip-box{background:linear-gradient(135deg,#fffbeb,#fef3c7);border-left:5px solid #d97706;border-radius:0 12px 12px 0;padding:20px 24px;margin:20px 0}
  .tip-box-header{display:flex;align-items:center;gap:8px;font-size:.75rem;font-weight:700;text-transform:uppercase;letter-spacing:.6px;color:#92400e;margin-bottom:12px}
  .tip-box ul{margin:0;padding-left:18px;color:#78350f}
  .tip-box ul li{margin-bottom:7px;font-size:.95rem}
  .warning-box{background:#fff5f5;border-left:5px solid #dc2626;border-radius:0 12px 12px 0;padding:20px 24px;margin:20px 0}
  .warning-box-header{display:flex;align-items:center;gap:8px;font-size:.75rem;font-weight:700;text-transform:uppercase;letter-spacing:.6px;color:#991b1b;margin-bottom:12px}
  .warning-box ul{margin:0;padding-left:18px;color:#7f1d1d}
  .warning-box ul li{margin-bottom:7px;font-size:.95rem}
  .app-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(185px,1fr));gap:14px;margin:18px 0}
  .app-card{background:white;border-radius:12px;padding:18px 16px;box-shadow:0 3px 10px rgba(0,0,0,.06);border-top:4px solid #1e3c72;text-align:center;transition:transform .2s}
  .app-card:hover{transform:translateY(-4px)}
  .app-card:nth-child(2){border-top-color:#7c3aed}
  .app-card:nth-child(3){border-top-color:#d97706}
  .app-card:nth-child(4){border-top-color:#059669}
  .app-card .app-icon{font-size:1.7rem;margin-bottom:8px}
  .app-card strong{color:#1e3c72;display:block;margin-bottom:4px;font-size:.9rem}
  .app-card p{font-size:.82rem;color:#555;margin:0;line-height:1.45}
  .revision-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:14px;margin:18px 0}
  .rev-card{border-radius:12px;padding:18px 16px;color:white}
  .rev-card.blue{background:linear-gradient(135deg,#1e3c72,#2a5298)}
  .rev-card.purple{background:linear-gradient(135deg,#7c3aed,#a855f7)}
  .rev-card.green{background:linear-gradient(135deg,#059669,#10b981)}
  .rev-card h4{font-size:.78rem;opacity:.8;text-transform:uppercase;letter-spacing:1px;margin:0 0 8px}
  .rev-card p{font-size:.9rem;margin:0;line-height:1.6}
  .summary-table{width:100%;border-collapse:collapse;margin:18px 0;border-radius:12px;overflow:hidden;box-shadow:0 4px 14px rgba(0,0,0,.07);font-size:.88rem}
  .summary-table th{background:linear-gradient(135deg,#1e3c72,#2a5298);color:white;padding:13px 16px;text-align:left}
  .summary-table td{padding:11px 16px;color:#333;border-bottom:1px solid #e5e7eb}
  .summary-table tr:nth-child(even) td{background:#f8faff}
  .summary-table tr:last-child td{border-bottom:none}
  .summary-table td:first-child{font-weight:700;color:#1e3c72}
  @media(max-width:640px){.post-hero{padding:26px 18px}.post-hero h1{font-size:1.5rem}.stats-strip{flex-direction:column;align-items:center}}
</style>
<link href="https://fonts.googleapis.com/css2?family=Hind:wght@400;600;700&display=swap" rel="stylesheet">

<div class="math-post-hi">

<div class="post-hero">
  <h1>वास्तविक संख्याओं की नींव: संख्या प्रणाली की समझ</h1>
  <p>ℕ से ℝ तक की यात्रा — क्रम, अभिगृहीत और गुणधर्म।</p>
  <div class="eng-subtitle">Foundations of Real Numbers: Understanding the Number System</div>
</div>

<div class="stats-strip"><div class="stat-item"><span class="num">ℕ→ℝ</span><span class="lbl">संख्या क्रम</span></div><div class="stat-item"><span class="num">4</span><span class="lbl">हल किए उदाहरण</span></div><div class="stat-item"><span class="num">★★★</span><span class="lbl">CSIR NET</span></div><div class="stat-item"><span class="num">EN+HI</span><span class="lbl">द्विभाषी</span></div></div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-book-open"></i></span> परिभाषा एवं कथन</h2>
<div class="info-card">
  <div class="info-card-header"><i class="fas fa-bookmark"></i> संख्या प्रणाली का क्रम</div>
  <ul>
    <li><strong>ℕ (प्राकृत संख्याएँ):</strong> {1, 2, 3, …} — गिनती की संख्याएँ।</li>
    <li><strong>ℤ (पूर्णांक):</strong> {…, −2, −1, 0, 1, 2, …} — ℕ + ऋणात्मक + शून्य।</li>
    <li><strong>ℚ (परिमेय):</strong> {p/q : p, q ∈ ℤ, q ≠ 0} — सभी भिन्न।</li>
    <li><strong>ℝ (वास्तविक):</strong> ℚ ∪ ℚ<sup>c</sup> — परिमेय और अपरिमेय।</li>
  </ul>
  <p>प्रत्येक उचित उपसमुच्चय: <strong>ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ</strong>।</p>
  <p><em>सन्दर्भ: Rudin, Chapter 1; Apostol, §I 1.1–1.4।</em></p>
</div>
<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-lightbulb"></i></span> सहज व्याख्या</h2>
<p>संख्या प्रणाली को एक के अन्दर एक डिब्बों की तरह सोचें। प्रत्येक डिब्बा पिछले को सम्मिलित करता है पर कुछ नया जोड़ता है।</p>
<div class="info-card">
  <div class="info-card-header"><i class="fas fa-question-circle"></i> प्रत्येक विस्तार क्यों आवश्यक था?</div>
  <ul>
    <li><strong>ℕ → ℤ:</strong> x + 3 = 1 हल करने के लिए (ऋणात्मक चाहिए)।</li>
    <li><strong>ℤ → ℚ:</strong> 2x = 1 हल करने के लिए (भिन्न चाहिए)।</li>
    <li><strong>ℚ → ℝ:</strong> x² = 2 हल करने के लिए (√2 ∉ ℚ)।</li>
  </ul>
</div>
<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-pencil-alt"></i></span> हल किए गए उदाहरण</h2>
<div class="example-card">
  <div class="example-label">उदाहरण 1 — सरल</div><div class="example-num">1</div>
  <p>उदाहरण देकर <strong>ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ</strong> दिखाएँ।</p>
  <div class="solution-box"><strong>हल:</strong><ul><li>3 ∈ ℕ, अतः 3 ∈ ℤ, 3 ∈ ℚ, 3 ∈ ℝ।</li><li>−5 ∈ ℤ पर −5 ∉ ℕ।</li><li>1/2 ∈ ℚ पर 1/2 ∉ ℤ।</li><li>√2 ∈ ℝ पर √2 ∉ ℚ। ∎</li></ul></div>
</div>
<div class="example-card">
  <div class="example-label">उदाहरण 2 — मध्यम</div><div class="example-num">2</div>
  <p>क्या <strong>ℤ एक Field है</strong>? कारण बताएँ।</p>
  <div class="solution-box"><strong>हल:</strong><p>नहीं। Field में हर अशून्य तत्त्व का गुणात्मक प्रतिलोम होना चाहिए। 2 ∈ ℤ का प्रतिलोम 1/2 ∉ ℤ। अतः ℤ M5 विफल करता है — Field नहीं है। ∎</p></div>
</div>
<div class="example-card">
  <div class="example-label">उदाहरण 3 — मध्यम</div><div class="example-num">3</div>
  <p>सिद्ध करें: किन्हीं दो भिन्न परिमेय संख्याओं के बीच एक और परिमेय संख्या है।</p>
  <div class="solution-box"><strong>हल:</strong><p>a, b ∈ ℚ, a &lt; b। तब (a+b)/2 ∈ ℚ और a &lt; (a+b)/2 &lt; b। ∎</p></div>
</div>
<div class="example-card">
  <div class="example-label">उदाहरण 4 — CSIR NET / GATE प्रकार</div><div class="example-num">4</div>
  <p>निम्नलिखित में से <strong>असत्य</strong> कौन-सा है?</p>
  <p>(a) ℕ ⊂ ℝ &nbsp;&nbsp; (b) ℚ सम्पूर्ण है &nbsp;&nbsp; (c) ℝ क्रमित क्षेत्र है &nbsp;&nbsp; (d) ℚ, ℝ में सघन है</p>
  <div class="solution-box"><strong>हल:</strong> (b) असत्य है — ℚ सम्पूर्ण नहीं। <strong>उत्तर: (b)</strong> ∎</div>
</div>
<h2 class="section-title"><span class="sec-icon" style="background:#fef9c3;color:#d97706;"><i class="fas fa-layer-group"></i></span> त्वरित पुनरावृत्ति कार्ड</h2>
<div class="revision-grid">
  <div class="rev-card blue"><h4>Card A — क्रम</h4><p>ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ<br>प्रत्येक उचित उपसमुच्चय<br>ℝ = ℚ ∪ ℚ<sup>c</sup></p></div>
  <div class="rev-card purple"><h4>Card B — विस्तार क्यों?</h4><p>ℕ: गणना<br>ℤ: व्यवकलन<br>ℚ: विभाजन<br>ℝ: सम्पूर्णता (रेखा भरती है)</p></div>
  <div class="rev-card green"><h4>Card C — Fields</h4><p>ℚ और ℝ: Field हैं<br>ℤ: Field नहीं (M5 विफल)<br>ℕ: Ring भी नहीं</p></div>
</div>
<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> सामान्य गलतियाँ</h2>
<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> परीक्षा में न करें ये गलतियाँ</div>
  <ul>
    <li><strong>ℝ = ℚ:</strong> ℝ, ℚ को उचित रूप से सम्मिलित करता है — √2, π, e भी वास्तविक हैं।</li>
    <li><strong>ℤ Field है:</strong> ℤ M5 (गुणात्मक प्रतिलोम) विफल करता है।</li>
    <li><strong>ℕ में 0 शामिल है:</strong> अधिकांश Real Analysis में ℕ = {1, 2, 3, …}।</li>
    <li><strong>ℚ सम्पूर्ण है:</strong> ℚ सम्पूर्ण नहीं — Cauchy अनुक्रम ℚ में अभिसारी नहीं हो सकते।</li>
  </ul>
</div>
<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> सारांश सारणी</h2>
<table class="summary-table">
  <thead><tr><th>संख्या प्रणाली</th><th>प्रतीक</th><th>उदाहरण</th><th>Field?</th><th>सम्पूर्ण?</th></tr></thead>
  <tbody>
    <tr><td>प्राकृत</td><td>ℕ</td><td>1, 2, 3, …</td><td>नहीं</td><td>नहीं</td></tr>
    <tr><td>पूर्णांक</td><td>ℤ</td><td>…, −1, 0, 1, …</td><td>नहीं</td><td>नहीं</td></tr>
    <tr><td>परिमेय</td><td>ℚ</td><td>1/2, −3/4</td><td>हाँ</td><td>नहीं</td></tr>
    <tr><td>अपरिमेय</td><td>ℚ<sup>c</sup></td><td>√2, π, e</td><td>नहीं</td><td>नहीं</td></tr>
    <tr><td>वास्तविक</td><td>ℝ</td><td>सभी उपरोक्त</td><td>हाँ</td><td>हाँ</td></tr>
  </tbody>
</table>


</div>