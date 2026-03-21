---
layout: post
title: "ℝ में Point Set Topology का परिचय — मूल अवधारणाएँ"
date: 2026-03-21
category: maths
lang: hi
lang_pair: "/blog/introduction-to-point-set-topology/"
permalink: /blog/introduction-to-point-set-topology-hindi/
listed: false
description: "ℝ में Point Set Topology का सरल परिचय — वास्तविक संख्या रेखा, निरपेक्ष मान, ε-पड़ोस और Supremum की अवधारणाएँ।"
---

<link href="https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
  .math-post-hi { font-family: 'Hind', 'Noto Sans Devanagari', sans-serif; font-size: 1.05rem; line-height: 1.9; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 60%, #7c3aed 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "ℝ"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
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
  @media (max-width: 640px) { .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.4rem; } .stats-strip { flex-direction: column; align-items: center; } }
</style>

<div class="math-post-hi">

<div class="post-hero">
  <h1>ℝ में Point Set Topology का परिचय</h1>
  <p><strong>Point Set Topology</strong> वास्तविक संख्या रेखा के उपसमुच्चयों की संरचना का अध्ययन है — खुलेपन (openness), बंदपन (closedness), सीमाओं और सातत्य की अवधारणाओं के माध्यम से। यह वास्तविक विश्लेषण (Real Analysis) की कठोर नींव है।</p>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">ℝ</span><span class="lbl">वास्तविक रेखा</span></div>
  <div class="stat-item"><span class="num">ε</span><span class="lbl">पड़ोस</span></div>
  <div class="stat-item"><span class="num">★★★</span><span class="lbl">CSIR NET महत्त्व</span></div>
  <div class="stat-item"><span class="num">sup</span><span class="lbl">पूर्णता</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-infinity"></i></span> वास्तविक संख्या रेखा ℝ</h2>

<p>सभी वास्तविक संख्याओं का समुच्चय $\mathbb{R}$ एक <strong>पूर्ण क्रमित क्षेत्र (complete ordered field)</strong> है। इसके तीन मूलभूत गुण हैं:</p>

<div class="info-card">
  <div class="info-card-header"><i class="fas fa-list"></i> तीन मूलभूत गुण</div>
  <ul>
    <li><strong>क्रमित (Ordered):</strong> किसी भी $a, b \in \mathbb{R}$ के लिए, $a &lt; b$, $a = b$ या $a &gt; b$ में से ठीक एक सत्य होता है।</li>
    <li><strong>क्षेत्र (Field):</strong> जोड़ और गुणन भली-भाँति परिभाषित हैं तथा इनके व्युत्क्रम (inverse) विद्यमान हैं।</li>
    <li><strong>पूर्ण (Complete):</strong> ऊपर से परिबद्ध (bounded above) प्रत्येक अरिक्त उपसमुच्चय का <strong>न्यूनतम ऊपरी परिबंध (supremum)</strong> $\mathbb{R}$ में विद्यमान है।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-ruler"></i></span> निरपेक्ष मान (Absolute Value) और दूरी</h2>

<p>$x \in \mathbb{R}$ का <strong>निरपेक्ष मान</strong> है:</p>

$$|x| = \begin{cases} x & \text{यदि } x \geq 0 \\ -x & \text{यदि } x < 0 \end{cases}$$

<p>दो वास्तविक संख्याओं $a$ और $b$ के बीच <strong>दूरी</strong>: $d(a, b) = |a - b|$।</p>

<div class="sub-title">Absolute Value के गुण</div>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-check-circle"></i> चार प्रमुख गुण</div>
  <ol style="margin:0;padding-left:20px;color:#4c1d95;">
    <li style="margin-bottom:6px;">$\lvert a\rvert \geq 0$, और $\lvert a\rvert = 0 \iff a = 0$</li>
    <li style="margin-bottom:6px;">$\lvert ab\rvert = \lvert a\rvert\lvert b\rvert$</li>
    <li style="margin-bottom:6px;"><strong>Triangle Inequality (त्रिभुज असमानता):</strong> $\lvert a + b\rvert \leq \lvert a\rvert + \lvert b\rvert$</li>
    <li style="margin-bottom:6px;"><strong>Reverse Triangle Inequality:</strong> $\big\lvert\lvert a\rvert - \lvert b\rvert\big\rvert \leq \lvert a - b\rvert$</li>
  </ol>
</div>

<div class="sub-title">Triangle Inequality का प्रमाण</div>

