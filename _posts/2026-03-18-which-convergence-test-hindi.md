---
layout: post
title: "कौन सा अभिसरण परीक्षण उपयोग करें? — पूर्ण निर्णय मार्गदर्शिका"
date: 2026-03-18
category: maths
lang: hi
lang_pair: "/blog/which-convergence-test-english/"
permalink: /blog/which-convergence-test-hindi/
listed: false
description: "किसी भी श्रृंखला के लिए सही अभिसरण परीक्षण चुनने की पूर्ण मार्गदर्शिका — निर्णय तालिका, हल उदाहरण और परीक्षा युक्तियाँ।"
---

<link href="https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
  .math-post-hi { font-family: 'Hind', 'Noto Sans Devanagari', sans-serif; font-size: 1.05rem; line-height: 1.9; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 60%, #ff4b2b 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "∑"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
  .post-hero h1 { font-size: 1.75rem; font-weight: 800; color: white; margin: 0 0 10px; line-height: 1.35; }
  .post-hero p { font-size: 1rem; opacity: 0.9; margin: 0; }
  .stats-strip { background: linear-gradient(135deg, #1e3c72, #7c3aed); border-radius: 14px; padding: 22px 28px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 16px; margin-bottom: 35px; text-align: center; color: white; }
  .stat-item .num { font-size: 1.9rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.7rem; opacity: 0.8; margin-top: 4px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }
  .section-title { display: flex; align-items: center; gap: 12px; font-size: 1.35rem; font-weight: 800; color: #1e3c72; margin: 42px 0 20px; padding-bottom: 10px; border-bottom: 3px solid transparent; border-image: linear-gradient(to right, #1e3c72, #7c3aed, #ff4b2b, transparent) 1; }
  .sec-icon { width: 38px; height: 38px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .sub-title { font-size: 1.1rem; font-weight: 700; color: #2a5298; margin: 26px 0 12px; display: flex; align-items: center; gap: 8px; }
  .sub-title::before { content: ''; width: 4px; height: 18px; background: linear-gradient(to bottom, #ff4b2b, #fbbf24); border-radius: 2px; flex-shrink: 0; }
  .info-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-left: 5px solid #1e3c72; }
  .info-card.gold { border-left-color: #d97706; background: #fffbeb; }
  .info-card-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px; color: #1e3a5f; }
  .info-card.gold .info-card-header { color: #92400e; }
  .example-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-top: 5px solid #1e3c72; transition: transform 0.2s; }
  .example-card:hover { transform: translateY(-3px); }
  .example-card:nth-child(2) { border-top-color: #7c3aed; }
  .example-card:nth-child(3) { border-top-color: #d97706; }
  .example-card:nth-child(4) { border-top-color: #dc2626; }
  .example-card:nth-child(5) { border-top-color: #059669; }
  .example-card:nth-child(6) { border-top-color: #0891b2; }
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
  @media (max-width: 640px) { .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.4rem; } .stats-strip { flex-direction: column; align-items: center; } }
</style>

<div class="math-post-hi">

<div class="post-hero">
  <h1>कौन सा अभिसरण परीक्षण उपयोग करें? — पूर्ण निर्णय मार्गदर्शिका</h1>
  <p>श्रृंखला के अध्ययन में सबसे कठिन प्रश्न यही होता है कि <strong>कौन सा परीक्षण लगाएँ।</strong> यह मार्गदर्शिका आपको एक स्पष्ट, क्रमबद्ध निर्णय प्रक्रिया देती है — ताकि परीक्षा में कभी भ्रम न हो।</p>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">9</span><span class="lbl">परीक्षण</span></div>
  <div class="stat-item"><span class="num">6</span><span class="lbl">हल उदाहरण</span></div>
  <div class="stat-item"><span class="num">★★★</span><span class="lbl">CSIR NET महत्त्व</span></div>
  <div class="stat-item"><span class="num">∑</span><span class="lbl">श्रृंखला विश्लेषण</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-sitemap"></i></span> चरणबद्ध निर्णय प्रक्रिया</h2>

<div class="sub-title">चरण 1 — हमेशा यहाँ से शुरू करें: अपसरण परीक्षण</div>

<p>किसी भी अन्य परीक्षण से पहले यह परिकलित करें:</p>
$$\lim_{n\to\infty} a_n$$

<div class="info-card">
  <div class="info-card-header"><i class="fas fa-traffic-light"></i> निर्णय नियम</div>
  <ul>
    <li>यदि सीमा <strong>≠ 0</strong> या <strong>अस्तित्व नहीं</strong> → श्रृंखला <strong>अपसरित होती है</strong> — यहीं रुकें।</li>
    <li>यदि सीमा <strong>= 0</strong> → अनिर्णायक — चरण 2 पर जाएँ।</li>
  </ul>
</div>

<div class="sub-title">चरण 2 — $a_n$ का रूप पहचानें</div>

<table class="summary-table">
  <thead><tr><th>$a_n$ का रूप</th><th>सर्वश्रेष्ठ परीक्षण</th></tr></thead>
  <tbody>
    <tr><td>$\dfrac{1}{n^p}$</td><td>p-श्रृंखला परीक्षण</td></tr>
    <tr><td>$ar^n$</td><td>गुणोत्तर श्रृंखला परीक्षण</td></tr>
    <tr><td>$n!$ या $n^n$ उपस्थित</td><td>अनुपात परीक्षण (Ratio Test)</td></tr>
    <tr><td>$(f(n))^n$ रूप</td><td>मूल परीक्षण (Root Test)</td></tr>
    <tr><td>एकान्तर चिह्न $(-1)^n$</td><td>एकान्तर श्रृंखला परीक्षण</td></tr>
    <tr><td>$n$ का परिमेय फ़ंक्शन</td><td>सीमा तुलना परीक्षण</td></tr>
    <tr><td>सरलता से समाकलनीय $f(n)$</td><td>समाकल परीक्षण</td></tr>
    <tr><td>सीमित आंशिक योग वाला गुणनफल</td><td>दिरिक्ले का परीक्षण</td></tr>
    <tr><td>अनुपात/मूल परीक्षण $L = 1$ दे</td><td>राबे का परीक्षण</td></tr>
  </tbody>
</table>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-table"></i></span> त्वरित संदर्भ तालिका</h2>

<table class="summary-table">
  <thead><tr><th>परीक्षण</th><th>अभिसरण</th><th>अपसरण</th><th>अनिर्णायक</th></tr></thead>
  <tbody>
    <tr><td>अपसरण परीक्षण</td><td>कभी नहीं</td><td>$\lim a_n \neq 0$</td><td>$\lim a_n = 0$</td></tr>
    <tr><td>p-श्रृंखला</td><td>$p &gt; 1$</td><td>$p \leq 1$</td><td>—</td></tr>
    <tr><td>गुणोत्तर श्रृंखला</td><td>$\lvert r\rvert &lt; 1$</td><td>$\lvert r\rvert \geq 1$</td><td>—</td></tr>
    <tr><td>अनुपात परीक्षण</td><td>$L &lt; 1$</td><td>$L &gt; 1$</td><td>$L = 1$</td></tr>
    <tr><td>मूल परीक्षण</td><td>$L &lt; 1$</td><td>$L &gt; 1$</td><td>$L = 1$</td></tr>
    <tr><td>एकान्तर श्रृंखला</td><td>$b_n \searrow 0$</td><td>—</td><td>$b_n \not\to 0$</td></tr>
    <tr><td>राबे का परीक्षण</td><td>$R &gt; 1$</td><td>$R &lt; 1$</td><td>$R = 1$</td></tr>
  </tbody>
</table>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-pencil-alt"></i></span> हल उदाहरण</h2>

<div class="example-card">
  <div class="example-label">उदाहरण 1 — सरल</div>
  <div class="example-num">१</div>
  <p><strong>परीक्षण करें:</strong> $\displaystyle\sum \frac{n^2+1}{n^4+3}$</p>
  <p><strong>पहचान:</strong> $n$ का परिमेय फ़ंक्शन। प्रमुख पद से $\dfrac{n^2}{n^4} = \dfrac{1}{n^2}$।</p>
  <p><strong>परीक्षण:</strong> सीमा तुलना, $b_n = \dfrac{1}{n^2}$ के साथ।</p>
  $$L = \lim_{n\to\infty} \frac{(n^2+1)/(n^4+3)}{1/n^2} = \lim_{n\to\infty}\frac{n^4+n^2}{n^4+3} = 1$$
  <p>$0 &lt; L &lt; \infty$ और $\sum \dfrac{1}{n^2}$ अभिसरित होती है (p-श्रृंखला, $p=2$) → श्रृंखला <strong>अभिसरित होती है</strong>। ✓</p>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 2 — सरल-मध्यम</div>
  <div class="example-num">२</div>
  <p><strong>परीक्षण करें:</strong> $\displaystyle\sum \frac{3^n}{n!}$</p>
  <p><strong>पहचान:</strong> $n!$ उपस्थित है → <strong>अनुपात परीक्षण</strong>।</p>
  $$\frac{a_{n+1}}{a_n} = \frac{3^{n+1}}{(n+1)!}\cdot\frac{n!}{3^n} = \frac{3}{n+1}$$
  $$L = \lim_{n\to\infty}\frac{3}{n+1} = 0 < 1 \implies \textbf{अभिसरित।}\ ✓$$
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 3 — मध्यम</div>
  <div class="example-num">३</div>
  <p><strong>परीक्षण करें:</strong> $\displaystyle\sum \left(\frac{n}{2n+1}\right)^n$</p>
  <p><strong>पहचान:</strong> $(f(n))^n$ रूप → <strong>मूल परीक्षण</strong>।</p>
  $$(a_n)^{1/n} = \frac{n}{2n+1} \implies L = \lim_{n\to\infty}\frac{n}{2n+1} = \frac{1}{2} < 1 \implies \textbf{अभिसरित।}\ ✓$$
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 4 — मध्यम-कठिन</div>
  <div class="example-num">४</div>
  <p><strong>परीक्षण करें:</strong> $\displaystyle\sum \frac{(-1)^n}{\sqrt{n}}$</p>
  <p><strong>पहचान:</strong> एकान्तर चिह्न → <strong>एकान्तर श्रृंखला परीक्षण</strong>। $b_n = \dfrac{1}{\sqrt{n}}$ लें।</p>
  <ul>
    <li>$b_n > 0$ ✓</li>
    <li>$b_n$ ह्रासमान: $\dfrac{1}{\sqrt{n+1}} &lt; \dfrac{1}{\sqrt{n}}$ ✓</li>
    <li>$\lim_{n\to\infty} b_n = 0$ ✓</li>
  </ul>
  <p>तीनों शर्तें पूर्ण → श्रृंखला <strong>सशर्त अभिसरित होती है</strong>। ✓ (निरपेक्ष अभिसरण नहीं, क्योंकि $\sum \dfrac{1}{\sqrt{n}}$ अपसरित है।)</p>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 5 — कठिन</div>
  <div class="example-num">५</div>
  <p><strong>परीक्षण करें:</strong> $\displaystyle\sum \frac{n}{e^n}$</p>
  <p><strong>पहचान:</strong> घातांकीय → <strong>अनुपात परीक्षण</strong>।</p>
  $$\frac{a_{n+1}}{a_n} = \frac{n+1}{e^{n+1}}\cdot\frac{e^n}{n} = \frac{n+1}{n}\cdot\frac{1}{e}$$
  $$L = \lim_{n\to\infty}\frac{n+1}{n}\cdot\frac{1}{e} = \frac{1}{e} < 1 \implies \textbf{अभिसरित।}\ ✓$$
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 6 — परीक्षा स्तर</div>
  <div class="example-num">६</div>
  <p><strong>परीक्षण करें:</strong> $\displaystyle\sum \frac{1}{n\ln n}$</p>
  <p><strong>पहचान:</strong> अनुपात परीक्षण $L=1$ देता है (अनिर्णायक) → <strong>समाकल परीक्षण</strong>।</p>
  $$\int_2^{\infty}\frac{1}{x\ln x}\,dx = \Big[\ln(\ln x)\Big]_2^{\infty} = \infty$$
  <p>समाकल अपसरित → श्रृंखला <strong>अपसरित होती है</strong>। ✗</p>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> CSIR NET / GATE / IIT JAM परीक्षा युक्तियाँ</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> परीक्षा रणनीतियाँ</div>
  <ul>
    <li><strong>सबसे पहले अपसरण परीक्षण लगाएँ</strong> — यदि $a_n \not\to 0$, तो 10 सेकंड में उत्तर।</li>
    <li><strong>$n!$ या $n^n$ दिखे?</strong> → तुरंत अनुपात परीक्षण। कोई अपवाद नहीं।</li>
    <li><strong>$(f(n))^n$ रूप है?</strong> → तुरंत मूल परीक्षण।</li>
    <li><strong>परिमेय फ़ंक्शन है?</strong> → प्रमुख पदों से p-श्रृंखला के साथ सीमा तुलना परीक्षण।</li>
    <li><strong>अनुपात/मूल परीक्षण $L=1$ दे?</strong> → राबे का परीक्षण: $R = \lim n\!\left(\dfrac{a_n}{a_{n+1}}-1\right)$।</li>
    <li><strong>एकान्तर श्रृंखला?</strong> → पहले निरपेक्ष अभिसरण जाँचें। यदि $\sum\lvert a_n\rvert$ अभिसरित हो, काम हो गया।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> सामान्य गलतियाँ</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> इन गलतियों से बचें</div>
  <ul>
    <li><strong>परिमेय फ़ंक्शन पर अनुपात परीक्षण:</strong> हमेशा $L=1$ देता है — अनिर्णायक। $a_n$ के रूप के अनुसार परीक्षण चुनें।</li>
    <li><strong>अपसरण परीक्षण छोड़ना:</strong> पहले $a_n\to 0$ जाँचें — बहुत समय बचता है।</li>
    <li><strong>"$\lim a_n = 0$ मतलब अभिसरण":</strong> बिल्कुल गलत। हार्मोनिक श्रृंखला $\sum \frac{1}{n}$ इसका सबसे बड़ा उदाहरण है।</li>
    <li><strong>निरपेक्ष और सशर्त अभिसरण में भ्रम:</strong> सशर्त अभिसरण और निरपेक्ष अभिसरण अलग-अलग हैं — हमेशा स्पष्ट करें।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> वास्तविक जीवन में अनुप्रयोग</h2>

<div class="app-grid">
  <div class="app-card"><div class="app-icon">📡</div><strong>संकेत प्रसंस्करण</strong><p>फ़ूरिए श्रृंखला विस्तार की वैधता जाँचने के लिए अभिसरण परीक्षण आवश्यक हैं।</p></div>
  <div class="app-card"><div class="app-icon">⚛️</div><strong>क्वाण्टम यांत्रिकी</strong><p>विक्षोभ श्रृंखलाएँ अभिसरित होनी चाहिए — भौतिकशास्त्री अनुपात परीक्षण से वैधता जाँचते हैं।</p></div>
  <div class="app-card"><div class="app-icon">💻</div><strong>संख्यात्मक विश्लेषण</strong><p>पुनरावृत्ति एल्गोरिदम के विश्वसनीय परिणाम सुनिश्चित करने के लिए अभिसरण परीक्षण आवश्यक हैं।</p></div>
  <div class="app-card"><div class="app-icon">📈</div><strong>वित्त</strong><p>अनंत गुणोत्तर श्रृंखला शाश्वत भुगतान धाराओं के वर्तमान मूल्य को मॉडल करती है।</p></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-star"></i></span> स्वर्णिम नियम — सारांश</h2>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-trophy"></i> छः स्वर्णिम नियम</div>
  <ol style="margin:0;padding-left:20px;color:#78350f;">
    <li style="margin-bottom:7px;"><strong>सबसे पहले अपसरण परीक्षण लगाएँ।</strong></li>
    <li style="margin-bottom:7px;"><strong>$n!$ या $n^n$ है?</strong> → अनुपात परीक्षण।</li>
    <li style="margin-bottom:7px;"><strong>$(f(n))^n$ रूप है?</strong> → मूल परीक्षण।</li>
    <li style="margin-bottom:7px;"><strong>परिमेय फ़ंक्शन है?</strong> → p-श्रृंखला के साथ सीमा तुलना परीक्षण।</li>
    <li style="margin-bottom:7px;"><strong>एकान्तर चिह्न है?</strong> → पहले निरपेक्ष अभिसरण, फिर एकान्तर श्रृंखला परीक्षण।</li>
    <li style="margin-bottom:7px;"><strong>अनुपात/मूल परीक्षण $L=1$ दे?</strong> → राबे का परीक्षण या समाकल परीक्षण।</li>
  </ol>
</div>

</div>
