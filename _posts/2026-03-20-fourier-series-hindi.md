---
layout: post
title: "फ़ूरिए श्रृंखला — परिभाषा, गुणांक और हल उदाहरण"
date: 2026-03-20
category: maths
lang: hi
lang_pair: "/blog/fourier-series-english/"
permalink: /blog/fourier-series-hindi/
listed: false
description: "फ़ूरिए श्रृंखला का पूर्ण परिचय — ऑयलर के सूत्र, दिरिक्ले की शर्तें, सम-विषम फ़ंक्शन और बेसल समस्या सहित हल उदाहरण।"
---

<link href="https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
  .math-post-hi { font-family: 'Hind', 'Noto Sans Devanagari', sans-serif; font-size: 1.05rem; line-height: 1.9; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 50%, #059669 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "∫"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
  .post-hero h1 { font-size: 1.75rem; font-weight: 800; color: white; margin: 0 0 10px; line-height: 1.35; }
  .post-hero p { font-size: 1rem; opacity: 0.9; margin: 0; }
  .stats-strip { background: linear-gradient(135deg, #1e3c72, #059669); border-radius: 14px; padding: 22px 28px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 16px; margin-bottom: 35px; text-align: center; color: white; }
  .stat-item .num { font-size: 1.9rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.7rem; opacity: 0.8; margin-top: 4px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }
  .section-title { display: flex; align-items: center; gap: 12px; font-size: 1.35rem; font-weight: 800; color: #1e3c72; margin: 42px 0 20px; padding-bottom: 10px; border-bottom: 3px solid transparent; border-image: linear-gradient(to right, #1e3c72, #059669, #ff4b2b, transparent) 1; }
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
  .info-card.green  { border-left-color: #059669; background: #ecfdf5; }
  .info-card.purple { border-left-color: #7c3aed; background: #f5f3ff; }
  .info-card-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px; color: #1e3a5f; }
  .info-card.green  .info-card-header { color: #065f46; }
  .info-card.purple .info-card-header { color: #5b21b6; }
  .example-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-top: 5px solid #059669; transition: transform 0.2s; }
  .example-card:hover { transform: translateY(-3px); }
  .example-card:nth-child(2) { border-top-color: #7c3aed; }
  .example-card:nth-child(3) { border-top-color: #d97706; }
  .example-card:nth-child(4) { border-top-color: #dc2626; }
  .example-num { display: inline-flex; align-items: center; justify-content: center; width: 32px; height: 32px; background: linear-gradient(135deg, #059669, #1e3c72); color: white; border-radius: 50%; font-size: 0.85rem; font-weight: 800; margin-bottom: 10px; }
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
  @media (max-width: 640px) { .compare-grid { grid-template-columns: 1fr; } .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.4rem; } .stats-strip { flex-direction: column; align-items: center; } }
</style>

<div class="math-post-hi">

<div class="post-hero">
  <h1>फ़ूरिए श्रृंखला — परिभाषा, गुणांक और हल उदाहरण</h1>
  <p><strong>फ़ूरिए श्रृंखला</strong> एक आवर्ती फ़ंक्शन को ज्यावक्र और सहज्यावक्र के अनंत योग के रूप में व्यक्त करती है। यह गणित, भौतिकी और अभियांत्रिकी का एक अत्यंत शक्तिशाली उपकरण है — और CSIR NET व GATE का एक मूलभूत विषय है।</p>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">3</span><span class="lbl">गुणांक सूत्र</span></div>
  <div class="stat-item"><span class="num">4</span><span class="lbl">हल उदाहरण</span></div>
  <div class="stat-item"><span class="num">★★★</span><span class="lbl">CSIR NET महत्त्व</span></div>
  <div class="stat-item"><span class="num">π²/6</span><span class="lbl">बेसल समस्या</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-book-open"></i></span> परिभाषा</h2>

<p>माना $f(x)$ आवर्तकाल $2\pi$ वाला एक आवर्ती फ़ंक्शन है। इसकी <strong>फ़ूरिए श्रृंखला</strong> है:</p>

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty}\left(a_n\cos nx + b_n\sin nx\right)$$

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-calculator"></i></span> ऑयलर के गुणांक सूत्र</h2>

<div class="info-card green">
  <div class="info-card-header"><i class="fas fa-function"></i> तीन ऑयलर सूत्र</div>
  $$a_0 = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\,dx$$
  $$a_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\cos(nx)\,dx, \quad n = 1, 2, 3, \ldots$$
  $$b_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\sin(nx)\,dx, \quad n = 1, 2, 3, \ldots$$
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-exchange-alt"></i></span> सम और विषम फ़ंक्शन</h2>

<div class="compare-grid">
  <div class="compare-card blue">
    <h4><i class="fas fa-mirror"></i> सम फ़ंक्शन: $f(-x) = f(x)$</h4>
    <ul>
      <li>$b_n = 0$ (कोई ज्यावक्र पद नहीं)</li>
      <li>$a_0 = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} f(x)\,dx$</li>
      <li>$a_n = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} f(x)\cos(nx)\,dx$</li>
    </ul>
    $$f(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty} a_n\cos nx$$
  </div>
  <div class="compare-card green">
    <h4><i class="fas fa-sort-alt"></i> विषम फ़ंक्शन: $f(-x) = -f(x)$</h4>
    <ul>
      <li>$a_0 = a_n = 0$ (कोई सहज्यावक्र पद नहीं)</li>
      <li>$b_n = \dfrac{2}{\pi}\displaystyle\int_0^{\pi} f(x)\sin(nx)\,dx$</li>
    </ul>
    $$f(x) = \sum_{n=1}^{\infty} b_n\sin nx$$
  </div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-check-square"></i></span> दिरिक्ले की अभिसरण शर्तें</h2>

<div class="info-card">
  <div class="info-card-header"><i class="fas fa-list-check"></i> $f(x)$ की फ़ूरिए श्रृंखला अभिसरित होती है यदि:</div>
  <ol style="margin:0;padding-left:20px;color:#333;">
    <li style="margin-bottom:6px;">$f(x)$ <strong>आवर्ती</strong> है</li>
    <li style="margin-bottom:6px;">$f(x)$ $[-\pi,\pi]$ पर <strong>खंडशः सतत</strong> है</li>
    <li style="margin-bottom:6px;">एक आवर्तकाल में $f(x)$ के <strong>परिमित उच्चिष्ठ और निम्निष्ठ</strong> हैं</li>
    <li style="margin-bottom:6px;">एक आवर्तकाल में $f(x)$ की <strong>परिमित असातत्यताएँ</strong> हैं</li>
  </ol>
  <p style="margin-top:12px;"><strong>असातत्यता बिंदु</strong> $x = c$ पर:</p>
  $$\text{फ़ूरिए श्रृंखला} = \frac{f(c^+) + f(c^-)}{2}$$
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-pencil-alt"></i></span> हल उदाहरण</h2>

<div class="example-card">
  <div class="example-label">उदाहरण 1 — सरल (वर्गाकार तरंग)</div>
  <div class="example-num">१</div>
  <p><strong>फ़ूरिए श्रृंखला ज्ञात करें:</strong></p>
  $$f(x) = \begin{cases} -1 & -\pi &lt; x &lt; 0 \\ 1 & 0 &lt; x &lt; \pi \end{cases}$$
  <p><strong>चरण 1:</strong> $f(x)$ <strong>विषम फ़ंक्शन</strong> है → $a_0 = 0$, $a_n = 0$।</p>
  <p><strong>चरण 2:</strong> $b_n$ परिकलित करें:</p>
  $$b_n = \frac{2}{\pi}\int_0^{\pi}\sin(nx)\,dx = \frac{2}{\pi}\cdot\frac{1-(-1)^n}{n} = \frac{2(1-(-1)^n)}{n\pi}$$
  <p><strong>चरण 3:</strong> सम $n$ के लिए $b_n = 0$; विषम $n$ के लिए $b_n = \dfrac{4}{n\pi}$।</p>
  $$\boxed{f(x) = \frac{4}{\pi}\left(\sin x + \frac{\sin 3x}{3} + \frac{\sin 5x}{5} + \cdots\right)}$$
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 2 — मध्यम (बेसल समस्या)</div>
  <div class="example-num">२</div>
  <p><strong>$f(x) = x^2$ की फ़ूरिए श्रृंखला ज्ञात करें और इससे $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^2}$ निकालें।</strong></p>
  <p><strong>चरण 1:</strong> $f(x) = x^2$ <strong>सम फ़ंक्शन</strong> है → $b_n = 0$।</p>
  <p><strong>चरण 2:</strong> $a_0 = \dfrac{2\pi^2}{3}$।</p>
  <p><strong>चरण 3:</strong> खंडशः समाकलन से $a_n = \dfrac{4(-1)^n}{n^2}$।</p>
  <p><strong>चरण 4:</strong> फ़ूरिए श्रृंखला:</p>
  $$x^2 = \frac{\pi^2}{3} + 4\sum_{n=1}^{\infty}\frac{(-1)^n}{n^2}\cos(nx)$$
  <p><strong>चरण 5:</strong> $x = \pi$ रखें:</p>
  $$\pi^2 = \frac{\pi^2}{3} + 4\sum_{n=1}^{\infty}\frac{1}{n^2}$$
  <div class="highlight-result">
    $$\sum_{n=1}^{\infty}\frac{1}{n^2} = \frac{\pi^2}{6}$$
    <p style="margin:8px 0 0;font-size:0.88rem;color:#065f46;"><strong>यह प्रसिद्ध बेसल समस्या है — जिसे ऑयलर ने 1734 में हल किया था!</strong></p>
  </div>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 3 — मध्यम-कठिन (असतत फ़ंक्शन)</div>
  <div class="example-num">३</div>
  <p><strong>$f(x) = x$, $(-\pi, \pi)$ पर, की फ़ूरिए श्रृंखला ज्ञात करें।</strong></p>
  <p><strong>चरण 1:</strong> $f(x) = x$ <strong>विषम</strong> है → $a_0 = 0$, $a_n = 0$।</p>
  <p><strong>चरण 2:</strong> खंडशः समाकलन से:</p>
  $$b_n = \frac{2}{\pi}\int_0^{\pi} x\sin(nx)\,dx = \frac{2(-1)^{n+1}}{n}$$
  $$\boxed{f(x) = x = 2\left(\sin x - \frac{\sin 2x}{2} + \frac{\sin 3x}{3} - \cdots\right), \quad x \in (-\pi, \pi)}$$
  <p><em>$x = \pm\pi$ (असातत्यता) पर:</em> फ़ूरिए श्रृंखला $\dfrac{\pi+(-\pi)}{2} = 0$ पर अभिसरित होती है। ✓</p>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 4 — परीक्षा स्तर (पार्सेवल का प्रमेय)</div>
  <div class="example-num">४</div>
  <p><strong>$f(x) = x$ की फ़ूरिए श्रृंखला का उपयोग कर $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^2}$ ज्ञात करें।</strong></p>
  <p><strong>चरण 1:</strong> पार्सेवल का प्रमेय:</p>
  $$\frac{1}{\pi}\int_{-\pi}^{\pi}[f(x)]^2\,dx = \frac{a_0^2}{2} + \sum_{n=1}^{\infty}(a_n^2 + b_n^2)$$
  <p><strong>चरण 2:</strong> बायाँ पक्ष: $\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} x^2\,dx = \dfrac{2\pi^2}{3}$।</p>
  <p><strong>चरण 3:</strong> दायाँ पक्ष ($a_n = 0$, $b_n = \dfrac{2(-1)^{n+1}}{n}$):</p>
  $$\sum_{n=1}^{\infty} b_n^2 = \sum_{n=1}^{\infty}\frac{4}{n^2}$$
  <p><strong>चरण 4:</strong> समान करने पर:</p>
  $$\frac{2\pi^2}{3} = 4\sum_{n=1}^{\infty}\frac{1}{n^2} \implies \sum_{n=1}^{\infty}\frac{1}{n^2} = \frac{\pi^2}{6}\ ✓$$
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-infinity"></i></span> पार्सेवल का प्रमेय</h2>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-wave-square"></i> कथन</div>
  $[-\pi,\pi]$ पर $f(x)$ की फ़ूरिए श्रृंखला के लिए:
  $$\frac{1}{\pi}\int_{-\pi}^{\pi}[f(x)]^2\,dx = \frac{a_0^2}{2} + \sum_{n=1}^{\infty}(a_n^2 + b_n^2)$$
  यह फ़ंक्शन की <strong>ऊर्जा</strong> को उसके फ़ूरिए गुणांकों से जोड़ता है — संकेत प्रसंस्करण में मूलभूत।
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> CSIR NET / GATE / IIT JAM परीक्षा युक्तियाँ</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> परीक्षा रणनीतियाँ</div>
  <ul>
    <li><strong>सम-विषम जाँच सबसे पहले करें:</strong> विषम → केवल $b_n$; सम → केवल $a_n$। इससे परिकलन आधा हो जाता है।</li>
    <li><strong>दिरिक्ले शर्तें MCQ में काम आती हैं:</strong> यदि $f$ सतत है और दिरिक्ले शर्तें पूर्ण हों, तो श्रृंखला $f(x_0)$ पर ही अभिसरित होती है।</li>
    <li><strong>असातत्यता सूत्र बहुत पूछा जाता है:</strong> $x = c$ पर श्रृंखला $\dfrac{f(c^+)+f(c^-)}{2}$ पर अभिसरित होती है। याद रखें।</li>
    <li><strong>बेसल प्रकार के योग $f(x) = x^2$ से आते हैं:</strong> $x = 0$ रखने पर $\sum \dfrac{(-1)^{n+1}}{n^2} = \dfrac{\pi^2}{12}$; $x = \pi$ रखने पर $\sum \dfrac{1}{n^2} = \dfrac{\pi^2}{6}$।</li>
    <li><strong>पार्सेवल का प्रमेय</strong> $\sum \dfrac{1}{n^4}$, $\sum \dfrac{1}{n^2}$ आदि के लिए सबसे तेज उपकरण है।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> सामान्य गलतियाँ</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> इन गलतियों से बचें</div>
  <ul>
    <li><strong>गलत गुणांक सूत्र:</strong> $a_0 = \dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\,dx$ परन्तु श्रृंखला में $\dfrac{a_0}{2}$ आता है। यह 2 का गुणनखंड परीक्षा का जाल है।</li>
    <li><strong>दिरिक्ले शर्तें न जाँचना:</strong> $f(x)$ पर अभिसरण का दावा करने से पहले शर्तें अवश्य जाँचें।</li>
    <li><strong>खंडशः समाकलन में त्रुटि:</strong> फ़ूरिए गुणांकों के लिए प्रायः खंडशः समाकलन आवश्यक है। $u = f(x)$, $dv = \cos(nx)\,dx$ या $\sin(nx)\,dx$ लें।</li>
    <li><strong>पार्सेवल में $\frac{1}{\pi}$ भूलना:</strong> बायाँ पक्ष $\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi}[f(x)]^2\,dx$ है — बिना $\frac{1}{\pi}$ के नहीं।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> वास्तविक जीवन में अनुप्रयोग</h2>

<div class="app-grid">
  <div class="app-card"><div class="app-icon">📡</div><strong>संकेत प्रसंस्करण</strong><p>प्रत्येक डिजिटल संकेत को फ़ूरिए श्रृंखला से आवृत्ति घटकों में विघटित किया जाता है — दूरसंचार का आधार।</p></div>
  <div class="app-card"><div class="app-icon">🌡️</div><strong>ऊष्मा चालन</strong><p>फ़ूरिए ने ही इस सिद्धांत को ऊष्मा समीकरण हल करने के लिए विकसित किया — ठोसों में तापमान वितरण का मॉडल।</p></div>
  <div class="app-card"><div class="app-icon">🎵</div><strong>संगीत और ध्वनिकी</strong><p>वाद्य यंत्रों की विशिष्ट ध्वनि उनके फ़ूरिए हार्मोनिकों के आयामों से निर्धारित होती है।</p></div>
  <div class="app-card"><div class="app-icon">🏗️</div><strong>संरचनात्मक अभियांत्रिकी</strong><p>पुलों और भवनों के कंपन विश्लेषण में फ़ूरिए श्रृंखला से अनुनाद आवृत्तियाँ निकाली जाती हैं।</p></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> सारांश तालिका</h2>

<table class="summary-table">
  <thead><tr><th>राशि</th><th>सूत्र</th><th>शर्त</th></tr></thead>
  <tbody>
    <tr><td>$a_0$</td><td>$\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\,dx$</td><td>सदैव</td></tr>
    <tr><td>$a_n$</td><td>$\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\cos(nx)\,dx$</td><td>$n \geq 1$</td></tr>
    <tr><td>$b_n$</td><td>$\dfrac{1}{\pi}\displaystyle\int_{-\pi}^{\pi} f(x)\sin(nx)\,dx$</td><td>$n \geq 1$</td></tr>
    <tr><td>$b_n = 0$</td><td>—</td><td>$f$ सम है</td></tr>
    <tr><td>$a_0 = a_n = 0$</td><td>—</td><td>$f$ विषम है</td></tr>
    <tr><td>असातत्यता पर</td><td>$\dfrac{f(c^+)+f(c^-)}{2}$</td><td>दिरिक्ले शर्तें पूर्ण हों</td></tr>
  </tbody>
</table>

</div>