<p>चूँकि $-\lvert a\rvert \leq a \leq \lvert a\rvert$ और $-\lvert b\rvert \leq b \leq \lvert b\rvert$, दोनों को जोड़ने पर:</p>

$$-(\lvert a\rvert+\lvert b\rvert) \leq a+b \leq \lvert a\rvert+\lvert b\rvert \implies \lvert a+b\rvert \leq \lvert a\rvert + \lvert b\rvert \quad \checkmark$$

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-circle"></i></span> ε-पड़ोस (ε-Neighbourhood)</h2>

<div class="info-card green">
  <div class="info-card-header"><i class="fas fa-book"></i> परिभाषा</div>
  बिंदु $a \in \mathbb{R}$ का <strong>ε-पड़ोस</strong> है:
  $$N_\varepsilon(a) = (a - \varepsilon,\, a + \varepsilon) = \{x \in \mathbb{R} : \lvert x - a\rvert < \varepsilon\}$$
  यह $a$ के केन्द्र पर त्रिज्या $\varepsilon$ वाली <strong>खुली गेंद (open ball)</strong> है। Topology में यह सबसे मूलभूत अवधारणा है।
</div>

<p><strong>उदाहरण:</strong> $N_{0.5}(3) = (2.5, 3.5)$ — $3$ से $0.5$ दूरी के भीतर स्थित सभी बिंदु।</p>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-pencil-alt"></i></span> हल उदाहरण</h2>

<div class="example-card">
  <div class="example-label">उदाहरण 1 — सरल</div>
  <div class="example-num">१</div>
  <p><strong>$\lvert x - 3\rvert &lt; 2$ को संतुष्ट करने वाले सभी $x \in \mathbb{R}$ ज्ञात करें।</strong></p>
  <p><strong>हल:</strong> $\lvert x-3\rvert &lt; 2 \iff -2 &lt; x-3 &lt; 2 \iff 1 &lt; x &lt; 5$।</p>
  <p>अतः हल समुच्चय खुला अंतराल $(1, 5) = N_2(3)$ है। ✓</p>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 2 — सरल-मध्यम</div>
  <div class="example-num">२</div>
  <p><strong>माना $S = \{1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots\}$। $\sup S$ और $\inf S$ ज्ञात करें।</strong></p>
  <p><strong>हल:</strong></p>
  <ul>
    <li>$\sup S = 1$ — अधिकतम अवयव $1$ है और यह $S$ में है। ✓</li>
    <li>$\inf S = 0$ — प्रत्येक पद $\frac{1}{n} &gt; 0$ है, किंतु किसी भी $\varepsilon &gt; 0$ के लिए, बड़े $n$ के लिए $\frac{1}{n} &lt; \varepsilon$, अतः $0$ ही महत्तम निम्न परिबंध है।</li>
    <li>ध्यान दें: $0 \notin S$ — infimum का समुच्चय में होना आवश्यक नहीं। ✓</li>
  </ul>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 3 — मध्यम</div>
  <div class="example-num">३</div>
  <p><strong>सिद्ध करें: सभी $a, b \in \mathbb{R}$ के लिए $\lvert a - b\rvert \geq \big\lvert \lvert a\rvert - \lvert b\rvert \big\rvert$।</strong></p>
  <p><strong>हल:</strong> Triangle Inequality से:</p>
  $$\lvert a\rvert = \lvert (a-b)+b\rvert \leq \lvert a-b\rvert + \lvert b\rvert \implies \lvert a\rvert - \lvert b\rvert \leq \lvert a-b\rvert$$
  <p>इसी प्रकार $\lvert b\rvert - \lvert a\rvert \leq \lvert a-b\rvert$। अतः $\big\lvert\lvert a\rvert - \lvert b\rvert\big\rvert \leq \lvert a-b\rvert$। $\blacksquare$</p>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 4 — परीक्षा स्तर</div>
  <div class="example-num">४</div>
  <p><strong>माना $A = \{x \in \mathbb{R} : x^2 &lt; 3\}$। $\sup A$ ज्ञात करें और Supremum की परिभाषा से सत्यापित करें।</strong></p>
  <p><strong>हल:</strong> $A = (-\sqrt{3}, \sqrt{3})$। दावा: $\sup A = \sqrt{3}$।</p>
  <ul>
    <li><strong>ऊपरी परिबंध:</strong> $A$ के प्रत्येक $x$ के लिए $x &lt; \sqrt{3}$। ✓</li>
    <li><strong>न्यूनतम ऊपरी परिबंध:</strong> किसी भी $\varepsilon &gt; 0$ के लिए, $\sqrt{3} - \varepsilon \in A$ (क्योंकि $(\sqrt{3}-\varepsilon)^2 &lt; 3$), अतः $\sqrt{3}$ से छोटी कोई संख्या ऊपरी परिबंध नहीं हो सकती। ✓</li>
  </ul>
  <p>अतः $\sup A = \sqrt{3} \notin A$ — supremum का समुच्चय में होना आवश्यक नहीं। $\blacksquare$</p>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> CSIR NET / GATE / IIT JAM परीक्षा युक्तियाँ</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> परीक्षा रणनीतियाँ</div>
  <ul>
    <li><strong>Triangle Inequality लगभग हर Analysis प्रमाण में आती है</strong> — इसे और इसके reverse रूप को पूरी तरह याद करें।</li>
    <li><strong>Supremum बनाम Maximum:</strong> परिबद्ध समुच्चयों के लिए $\sup S$ हमेशा विद्यमान है (completeness), किंतु $\max S$ तभी है जब $\sup S \in S$।</li>
    <li><strong>ε-neighbourhood प्रश्न:</strong> $\lvert x - a\rvert &lt; \varepsilon \iff x \in (a-\varepsilon, a+\varepsilon)$ — दोनों रूपों में आसानी से बदलना सीखें।</li>
    <li><strong>Archimedean Property:</strong> किसी भी $\varepsilon &gt; 0$ के लिए, $\exists\, n \in \mathbb{N}$ जिससे $\frac{1}{n} &lt; \varepsilon$ — यह प्रमाणों में बहुत उपयोगी है।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> सामान्य गलतियाँ</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> इन गलतियों से बचें</div>
  <ul>
    <li><strong>Supremum और Maximum में भ्रम:</strong> $S = (0,1)$ के लिए $\sup S = 1$ है, किंतु $\max S$ का अस्तित्व नहीं — क्योंकि $1 \notin S$।</li>
    <li><strong>Triangle Inequality की दिशा:</strong> असमानता $\lvert a+b\rvert \leq \lvert a\rvert + \lvert b\rvert$ है — यह समानता नहीं है।</li>
    <li><strong>ε-neighbourhood खुला है:</strong> $N_\varepsilon(a)$ खुला अंतराल है — इसमें अंतबिंदु $a \pm \varepsilon$ शामिल नहीं होते।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> वास्तविक जीवन में अनुप्रयोग</h2>

