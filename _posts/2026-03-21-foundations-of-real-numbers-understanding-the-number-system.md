---
layout: post
title: "Foundations of Real Numbers: Understanding the Number System"
date: 2026-03-21
category: maths
lang: en
lang_pair: "/blog/vastvik-sankhyaon-ki-neenv-sankhya-pranali-ki-samajh/"
permalink: /blog/foundations-of-real-numbers-understanding-the-number-system/
description: "A beginner-friendly guide to how our number system grew from counting to the real number line — the story of ℕ, ℤ, ℚ, irrationals, and ℝ with history, examples, and motivation."
---

<style>
  .math-post { font-family: Georgia, serif; font-size: 1.05rem; line-height: 1.9; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 50%, #7c3aed 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "ℝ"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
  .post-hero h1 { font-size: 1.85rem; font-weight: 800; color: white; margin: 0 0 10px; line-height: 1.3; }
  .post-hero p { font-size: 1rem; opacity: 0.9; margin: 0 0 14px; }
  .lang-switch { display: inline-flex; align-items: center; gap: 8px; background: rgba(255,255,255,0.15); border: 1px solid rgba(255,255,255,0.35); border-radius: 50px; padding: 7px 18px; font-size: 0.85rem; color: white; text-decoration: none; transition: background 0.2s; }
  .lang-switch:hover { background: rgba(255,255,255,0.28); color: white; text-decoration: none; }
  .stats-strip { background: linear-gradient(135deg, #1e3c72, #7c3aed); border-radius: 14px; padding: 22px 28px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 16px; margin-bottom: 35px; text-align: center; color: white; }
  .stat-item .num { font-size: 1.9rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.7rem; opacity: 0.8; margin-top: 4px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }
  .section-title { display: flex; align-items: center; gap: 12px; font-size: 1.4rem; font-weight: 800; color: #1e3c72; margin: 42px 0 20px; padding-bottom: 10px; border-bottom: 3px solid transparent; border-image: linear-gradient(to right, #1e3c72, #7c3aed, #ff4b2b, transparent) 1; }
  .sec-icon { width: 38px; height: 38px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .sub-title { font-size: 1.1rem; font-weight: 700; color: #2a5298; margin: 28px 0 12px; display: flex; align-items: center; gap: 8px; }
  .sub-title::before { content: ''; width: 4px; height: 18px; background: linear-gradient(to bottom, #ff4b2b, #fbbf24); border-radius: 2px; flex-shrink: 0; }
  .info-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-left: 5px solid #1e3c72; }
  .info-card.gold { border-left-color: #d97706; background: #fffbeb; }
  .info-card.green { border-left-color: #059669; background: #ecfdf5; }
  .info-card.purple { border-left-color: #7c3aed; background: #f5f3ff; }
  .info-card-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px; color: #1e3a5f; }
  .info-card.gold .info-card-header { color: #92400e; }
  .info-card.green .info-card-header { color: #065f46; }
  .info-card.purple .info-card-header { color: #5b21b6; }
  .floor-stack { margin: 24px 0; }
  .floor-item { display: flex; gap: 18px; position: relative; }
  .floor-item:not(:last-child)::after { content:''; position:absolute; left:19px; top:46px; bottom:0; width:2px; background:linear-gradient(to bottom,#1e3c72,#7c3aed,#059669); }
  .floor-badge { width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 0.95rem; font-weight: 900; color: white; flex-shrink: 0; margin-top: 2px; }
  .floor-badge.n { background: linear-gradient(135deg,#1e3c72,#2a5298); }
  .floor-badge.w { background: linear-gradient(135deg,#059669,#10b981); }
  .floor-badge.z { background: linear-gradient(135deg,#7c3aed,#a855f7); }
  .floor-badge.q { background: linear-gradient(135deg,#d97706,#f59e0b); }
  .floor-badge.r { background: linear-gradient(135deg,#dc2626,#ff4b2b); }
  .floor-body { background: white; border-radius: 12px; padding: 18px 20px; box-shadow: 0 3px 10px rgba(0,0,0,0.06); margin-bottom: 16px; flex: 1; }
  .floor-body h4 { margin: 0 0 5px; font-size: 1rem; font-weight: 800; color: #1e3c72; }
  .floor-body .floor-set { font-size: 0.82rem; color: #7c3aed; font-weight: 700; font-family: monospace; margin-bottom: 8px; }
  .floor-body p { margin: 0 0 8px; font-size: 0.93rem; color: #444; line-height: 1.7; }
  .floor-body p:last-child { margin-bottom: 0; }
  .problem-badge { display: inline-block; background: #fff5f5; border: 1px solid #fecaca; border-radius: 6px; padding: 3px 10px; font-size: 0.78rem; color: #dc2626; font-weight: 700; }
  .solved-badge { display: inline-block; background: #ecfdf5; border: 1px solid #6ee7b7; border-radius: 6px; padding: 3px 10px; font-size: 0.78rem; color: #059669; font-weight: 700; }
  .spotlight { background: linear-gradient(135deg, #1e3c72, #2a5298); border-radius: 14px; padding: 24px 26px; margin: 14px 0 10px; color: white; display: flex; gap: 16px; align-items: flex-start; border: 1px solid rgba(255,255,255,0.15); }
  .spotlight-icon { font-size: 2.4rem; flex-shrink: 0; }
  .spotlight h4 { margin: 0 0 8px; font-size: 1.05rem; color: #fbbf24; font-weight: 800; letter-spacing: 0.2px; }
  .spotlight p { margin: 0; font-size: 0.95rem; opacity: 1; line-height: 1.75; color: #e2e8f0; }
  .compare-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 20px 0; }
  .compare-card { border-radius: 12px; padding: 20px; }
  .compare-card.blue { background: #eff6ff; border: 2px solid #93c5fd; }
  .compare-card.green { background: #ecfdf5; border: 2px solid #6ee7b7; }
  .compare-card h4 { margin: 0 0 10px; font-size: 0.95rem; font-weight: 700; }
  .compare-card.blue h4 { color: #1e40af; }
  .compare-card.green h4 { color: #065f46; }
  .compare-card ul { margin: 0; padding-left: 18px; font-size: 0.88rem; color: #444; }
  .compare-card ul li { margin-bottom: 6px; }
  .pull-quote { border-left: 5px solid #7c3aed; padding: 14px 20px; margin: 24px 0; background: #f5f3ff; border-radius: 0 12px 12px 0; font-style: italic; font-size: 1.05rem; color: #4c1d95; line-height: 1.75; }
  .pull-quote cite { display: block; font-style: normal; font-size: 0.82rem; color: #7c3aed; margin-top: 8px; font-weight: 700; }
  .example-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-top: 5px solid #1e3c72; transition: transform 0.2s; }
  .example-card:hover { transform: translateY(-3px); }
  .example-card:nth-child(2) { border-top-color: #7c3aed; }
  .example-card:nth-child(3) { border-top-color: #d97706; }
  .example-card:nth-child(4) { border-top-color: #dc2626; }
  .example-num { display: inline-flex; align-items: center; justify-content: center; width: 32px; height: 32px; background: linear-gradient(135deg, #1e3c72, #7c3aed); color: white; border-radius: 50%; font-size: 0.85rem; font-weight: 800; margin-bottom: 10px; }
  .example-label { font-size: 0.7rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; color: #888; margin-bottom: 6px; }
  .solution-block { background: #f0fdf4; border-left: 4px solid #059669; border-radius: 0 8px 8px 0; padding: 14px 18px; margin-top: 12px; }
  .highlight-result { background: linear-gradient(135deg, #eff6ff, #e0e7ff); border: 2px solid #818cf8; border-radius: 12px; padding: 20px 24px; margin: 18px 0; text-align: center; }
  .tip-box { background: linear-gradient(135deg, #fffbeb, #fef3c7); border-left: 5px solid #d97706; border-radius: 0 12px 12px 0; padding: 20px 24px; margin: 20px 0; }
  .tip-box-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.6px; color: #92400e; margin-bottom: 12px; }
  .tip-box ul { margin: 0; padding-left: 18px; color: #78350f; }
  .tip-box ul li { margin-bottom: 8px; font-size: 0.95rem; }
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
  .summary-table th { background: linear-gradient(135deg, #1e3c72, #7c3aed); color: white; padding: 13px 16px; text-align: left; }
  .summary-table td { padding: 11px 16px; color: #333; border-bottom: 1px solid #e5e7eb; }
  .summary-table tr:nth-child(even) td { background: #f8faff; }
  .summary-table tr:last-child td { border-bottom: none; }
  .summary-table td:first-child { font-weight: 700; color: #1e3c72; }
  @media (max-width: 640px) { .compare-grid { grid-template-columns: 1fr; } .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.5rem; } .stats-strip { flex-direction: column; align-items: center; } .spotlight { flex-direction: column; } }
</style>

<div class="math-post">

<div class="post-hero">
  <h1>The Infinite Architecture: Foundations of Real Numbers</h1>
  <p>From ancient counting to the complete number line — a step-by-step journey through the five number systems that make all of mathematics possible.</p>
  <a class="lang-switch" href="/blog/vastvik-sankhyaon-ki-neenv-sankhya-pranali-ki-samajh/">
    <span>🇮🇳</span> हिंदी में पढ़ें
  </a>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">5</span><span class="lbl">Number Systems</span></div>
  <div class="stat-item"><span class="num">3000+</span><span class="lbl">Years of History</span></div>
  <div class="stat-item"><span class="num">4</span><span class="lbl">Solved Examples</span></div>
  <div class="stat-item"><span class="num">★★☆</span><span class="lbl">Beginner Friendly</span></div>
  <div class="stat-item"><span class="num">ℝ</span><span class="lbl">The Final System</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-building"></i></span> The Skyscraper Analogy</h2>

<p>Have you ever stopped to ask: <em>what is a number, really?</em> For most people, numbers are just tools — for bank balances, recipes, and measuring distances. But to a mathematician, the number system is a magnificent <strong>skyscraper</strong> built floor by floor over three thousand years of human thought.</p>

<div class="pull-quote">
  Every time humanity hit a wall — a problem that "couldn't be solved" — we didn't give up. We built a new floor.
  <cite>— The spirit of mathematical progress</cite>
</div>

<p>The important thing to understand is that <strong>each new type of number was born out of a real need</strong> — a problem the existing numbers simply could not solve. What began as counting sheep eventually grew into the most powerful mathematical system we have: the <strong>Real Number System ($\mathbb{R}$)</strong>.</p>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-layer-group"></i></span> The Five Floors: A Journey Through History</h2>

<div class="floor-stack">

  <div class="floor-item">
    <div class="floor-badge n">ℕ</div>
    <div class="floor-body">
      <h4>Floor 1 — Natural Numbers $\mathbb{N}$</h4>
      <div class="floor-set">$\mathbb{N} = \{1,\, 2,\, 3,\, 4,\, \ldots\}$</div>
      <p>The very first act of mathematics was <strong>counting</strong>. Ancient people counted cattle, days, and harvests. These are called natural numbers because they arise naturally — you discover them the moment you ask "how many?"</p>
      <p>You can always add them ($3 + 5 = 8$) and multiply them ($3 \times 4 = 12$), and the result is always a natural number. But subtraction quickly causes trouble.</p>
      <span class="problem-badge">❌ Gap: What is $3 - 5$? There is no natural number answer. We need a new floor.</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge w">𝕎</div>
    <div class="floor-body">
      <h4>Floor 2 — Whole Numbers $\mathbb{W}$</h4>
      <div class="floor-set">$\mathbb{W} = \{0,\, 1,\, 2,\, 3,\, \ldots\}$</div>
      <p>We add just one new idea: <strong>zero</strong>. This may seem small, but it was one of the most important discoveries in human history. Zero is not just "nothing" — it is a number that holds a place and makes our entire decimal system work.</p>

      <div class="spotlight">
        <div class="spotlight-icon">🏛️</div>
        <div>
          <h4>Aryabhata and the Power of Zero — Aryabhatiya (499 CE)</h4>
          <p>The Indian mathematician Aryabhata, in his treatise <em>Aryabhatiya</em> (499 CE), used a decimal place-value system that made zero a proper working digit — not merely a blank space. His system made it possible to clearly tell apart numbers like 42, 402, and 420. Without a working zero, these three look the same in older systems like Roman numerals (XLII cannot easily show the difference). This contribution transformed how all of humanity does arithmetic, and its influence spread across the world through Arabic translations.</p>
        </div>
      </div>

      <span class="problem-badge">❌ Gap: $5 - 8 = ?$ Still no answer. We need numbers that go below zero.</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge z">ℤ</div>
    <div class="floor-body">
      <h4>Floor 3 — Integers $\mathbb{Z}$</h4>
      <div class="floor-set">$\mathbb{Z} = \{\ldots,\, -3,\, -2,\, -1,\, 0,\, 1,\, 2,\, 3,\, \ldots\}$</div>
      <p>We extend the number line in both directions by adding <strong>negative numbers</strong>. Now subtraction always has an answer. The symbol $\mathbb{Z}$ comes from the German word <em>Zahlen</em>, simply meaning "numbers."</p>
      <p>Negative numbers gave mathematics the idea of <strong>direction</strong> (left or right, above or below sea level), <strong>debt</strong> (you owe money), and <strong>temperature below zero</strong>. The Indian mathematician Brahmagupta gave the first clear rules for arithmetic with negative numbers and zero in his work <em>Brahmasphutasiddhanta</em> (628 CE).</p>
      <span class="problem-badge">❌ Gap: $1 \div 2 = ?$ There is no integer answer. We need fractions.</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge q">ℚ</div>
    <div class="floor-body">
      <h4>Floor 4 — Rational Numbers $\mathbb{Q}$</h4>
      <div class="floor-set">$\mathbb{Q} = \left\{\dfrac{p}{q} : p,\, q \in \mathbb{Z},\ q \neq 0\right\}$</div>
      <p>The word <em>rational</em> comes from the Latin <em>ratio</em>, meaning a relationship between two numbers. Rational numbers are all fractions where the top and bottom are both integers and the bottom is not zero. Every decimal that either stops ($0.75$) or repeats forever in a pattern ($0.\overline{3} = \frac{1}{3}$) is rational.</p>
      <p>With rational numbers we can add, subtract, multiply, and divide (except by zero) and always stay within the system. Ancient Greek mathematicians were satisfied here — until one of them made a shocking discovery about a simple square.</p>
      <span class="problem-badge">❌ Gap: What number, squared, gives exactly 2? It is not any fraction. The number line still has holes!</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge r">ℝ</div>
    <div class="floor-body">
      <h4>Floor 5 — Real Numbers $\mathbb{R}$ &nbsp;<em>(The Complete Floor)</em></h4>
      <div class="floor-set">$\mathbb{R} = \mathbb{Q} \cup \mathbb{Q}^c \quad$ (All rationals + all irrationals)</div>
      <p>Real numbers fill <strong>every single point on the number line</strong> — no gaps, no holes, nothing missing. Every fraction is a real number. Every irrational number like $\sqrt{2}$, $\pi$, or $e$ is also a real number. Together they form a continuous (unbroken, flowing without any missing points) number line.</p>
      <p>This is the number system used in calculus, physics, and all of higher mathematics. When you draw a line on paper and say "every point on this line is a number," you are describing the real numbers.</p>
      <span class="solved-badge">✓ Complete: Every number that can be placed on a straight line is a real number.</span>
    </div>
  </div>

</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-exclamation-circle"></i></span> The Crisis That Created Irrational Numbers</h2>

<p>The ancient Greek Pythagorean school had a firm belief: <em>every quantity in nature can be written as a fraction</em>. To them, rational numbers were all there was. Then one of their own made a discovery that shook the foundations of their philosophy.</p>

<div class="compare-grid">
  <div class="compare-card blue">
    <h4>📐 The Problem: A Simple Square</h4>
    <ul>
      <li>Draw a square where each side is exactly 1 unit long</li>
      <li>By the Pythagorean theorem, the diagonal (the line crossing corner to corner) has length $\sqrt{2}$</li>
      <li>The Pythagoreans asked: can $\sqrt{2}$ be written as $\frac{p}{q}$?</li>
      <li>They were certain the answer was yes — and tried to prove it.</li>
    </ul>
  </div>
  <div class="compare-card green">
    <h4>✗ The Shock: It Cannot Be a Fraction</h4>
    <ul>
      <li>Assume $\sqrt{2} = \frac{p}{q}$ in its simplest form (no shared factors)</li>
      <li>Then $p^2 = 2q^2$, so $p$ must be even — write $p = 2m$</li>
      <li>Then $4m^2 = 2q^2$, so $q$ must also be even</li>
      <li>But then both $p$ and $q$ are even — they share the factor 2, which breaks the assumption of simplest form. Contradiction!</li>
    </ul>
  </div>
</div>

<p>So $\sqrt{2}$ is <strong>irrational</strong> — it is a real number but it cannot be any fraction. The legend says the Pythagorean who revealed this (Hippasus, around 5th century BCE) was thrown into the sea by his brotherhood, who found the discovery too disturbing. Whether this is true or not, the mathematical point is clear: rational numbers are not enough to fill the number line.</p>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-lightbulb"></i> What Are Irrational Numbers?</div>
  <p>An <strong>irrational number</strong> is any real number that <em>cannot</em> be written as a fraction $\frac{p}{q}$ where $p$ and $q$ are integers. In decimal form, irrational numbers go on forever <em>without any repeating pattern</em>.</p>
  <ul style="margin:10px 0 0;padding-left:20px;color:#333;">
    <li>$\sqrt{2} = 1.41421356\ldots$ — never ends, never repeats</li>
    <li>$\pi = 3.14159265\ldots$ — the ratio of a circle's circumference (total boundary length) to its diameter</li>
    <li>$e = 2.71828182\ldots$ — Euler's number, the base of natural logarithms, used to model growth and decay</li>
    <li>$\sqrt{3},\, \sqrt{5},\, \sqrt{7}$ — square roots of numbers that are not perfect squares</li>
  </ul>
  <p style="margin-top:10px;"><strong>Important:</strong> Not every square root is irrational. $\sqrt{4} = 2$ and $\sqrt{9} = 3$ are rational — always simplify before deciding!</p>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-history"></i></span> How the Number System Grew — A Historical Timeline</h2>

<p>This was not a single invention. It took thousands of years and contributions from many civilisations, each solving the problems left by the previous generation.</p>

<table class="summary-table">
  <thead>
    <tr>
      <th>Period</th>
      <th>Who</th>
      <th>Contribution</th>
      <th>Number System Reached</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>~3000 BCE</td>
      <td>Mesopotamia &amp; Egypt</td>
      <td>Counting objects; tally marks and early numerals</td>
      <td>Natural Numbers $\mathbb{N}$</td>
    </tr>
    <tr>
      <td>~500 BCE</td>
      <td>Ancient Greece</td>
      <td>Study of ratios and proportions in geometry</td>
      <td>Rational Numbers $\mathbb{Q}$</td>
    </tr>
    <tr>
      <td>~500 BCE</td>
      <td>Pythagoreans (Greece)</td>
      <td>Discovered $\sqrt{2}$ cannot be a fraction — the first known irrational number</td>
      <td>First irrational number found</td>
    </tr>
    <tr>
      <td>499 CE</td>
      <td>Aryabhata (India)</td>
      <td><em>Aryabhatiya</em> — decimal place-value system with zero as a working digit</td>
      <td>Whole Numbers $\mathbb{W}$ formalised</td>
    </tr>
    <tr>
      <td>628 CE</td>
      <td>Brahmagupta (India)</td>
      <td><em>Brahmasphutasiddhanta</em> — first systematic rules for arithmetic with zero and negative numbers</td>
      <td>Integers $\mathbb{Z}$ formalised</td>
    </tr>
    <tr>
      <td>1872 CE</td>
      <td>Richard Dedekind (Germany)</td>
      <td>Gave a rigorous (logically complete and precise) construction of real numbers using "Dedekind cuts"</td>
      <td>Real Numbers $\mathbb{R}$ defined</td>
    </tr>
    <tr>
      <td>1874 CE</td>
      <td>Georg Cantor (Germany)</td>
      <td>Proved that there are far more irrational numbers than rational numbers on the number line</td>
      <td>Full theory of $\mathbb{R}$ established</td>
    </tr>
  </tbody>
</table>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-pencil-alt"></i></span> Solved Examples</h2>

<div class="example-card">
  <div class="example-label">Example 1 — Classify Each Number</div>
  <div class="example-num">1</div>
  <p>For each number, state the <strong>smallest set</strong> it belongs to from $\mathbb{N}$, $\mathbb{W}$, $\mathbb{Z}$, $\mathbb{Q}$, or irrational.</p>
  <p style="margin-top:8px;">$7, \quad -3, \quad \dfrac{5}{4}, \quad \sqrt{5}, \quad 0, \quad -\dfrac{2}{7}, \quad \sqrt{9}, \quad 0.\overline{6}$</p>
  <div class="solution-block">
    <strong>Solution:</strong>
    <ul style="margin:8px 0 0;padding-left:20px;">
      <li>$7$ → <strong>Natural</strong> $\mathbb{N}$ — a positive whole counting number</li>
      <li>$0$ → <strong>Whole</strong> $\mathbb{W}$ — not a natural number, but whole</li>
      <li>$-3$ → <strong>Integer</strong> $\mathbb{Z}$ — negative, so not natural or whole</li>
      <li>$\frac{5}{4}$ → <strong>Rational</strong> $\mathbb{Q}$ — a fraction of two integers, equals $1.25$</li>
      <li>$-\frac{2}{7}$ → <strong>Rational</strong> $\mathbb{Q}$ — a negative fraction, still rational</li>
      <li>$\sqrt{9} = 3$ → <strong>Natural</strong> $\mathbb{N}$ — simplifies to 3; not irrational at all!</li>
      <li>$0.\overline{6} = \frac{2}{3}$ → <strong>Rational</strong> $\mathbb{Q}$ — repeating decimal equals a fraction</li>
      <li>$\sqrt{5}$ → <strong>Irrational</strong> — 5 is not a perfect square, so $\sqrt{5}$ cannot be written as a fraction $\blacksquare$</li>
    </ul>
  </div>
</div>

<div class="example-card">
  <div class="example-label">Example 2 — Prove that √2 is Irrational</div>
  <div class="example-num">2</div>
  <p>Prove that $\sqrt{2}$ is irrational — that is, it cannot be written as $\frac{p}{q}$ where $p$ and $q$ are integers.</p>
  <p style="font-size:0.85rem;color:#666;margin-top:4px;"><em>Reference: W. Rudin, Principles of Mathematical Analysis, 3rd ed. (McGraw-Hill, 1976), Example 1.1, p. 2</em></p>
  <div class="solution-block">
    <strong>Solution — Proof by Contradiction</strong> (we assume the opposite is true, then show it leads to an impossibility):
    <p><strong>Step 1.</strong> Suppose $\sqrt{2} = \dfrac{p}{q}$, where $p$ and $q$ are positive integers with no common factor (the fraction is already in its simplest, or <em>lowest</em>, form).</p>
    <p><strong>Step 2.</strong> Squaring both sides: $p^2 = 2q^2$. So $p^2$ is even. Since a perfect square is even only when its square root is even, $p$ itself must be even. Write $p = 2m$ for some integer $m$.</p>
    <p><strong>Step 3.</strong> Substitute $p = 2m$ back: $(2m)^2 = 2q^2 \Rightarrow 4m^2 = 2q^2 \Rightarrow q^2 = 2m^2$. So $q^2$ is also even, which means $q$ is also even.</p>
    <p><strong>Step 4.</strong> Now both $p$ and $q$ are even — meaning 2 divides both. But this directly contradicts our starting assumption that $\frac{p}{q}$ was in its simplest form.</p>
    <p><strong>Conclusion:</strong> Our assumption was wrong. No such fraction $\frac{p}{q}$ can equal $\sqrt{2}$. Therefore $\sqrt{2}$ is irrational. $\blacksquare$</p>
  </div>
</div>

<div class="example-card">
  <div class="example-label">Example 3 — Rational or Irrational?</div>
  <div class="example-num">3</div>
  <p>Decide whether each expression is rational or irrational, and give a brief reason.</p>
  <p style="margin-top:8px;">(a) $0.\overline{142857}$ &nbsp;&nbsp; (b) $\sqrt{2} + \sqrt{2}$ &nbsp;&nbsp; (c) $\sqrt{2} \times \sqrt{2}$ &nbsp;&nbsp; (d) $\pi - \pi$ &nbsp;&nbsp; (e) $2 + \sqrt{3}$</p>
  <div class="solution-block">
    <strong>Solution:</strong>
    <p>(a) $0.\overline{142857}$ — <strong>Rational.</strong> Any decimal with a repeating pattern is rational. In fact, $0.\overline{142857} = \dfrac{1}{7}$.</p>
    <p>(b) $\sqrt{2} + \sqrt{2} = 2\sqrt{2}$ — <strong>Irrational.</strong> An irrational number multiplied by a non-zero rational number (here, 2) stays irrational.</p>
    <p>(c) $\sqrt{2} \times \sqrt{2} = 2$ — <strong>Rational!</strong> This is the most important trap: the product (result of multiplication) of two irrational numbers can be rational. Never assume without checking.</p>
    <p>(d) $\pi - \pi = 0$ — <strong>Rational.</strong> Any number minus itself is zero, which is rational (it equals $\frac{0}{1}$).</p>
    <p>(e) $2 + \sqrt{3}$ — <strong>Irrational.</strong> Adding a rational to an irrational always gives an irrational. Here is why: if $2 + \sqrt{3}$ were rational, then $\sqrt{3} = (2 + \sqrt{3}) - 2$ would also be rational (since subtracting a rational from a rational gives a rational) — but we know $\sqrt{3}$ is not rational. Contradiction. $\blacksquare$</p>
  </div>
</div>

<div class="example-card">
  <div class="example-label">Example 4 — A Common Misconception</div>
  <div class="example-num">4</div>
  <p>A student says: <em>"Since $\frac{22}{7}$ is used as $\pi$ in calculations, $\pi$ must be a rational number."</em> Is the student right? Explain clearly.</p>
  <div class="solution-block">
    <strong>Solution:</strong>
    <p>The student is <strong>incorrect</strong>.</p>
    <p>$\frac{22}{7}$ is only an <em>approximation</em> (a close estimate, not the exact value) of $\pi$. In decimal form, $\frac{22}{7} = 3.142857142857\ldots$ — this repeats forever and is indeed rational. But $\pi = 3.14159265\ldots$ — this goes on forever <em>without any repeating pattern</em>, making it irrational.</p>
    <p>The two numbers match only in the first two decimal places. After that, they differ. Using $\frac{22}{7}$ in calculations is practical (easy to work with) and gives a good enough answer for most everyday problems. But it does not mean $\pi$ and $\frac{22}{7}$ are the same number.</p>
    <p>$\pi$ was proved to be irrational by the German mathematician Johann Heinrich Lambert in 1761. It is a real number, but not a rational one. $\blacksquare$</p>
  </div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> Key Points to Remember</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> Things Worth Remembering</div>
  <ul>
    <li><strong>The hierarchy is a chain:</strong> $\mathbb{N} \subset \mathbb{W} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$. Every natural number is also a whole number, an integer, a rational, and a real number.</li>
    <li><strong>Not every square root is irrational:</strong> $\sqrt{4} = 2$, $\sqrt{16} = 4$, $\sqrt{25} = 5$ are all rational. Only square roots of non-perfect-squares (like $\sqrt{2}$, $\sqrt{3}$, $\sqrt{5}$) are irrational.</li>
    <li><strong>A repeating decimal is always rational:</strong> $0.333\ldots = \frac{1}{3}$, $0.142857142857\ldots = \frac{1}{7}$. A pattern that repeats, no matter how long, means the number is rational.</li>
    <li><strong>Watch the product trap:</strong> $\sqrt{2} \times \sqrt{2} = 2$ is rational, even though both factors are irrational. The product of two irrationals is <em>not always</em> irrational.</li>
    <li><strong>$\frac{22}{7}$ is not $\pi$:</strong> It is only an approximation. $\pi$ is irrational, as proved by Lambert in 1761.</li>
    <li><strong>$e$ is also irrational:</strong> Euler's number $e \approx 2.718$, used in compound interest and natural growth, is irrational. This was confirmed by Hermite in 1873.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> Common Mistakes</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> Avoid These Errors</div>
  <ul>
    <li><strong>"All decimals are irrational":</strong> Not true. $0.5 = \frac{1}{2}$ is rational. Only non-terminating (never-ending), non-repeating (no fixed pattern) decimals are irrational.</li>
    <li><strong>"Every square root is irrational":</strong> $\sqrt{9} = 3 \in \mathbb{N}$. Always simplify the square root before deciding.</li>
    <li><strong>"Irrational + Irrational = Irrational":</strong> Not always. $\sqrt{2} + (-\sqrt{2}) = 0$, which is rational.</li>
    <li><strong>"Irrational × Irrational = Irrational":</strong> Not always. $\sqrt{3} \times \sqrt{3} = 3$, which is rational.</li>
    <li><strong>"$\frac{22}{7} = \pi$":</strong> This is only an approximation. $\pi$ is irrational and cannot equal any fraction exactly.</li>
    <li><strong>"$\mathbb{N}$ includes 0":</strong> In most mathematics courses (and in Rudin's <em>Principles of Mathematical Analysis</em>), $\mathbb{N} = \{1, 2, 3, \ldots\}$. Zero is a whole number, not a natural number, though conventions can vary by country.</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> Why Do Real Numbers Matter?</h2>

<div class="app-grid">
  <div class="app-card">
    <div class="app-icon">📐</div>
    <strong>Geometry</strong>
    <p>The diagonal of a unit square ($\sqrt{2}$) and the boundary-to-width ratio of a circle ($\pi$) are irrational — they simply cannot be measured exactly using only fractions.</p>
  </div>
  <div class="app-card">
    <div class="app-icon">⚙️</div>
    <strong>Engineering</strong>
    <p>Calculations involving angles, waves, and signals all use irrational numbers like $\pi$ and $\sqrt{2}$. Without real numbers, modern engineering would not exist.</p>
  </div>
  <div class="app-card">
    <div class="app-icon">📈</div>
    <strong>Finance</strong>
    <p>Compound interest and continuous growth use Euler's number $e \approx 2.718$, which is irrational. Every bank uses it, often without knowing it.</p>
  </div>
  <div class="app-card">
    <div class="app-icon">⚛️</div>
    <strong>Physics</strong>
    <p>Speed, temperature, and distance in nature are continuous (no jumps or gaps). Real numbers are the natural (fitting and correct) language for every physical quantity.</p>
  </div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> Summary — The Number System at a Glance</h2>

<table class="summary-table">
  <thead>
    <tr>
      <th>System</th>
      <th>Symbol</th>
      <th>Examples</th>
      <th>New Idea Introduced</th>
      <th>Problem It Solved</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Natural Numbers</td>
      <td>$\mathbb{N}$</td>
      <td>$1,\, 2,\, 3$</td>
      <td>Counting</td>
      <td>How many things are there?</td>
    </tr>
    <tr>
      <td>Whole Numbers</td>
      <td>$\mathbb{W}$</td>
      <td>$0,\, 1,\, 2$</td>
      <td>Zero</td>
      <td>How to represent "none"?</td>
    </tr>
    <tr>
      <td>Integers</td>
      <td>$\mathbb{Z}$</td>
      <td>$-3,\, 0,\, 5$</td>
      <td>Negative numbers</td>
      <td>What is $3 - 5$?</td>
    </tr>
    <tr>
      <td>Rational Numbers</td>
      <td>$\mathbb{Q}$</td>
      <td>$\frac{1}{2},\, -\frac{3}{4},\, 0.\overline{3}$</td>
      <td>Fractions and ratios</td>
      <td>What is $1 \div 2$?</td>
    </tr>
    <tr>
      <td>Irrational Numbers</td>
      <td>$\mathbb{Q}^c$</td>
      <td>$\sqrt{2},\, \pi,\, e$</td>
      <td>Non-fraction lengths</td>
      <td>What is the diagonal of a unit square?</td>
    </tr>
    <tr>
      <td><strong>Real Numbers</strong></td>
      <td>$\mathbb{R}$</td>
      <td>All of the above</td>
      <td>Gapless number line</td>
      <td>Every point on a line has a number</td>
    </tr>
  </tbody>
</table>

<div class="highlight-result">
  <p style="margin:0;font-size:1.1rem;font-weight:700;">$\mathbb{N} \subset \mathbb{W} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$</p>
  <p style="margin:8px 0 0;font-size:0.9rem;color:#4338ca;">Every number system is contained inside the next. Real numbers are the largest — they include every number that can be placed on a straight number line, with no gaps whatsoever.</p>
</div>

</div>


<!-- ═══════════════════════════════════════════════════════════
     PDF GENERATION — html2pdf.js  (client-side, no upload needed)
     The #pdf-content div is hidden on the page but becomes the
     source for the PDF when the button is clicked.
═══════════════════════════════════════════════════════════ -->

<!-- PDF styles — only applied inside the hidden pdf-content div -->
<style>
/* ── Download button ─────────────────────────────────── */
.pdf-section { text-align:center; margin:44px 0 28px; }
.pdf-btn {
  display:inline-flex; align-items:center; gap:14px;
  background:linear-gradient(135deg,#1e3c72,#7c3aed);
  color:white; text-decoration:none;
  padding:15px 34px; border-radius:50px; border:none; cursor:pointer;
  font-family:Georgia,serif; font-size:1rem; font-weight:700;
  box-shadow:0 6px 22px rgba(30,60,114,0.38);
  transition:transform .2s, box-shadow .2s;
}
.pdf-btn:hover { transform:translateY(-3px); box-shadow:0 10px 30px rgba(30,60,114,0.48); color:white; }
.pdf-btn .pi { font-size:1.45rem; }
.pdf-btn .pt { display:flex; flex-direction:column; text-align:left; line-height:1.3; }
.pdf-btn .pt span:first-child { font-size:1rem; }
.pdf-btn .pt span:last-child  { font-size:0.72rem; opacity:.82; font-weight:400; }
.pdf-generating { opacity:.65; pointer-events:none; }
/* ── PDF source div — hidden on page ────────────────── */
#pdf-content { visibility:hidden; position:absolute; left:-9999px; top:0; height:0; overflow:hidden; pointer-events:none; }

/* ── PDF internal styles ─────────────────────────────── */
.pdoc {
  font-family: 'Georgia', serif;
  font-size: 11pt;
  line-height: 1.7;
  color: #1a1a2e;
  width: 176mm;
  margin: 0 auto;
  padding: 0;
}
/* Hero */
.pdoc .p-hero {
  background: linear-gradient(135deg,#1e3c72 0%,#2a5298 55%,#7c3aed 100%);
  border-radius: 10px;
  padding: 22px 26px 18px;
  color: white;
  margin-bottom: 18px;
  position: relative;
  page-break-inside: avoid;
}
.pdoc .p-hero-bg {
  position:absolute; right:14px; top:-6px;
  font-size:72pt; color:rgba(255,255,255,0.07);
  font-family:serif; line-height:1;
}
.pdoc .p-hero h1 { margin:0 0 6px; font-size:17pt; font-weight:800; color:white; line-height:1.25; }
.pdoc .p-hero p  { margin:0 0 4px; font-size:10pt; opacity:.9; }
.pdoc .p-hero .p-meta { font-size:8.5pt; opacity:.75; margin-top:6px; }
/* Stats strip */
.pdoc .p-stats {
  display:flex; justify-content:space-around; flex-wrap:wrap;
  background:linear-gradient(135deg,#1e3c72,#7c3aed);
  border-radius:8px; padding:12px 10px; margin-bottom:18px;
  color:white; text-align:center; gap:8px;
  page-break-inside: avoid;
}
.pdoc .p-stats .ps { min-width:50px; }
.pdoc .p-stats .ps-num { font-size:16pt; font-weight:900; display:block; line-height:1.1; }
.pdoc .p-stats .ps-lbl { font-size:6.5pt; opacity:.8; text-transform:uppercase; letter-spacing:.4px; }
/* Section headers */
.pdoc .p-sec {
  font-size:13pt; font-weight:800; color:#1e3c72;
  margin:22px 0 10px; padding-bottom:6px;
  border-bottom:2.5px solid #1e3c72;
  page-break-after: avoid;
}
.pdoc .p-sub {
  font-size:10.5pt; font-weight:700; color:#2a5298;
  margin:14px 0 6px;
}
/* Body text */
.pdoc p { margin:0 0 7px; }
/* Pull quote */
.pdoc .p-quote {
  border-left:4px solid #7c3aed;
  background:#f5f3ff;
  padding:10px 14px;
  margin:12px 0;
  font-style:italic;
  color:#4c1d95;
  border-radius:0 8px 8px 0;
  font-size:10.5pt;
  page-break-inside:avoid;
}
/* Floor cards */
.pdoc .p-floor {
  display:flex; gap:12px; margin-bottom:10px;
  border:1px solid #e5e7eb; border-radius:8px;
  background:white; padding:12px 14px;
  page-break-inside:avoid;
}
.pdoc .p-floor-badge {
  width:34px; height:34px; border-radius:50%;
  display:flex; align-items:center; justify-content:center;
  font-weight:900; font-size:9pt; color:white; flex-shrink:0; margin-top:2px;
}
.pdoc .p-floor-badge.fn { background:linear-gradient(135deg,#1e3c72,#2a5298); }
.pdoc .p-floor-badge.fw { background:linear-gradient(135deg,#059669,#10b981); }
.pdoc .p-floor-badge.fz { background:linear-gradient(135deg,#7c3aed,#a855f7); }
.pdoc .p-floor-badge.fq { background:linear-gradient(135deg,#d97706,#f59e0b); }
.pdoc .p-floor-badge.fr { background:linear-gradient(135deg,#dc2626,#ff4b2b); }
.pdoc .p-floor-body { flex:1; }
.pdoc .p-floor-body h4 { margin:0 0 2px; font-size:10pt; font-weight:800; color:#1e3c72; }
.pdoc .p-floor-body .p-set { font-size:8.5pt; color:#7c3aed; font-family:monospace; font-weight:700; margin-bottom:4px; }
.pdoc .p-floor-body p { font-size:9.5pt; color:#333; margin:0 0 5px; }
.pdoc .p-badge-red {
  display:inline-block; background:#fff5f5; border:1px solid #fecaca;
  border-radius:4px; padding:2px 8px; font-size:8pt; color:#dc2626; font-weight:700;
}
.pdoc .p-badge-green {
  display:inline-block; background:#ecfdf5; border:1px solid #6ee7b7;
  border-radius:4px; padding:2px 8px; font-size:8pt; color:#059669; font-weight:700;
}
/* Two-column proof */
.pdoc .p-twocol { display:flex; gap:10px; margin:12px 0; page-break-inside:avoid; }
.pdoc .p-twocol .p-col { flex:1; border-radius:8px; padding:12px; font-size:9.5pt; }
.pdoc .p-twocol .p-col.blue  { background:#eff6ff; border:1.5px solid #93c5fd; }
.pdoc .p-twocol .p-col.green { background:#ecfdf5; border:1.5px solid #6ee7b7; }
.pdoc .p-twocol .p-col h4 { margin:0 0 6px; font-size:9.5pt; font-weight:700; }
.pdoc .p-twocol .p-col.blue h4  { color:#1e40af; }
.pdoc .p-twocol .p-col.green h4 { color:#065f46; }
.pdoc .p-twocol .p-col ul { margin:0; padding-left:16px; }
.pdoc .p-twocol .p-col li { margin-bottom:4px; }
/* Info box */
.pdoc .p-infobox {
  border-radius:8px; margin:12px 0; overflow:hidden;
  page-break-inside:avoid;
}
.pdoc .p-infobox-hd {
  padding:7px 14px; font-size:8pt; font-weight:700;
  text-transform:uppercase; letter-spacing:.5px; color:white;
}
.pdoc .p-infobox-body {
  padding:12px 14px; font-size:9.5pt;
}
.pdoc .p-infobox-body ul { margin:6px 0 0; padding-left:18px; }
.pdoc .p-infobox-body li { margin-bottom:4px; }
.pdoc .p-infobox.gold   .p-infobox-hd   { background:#d97706; }
.pdoc .p-infobox.gold   .p-infobox-body { background:#fffbeb; color:#78350f; }
/* Spotlight box */
.pdoc .p-spotlight {
  background:linear-gradient(135deg,#1e3c72,#2a5298);
  border-radius:8px; padding:14px 16px; color:white;
  display:flex; gap:12px; margin:10px 0;
  page-break-inside:avoid;
}
.pdoc .p-spotlight-icon { font-size:22pt; flex-shrink:0; }
.pdoc .p-spotlight h4 { margin:0 0 5px; font-size:10pt; color:#fbbf24; font-weight:800; }
.pdoc .p-spotlight p  { margin:0; font-size:9pt; color:#e2e8f0; line-height:1.6; }
/* Example cards */
.pdoc .p-example {
  border:1px solid #e5e7eb; border-radius:8px;
  margin:12px 0; overflow:hidden;
  page-break-inside:avoid;
}
.pdoc .p-ex-hd {
  padding:7px 14px; font-size:8.5pt; font-weight:700;
  text-transform:uppercase; letter-spacing:.5px; color:white;
}
.pdoc .p-ex-body { padding:12px 14px; background:white; }
.pdoc .p-ex-q { font-size:10pt; color:#1a1a2e; margin-bottom:8px; font-weight:600; }
.pdoc .p-ex-sol { background:#f0fdf4; border-left:3px solid #059669; padding:10px 12px; border-radius:0 6px 6px 0; font-size:9.5pt; color:#1a5c38; }
.pdoc .p-ex-sol strong { display:block; margin-bottom:4px; }
.pdoc .p-ex-sol ul { margin:4px 0; padding-left:18px; }
.pdoc .p-ex-sol li { margin-bottom:3px; }
.pdoc .p-ex-sol p  { margin:0 0 4px; }
/* Tip/Warning boxes */
.pdoc .p-tip {
  background:#fffbeb; border-left:4px solid #d97706;
  padding:10px 14px; margin:12px 0; border-radius:0 8px 8px 0;
  page-break-inside:avoid;
}
.pdoc .p-tip-hd   { font-size:8.5pt; font-weight:700; color:#92400e; text-transform:uppercase; letter-spacing:.4px; margin-bottom:7px; }
.pdoc .p-tip ul   { margin:0; padding-left:16px; color:#78350f; font-size:9.5pt; }
.pdoc .p-tip li   { margin-bottom:4px; }
.pdoc .p-warn {
  background:#fff5f5; border-left:4px solid #dc2626;
  padding:10px 14px; margin:12px 0; border-radius:0 8px 8px 0;
  page-break-inside:avoid;
}
.pdoc .p-warn-hd  { font-size:8.5pt; font-weight:700; color:#991b1b; text-transform:uppercase; letter-spacing:.4px; margin-bottom:7px; }
.pdoc .p-warn ul  { margin:0; padding-left:16px; color:#7f1d1d; font-size:9.5pt; }
.pdoc .p-warn li  { margin-bottom:4px; }
/* Timeline table */
.pdoc .p-table { width:100%; border-collapse:collapse; margin:12px 0; font-size:9pt; page-break-inside:avoid; }
.pdoc .p-table th { background:#1e3c72; color:white; padding:7px 8px; text-align:left; }
.pdoc .p-table td { padding:6px 8px; border-bottom:1px solid #e5e7eb; color:#333; vertical-align:top; }
.pdoc .p-table tr:nth-child(even) td { background:#f8faff; }
.pdoc .p-table td:first-child { font-style:italic; color:#1e3c72; }
/* App grid */
.pdoc .p-appgrid { display:flex; gap:8px; flex-wrap:wrap; margin:10px 0; }
.pdoc .p-app { flex:1; min-width:80px; background:white; border:1px solid #e5e7eb; border-radius:8px; padding:10px; text-align:center; font-size:9pt; }
.pdoc .p-app .p-app-icon { font-size:16pt; display:block; margin-bottom:4px; }
.pdoc .p-app strong { color:#1e3c72; display:block; margin-bottom:3px; font-size:9pt; }
/* Summary table */
.pdoc .p-sum-table { width:100%; border-collapse:collapse; margin:12px 0; font-size:9pt; }
.pdoc .p-sum-table th { background:linear-gradient(135deg,#1e3c72,#7c3aed); color:white; padding:7px 8px; text-align:left; }
.pdoc .p-sum-table td { padding:6px 8px; border-bottom:1px solid #e5e7eb; color:#333; vertical-align:middle; }
.pdoc .p-sum-table tr:nth-child(even) td { background:#f8faff; }
.pdoc .p-sum-table tr:last-child td { background:#e0e7ff; font-weight:700; color:#1e3c72; }
.pdoc .p-sum-table td:first-child { font-weight:700; color:#1e3c72; }
/* Highlight result */
.pdoc .p-highlight {
  background:linear-gradient(135deg,#eff6ff,#e0e7ff);
  border:2px solid #818cf8; border-radius:10px;
  padding:14px 16px; text-align:center; margin:14px 0;
  page-break-inside:avoid;
}
.pdoc .p-highlight .ph-main { font-size:13pt; font-weight:800; color:#1e3c72; margin-bottom:5px; }
.pdoc .p-highlight .ph-sub  { font-size:9pt; color:#4338ca; }
/* Watermark (drawn by JS, not CSS) */
.pdoc .p-watermark-text { display:none; }
/* Social footer */
.pdoc .p-footer {
  margin-top:20px; padding-top:12px;
  border-top:1.5px solid #e5e7eb; text-align:center;
  page-break-inside:avoid;
}
.pdoc .p-footer .pf-title { font-size:10.5pt; font-weight:800; color:#1e3c72; margin-bottom:6px; }
.pdoc .p-footer .pf-links { display:flex; justify-content:center; gap:18px; flex-wrap:wrap; margin-bottom:6px; }
.pdoc .p-footer .pf-links a { font-size:9pt; color:#2a5298; font-weight:600; text-decoration:none; }
.pdoc .p-footer .pf-copy { font-size:8pt; color:#6b7280; }
/* Ref note */
.pdoc .p-ref { font-style:italic; font-size:8.5pt; color:#6b7280; margin-top:5px; }
</style>

<!-- ═══ HIDDEN PDF SOURCE CONTENT ════════════════════════ -->
<div id="pdf-content">
<div class="pdoc">

  <!-- Hero -->
  <div class="p-hero">
    <div class="p-hero-bg">&#8477;</div>
    <h1>The Infinite Architecture:<br>Foundations of Real Numbers</h1>
    <p>Understanding the Number System — from Ancient Counting to &#8477;</p>
    <div class="p-meta">Author: Dr. Praveendra Singh &nbsp;|&nbsp; Fractal Frontier Maths &nbsp;|&nbsp; B.Sc. / M.Sc. Mathematics &nbsp;|&nbsp; Real Analysis — Unit 1</div>
  </div>

  <!-- Stats strip -->
  <div class="p-stats">
    <div class="ps"><span class="ps-num">5</span><span class="ps-lbl">Number Systems</span></div>
    <div class="ps"><span class="ps-num">3000+</span><span class="ps-lbl">Years of History</span></div>
    <div class="ps"><span class="ps-num">4</span><span class="ps-lbl">Solved Examples</span></div>
    <div class="ps"><span class="ps-num">&#9733;&#9733;&#9734;</span><span class="ps-lbl">Beginner Friendly</span></div>
    <div class="ps"><span class="ps-num">&#8477;</span><span class="ps-lbl">The Final System</span></div>
  </div>

  <!-- Section 1 -->
  <div class="p-sec">The Skyscraper Analogy</div>
  <p>Have you ever stopped to ask: <em>what is a number, really?</em> For most people, numbers are just tools — for bank balances, recipes, and distances. But to a mathematician, the number system is a magnificent <strong>skyscraper</strong> built floor by floor over three thousand years of human thought.</p>
  <div class="p-quote">"Every time humanity hit a wall — a problem that couldn't be solved — we didn't give up. We built a new floor."</div>
  <p>The important thing is that <strong>each new type of number was born out of a real need</strong> — a problem the existing numbers simply could not solve. What began as counting sheep eventually grew into the most powerful mathematical system we have: the <strong>Real Number System (&#8477;)</strong>.</p>

  <!-- Section 2: Five Floors -->
  <div class="p-sec">The Five Floors: A Journey Through History</div>

  <!-- Floor 1 -->
  <div class="p-floor">
    <div class="p-floor-badge fn">&#8469;</div>
    <div class="p-floor-body">
      <h4>Floor 1 — Natural Numbers &#8469; = {1, 2, 3, 4, &hellip;}</h4>
      <div class="p-set">&#8469; = { 1, 2, 3, 4, &hellip; }</div>
      <p>The first act of mathematics: <strong>counting</strong>. Ancient people counted cattle, days, and harvests. You can add and multiply naturals and always stay within the system. But subtraction quickly causes trouble.</p>
      <span class="p-badge-red">&#10060; Gap: What is 3 &minus; 5? No natural number answer. We need a new floor.</span>
    </div>
  </div>

  <!-- Floor 2 -->
  <div class="p-floor">
    <div class="p-floor-badge fw">&#120142;</div>
    <div class="p-floor-body">
      <h4>Floor 2 — Whole Numbers &#120142; = {0, 1, 2, 3, &hellip;}</h4>
      <div class="p-set">&#120142; = { 0, 1, 2, 3, &hellip; }</div>
      <p>We add <strong>zero</strong>. Zero is not just "nothing" — it holds a place and makes our entire decimal system work.</p>
      <div class="p-spotlight">
        <div class="p-spotlight-icon">&#127963;</div>
        <div>
          <h4>Aryabhata and the Power of Zero — Aryabhatiya (499 CE)</h4>
          <p>Aryabhata used a decimal place-value system that made zero a proper working digit, not merely a blank space. His system made it possible to tell apart 42, 402, and 420 — impossible in Roman numerals. This contribution, spread via Arabic translations, transformed arithmetic worldwide.</p>
        </div>
      </div>
      <span class="p-badge-red">&#10060; Gap: 5 &minus; 8 = ? Still no answer. We need numbers below zero.</span>
    </div>
  </div>

  <!-- Floor 3 -->
  <div class="p-floor">
    <div class="p-floor-badge fz">&#8484;</div>
    <div class="p-floor-body">
      <h4>Floor 3 — Integers &#8484; = {&hellip;, &minus;2, &minus;1, 0, 1, 2, &hellip;}</h4>
      <div class="p-set">&#8484; = { &hellip;, &minus;3, &minus;2, &minus;1, 0, 1, 2, 3, &hellip; }</div>
      <p><strong>Negative numbers</strong> extend the number line in both directions. Now subtraction always has an answer. &#8484; comes from German <em>Zahlen</em> (numbers). Brahmagupta's <em>Brahmasphutasiddhanta</em> (628 CE) gave the first clear rules for arithmetic with negatives and zero.</p>
      <span class="p-badge-red">&#10060; Gap: 1 &divide; 2 = ? No integer answer. We need fractions.</span>
    </div>
  </div>

  <!-- Floor 4 -->
  <div class="p-floor">
    <div class="p-floor-badge fq">&#8474;</div>
    <div class="p-floor-body">
      <h4>Floor 4 — Rational Numbers &#8474; = { p/q : p, q &isin; &#8484;, q &ne; 0 }</h4>
      <div class="p-set">&#8474; = { p/q : p, q integers, q &ne; 0 }</div>
      <p>From Latin <em>ratio</em>. All fractions — every terminating or repeating decimal is rational. With &#8474; we can add, subtract, multiply, and divide (except by 0) and always stay within the system. Ancient Greeks were satisfied here — until a simple square broke everything.</p>
      <span class="p-badge-red">&#10060; Gap: No fraction squares to exactly 2. The number line has holes!</span>
    </div>
  </div>

  <!-- Floor 5 -->
  <div class="p-floor">
    <div class="p-floor-badge fr">&#8477;</div>
    <div class="p-floor-body">
      <h4>Floor 5 — Real Numbers &#8477; = &#8474; &cup; &#8474;<sup>c</sup> (Rationals + Irrationals)</h4>
      <div class="p-set">&#8477; = &#8474; &cup; &#8474;<sup>c</sup></div>
      <p>Every single point on the number line is a real number. <strong>No gaps. No holes.</strong> &radic;2, &pi;, <em>e</em> are all real. This is the number system used in calculus, physics, and all of higher mathematics.</p>
      <span class="p-badge-green">&#10003; Complete: Every number that can be placed on a line is a real number.</span>
    </div>
  </div>

  <!-- Section 3: Crisis -->
  <div class="p-sec">The Crisis That Created Irrational Numbers</div>
  <p>The ancient Greek Pythagorean school had a firm belief: <em>every quantity in nature can be written as a fraction</em>. Then one of their own made a discovery that shook the foundations of their philosophy.</p>

  <div class="p-twocol">
    <div class="p-col blue">
      <h4>&#128208; The Problem: A Simple Square</h4>
      <ul>
        <li>Draw a square with each side exactly 1 unit long</li>
        <li>By the Pythagorean theorem, the diagonal = &radic;2</li>
        <li>Pythagoreans asked: can &radic;2 be written as p/q?</li>
        <li>They were certain the answer was yes — and tried to prove it.</li>
      </ul>
    </div>
    <div class="p-col green">
      <h4>&#10007; The Shock: It Cannot Be a Fraction</h4>
      <ul>
        <li>Assume &radic;2 = p/q in simplest form (no shared factors)</li>
        <li>p&sup2; = 2q&sup2; &rArr; p is even &rArr; write p = 2m</li>
        <li>Then 4m&sup2; = 2q&sup2; &rArr; q is also even</li>
        <li>Both even &rArr; share factor 2 &rArr; contradicts simplest form!</li>
      </ul>
    </div>
  </div>

  <p>So &radic;2 is <strong>irrational</strong> — a real number that cannot be any fraction. The legend says Hippasus (~5th century BCE), who revealed this, was thrown into the sea. Mathematical point: rational numbers alone cannot fill the number line.</p>

  <!-- Irrational info box -->
  <div class="p-infobox gold">
    <div class="p-infobox-hd">&#128161; What Are Irrational Numbers?</div>
    <div class="p-infobox-body">
      <p>An <strong>irrational number</strong> is any real number that <em>cannot</em> be written as p/q where p and q are integers. In decimal form: they go on forever <em>without any repeating pattern</em>.</p>
      <ul>
        <li>&radic;2 = 1.41421356&hellip; &nbsp; (never ends, never repeats)</li>
        <li>&pi; = 3.14159265&hellip; &nbsp; (ratio of circle's circumference to its diameter)</li>
        <li><em>e</em> = 2.71828182&hellip; &nbsp; (Euler's number, used in growth and decay)</li>
        <li>&radic;3, &radic;5, &radic;7 &nbsp; (square roots of non-perfect-squares)</li>
      </ul>
      <p><strong>Important:</strong> &radic;4 = 2 and &radic;9 = 3 are rational. Always simplify before deciding!</p>
    </div>
  </div>

  <!-- Section 4: Timeline -->
  <div class="p-sec">Historical Timeline — How the Number System Grew</div>
  <p>This took thousands of years and contributions from many civilisations — each generation solving the problems left by the previous one.</p>

  <table class="p-table">
    <thead><tr><th>Period</th><th>Who</th><th>Contribution</th><th>System Reached</th></tr></thead>
    <tbody>
      <tr><td>~3000 BCE</td><td>Mesopotamia &amp; Egypt</td><td>Counting; tally marks and early numerals</td><td>&#8469; Natural Numbers</td></tr>
      <tr><td>~500 BCE</td><td>Ancient Greece</td><td>Study of ratios and proportions in geometry</td><td>&#8474; Rational Numbers</td></tr>
      <tr><td>~500 BCE</td><td>Pythagoreans (Greece)</td><td>&radic;2 cannot be a fraction — first known irrational</td><td>Need for irrationals</td></tr>
      <tr><td>499 CE</td><td>Aryabhata (India)</td><td><em>Aryabhatiya</em> — decimal place-value, zero as working digit</td><td>&#120142; Whole Numbers</td></tr>
      <tr><td>628 CE</td><td>Brahmagupta (India)</td><td><em>Brahmasphutasiddhanta</em> — rules for zero and negatives</td><td>&#8484; Integers</td></tr>
      <tr><td>1872 CE</td><td>Dedekind (Germany)</td><td>Rigorous (logically complete) construction via Dedekind cuts</td><td>&#8477; Reals defined</td></tr>
      <tr><td>1874 CE</td><td>Cantor (Germany)</td><td>Proved irrationals far outnumber rationals on the line</td><td>Full theory of &#8477;</td></tr>
    </tbody>
  </table>

  <!-- Section 5: Examples -->
  <div class="p-sec">Solved Examples</div>

  <!-- Example 1 -->
  <div class="p-example">
    <div class="p-ex-hd" style="background:#1e3c72;">EXAMPLE 1 — Classify Each Number</div>
    <div class="p-ex-body">
      <div class="p-ex-q">For each number, state the smallest set it belongs to (&#8469;, &#120142;, &#8484;, &#8474;, or irrational):<br>7 &nbsp; &minus;3 &nbsp; 5/4 &nbsp; &radic;5 &nbsp; 0 &nbsp; &minus;2/7 &nbsp; &radic;9 &nbsp; 0.666&hellip;</div>
      <div class="p-ex-sol">
        <strong>Solution:</strong>
        <ul>
          <li>7 &rarr; <strong>Natural &#8469;</strong> (positive counting number)</li>
          <li>0 &rarr; <strong>Whole &#120142;</strong> (not natural, but whole)</li>
          <li>&minus;3 &rarr; <strong>Integer &#8484;</strong> (negative)</li>
          <li>5/4 &rarr; <strong>Rational &#8474;</strong> (fraction of integers = 1.25)</li>
          <li>&minus;2/7 &rarr; <strong>Rational &#8474;</strong> (negative fraction)</li>
          <li>&radic;9 = 3 &rarr; <strong>Natural &#8469;</strong> (simplifies to 3 — rational!)</li>
          <li>0.666&hellip; = 2/3 &rarr; <strong>Rational &#8474;</strong> (repeating decimal = fraction)</li>
          <li>&radic;5 &rarr; <strong>Irrational</strong> (5 is not a perfect square) &#9632;</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- Example 2 -->
  <div class="p-example">
    <div class="p-ex-hd" style="background:#7c3aed;">EXAMPLE 2 — Prove that &radic;2 is Irrational</div>
    <div class="p-ex-body">
      <div class="p-ex-q">Prove that &radic;2 is irrational — it cannot be written as p/q where p and q are integers.</div>
      <div class="p-ex-sol">
        <strong>Solution — Proof by Contradiction:</strong>
        <p><strong>Step 1.</strong> Suppose &radic;2 = p/q, where p, q are positive integers with no common factor (simplest form).</p>
        <p><strong>Step 2.</strong> Squaring: p&sup2; = 2q&sup2;. So p&sup2; is even &rArr; p is even. Write p = 2m.</p>
        <p><strong>Step 3.</strong> Substituting: (2m)&sup2; = 2q&sup2; &rArr; 4m&sup2; = 2q&sup2; &rArr; q&sup2; = 2m&sup2;. So q is also even.</p>
        <p><strong>Step 4.</strong> Both p and q are even — they share factor 2. This contradicts our assumption of simplest form.</p>
        <p><strong>Conclusion:</strong> No fraction p/q can equal &radic;2. Therefore &radic;2 is irrational. &#9632;</p>
        <p class="p-ref">Reference: W. Rudin, Principles of Mathematical Analysis, 3rd ed. (McGraw-Hill, 1976), Example 1.1, p. 2</p>
      </div>
    </div>
  </div>

  <!-- Example 3 -->
  <div class="p-example">
    <div class="p-ex-hd" style="background:#d97706;">EXAMPLE 3 — Rational or Irrational?</div>
    <div class="p-ex-body">
      <div class="p-ex-q">Decide whether each is rational or irrational, with a brief reason:<br>(a) 0.142857142857&hellip; &nbsp; (b) &radic;2 + &radic;2 &nbsp; (c) &radic;2 &times; &radic;2 &nbsp; (d) &pi; &minus; &pi; &nbsp; (e) 2 + &radic;3</div>
      <div class="p-ex-sol">
        <strong>Solution:</strong>
        <p><strong>(a)</strong> 0.142857&hellip; = 1/7 &rarr; <strong>Rational.</strong> Any repeating decimal is rational.</p>
        <p><strong>(b)</strong> &radic;2 + &radic;2 = 2&radic;2 &rarr; <strong>Irrational.</strong> Irrational &times; non-zero rational stays irrational.</p>
        <p><strong>(c)</strong> &radic;2 &times; &radic;2 = 2 &rarr; <strong>Rational!</strong> Key trap — product of two irrationals CAN be rational.</p>
        <p><strong>(d)</strong> &pi; &minus; &pi; = 0 &rarr; <strong>Rational.</strong> Any number minus itself = 0 = 0/1.</p>
        <p><strong>(e)</strong> 2 + &radic;3 &rarr; <strong>Irrational.</strong> If it were rational r, then &radic;3 = r &minus; 2 would be rational — contradiction. &#9632;</p>
      </div>
    </div>
  </div>

  <!-- Example 4 -->
  <div class="p-example">
    <div class="p-ex-hd" style="background:#dc2626;">EXAMPLE 4 — A Common Misconception about &pi;</div>
    <div class="p-ex-body">
      <div class="p-ex-q">A student says: "Since 22/7 is used for &pi; in calculations, &pi; must be rational." Is the student correct?</div>
      <div class="p-ex-sol">
        <strong>Solution:</strong> The student is <strong>incorrect.</strong>
        <p>22/7 = 3.142857142857&hellip; (repeating, hence rational) is only an <em>approximation</em> of &pi;. The actual value &pi; = 3.14159265&hellip; never repeats and never ends — making it irrational.</p>
        <p>The two numbers match only in the first two decimal places. Using 22/7 in calculations is practical but does not make &pi; rational.</p>
        <p>&pi; was proved irrational by Johann Heinrich Lambert in 1761. &#9632;</p>
      </div>
    </div>
  </div>

  <!-- Section 6: Key Points -->
  <div class="p-sec">Key Points to Remember</div>
  <div class="p-tip">
    <div class="p-tip-hd">&#128161; Things Worth Remembering</div>
    <ul>
      <li><strong>The hierarchy:</strong> &#8469; &sub; &#120142; &sub; &#8484; &sub; &#8474; &sub; &#8477;. Every natural number is also whole, integer, rational, and real.</li>
      <li><strong>Not every square root is irrational:</strong> &radic;4 = 2, &radic;16 = 4, &radic;25 = 5 are rational. Only roots of non-perfect-squares are irrational.</li>
      <li><strong>Repeating decimal = rational:</strong> 0.333&hellip; = 1/3, &nbsp; 0.142857&hellip; = 1/7.</li>
      <li><strong>Product trap:</strong> &radic;2 &times; &radic;2 = 2 is rational. Product of two irrationals is NOT always irrational.</li>
      <li><strong>22/7 is not &pi;:</strong> Only an approximation. &pi; is irrational — proved by Lambert, 1761.</li>
      <li><strong><em>e</em> is also irrational:</strong> Euler's number <em>e</em> &asymp; 2.718 is irrational — proved by Hermite, 1873.</li>
    </ul>
  </div>

  <!-- Section 7: Mistakes -->
  <div class="p-sec">Common Mistakes</div>
  <div class="p-warn">
    <div class="p-warn-hd">&#9888; Avoid These Errors</div>
    <ul>
      <li><strong>"All decimals are irrational":</strong> 0.5 = 1/2 is rational. Only non-terminating, non-repeating decimals are irrational.</li>
      <li><strong>"Every square root is irrational":</strong> &radic;9 = 3 &isin; &#8469;. Always simplify before deciding.</li>
      <li><strong>"Irrational + Irrational = Irrational":</strong> &radic;2 + (&minus;&radic;2) = 0, which is rational.</li>
      <li><strong>"Irrational &times; Irrational = Irrational":</strong> &radic;3 &times; &radic;3 = 3, which is rational.</li>
      <li><strong>"22/7 = &pi;":</strong> Only an approximation. &pi; is irrational and equals no fraction exactly.</li>
      <li><strong>"&#8469; includes 0":</strong> Most courses define &#8469; = {1, 2, 3, &hellip;}. Zero is whole, not natural.</li>
    </ul>
  </div>

  <!-- Section 8: Applications -->
  <div class="p-sec">Why Do Real Numbers Matter?</div>
  <div class="p-appgrid">
    <div class="p-app"><span class="p-app-icon">&#128208;</span><strong>Geometry</strong><p>The diagonal of a unit square (&radic;2) and circle ratio (&pi;) are irrational — exact measurement needs &#8477;.</p></div>
    <div class="p-app"><span class="p-app-icon">&#9881;&#65039;</span><strong>Engineering</strong><p>Angles, waves, signals all use &pi; and &radic;2. Without &#8477;, modern engineering is impossible.</p></div>
    <div class="p-app"><span class="p-app-icon">&#128200;</span><strong>Finance</strong><p>Compound interest uses <em>e</em> &asymp; 2.718. Every bank uses it.</p></div>
    <div class="p-app"><span class="p-app-icon">&#9883;&#65039;</span><strong>Physics</strong><p>Speed, temperature, distance are continuous. &#8477; is the natural language for physical quantities.</p></div>
  </div>

  <!-- Section 9: Summary Table -->
  <div class="p-sec">Summary — The Number System at a Glance</div>
  <table class="p-sum-table">
    <thead><tr><th>System</th><th>Symbol</th><th>Examples</th><th>New Idea</th><th>Problem Solved</th></tr></thead>
    <tbody>
      <tr><td>Natural</td><td>&#8469;</td><td>1, 2, 3</td><td>Counting</td><td>How many things?</td></tr>
      <tr><td>Whole</td><td>&#120142;</td><td>0, 1, 2</td><td>Zero</td><td>How to show "none"?</td></tr>
      <tr><td>Integers</td><td>&#8484;</td><td>&minus;3, 0, 5</td><td>Negatives</td><td>What is 3 &minus; 5?</td></tr>
      <tr><td>Rational</td><td>&#8474;</td><td>1/2, &minus;3/4, 0.3&#773;</td><td>Fractions</td><td>What is 1 &divide; 2?</td></tr>
      <tr><td>Irrational</td><td>&#8474;<sup>c</sup></td><td>&radic;2, &pi;, <em>e</em></td><td>Non-fraction lengths</td><td>Diagonal of unit square?</td></tr>
      <tr><td>Real Numbers</td><td>&#8477;</td><td>All of the above</td><td>Gapless line</td><td>Every point has a number</td></tr>
    </tbody>
  </table>

  <div class="p-highlight">
    <div class="ph-main">&#8469; &sub; &#120142; &sub; &#8484; &sub; &#8474; &sub; &#8477;</div>
    <div class="ph-sub">Every number system is contained inside the next. Real numbers include every number that can be placed on a straight line.</div>
  </div>

  <!-- Footer -->
  <div class="p-footer">
    <div class="pf-title">Fractal Frontier Maths &nbsp;&bull;&nbsp; Empowering students in Real Analysis, Topology, and beyond</div>
    <div class="pf-links">
      <a href="https://drpraveendra.github.io">&#127760; drpraveendra.github.io</a>
      <a href="https://t.me/fractalfrontiermaths">&#9992; t.me/fractalfrontiermaths</a>
      <a href="https://www.youtube.com/@FractalFrontierMaths">&#9654; YouTube: FractalFrontierMaths</a>
      <a href="https://www.instagram.com/mathsworld007">&#128247; Instagram: mathsworld007</a>
    </div>
    <div class="pf-copy">&copy; 2026 Fractal Frontier Maths &nbsp;&bull;&nbsp; Dr. Praveendra Singh, Govt. College Kherwara, Rajasthan</div>
  </div>

</div><!-- .pdoc -->
</div><!-- #pdf-content -->

<!-- ═══ DOWNLOAD BUTTON ═══════════════════════════════════ -->
<style>
.pdf-section { text-align:center; margin:44px 0 28px; }
.pdf-btn {
  display:inline-flex; align-items:center; gap:14px;
  background:linear-gradient(135deg,#1e3c72,#7c3aed);
  color:white; border:none; cursor:pointer;
  padding:15px 34px; border-radius:50px;
  font-family:Georgia,serif; font-size:1rem; font-weight:700;
  box-shadow:0 6px 22px rgba(30,60,114,0.38);
  transition:transform .2s, box-shadow .2s;
}
.pdf-btn:hover { transform:translateY(-3px); box-shadow:0 10px 30px rgba(30,60,114,0.48); color:white; }
.pdf-btn.generating { opacity:.65; pointer-events:none; }
.pdf-btn .pi { font-size:1.45rem; }
.pdf-btn .pt { display:flex; flex-direction:column; text-align:left; line-height:1.3; }
.pdf-btn .pt .pt1 { font-size:1rem; }
.pdf-btn .pt .pt2 { font-size:0.72rem; opacity:.82; font-weight:400; }
</style>

<div class="pdf-section">
  <button class="pdf-btn" id="pdfDownloadBtn" onclick="generatePDF()">
    <span class="pi">📥</span>
    <span class="pt">
      <span class="pt1">Download PDF Notes</span>
      <span class="pt2">Foundations of Real Numbers — Fractal Frontier Maths</span>
    </span>
  </button>
</div>

<!-- html2pdf.js from CDN -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>

<script>
function generatePDF() {
  var btn = document.getElementById('pdfDownloadBtn');
  btn.classList.add('generating');
  btn.querySelector('.pt1').textContent = 'Generating PDF…';

  var source = document.getElementById('pdf-content');

  // Clone the source so we never touch the original hidden div
  var clone = source.cloneNode(true);
  clone.removeAttribute('id');

  // Create a full-screen overlay — html2canvas MUST be able to see the element
  var overlay = document.createElement('div');
  overlay.style.cssText = [
    'position:fixed',
    'top:0','left:0',
    'width:210mm',
    'min-height:100vh',
    'background:#fff',
    'z-index:99999',
    'overflow:visible',
    'padding:0',
    'margin:0',
    'box-sizing:border-box'
  ].join(';');

  overlay.appendChild(clone);
  document.body.appendChild(overlay);

  // Wait two animation frames so browser fully paints before capture
  requestAnimationFrame(function() {
    requestAnimationFrame(function() {

      var opt = {
        margin:      [12, 14, 16, 14],
        filename:    'foundations-real-numbers-fractalfrontiermaths.pdf',
        image:       { type: 'jpeg', quality: 0.97 },
        html2canvas: {
          scale: 2,
          useCORS: true,
          allowTaint: true,
          letterRendering: true,
          logging: false,
          backgroundColor: '#ffffff',
          windowWidth: 794,
          scrollX: 0,
          scrollY: 0
        },
        jsPDF: {
          unit: 'mm',
          format: 'a4',
          orientation: 'portrait',
          compress: true
        },
        pagebreak: { mode: ['css', 'legacy'] }
      };

      html2pdf()
        .set(opt)
        .from(clone)
        .toPdf()
        .get('pdf')
        .then(function(pdf) {
          var totalPages = pdf.internal.getNumberOfPages();
          for (var i = 1; i <= totalPages; i++) {
            pdf.setPage(i);
            var pw = pdf.internal.pageSize.getWidth();
            var ph = pdf.internal.pageSize.getHeight();

            // Diagonal watermark
            pdf.saveGraphicsState();
            pdf.setGState(new pdf.GState({ opacity: 0.07 }));
            pdf.setFont('helvetica', 'bold');
            pdf.setFontSize(28);
            pdf.setTextColor(30, 60, 114);
            pdf.text('Fractal Frontier Maths', pw / 2, ph / 2, {
              align: 'center', angle: 45
            });
            pdf.restoreGraphicsState();

            // Footer separator line
            pdf.setDrawColor(220, 220, 220);
            pdf.setLineWidth(0.3);
            pdf.line(14, ph - 11, pw - 14, ph - 11);

            // Footer text
            pdf.setFont('helvetica', 'normal');
            pdf.setFontSize(7);
            pdf.setTextColor(120, 120, 120);
            pdf.text('drpraveendra.github.io  |  Fractal Frontier Maths', 14, ph - 7.5);
            pdf.text('Page ' + i + ' of ' + totalPages, pw - 14, ph - 7.5, { align: 'right' });
          }
        })
        .save()
        .then(function() {
          document.body.removeChild(overlay);
          btn.classList.remove('generating');
          btn.querySelector('.pt1').textContent = 'Download PDF Notes';
        })
        .catch(function(err) {
          console.error('PDF error:', err);
          document.body.removeChild(overlay);
          btn.classList.remove('generating');
          btn.querySelector('.pt1').textContent = 'Download PDF Notes';
        });

    }); // end second rAF
  }); // end first rAF
}
</script>