<div class="app-grid">
  <div class="app-card"><div class="app-icon">📡</div><strong>Signal Processing</strong><p>ε-neighbourhood डिजिटल फिल्टरों में संकेत मानों के चारों ओर Tolerance Band को मॉडल करता है।</p></div>
  <div class="app-card"><div class="app-icon">💻</div><strong>Numerical Analysis</strong><p>Supremum और Infimum का उपयोग संख्यात्मक सन्निकटनों में त्रुटि परिबंध निर्धारित करने के लिए किया जाता है।</p></div>
  <div class="app-card"><div class="app-icon">⚡</div><strong>Control Theory</strong><p>ℝ की Completeness गारंटी देती है कि Feedback Control Systems अभिसरित होते हैं।</p></div>
  <div class="app-card"><div class="app-icon">📐</div><strong>ज्यामिति</strong><p>दूरी की अवधारणा Metric Spaces तक सामान्यीकृत होती है जो Computer Graphics में उपयोगी है।</p></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> ℝ में Intervals — सारांश</h2>

<table class="summary-table">
  <thead><tr><th>संकेतन</th><th>नाम</th><th>परिभाषा</th></tr></thead>
  <tbody>
    <tr><td>$(a,b)$</td><td>खुला अंतराल (Open interval)</td><td>$\{x : a &lt; x &lt; b\}$</td></tr>
    <tr><td>$[a,b]$</td><td>बंद अंतराल (Closed interval)</td><td>$\{x : a \leq x \leq b\}$</td></tr>
    <tr><td>$[a,b)$</td><td>अर्ध-खुला (Half-open)</td><td>$\{x : a \leq x &lt; b\}$</td></tr>
    <tr><td>$(a,\infty)$</td><td>असीमित खुला (Unbounded open)</td><td>$\{x : x &gt; a\}$</td></tr>
    <tr><td>$(-\infty,\infty)$</td><td>पूरी वास्तविक रेखा</td><td>$\mathbb{R}$</td></tr>
  </tbody>
</table>

</div>
