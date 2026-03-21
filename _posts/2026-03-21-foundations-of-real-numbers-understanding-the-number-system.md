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


<!-- ═══════════════════════════════════════════════════
     PDF DOWNLOAD — pre-built academic PDF embedded as
     base64 data URI. No server, no upload needed.
     Click → instant client-side download.
═══════════════════════════════════════════════════ -->
<style>
.pdf-section {
  text-align: center;
  margin: 44px 0 28px;
}
.pdf-btn {
  display: inline-flex;
  align-items: center;
  gap: 14px;
  background: linear-gradient(135deg, #1B2A4A, #2A5298);
  color: white;
  border: none;
  cursor: pointer;
  padding: 15px 36px;
  border-radius: 6px;
  font-family: Georgia, serif;
  font-size: 1rem;
  font-weight: 700;
  box-shadow: 0 4px 18px rgba(27,42,74,0.40);
  transition: transform .2s, box-shadow .2s;
  text-decoration: none;
}
.pdf-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 26px rgba(27,42,74,0.50);
  color: white;
  text-decoration: none;
}
.pdf-btn .pi { font-size: 1.5rem; }
.pdf-btn .pt {
  display: flex;
  flex-direction: column;
  text-align: left;
  line-height: 1.35;
}
.pdf-btn .pt1 { font-size: 1rem; }
.pdf-btn .pt2 {
  font-size: 0.72rem;
  opacity: 0.82;
  font-weight: 400;
  font-family: Georgia, serif;
}
</style>

<div class="pdf-section">
  <a class="pdf-btn"
     href="data:application/pdf;base64,JVBERi0xLjQKJZOMi54gUmVwb3J0TGFiIEdlbmVyYXRlZCBQREYgZG9jdW1lbnQgKG9wZW5zb3VyY2UpCjEgMCBvYmoKPDwKL0YxIDIgMCBSIC9GMiAzIDAgUiAvRjMgNCAwIFIgL0Y0IDUgMCBSIC9GNSA2IDAgUiAvRjYgNyAwIFIgCiAgL0Y3IDggMCBSIC9GOCA5IDAgUgo+PgplbmRvYmoKMiAwIG9iago8PAovQmFzZUZvbnQgL0hlbHZldGljYSAvRW5jb2RpbmcgL1dpbkFuc2lFbmNvZGluZyAvTmFtZSAvRjEgL1N1YnR5cGUgL1R5cGUxIC9UeXBlIC9Gb250Cj4+CmVuZG9iagozIDAgb2JqCjw8Ci9CYXNlRm9udCAvSGVsdmV0aWNhLUJvbGQgL0VuY29kaW5nIC9XaW5BbnNpRW5jb2RpbmcgL05hbWUgL0YyIC9TdWJ0eXBlIC9UeXBlMSAvVHlwZSAvRm9udAo+PgplbmRvYmoKNCAwIG9iago8PAovQmFzZUZvbnQgL1RpbWVzLUJvbGQgL0VuY29kaW5nIC9XaW5BbnNpRW5jb2RpbmcgL05hbWUgL0YzIC9TdWJ0eXBlIC9UeXBlMSAvVHlwZSAvRm9udAo+PgplbmRvYmoKNSAwIG9iago8PAovQmFzZUZvbnQgL1RpbWVzLUl0YWxpYyAvRW5jb2RpbmcgL1dpbkFuc2lFbmNvZGluZyAvTmFtZSAvRjQgL1N1YnR5cGUgL1R5cGUxIC9UeXBlIC9Gb250Cj4+CmVuZG9iago2IDAgb2JqCjw8Ci9CYXNlRm9udCAvVGltZXMtUm9tYW4gL0VuY29kaW5nIC9XaW5BbnNpRW5jb2RpbmcgL05hbWUgL0Y1IC9TdWJ0eXBlIC9UeXBlMSAvVHlwZSAvRm9udAo+PgplbmRvYmoKNyAwIG9iago8PAovQmFzZUZvbnQgL1phcGZEaW5nYmF0cyAvTmFtZSAvRjYgL1N1YnR5cGUgL1R5cGUxIC9UeXBlIC9Gb250Cj4+CmVuZG9iago4IDAgb2JqCjw8Ci9CYXNlRm9udCAvU3ltYm9sIC9OYW1lIC9GNyAvU3VidHlwZSAvVHlwZTEgL1R5cGUgL0ZvbnQKPj4KZW5kb2JqCjkgMCBvYmoKPDwKL0Jhc2VGb250IC9UaW1lcy1Cb2xkSXRhbGljIC9FbmNvZGluZyAvV2luQW5zaUVuY29kaW5nIC9OYW1lIC9GOCAvU3VidHlwZSAvVHlwZTEgL1R5cGUgL0ZvbnQKPj4KZW5kb2JqCjEwIDAgb2JqCjw8Ci9BIDw8Ci9TIC9VUkkgL1R5cGUgL0FjdGlvbiAvVVJJIChodHRwczovL2RycHJhdmVlbmRyYS5naXRodWIuaW8pCj4+IC9Cb3JkZXIgWyAwIDAgMCBdIC9SZWN0IFsgODkuMzEwNzEgNjk1LjgzNDYgMTY5LjM1MDcgNzA2LjgzNDYgXSAvU3VidHlwZSAvTGluayAvVHlwZSAvQW5ub3QKPj4KZW5kb2JqCjExIDAgb2JqCjw8Ci9BIDw8Ci9TIC9VUkkgL1R5cGUgL0FjdGlvbiAvVVJJIChodHRwczovL3QubWUvZnJhY3RhbGZyb250aWVybWF0aHMpCj4+IC9Cb3JkZXIgWyAwIDAgMCBdIC9SZWN0IFsgMjAzLjEzNTggNjk1LjgzNDYgMjg5LjM4MzggNzA2LjgzNDYgXSAvU3VidHlwZSAvTGluayAvVHlwZSAvQW5ub3QKPj4KZW5kb2JqCjEyIDAgb2JqCjw8Ci9BIDw8Ci9TIC9VUkkgL1R5cGUgL0FjdGlvbiAvVVJJIChodHRwczovL3d3dy55b3V0dWJlLmNvbS9ARnJhY3RhbEZyb250aWVyTWF0aHMpCj4+IC9Cb3JkZXIgWyAwIDAgMCBdIC9SZWN0IFsgMzIyLjIzMyA2OTUuODM0NiA0MDQuMTQ1IDcwNi44MzQ2IF0gL1N1YnR5cGUgL0xpbmsgL1R5cGUgL0Fubm90Cj4+CmVuZG9iagoxMyAwIG9iago8PAovQSA8PAovUyAvVVJJIC9UeXBlIC9BY3Rpb24gL1VSSSAoaHR0cHM6Ly93d3cuaW5zdGFncmFtLmNvbS9tYXRoc3dvcmxkMDA3KQo+PiAvQm9yZGVyIFsgMCAwIDAgXSAvUmVjdCBbIDQ1Mi45OTgxIDY5NS44MzQ2IDUwNy4yMzgxIDcwNi44MzQ2IF0gL1N1YnR5cGUgL0xpbmsgL1R5cGUgL0Fubm90Cj4+CmVuZG9iagoxNCAwIG9iago8PAovQ29udGVudHMgMjYgMCBSIC9NZWRpYUJveCBbIDAgMCA1OTUuMjc1NiA4NDEuODg5OCBdIC9QYXJlbnQgMjUgMCBSIC9SZXNvdXJjZXMgPDwKL0V4dEdTdGF0ZSA8PAovZ1JMczAgPDwKL2NhIC4xMwo+Pgo+PiAvRm9udCAxIDAgUiAvUHJvY1NldCBbIC9QREYgL1RleHQgL0ltYWdlQiAvSW1hZ2VDIC9JbWFnZUkgXQo+PiAvUm90YXRlIDAgL1RyYW5zIDw8Cgo+PiAKICAvVHlwZSAvUGFnZQo+PgplbmRvYmoKMTUgMCBvYmoKPDwKL0NvbnRlbnRzIDI3IDAgUiAvTWVkaWFCb3ggWyAwIDAgNTk1LjI3NTYgODQxLjg4OTggXSAvUGFyZW50IDI1IDAgUiAvUmVzb3VyY2VzIDw8Ci9FeHRHU3RhdGUgPDwKL2dSTHMwIDw8Ci9jYSAuMTMKPj4KPj4gL0ZvbnQgMSAwIFIgL1Byb2NTZXQgWyAvUERGIC9UZXh0IC9JbWFnZUIgL0ltYWdlQyAvSW1hZ2VJIF0KPj4gL1JvdGF0ZSAwIC9UcmFucyA8PAoKPj4gCiAgL1R5cGUgL1BhZ2UKPj4KZW5kb2JqCjE2IDAgb2JqCjw8Ci9Db250ZW50cyAyOCAwIFIgL01lZGlhQm94IFsgMCAwIDU5NS4yNzU2IDg0MS44ODk4IF0gL1BhcmVudCAyNSAwIFIgL1Jlc291cmNlcyA8PAovRXh0R1N0YXRlIDw8Ci9nUkxzMCA8PAovY2EgLjEzCj4+Cj4+IC9Gb250IDEgMCBSIC9Qcm9jU2V0IFsgL1BERiAvVGV4dCAvSW1hZ2VCIC9JbWFnZUMgL0ltYWdlSSBdCj4+IC9Sb3RhdGUgMCAvVHJhbnMgPDwKCj4+IAogIC9UeXBlIC9QYWdlCj4+CmVuZG9iagoxNyAwIG9iago8PAovQ29udGVudHMgMjkgMCBSIC9NZWRpYUJveCBbIDAgMCA1OTUuMjc1NiA4NDEuODg5OCBdIC9QYXJlbnQgMjUgMCBSIC9SZXNvdXJjZXMgPDwKL0V4dEdTdGF0ZSA8PAovZ1JMczAgPDwKL2NhIC4xMwo+Pgo+PiAvRm9udCAxIDAgUiAvUHJvY1NldCBbIC9QREYgL1RleHQgL0ltYWdlQiAvSW1hZ2VDIC9JbWFnZUkgXQo+PiAvUm90YXRlIDAgL1RyYW5zIDw8Cgo+PiAKICAvVHlwZSAvUGFnZQo+PgplbmRvYmoKMTggMCBvYmoKPDwKL0NvbnRlbnRzIDMwIDAgUiAvTWVkaWFCb3ggWyAwIDAgNTk1LjI3NTYgODQxLjg4OTggXSAvUGFyZW50IDI1IDAgUiAvUmVzb3VyY2VzIDw8Ci9FeHRHU3RhdGUgPDwKL2dSTHMwIDw8Ci9jYSAuMTMKPj4KPj4gL0ZvbnQgMSAwIFIgL1Byb2NTZXQgWyAvUERGIC9UZXh0IC9JbWFnZUIgL0ltYWdlQyAvSW1hZ2VJIF0KPj4gL1JvdGF0ZSAwIC9UcmFucyA8PAoKPj4gCiAgL1R5cGUgL1BhZ2UKPj4KZW5kb2JqCjE5IDAgb2JqCjw8Ci9Db250ZW50cyAzMSAwIFIgL01lZGlhQm94IFsgMCAwIDU5NS4yNzU2IDg0MS44ODk4IF0gL1BhcmVudCAyNSAwIFIgL1Jlc291cmNlcyA8PAovRXh0R1N0YXRlIDw8Ci9nUkxzMCA8PAovY2EgLjEzCj4+Cj4+IC9Gb250IDEgMCBSIC9Qcm9jU2V0IFsgL1BERiAvVGV4dCAvSW1hZ2VCIC9JbWFnZUMgL0ltYWdlSSBdCj4+IC9Sb3RhdGUgMCAvVHJhbnMgPDwKCj4+IAogIC9UeXBlIC9QYWdlCj4+CmVuZG9iagoyMCAwIG9iago8PAovQ29udGVudHMgMzIgMCBSIC9NZWRpYUJveCBbIDAgMCA1OTUuMjc1NiA4NDEuODg5OCBdIC9QYXJlbnQgMjUgMCBSIC9SZXNvdXJjZXMgPDwKL0V4dEdTdGF0ZSA8PAovZ1JMczAgPDwKL2NhIC4xMwo+Pgo+PiAvRm9udCAxIDAgUiAvUHJvY1NldCBbIC9QREYgL1RleHQgL0ltYWdlQiAvSW1hZ2VDIC9JbWFnZUkgXQo+PiAvUm90YXRlIDAgL1RyYW5zIDw8Cgo+PiAKICAvVHlwZSAvUGFnZQo+PgplbmRvYmoKMjEgMCBvYmoKPDwKL0NvbnRlbnRzIDMzIDAgUiAvTWVkaWFCb3ggWyAwIDAgNTk1LjI3NTYgODQxLjg4OTggXSAvUGFyZW50IDI1IDAgUiAvUmVzb3VyY2VzIDw8Ci9FeHRHU3RhdGUgPDwKL2dSTHMwIDw8Ci9jYSAuMTMKPj4KPj4gL0ZvbnQgMSAwIFIgL1Byb2NTZXQgWyAvUERGIC9UZXh0IC9JbWFnZUIgL0ltYWdlQyAvSW1hZ2VJIF0KPj4gL1JvdGF0ZSAwIC9UcmFucyA8PAoKPj4gCiAgL1R5cGUgL1BhZ2UKPj4KZW5kb2JqCjIyIDAgb2JqCjw8Ci9Bbm5vdHMgWyAxMCAwIFIgMTEgMCBSIDEyIDAgUiAxMyAwIFIgXSAvQ29udGVudHMgMzQgMCBSIC9NZWRpYUJveCBbIDAgMCA1OTUuMjc1NiA4NDEuODg5OCBdIC9QYXJlbnQgMjUgMCBSIC9SZXNvdXJjZXMgPDwKL0V4dEdTdGF0ZSA8PAovZ1JMczAgPDwKL2NhIC4xMwo+Pgo+PiAvRm9udCAxIDAgUiAvUHJvY1NldCBbIC9QREYgL1RleHQgL0ltYWdlQiAvSW1hZ2VDIC9JbWFnZUkgXQo+PiAvUm90YXRlIDAgCiAgL1RyYW5zIDw8Cgo+PiAvVHlwZSAvUGFnZQo+PgplbmRvYmoKMjMgMCBvYmoKPDwKL1BhZ2VNb2RlIC9Vc2VOb25lIC9QYWdlcyAyNSAwIFIgL1R5cGUgL0NhdGFsb2cKPj4KZW5kb2JqCjI0IDAgb2JqCjw8Ci9BdXRob3IgKERyLiBQcmF2ZWVuZHJhIFNpbmdoIFwyMDQgRnJhY3RhbCBGcm9udGllciBNYXRocykgL0NyZWF0aW9uRGF0ZSAoRDoyMDI2MDMyMTE0NDIwNiswMCcwMCcpIC9DcmVhdG9yIChGcmFjdGFsIEZyb250aWVyIE1hdGhzIFwyMDQgUmVwb3J0TGFiKSAvS2V5d29yZHMgKCkgL01vZERhdGUgKEQ6MjAyNjAzMjExNDQyMDYrMDAnMDAnKSAvUHJvZHVjZXIgKFJlcG9ydExhYiBQREYgTGlicmFyeSAtIFwob3BlbnNvdXJjZVwpKSAKICAvU3ViamVjdCAoUmVhbCBBbmFseXNpcyBcMjA0IE51bWJlciBTeXN0ZW0gSGllcmFyY2h5KSAvVGl0bGUgKEZvdW5kYXRpb25zIG9mIFJlYWwgTnVtYmVycykgL1RyYXBwZWQgL0ZhbHNlCj4+CmVuZG9iagoyNSAwIG9iago8PAovQ291bnQgOSAvS2lkcyBbIDE0IDAgUiAxNSAwIFIgMTYgMCBSIDE3IDAgUiAxOCAwIFIgMTkgMCBSIDIwIDAgUiAyMSAwIFIgMjIgMCBSIF0gL1R5cGUgL1BhZ2VzCj4+CmVuZG9iagoyNiAwIG9iago8PAovRmlsdGVyIFsgL0FTQ0lJODVEZWNvZGUgL0ZsYXRlRGVjb2RlIF0gL0xlbmd0aCAzMjkwCj4+CnN0cmVhbQpHYiIvKT5CQU9XKDRPbD1eZyEoYSFZWkIlQTlXMlg6MjIwNWBfTDghZ1diW2FCRjonWDtQWlpYRzVVaCciJVwkLkFdQlU/Z083MWdAUztLbFxgOTRLSjc2QzYmJHMkNzInSzBjalBaQztgbFwuSTBNKlJZXkVaOD9hbGB0RzxzQl1UUSIjcE9fUDpFSyMyIl5PUF4uXXBFXkgxV0pZcmU4T2lKWTdiMmpuQEtbZmBhLFFdWiU6U10oMGNGQ2BYQ2EsLjsmSk87Yjt1bUdxbnFqJDVhIThRTE1WRmFzKjAjWjhFaD9QV05ZS3BfazdNXT09aT4lNHFrLyR0KkA5c1hFalRaQkEzNjczWmg5ajhBRSo4U0FiYjlZXElYO3JFOiUwblxjLVJNTl1gSTVjSmNWb0tYNCJhIjcpYGBwS2JDKDlzP2RRcGYrNUs4J0VRPTN1K1piJS8/LFVJKitkcUc4W1xfOzFxVU8uMXFQISdBS1ohVy51TDZxKTdmOjIkMk1nR0o4MjxvWTBdLW09ITBXMDlBJCxRPlxqbj84J2hnZjtZJWcwPE5lZ0xYcltNSiRiNWJlPTVTTjtETiIjJCJBRWksdWIpczduYWI0XjNTQUxAWlpYRzgvREcpNlFxXm85ZmFkcl9pUjwoM1wpW2soXypyMWIjUCpeZmktXSpKXjU/UmksXWwmTyF0WVJhNEA2TFVjTSxyWDYiJEpgIUxXRVlAbS8xMj1aRE5HZU1ccl9kSiRTb1d0PVxnPHIhLTRSNEBHVXNfWWZxI10qYk1yN0lQKGxfTVlwR0NOUj1zUkxZLDtIJmhpZzwvdDdLRjttOGpFUkMrZEQ+LWFQKWBWZCdAXSFPS291XzQnVWk1PkxAYSszX0lnTmc2JzBCaUtGXSZAJiFpcEA/YmNFSFYxPT49PzBRX0JmO2MwcCxNS2NrKGdaY1VMOSE8LV9bTm0mUU5caWBeXW1BYWB1U1VEYjBDYmNhbCQxSmIyZSRmNDkyVkZTTGs5U2ZQUUJGRSk9ZS9pZEQ0bmEkQ2o/QkZ0KUFIJkBfQW49NFYudGs3LFVwUlM3TGpENXBRXVo7bkQiOiMiVmFYcFNpZ1FEJzMkVygqb3AlLzFMTjhLIWJWZ1MwR3E0WSJkcD07TmVlLUUvVGw5c2sjYGRWUkRyY0FrKEQnSGFxJysoTVVnRTpkLl8zJ21DOyJOT11lNTQjMz9yWjRjM01LNzpSXXVbUWpDM187QlxsJCdLTFhGSUUzR1doYXA2KyRFWlxJa1ZbdGc7QEk0VlxYOWFwb2crWzlIcFQ4KTVxdT1gODgtPmxMZ0EoTzpHQ1xbRm5mdFVwQU9lU2Y1XTdyWFJBOjddPEIzW2IoYj9OKERyYVlQYSRQRGonL1lXNzJfOXNHXG0lTF9LMFNYY0grQGVQSSQyQ2FvKDJza2gwUWk+ZHFxJTtyI3JnXUlwS2AwL2BRSlY5P0tcTitfMzZyWmVUMjxMailNQ19HTyQmXzpnUEZTdScwMy4+KV9dVjYySyxtV008clZRSE5qSURfXEpNREZrXEVnXkg+P1ZjOTxlN0oyRU8+YFQyJC5bZFwzSHAlZiMwPT1DKWwta1pIMj5HOCpNazU9JCo7cz1MIytscURQNVUjNTdnOGk/PCdsTF83MEdEZDZWc0FRbDhxPSM7SzUsKElNVkBqbVZZVjVRWmFWKjtIaiNMdEMrTiw8ImhfblhxVUg6MTNPN2YyLHIyYTIpMUNFM205J0VWbS5xJlBtSz0xWmcqMDU9ZFRTJEtPdShSaTo8V2xuKzdEYkBcY0JqUi5GIW9IZmg6JTlzZ2wkQnM6KVViOVpcdUlXcVtOP0tpI1ArZDxxciIvV2UmclAlWFRRVmhEazlnaSJ0REMpZVMpVGIrPm5WRSNwYGlEblFPZmJqZSgwPGY0OEB1a3RNTW1pW2NtY2BIZSEwPShzTjo9SWo5NiU2Z0swUCcpPjAzTjgwQGtEPyhzRz4yZ19ONC0wcmRdK29sX2dia3MrIyhWKSw6SHVGQUIhIV5ZZ0JqPy5yTnAhWUY/X1EkWzwqU3AkTGUtYz1tLz5DZGNWMDFpbVhuKkNlKWtNV2NfJGM3P2hQYj1HKk5WVTNocFEjMUAvLUVMMlxlcDo9M1MpcWRWTTZqJW0uY1c/P1xUPSYjRmsrRT0/LkErVT5hdEBPUTI9Uz1fYiZIb1QlXUVzUkI4bzdgQTpzaVZcYFBVOV9GYHNJP1duUjtMTDZMZV5lYTktWG1KMUcjS1QnRiI4RUNXYDhZPlZHNS0tY3BjdDdXSz51Uj8ibl5fcU1fQ0U7SmFLSj03a2BlLjYxU0Q6amhuOyRJY2xIImVXOU0qX3MoKkhkJWRSSywzMitsS1g3QWcsLTJzZSZVRG5kZ3I5LXAjZiRWU1RYVD1HbmpFTWxaS2o4WlNYOm8qSSJHMmAtYmdsMjJuNk1NZWQscCFiOyZwcHBwS1RSJVpVPUgnMCdWKUwlXF1PMzpzWSozQWheKSVrdF5rUU9DTVNMLzl0cSFSN3UxczlMJURsLCZtZUUpVTxPPyNhQC1calZhNkJUTyxjQkA/MmJIbl0wLl5WJE9PZEBgcG5AL2FUNTlZKCZqLlVFImJpOmVfcXEoJTolZ15bRDhhQEdsSFBZaChhVV5ASkIpIitWT3U4cCJsMihUQmFnanVRRC9VJ1JhL3FvPzJEWzIhaCYvWjA1VVtsJTs0P19fTUA/Qzw6L3VnLjNMbjc9VUhOTUNYUVFhYik2RiYrRm0oNnE1aEQkLlZEOHU1X2sscl4+ZU9JQik5U0lNQWdoXm0zc08hNSpLVFEsamo7bjhcRVJycSZJUWtlZURWKWowUjA4ZiVxbCU2IW07aj8iW1laK21qV240KUZxXVxealI9RV9vcEg7U1ZJPmZnYzs2cThCUWBKKj84WDA+TjlETWAhTFdFVmtFKSw7YFlwJ1toRkJVKihQJ0RoMXNoSks7ajJXSmFILF9PJFpsLEo0MF9zQ01sRyxsIkZfXGc2OCN1V05hOlsoOlZjZW85NFlHYzszO2hUbSItSjcjcTcmNTxBW3FiaGpKKFpdRCNmTm0+YmNWaTFBdWwtRl8rJUgwN3BiaWxWIU9WcjQwVENdaV1oXUgzXj9qcENOMzBrLz8qUFE4bWZZKzkoX2NDO0UkKD1wMlFeQGJqaWosLWJkImJuRD5JOXEtZEJzQlIxRGdQbSsuQTNgSWlxOEFTWGIiaCtVK3FfR0IhZjU8W01MSD04MExTOFdiQnNYcmhCOTomZCt0a1YjY05hRFVsPTNiUGxUOHRaXHI3PFQnZ0E7bkY/LG1adCZxLj0kX20wSWtIJGhyMU1TK1tXSEgvcDdVMGsidUhuRSRoaHFEWyskW3R1UFYkYjs/ajVaVkUoWlFsRk1dXSxhZ0NES208YDNCJytDUWA0SkFLY2xJTDNLWzQoXyxfMVI1TU9oLEctcCtaQ206c2ptTW5Iaz1TU2BHXG06L2JLcWlucyJPPys9Vl9NVzJgWj4oYFo5XiNKVGovNyQnJVNlWkVhRy1WbExNdVQiLGc+OGVqW3JtMXNOczhKSkMoNF1HTS8uVkIuV1w5Nl03RkYpJlxfITlla3BBWSZmUEtSSj1BLEVBJilFW0xcRzAuI1VDKiFCO1ZPN0lpVllIciUmV15JRlpoITMrJGlhaWU9THM6OmJBIkFwMThDRCJSQWpNNEZyMCU7YnM4IT5RUzgmZ1MvNlNhOUc4OUMpMWApYSFnPUVLIURFKCVnTVhzMnA1K05MMj1pc0wyQiVOWiQzZHEiaW8hN09Sb1tqMkhQWkQ2Kj1ZTkpmLHFVR3JqJmtZOGgvbkNGZSoiOGhKPCc5PS5LMjAxa0tGRWcxclY9U2JAX3U3OkYpSmRAI1FIOllAJzo1MWhDWDtOP0kmIm9rTFFHQ29ra2k0Jkw0PnBBIWxZLF9WOC5hQWhkUCpERl1gTTw9YCw7RUMnQnFxbWFqLiM9cm0nKWhHcUdtXlReUSg3cGxDTHJuSjBJZVVidUxiPzM0aDZoNV1zLjVfVi1CaTQxPUtxbGJcPEZtOUpOLSZxSGlFJDc9IkRRLDtWLiR1VHJJRlxkNXI6YUxeVDhGRmw7cUhcOyRUcC8kXGNoZ3JFJj9OX1tBISZVWGxYNSM7WTRCWj4pVE1MdChDVUQoSCVpbF5tSlVzIjEvXS9NVFY4blFPQEI5Zl45QjkpVWpfZGA/YSknNz82J1MhUEl1PFppRm1pWz9PdSN0TjhFKG8yPUt1QV0ubk41RzYoYT9zMltqInI9Q0lpYy0oNUNKPiNyMz9IZCQ3ZHIuO0BaSGk0Mkl0JD4xRV1zS25pWlYyWGc1NjMpciJoWiY6OSJ+PmVuZHN0cmVhbQplbmRvYmoKMjcgMCBvYmoKPDwKL0ZpbHRlciBbIC9BU0NJSTg1RGVjb2RlIC9GbGF0ZURlY29kZSBdIC9MZW5ndGggMzE4OQo+PgpzdHJlYW0KR2IiLyloL2g+aiZWJnROWiM/S3FvX0g0PyEnOUw3PllETTtAUlpSN2wqUjMlI1giNT81WDVOPS47QzQwSGhTI2NpPzQ7QF9UNlZjZyk8V0IhbmN0cnJTOE00OyNGYnFHSWUhJzFQYVQmJGxGY3EyKSVUSWJlSmUqcTtnUmhGXGRhVjZxVDA/LlY7J1AsL0VzQjJJU0Z1K3FCOFQpLF5Xa2EtPU9NV29eJUQ4QVlLLCYtRjtCT0BoISk6U1xXQT85MjhNWyIoT3E/aXMtJ09HJDoyK0Ehc3FpdVRLbFpySkJCMyNec0pLY3BnVVlGWkxAYiFYKGBFRT1GSjBiWjgpY3IzaDxmOko6KChkVllCMW0kcTpQbiQuMCNwJENxblVqY28wbFY7UUdwSnJeLUouLUs4L1VodTFAdVkpR1wtZGouMz5wSE4oPzMmLzQnVnU7RlY+bFVKTjNrZTpFb102cHI6LklAPnRLX1QrP0YsU2hrcV8qRSE2ZHRzaT5MQUpsT1ohc0IiV2Elc28qLVgiQU5NVlRNbC8zdVNUVz1qTCcuO1NfUzpaZHU1ajxEXi1dWz5Wam9gal9GVmllbjQlZVtJUyl0XC1aWTsjdG4nVzEzKytNWWhwY3RKQCRtISxtJG5wV1hTLGV1JGYuYzs+QEskQVFeRzBbKigyYmxNLCo1LU1cXXMiUl88S2lBXUsmJC5NZ28nV08kNmhIJC9RXkRUOkRMczpWSycsSjhcNkBfVitiWkIxTS5WUEc4TF1vXF0uTmZAbC9iSyEjYyFEPTJcIicjQjF1cFFiKzZKK1Y5aGtmVV0+YmBqalFvZUBATyVIWjxHcGtPQCItJGtKJyEnIV1BOXBPZFlcbGlEKVdkXU87NXRHTlNwUjthIzdNdDtvJCxUNykrOTMlYC0mQXNlYGw0UCdXbCMuLitpYisxXFI/KCsrLDRNclliVlJEJU1VUj8qMCJycVghNzhcJS0lQ0Y9RmFuPWxRL0Q2KStsOio7N3FqMlshXmskM3VXNkhXPXMhJ040Nz0kVFd1LHUqaF1bPTRCQShbJk1jITBoVFtEa2lCaE9iTUhgY2EvZXFETllCImtWQ2o2OkUmK0YuQGltRnVGYFtLWkpGZiclPCxUWUQqU0UsP2FTQ0ZnP0tASkNzYGNXJVhCXklGYiNGcTdqaGZbXUUuaC5SN28pLjtIUWJxUzFTMjhJJ2tmW0dqUTNZRExSITlrbXJPVTEuJjVhIUlKTUgtJjdVUl8tPkNFJVc9ZCwqUyMqTSwjX0BnPC4kZ1UvNTkvMSY0MWY1SVo9TDxtJFZuaUk8VGdDLkBSMS9iIj50dUpAWE5RcyVeck5gR1FuMCgqTGdxVlxESExFSU5zUmIsXnNSMjRuNEswcyM3R1gvLl5oc1JlSUtEdWQkRVZKOEw4VnFkU1Q2NmIlbjROcG5gPUBGRVNGK0FiSSE7K2ZmJFs+ZCJzKm0nIzI+SGFGRGVBP2ArYyoySiJgbz48ZistLUdjQXErY2kiKXIqJT8kaUNFTCMoLVZhIycncDdTLUpLK1k4XT5BVihKSUhUcWJWJEYwJUAwb1hkSy07ZW5xLl5iY24sWytsP2k8XDQsdWJUUDBSKUxdQEwoOm8qLloiVEloO0NsNGhhZF9XRGNkS2FuI2tXWzNiVnBBT3JHZSVXZ246bWBYQkBqO3FoNXJwJkRWcUkuJy83WENXWyFMMT40TVkxTjw3Rm5HY3FWTkJvRT87ST0oSkwsNUE3amJrJVtaV20oSDpLYjYyaUd0QSVCdGReZUgsYGlzLW9qYG4yLmxQUWVgaGhsbiNxalZNRTc9Q01iUnErRlNWKF5NIkRiWCZLImM2PEhUdGleZjR1Xzc+RiZAJUlqT1c+NitbcGQ+JmhbUClpZHQxNUphJl1gOVE5TWFQNXFGSGZXVWtcLV90ZCpfJ21RND9lJzczS0pIX2xQZDkpZyMlJSIqRUZ1Nm0wV2c/LGNqaV9HKDQubk9JNldbUjNPWl9gPmlWKy5lWyJZMS87VUIoWEpCbEhtUW01Q1JBPm5cc1ZGQGdIVXAwKCkxT09ra3EhPDpFKVBTJEs9Z2pnOGhcRnE1V1goQ2w5OkA1NS9MYDA1RityTzA6NVkjXCxYPUQ/LTNiakgtXD91WlUpNFc2XE83b0pDSzFncSg9QlgiZko5Y1MhXDFpWD5kSTFVc29oJmJTPDxbJyIrI0lacnRZLVhwU1s0QzR1UE9sWCJaMyIoWldnWlBMQXRmKj4sNnUwSHEuTCMnXFhgQTJSdDRvJ2pRNCZVMkArPE5DbjlYXjUoXXFuNmNFbjhcTEQ9S0dWU3BiSUdPKkVbXDBGSWxhIkM6MT1Nb3JYZkUnSFAyVis/SnVvPWtmOFpxcm1dQXBkYmFMR0c3RzVJWz0kIis6TE11YC9lWjFJRzdWWHUvPGZeNWwuYz9qKWxYWltpSChaWDBHKGplOi42Q0RNOWllSVU4aUxydChIbGVoSEJZTGo2NSY3O1YiaS0/PU5UZTltVCxhZEtpS0VMNDpWWlEqRCs6XkxvQCZNR11gay9cXS8kQSd0Z1RTcm07IyJRI2ZMUCFZRltQZiVAVVEtdWk2M1hPJ0NnZXNgYiRLSEc7TmQ6aUVLTT1LNlwjY2c3XDVndU1xLGRRInIjWlI5NUpcX3MiNWxrJ100LnRyMC5Ucm07amxXR24oJic+IVthVigkWGhJcVRSXFw0RU1jRVtBQThqUUpePG42JWxiS21HLWFUTypHKVpPREZdUiUrNTpZUWBbXVNcWi5jP18pK11iJ2cobVtLQWQxOyVVXSY1XmBXSkNnXVFsMTs9NzRLZC0lbTgvdExCRz1WME9PTSVMSC5bVSZ0NHVsOko2XkwxbzBZU1RCOFAhOmNqWC9IPFYncygna1diXiEyTUpVQnBPOjtCPGFCRDMhY08yRmpNRT48NT1SO0M0RyVLWT8jcy9qMkg3O3IjPklpPzlbYG0nXVBMNy0xdSQkMjw2OWZbPChOWlhQQzNsYj5JLXEjXjBVcTUtMXJtSCxLcDtrOiY8cVg6JEBOKz8zaDd0cDlVUj8hSD1SUm5TXDNTR1A0LGdsOnA4YzFcLFNOQ1dLVUQnMzlhIVYtN2ddWEdvVC0zcWBHMjk5PnFwcVRPb1Q5cj5WUz42ME8/N2gyUE0hbGVnWjl1JEhRVSgrai5oQXI8Qkg1PjokVi1USzUnYmNFLmlkbSJwcV1EKjozTFMhb1sjLWdwYWJVND42LzxmW0wsXzxWaVRAMjtYJyg3OVNnai9cbDBpZ1drPjQrOCRJKzooP1klY0Yycy1lU1VJZkZIOVkwMmBYMlomIjhaKTJlMkNFbWdBLj1HakM0JUxhMXNkUGAjMyYlTjJiXVNkLSk9IkBhYi1VUitjbjZzTiwqJ1Jdb10oTHROQVBbPXMycnFHP3RmKXIyVW4hczdwI0AtN2UrKXBuTGw0ODZJUTIuaV9PKyFnOEU3akxoMzslJWRxcjVFY3BqcWxXRzIsUUtjWXJsPm02NmM5KkU9LEU3ZWM1TDEtW0dzanEtbjFOLU1AQ0Q1I2NJPygiOjtwOTxkZ2FYWW9zWE5ZZGNrXVw/PyozRSJENC9VYlgidW1SPF4vcmYwLjI8V0M6QCQvKTteTS5pQ1VXaTluOW9TW0RmbXBpNzxZLyclKGdSPzxnOmk9QVghJEVcWl5jU1VtWWUqYElaPUBUW3NVbVpEKTYiLDFXJiVFK3NLc0h0OzBMTkMqRiwmRyspY19oXS1zLkA7czo2Iiomay05XHJAclhPdVZsbDlHRTdgKHUibEpCKmpDZjIvcCE/WlVzbVpMKlQrVFJlKV5WIW1FSW9mUU5mKUFRcGA8RjApQ3Nbck8wdWtYQEUhcFxrUSs0SEJdSlpVbWooZD0rW10kTmhdJ21zLloqajcsM0swNTtlbm8xYS9vZDwzLz9fY1gzN2c3LEdMaDJ1Mik5Ym5VLG9oK0YrTi0sOmtpS0JEXnRtJTxIPi1fWilBO0ZhR1QpWmMvO3FkUVw+KCYodTxnYmMhWzs4SjczZipbKFkiclZuS3QoKVczZSZMajFvKzlRMGs9XUU3SSJtMiY0cz9CL1dCRmUvbG4rTjAlKF5qV2NAMywpN0czI0BdJ2VxVkVhYWldQ2Elc0dwP0RqQyRtbmpvTGstP0ZVNzJAPWlwVSJrNE0iVmBpU2ZNYjdbY0I+Im4zTEYiPy4lK043KzI1Sy8hV34+ZW5kc3RyZWFtCmVuZG9iagoyOCAwIG9iago8PAovRmlsdGVyIFsgL0FTQ0lJODVEZWNvZGUgL0ZsYXRlRGVjb2RlIF0gL0xlbmd0aCAyOTEyCj4+CnN0cmVhbQpHYiIvKTk2OSxPJyMqWzVvTUpBL0AoXGQjUG4yUFldXDA7Vi5bZmhgRkoxKmJpZUFYb1A0RStscDprTnUsIWVocTFjQWhrNCZvM1gqYEVXc050NzY8JW8ialFwbEV1KmEocDQ/PyxPVnIiMzA8ciMrLVlLWSE5ZFlsY0l0OTIpPltmSl8hTUhfNjhRYyMxbFJ1KWsqRkY1UWtUYnFuIS5ANlZVOFQsUmFgLCdgT3Q8NVVALGY4TidGNmxdP2xzX0ttQ2AtV0QiRSsmYCQwI1JkJHMrTE5BSUJhKCJUVHEjUlZpbikzYTU4SSc+J0dZJS5VYEMrOiMjWVReYDxNYy0oP3VJRDxeLjRAQikvXVJpZydCcWc1MllzZXAnTUNaVnBfWihdJnBEIjlhNFtSYlc5TDVzKCdsIylHKjYwZClFMktmV3Q1MyFrOGY7Vio+aVFEUDxfXDNSRVQxT3FJWF8+a2ZjKW0qWDBpbikzYTVESCZBNWlGbyZdZU4qO2lgKEZFbFs6b2EsanJuQVUhdE9bVSIic3JTXnQ6VFZITkBhbmRHQ2BEaDpKLmxRXlZQXlRfWXNiIm1NWiYtV1UlVTk5S2VjXWU0UEVzTj9vR050U1xvdUVnPlFhR29yazZobSMhNDpNPTBZa1lDUiF1QCxXOyVDQk9lJz5dXlludCMnQ3NxRSNlKStOLy84ZDk7UGRiMSZ0XzJFXGY0PCRGImNHRzI/JzpFMydAV3UjaVVeZD5VY0gscVM/YCRqYT1fTjtTX01JRG8rakhtRDg3IyQuSjQqS2Q8X2NkTT0uYWpNYCNdVztYPDsmbWlAMWNJX0FWJ2lpQWhLZCtYKWMmPkU6J1ZdRHA1NkdcOmtzXmlSLCUhaTMyUiU5XVhdPzMpNDJSVUBMT1wmJkolJXU6UDs0ZjZwUTQxOzY9bVZRKUE3XGNDMS09U0AtVCZiRzRWWSJOSCEsOzdfMipzW2hZWTlNQUZiLFUmIlxnRiRNQ2FCQS80STVbSFMxZz1bP3BUQ041NkRpPTQsayE7bFRXNj1hSEJKODxrWjA7PlAyTkJcbEZjTzphUD8sZUJSYCpyLzgyPCIqXlBYKHJIanIjM1AyXU8kXUgoK1A5azQ5WzxFLVFDRDNwNGNSSW5lW0RwPyVqIW1PJUU6ckE7cEUlOmQ9XWJANjRXXGxLRDRcIkY2YSwiNTshVmg/I2o7RV5LMDpWVlNyUzAyUF5eXylvJmZOQmApQ2giIU4oTWxIJTpTYiksS0lUMTZQNm89QGk3dE1Qcm42JSQpQl5oRlAzNlcxZkZSUGJQJENcUWdPYFIwQUhAWWxEN0NeRVwsKzk8JDtGX2pMWVNuZ1JnRiEoc1svWk11KzNAI3FSdFhDQTIyTlgrdTV0LXE0YENOW2FUZEM7ZU9xbGAzbmxZSCs/NjgkSUFGTnEmQ1JnYVJcbDQ7TlxYIyVNT3QpaFJVVF1oLE5KQUozY2hmdWtQSDJAM2ZvJFtsYDNCbmtbTlBDYVBuYTBcOVdUWGRwSFxyN3NTU04iMGxCJS1eSzIqOi1RUk0wLDZhKGxNKlVySzpQQ10pZnM/NSJPViMrPHEqKDlZbiQ2WThxcDYlMVcqNl0wSUJYSSNIJGxRMkE1S2BnM1ZQcllHS14lay4tMVB0QWtRLUEsKF4mTWtZXFxFZ3RfIVQpXV1TRzZfXDgtZWNfak48c29FZE4mXF4zcC1hTDRpV1YiITdwQSsoKiEhOzojL18kUXVHS2k6TElpcHBlSGNkUyQ/MDVRMWojb1JsOm0pW1NQTnUzOjRqUkAmTj0sRzArPTtaVCJhSGA/KTA1YlBQJ3FwND09bFowJ11UJzVGamJkZGY8PmBRYV1HOzA1KDk2TSsySzo5cF5rQmlHbFFnUUYlSXM7SmU8MitERWZLZiQsYmZNcVJbam1kPSFYXEhbPkU/KCQjXC9oSSQpQGZqZm8xak1cQUckMyl1IXJbXG49K11vQ0xSYDFzcmQmSCxsT1slbWNGU3FAKDJfZ0JcK150VCVwWkYzYUc2XVVsay4kcjVsYTRUNjAwVkguNDMsJUpOb3FfZDNHSUpROTkuR19jM2RIOlZkPWRyUCVyTFBhSCJGSEgyOXNCIlgnLTRvTGhmWEdEampPUFBlbWN0NVRQKEVDWUU/bmAyXlQoXC1OUERoZT89TE1YSWd0b09wWlRkXGRpST1KJlgkQSRjbkI0MDtqXV0qcUVjcXNDWyNiUDV0ZWJrbF5COD4iKEsuITpjXUxKZlhnRyQ4Nz5iSTUiXV9LT1U2KGozJTUvaS5CdCYpKFRCPDRnQHFYPCtNOUBrVmJlW0c2OUVRWlxOMjZPcGgrWCZabDpZNVdBXlZINV9tMkNuLyssOT5HYl8pYUtgZVV0N0koOS9hXCpjZT5vLSElRmBucTxgakQ7MzwhaV0iJDVqWV0+O15SaCFlNlcwSW0pdTBPY0FPKy9FXjtnIUYyUlYoYzFbazU7aS5rdFpZRl91VmhlZDBGLD83KFleLyouY1EjX3VobEBWJz9dcVptPmNiL3RuVktSclBVSVkjSlFGR1FNJGxNL29HYjFFOT46LVg1JStyLCZMPVE8QCsnSjIkbm9KZCpgQmkhdTFPP1txKWFrVCcrXGdOWkZjcml0JzRkWFk8am8qV1JiS1loJEEySG8hXVxYTlJTRCVDPWkqT1gnUF9NLz10QyRZTi0jPFxyWzZRKTB0MDkrMT5xQ0IkNlA9LSMxITEjZjRpUFshO0smXV1YVTZUUXVYaihOYHNSNlZIZVRdcTo7MjhldDtpalRETytwXE5jaVJWciMhTEdGNWM6YlJSb0RNKkJAXUBtU1JVRVJcalxiSycnK1JfLVNaK2pHNk9tYTc6c1o+Yyc8Q1hCbF83WlowSmloOlJRNlghNm5iS1Q6XWI3XDorcShsbEdVTU8vbj8xWHRuXmVuNW5xZWt1IWshbz8wWTNaJlJRTF1nLD41Yi9fZ2pZNSlMYC5fJzJGY0giNW0hKEM7aSo1O29BT1NOZ2RgZlZeXCJMU2xUM0IlNldQJThjaWxjVUE0UGoicD9tIz1iazZDPWY6P2AjQWJkdFJLdFhuJSRDSWA6ci1RM0VLYSZXJD5BY09OXEQpMF0uXklpM1lUNlZkLVxMXnQkMlZKUz4qJFNfZlczJFlGbCk1b1hOVD8mT3MlVXEtSCJZKUg2K1s5bi8rL2w+Sj5TcSJ1c2xEMDpVXHNRN2hSbSNOcWpuTS0/MlcuImhmczk8ckcyXid0WCw4WiJoVzxJSk1KOWc7KiJgJSZGQyhzVWlJY2JlZF1adVJfZiE+Ilt0PW43YjwsRi00b0pJcmEzY1haaUdDUCNXZ2kmSEttZTUoPDBbXWVOMUdsJixGY19NW1UuSzoxZGFROEJxOVkuTzM2UkVZX1VbOyJXJTxxMWlANS1TWThqXEBoTGwzNHArXz8pY0dmS2plJ0dcLWxCQU1tZD1GVSpLO0hUNjVKKT42c0d1NlYva19mQz8mXUdKR0VFMigmUSFqMVozTj8sbF4sMihMM1RDQVRJaTdNP0orPUZrOCMqTWdqIXJxc01sJVNWQyQ+bmJib11taDoycmdIVVVNVVVUXy1UJVpSYnNvSyMiUVlGRGwkKS1tSkdGYWApc2NCUHVhZG1MbiFVTldZdDdfRldyJVpEYjxvWExWKlBUQyE7NCpFP0gpXGBxKlJmNk1vdUwhNlhXOWpYLC1GMFpdMGJdWFo6RUI+OVg2Jjt0IWM4QWxBW2lRYSFgLzs2clA5ZiNqP09jRSJkPCFeZWFvZjthInRqcm4+M2ZIKm9rIzMzby1qJkE3RVtbUF02XHBjUTU5LiRCU0FPYSUkVVxsKEEsMXB+PmVuZHN0cmVhbQplbmRvYmoKMjkgMCBvYmoKPDwKL0ZpbHRlciBbIC9BU0NJSTg1RGVjb2RlIC9GbGF0ZURlY29kZSBdIC9MZW5ndGggMzk4Ngo+PgpzdHJlYW0KR2IiLyk+QkFULiduNSVJSl1Eby1eXVhyNGltdVNgJ0E3QFFFRWwpK29LYi5yPyMlPyM4WmtVZSghVWpzZ1xXIlEiTWhfNyg6ZDI8WixcM2MmMylaRUUsXV1GP2lnNjZvRGNJMm0uRDZDcl5KUmJnIj9OQk1DV2xEIiQ4XTk+WVJXRDEoSk9BNzcmYCI3VTNvcDY5ZmtbQmMnTEYpLERJbCM4JW0qYj1PX0E0R20lKTtXaE1gLDA5cCU5RGhvTkxaVGNtb0t1JiVPJSNrNGo+dGUhJjNHZDo1RykmSE85KEUqZUY5XTxPPSllb1FEb3JYJXM6NCdJUzxEJjQvIjNCMjZmTVE+JSJsRkcwJ0opRSRERlJfZmlAPj8zPEdSXFhab1AyO29iKzhLbyNnKkI3PCRKT2xPRywwPyRGNzRMJihIJHJiWFIqLjFIN1svU2wrOV1WVkUjSFdXPGZVWWRjUjVrMSxoTTVnLTY+blErTjxRMVhlImAwK0VKb3IjRWcqVCJCKlEoRTIxXGYxND1ZKGFgU1MwXUVULktkWUReYXImUz5zQCFWPGRfRFN0KTZnImEhZHR1YyFQLDVzSUctXD42cSVkNyhUNCsoXTZQcS4yQDsoWV46IWdMW2UqalQjXVpmLUMuXj4pXzFOckkiNDhYbyZSYURnQmJ1Y1kyX2NXJDQ9RGMnUTBVMl1MNzdlYjddZXJoMW5IYj4+YSgoWjk6VThaMl4jJ01HWmFyL0hrKUZQUiRBPjJWOkFjczEkRiMyYj9xUj4lIWJrLy9ZdUF1UWZmZl5dTygvY0dMPFVBRz4hbyUjLzhDWDNvL0UqYkNCLEREZlJEQ0UyRWVbcj1IZy5vXG1UK19jZWpEYWhtQjdQUUpFaGBZRSVxNWpVR0Uqa2gxUjQpQHFHN2lVN2k4MGgoRnRSLEtEKl1iPllmMGhgZ3Q0OWlPS0ViPm1VJzc5UHJJZjYwaHBYPUM5SyJGKi5CSzJfNCpEKD0vQj5eVjxTXnJAY0BuLFkxSDpJZUovYFFUNGBzWzhZYzBKWWFHOyRTOW5bbHNjTDokQyRMaUZXdGU/OXNxIWNQRUZhUCZcSWNXNyo5VUlRcFtlMlQsN2E4RDk/RFFMbSRoSG1NPW0waURxbFJGUkJMPmhIVzIvUE0iUV45Oi42MXJwQVBkK3JZTy5jMmErNEdEWig4QlhmS1JsRj5WYjBMQmRlaE5iO0hAVG8+O3BBITAnTCFpUmpLZVRdZ1NDPCM1Lzo6RE9OSTZZWmQoaGorciwzIkpNUmJNI0ZtPTpmJiMwNmtlQD9xOi1oSEBqXj48WiFNIVkyT19eb1dZXGVJZHI6Rl5YMlZmUDpIKig/PG9AOiE8UD8salMpWD5gQkNEbFpfZjJzVVtyJzRkN1BES1ByOFM3RUBhUUlgQmUydDBdIl5PcWcnLmdgJipqJTpvNFg7XShwKnFSKHMySCFUJTEvbklYMVBFaTlwNldRPF0pX0VgYjxfKUdoXV1hRDJ1X2VvNnMhU3IhZyVNTG45U01uSV4oKXVSMy8uZENWVjZAKjRdUVRHNHJgITAzLydjRmZfJSUqaU4sSFwkQGRrOW1gT1tDUU9iZVZrZlRzOTJIVT1mWDhXIyVxXDdpOHBIKHNFcWgibGZyTitNZ2wvIUFQP2MiPV4wLF5DUkQ2IjwwZ0pyWDQ1a1JRaFc1ZTF0JF9DU19XTE5USD8qNiM8V08rKC5bWWtEPkAvIj11cydRbmdLSzxaMjtMWTYuLUsoLCRAVjpQQUxrP2twT1BgYzppZFlUZUpzOENEL2UhQzRjRD0/XCM3TyZiYFNeYGpacU1MV0IrOmZuI0BDWk1ETCVZK1tRX2QhOHMpPG8iMjBhIVZTUFhaXlQ0c2dOO1NfJT47YyFfdDojKjpGJSNROVRKanFBbjxdYkEmIVUoSTRdOCpcTkE4dTRtbT9HNGpbUDJBWW1bazVqXlgqPlVSUF0nXHNiXyZZJTA8cGhLOlVbcFtST1NaLW5qXllfaWksTiZTLiNMMm1gQE46VylBMmc1WicnXUUqTksoLi05I1wuYSJscWQkQjZSZismdWxFVGFSY1FFTCduJ0QsYEg3UV9pb1RASl0nXU1JbkM2RUNvai4+QV5KPjpUImcwJjMoJClFKj8iUFdRJzIpRlRpZiZpLlg5LmNjQFdWOUkoaS46MlxnZFQuI0NcPjw9Ly9VJ10mQUZSX15RS2NRPi81dUdPZ1k9PHIobU9vRCJxMmVwY0ImUVZOJCo+Uz8rXzo7OkJmOUtZVypPcFcxWF0+Zi42OjI5a2JZYCdvJDQ5YTheQy5IP1Q1Y2dMS3MrKXRyXlxqT01xcVRBST9aSlxEKlxPMD1VPzpARjJNPD5tKDA5K0ZJR3BrRDxiZVY+KU8iYm0zbExoWGFNVzc+KjxtNUclXjZEbVkvYXQ1JStxL0NzO0A5RmNKLjlTSUFYSyVPV2YjaTkwUHFAPmVCQSI5WGclPS9fI2hcSF1PLS5JZitxWlB0JSRIVE1lUHBjOUVGZVtAcjAyRSlUPzAxIzpLYCtgTUpValtsSWozWFtbIUlubCo3NEgoZyEyMGcjaFoyPURZZUxBJmJmXWY2LFkkVkJVVWtkSCZJcjxkVGZvVmVpW2NQMytCMD5ORiZBMSpjVjo6OnFValQ4LDJVYnM4allkXE8jdS42IjZpWEA1Pk5FUlI3LVtNayJKUSVnJUEsbF4mOFk7KmVIQUdcKXNCQnVSNjJhdGRHQFQrbWsiW0psWlJhIU1VYU4+aCE2XVFtbVk0Q3FyQT4+J2FXKFAzZWMhXkVJW2NnTyNlVTpoYC5Way1zW2BqN2ZYIyYkRitcJUpDX1RTW19aYFxgIShGNGVORkVDPkBWMW9oRE46MjZZITtnSXNDb1l0ZCxUYW4kJVA0bFMiNjtiTmxvQG0pKWUhR0liRyJMb2RFa2M5ViZIaU5TVCcuT0NgKFM1cidLZDlvKl9yLi9UPUFjMnMtbHIjQzZuI0c0P2EtPyVkM2pWI0M9TWUqMC9jRyModTpZNz9ORzhPUG9AU2BmOyowbmNCSj9KVyQ7SDc3PGoxbDxcPEpfSUg8RjElY2guKE43YkxRWF8tblBTVCkjJl9wXFQ7JFNaaF05SjQoQ1w9ZGdCSUpsJjo3LlRSQlMtOSRjRWMnIldIRzVhbChsVitvPik7MF5IXVZCUmEuK0FKWzllXjhhNyIta0s6REApZT5LMjErJ1s1Lm9BNkxVXVtZaXMxQEZlJGgkQnEjXSxkYFlzKEU/dFNcVzZ0OWMsbkxnYkJmLGhBYks0bzZjIkBXaDU5ZEcodUY+JzMlNkE+YWNhRUc+NDEjQ0sqZUcsI2lpbEhMTGo8MFpIPilbPEkiLEdINGpEWU5jRXVAUkNPcFVhWFxwcUcpbnFdLjw+SV5eM2hLJjxSY1QtQjxHQ3VbO2V0I2wpIlpRZCdQOEhBazpDKVNkVSVyPzBHZXJOLWwtWV5LJVJKK0VZK0soK01sSHUnNzpyOyxbUVwvJUolNjVPaVZAUnRCTE0zLUpFIUdhLm1ATk1KLUotPVUjPU4uVTJIVi4/IXI7QF9jNVxVbTxEZk9gUlpvQCNJXl0nWSQ7OnRGX282ZVNRL14hPSY0KGBVS0hdaTRCaDJhZ2dSOmxiNFtPP1pjW28mXkArciNOdEIkTjooUUpdTGQ2OThkOD90bVpTXiIlPWRucXQiKl4sQ0xQYFZhWWRYVnNyO1JpdWhNTDpXRDA9WF5MaDYtWScxIihoX2FucVYmZyomWyU4NHEhR2pyUGM+KUYrPFw1azRHbjddS1tbcW0mcF9sK2RfSGEuciRPaGNhPmZqNGRkbVFSTWNOPUNaLyUycko1NC83QFJeY1k7LG0sMTIkaTdSITJyMTpsai5jRVpBb0poKmpSNSxgQWFRYSxzZEwhIylDdDRLPUxWbT5sTnVnRi8yTEo9Pk1PYWdQIjdfJDBvPkNbSlgvPVBhZmwtQDgwLF88YF1PXCkuM2JuXmo8WXIhZ2UpYnNzNHNiXTFBPUsrX1pib1BoOkBAQDYmMicvMzclSipSViNWcXRRUzchOyNUXikzYFBgOS0jcnNTPFpvaGZhPVpPZ1xINkReXlFoZTI7PlBcWzpgQkMqa29ZSDE8LkVuSGgiVj9AOGBSXlFGcSdTM0FeKUcoSFNhJHM3JDxnWU5BXzZvRCVvOz9QU1VaLzArUlojQ05TLlVpLE9BZF1mLScsSGs+ZzNkWk5cbGwwWEhtbk5NZHNvPWYnQ1RpKy1xKWhKRD5AbSVVKG9LcTdTXl1QM2peKm5aWEQ2MWM2QC8wPyE9aSg5KypCOzQmUkJlMiw4ZUlaVkdbYkhNQGkqR3A3XF0lW2VEaFYnVGdnVjhgOGBKRSMvXUNBQi9eNnFKL00xcFgiI29MVDkqYmJ1UlFmJSQ2XHNTNjdEMChgWXBMSiRWN1UsS2tJUVMtUVB0MyFcXC1dYkJqX21pOzRtSzRUY0wwdTkmQzBAa0lrNnQ1SCZfNmgoXyRqTlZmanFDPkdOMG9PUzBKP0VvT01hbUtzOzEqMVA3aSInb25JOnBhNzwqc2dYb0FdOiJeOHAqJ0A0Sz1sJmVBZCdmIVJtZG9IKVx0UT1zdDtYc0pnKVhNSkYyNz5POmBFRjg8Y0kkY1toTnJRKVo7ITYqTkRyPm0ramdrLy1oXzNdOXFvQ1NORyw8Vm05PXNSVGgrO2JqKFEncDFgTFtIQTVCRCJSPWxlXGxTdVpgTiY3aiZXb2RdOSYnUDs9SiJiPE4yUHVkdGNWVEpSOys/YTFCXWpUTkYrMGpqNUI2OG9mRzFJNzBGMSwjPTNULW5ALkIhW0EzPj9RZ1ZALHUmbTM6bUQ1bUtwWWdbSVkvMSVsbGUlamgpZSIuYWRbVSEscU4sXnNuUS1ea09tYWdJPy81JHNvWmNpZTE8cGdBUnJVJktUZVpWSSJhJTBbYz5wbVcyLDkrRENYMzYoXSZIXXVrN2pUSF5zQDdGYW9JW2lsPCFrVVNWOWdvOkdWIVZiK3IjPGY1ZWszMCIjIzlIbk82XE0yXyoqY2QuN1ZPclgjXWFDZnIkQU8oXE5gWCtyXClbLC4nRzBIZVkob0FQQS5EVEMqL2M3akEwbjdsNk4kVldSdW1PSCZzaGc1X01yJlsqNzRcNkZYWUVAWUUtP2pXVnRdc1xMQkFfcGEyNTRaQT8jJS1oJ3BOcCU6UjhEWzFSZDYjTDxeRF9KUC5HZGJlRWg4Z2QmclBsRUJfVTQpOS41QlYnQlBgUFEoVlMhYF9Hfj5lbmRzdHJlYW0KZW5kb2JqCjMwIDAgb2JqCjw8Ci9GaWx0ZXIgWyAvQVNDSUk4NURlY29kZSAvRmxhdGVEZWNvZGUgXSAvTGVuZ3RoIDQzMjAKPj4Kc3RyZWFtCkdiIi8qPWBgWjQmVXA/WkpaImFgLSJANW1pKmZcYls+L3E9UStcQkBpaFQxImUtbjFPLzw8cXNaYTAuYGhrIl9JQ2dcbDAsWVA6PkFhUWNsMjhPMSdkOWxZIis9MStpcnNKWidDISMjTkY4I05rP3BfMGouamJzM20vMCIuM00xXGlMZ2FnNm4wRW1FQFRrLUFOTVY2aWkmNG5WUHFucFg2J3Q6QlJFLzQyQWozMUBNRyNQTC1qOWU5NnEmOCNPYyYoYCFlL05aJks2cTguLUBkajFfVnRcS00lYmIqaFEzXytKJidvIk9jUVBBSiUkQyJZaDcoIWMwMEZQYDFRYUFFbWJxWj01VEMtO2leLiMwdUZTJyJEJ1puLV9CPHI6RmxaQGpkMlZlSU48N1VSSGwrLGgrU0xuLlJyIVpJPzhybkZRPHM1Rz1ecC04bCE4Nyk2Mj42SFB1RyNlOjN0cGwnMilXQW9cTlFfNVVgMFpOJUUwZ0pbLzhnLlVIOG9rYGVtKD9rIVQ6PEYraW02OVFeWSY+bTxuL2RLJmBSLEFDJzU/MEFnTEBvcjBQOW47LGpiVSVpRnEoJkclXmU3PzdncEBkbWBWQ0ZXY2MhZ10iZGdvXzYiKVY9YF1OTVxSbyRldFU0Ymg6Q3NDOlVFTUYzTGZQTC8lITZDVS4pLG1JSWhMQiYrWnNRc0poRjJtTXU0QCxeO25QZ09HT0RyNmlIY1lXRlQvJV0sVGBqIlBacWcsOm1FSnBqZV8uYF5IW0pxXF9wX09cY1pgS1YjcS9nZSJLVGlvaiM0aUpvaWkkJnVHMUMsSFdAVnNqP0IraCJUSEI1UHFWJjpzbFYoNmMoWE4kKHJZdGRJXWhgWGhBSkBIPm9fRTorYkJJbWBYcWJtbiI7NV9zY0s9S1ouVm5UaWM3XEYjXzpqOUtnN1IkZzY6VTBOcSVZUEI0M09cKCk1T0pcbz9HJnQvbTVgOkZeLGpeNCJOTS8hbmZHSzhqL1hhJiZZVTo8QURCVytHODRNP15uXDE8VTI3PDk7UlczW09yIktYPj1xSFlqdVxoa2A/JUtKb2xHcGhsKHNgSlk5XG1dPV8/amkvc1g+OFs/IVJbY1dLWCNlUEpxQC5YO2NCcGdHMERDdT5ZbEtdaU0jUFpjJExqWHU/ZHBgMGtVMSp0RWo2ZClnW09TOTwsSzwnRVA9VUNOKWRdWy48bjVmTS1uT2EyXlRuN3AzNlQodUQxNVYpRydVdTVSMyVrQUVdLCZVZyViXiNaTmJeKzAnX2MyYSpnc2tEZ287IklsOm9sUis+NUJBcXFWRmMjN21eW0A9bVZHaDBBXjhdNltcLFc8LiZRQzpXKUxnXiFgNWZPUiUkdDJYQ2xrbihfVyFbVklDUFVXVipZZmE6JChyOClXZVwrOjM8M2U/PSI1KU84MzBfOEpjJWNxIiQzNigmdTlkZVYoZUM0XDRbbUE9QWosVE0zKjErUVd1bUBaOEhyaWQuOlJkOkJEVHMzcko5NzVRc3FfUW5WRi02cC5cIlFFNjZbbERAIlVAUkEoKygtJl5RWlxtazhUI15DcyYoNi5qXmB1L2lMPj88RGA8c1prKEsrcU5ARCpxWytxTGNRb05iS2tAUDVQaC02WixsZ2NQVGQ0SD9kaCZwZiFmRUkvXjhcVj5NXDRJUDM2UTlpU18vWmowTSw/JE5RY1YpUW5rRzskbWkyZlxVQHRzL24maTteQShaIy9fO1dXN0NnTzo2UkhYKUNhN1UmTFw0bUlEdS4zW1tFcSpcJXBaVGZBQUE1PExXX0A5NlI+TyU1RDlwbWtHP2xSIUBDOlNPXUg9ZmFbSjBiRzdUUjFQX1JFQVJlOzc5NFBrbyUoQj0vPzhBSTw+bXFXITNrS2ZvZz1iJ1ddSy8uVi1lTzxDNTVEKEsrXyI+U2MhLDk5UjRbUHVUYlpnI09pJ2cjKU9dY3BRIXRkUEFEMloiNUM4Lzg5W1hoMmlxczxucXBEIUc6JVxxPyolZVxaJjhkJ3VlR2ZLO1ZRNVIiQVVZaDwjYSknJmxcZV5KbCVVZUspaWNkUFAkO2c5RERCVEFmLUhoI1RZRFRBVGQyZjhLNGdFZnJjV28qOkoiOStyQC1pPW1VWXJvIk8xbVxTZyhpZUVISVxdR2ZhJ1JVKS49NGtmQD9icilVXSVWT0ZuVFBCPEUuJ01nRG0tLzckM0dBLyxrRihuMy9mT0NPPGlzUzU3b09qOTUnR3RhPyJjNlFDOCU2N01WXl5aNGRhU08mJENsYSFbO0BuT1hFU1hhcjljbCdRJ19mUzRtQzFiIyk/RDBeZE8hSSFGYC8+Xjo2Kjt1OW5SIUkmPjwzbiRPUV1qKilKclJhYi5nLiM3R1MwaFkwXWVFS182QU1GOHNPUTQ7RUNBMSUoOTNqZ2c1NFxSJloqcSpmdFFFTD5JYUs1U0ItIU9LPWgyRUtcXVA4XDoxRkY3PHUrVzNnTSE7RyViW19uRmNAXWZfTkUrWTcjb3I+ZEFcXl1MaUZuRi1RLkwkXVRmMkZpQjQvOW88KWQ9JkFOJUNLRCsnakIpW2JJYitQOlQqWWZdbS5rMFREXFpLck1Sc2A6LVA5RDI8PiFnb3VsVHRPLlk5WUhNYyUlaDQkZC5Mb2ZBKV9cVmkzJDQsSEgrSC5OYEUtUFpCaDpoOHNtO1dqaDk+YVMpPVoqczpWSjxAQFgwOGJwQGIlS2tLT1dCZFslMmFwXXJCMHFxKENCZm1KN2QnV3VwaC1dP0RiJz5wYT4wNUJfdCkoZm9jZkBCKGcnYGljT2ExXDhkKUIkVjdVPlhDI0lZQFVZcj9BbEooJCtAaEAnR3RPaSdfTz09S2F0LCtPXVI5J1pUOXRHZWJSMj5USSYnMUZfMDsqOXRCIW1hQWVPL3A/aWlqMz9pdXNUMFxDNUNWMyc4cWYpKGQ8UlpXQTtKQVhQQV5JNCo7LixRM24wWFBuSk9wVjpbPVBbXGk1WSljJ0JubyEpVlRtTC5tJl8rMGRLdV1VOyFzKWs0c3NIYzJlNG0hW2tcXlgvI1M3RjUvYCpnVTdTalZXVlluZ10haWUyVj5HMlolcVJqZlYrQlBSJW1QP20sKGY0PmktJkQrdSJsNEU4Tkt0NGttLDUjOlBORCplWmtgbGhjYzBaNzckIjolUEg0T0JSZT1LUDRaWy5rZF9fOD9Ec2llXD9xMWVYa0ckRW89UWhgLS5lN2lZdGpqRj49WklsamFqdF1fMDM+K05NRFc+bCQ1PkJdQzRIOzg+VTsjTEwnJSY+KWhgPk51QSdWRWM1JiZoPm1maSg/TjVTXlg3T1A3NUloMGRpL0k5X3NELTVuUHMlMk4iJzU7KTRdUC4/LSokZzRROWlgRCZLKigmJyIzXiI4YCYoVldfU0Y6P0ExcFs6PVQmLVZAXVgtNVZUaVw0RCIxJG9xVUArb3AwRz9HNHVyX01sa0leQUIhYyJXSVA0PFloIkdGMWY4bVw/Z2Y+VSMsVzlXVF4rZGYrTipWSlVlbGMjXEBfTksmK0hGZlBfI1E1LWdeWSklKDBNKiYoKWFQZFVfU2hIMFVxOl5XUlhXJi5eIj0rS1YhRDUoJy1wWiRFZEBdWDYvay9CZiNAdDRwIltgY1I+VWRbJlxvRjBJSWkmO1NCLUZoZSw4RzFRMz9MWz5gOkc+N1RoIzRYMjw5MCVmVj9DKiZXSXVqTjEpayNEcEhCOHAsJEklLjEyYl9NM0hSSjJiSkg7TkE8SF87OkYrXSpZQ2tMIi1cRi1PYVwyW0dwWmlzZGk/XVBoPyUyWVJcdFxeaSQiI01ERGYkbGhKRWNXPjBHKlUlOkhdTkZTZl0zZkdHUWFYTkEoQ0JgTiNVSjdpZFdtS0FVQl8+VVNPJWJRbjIqUltPYmt1US49YElZMU1bQVhsSktPNV5GOyVLMzVDcUIyU0UwVSxwOlNUPjI3bm9SY1lpZ2QpMShwLig7JzNTY2laMlpMUGtcKj9iLk5UKk1SSFVcTGYnNjMqKCdOT19xcWxtcTUuQSxvPT9bLzJJN0JyaUlDQ2EuMCkmSmJEJzM1V0dxZ0NFViQnN2tLanQ7YDBZXk40MD9bPT4mR2A9cGslJDsuVTsoMGdUYENIJVdhIzJHTjM3YStSZDcsa0liWklscGYyMm9dJ09xSGtxJzJsK3BqOzRCZjpsb1VzN2BFPFNRTEJUWiJUXDhAbG1sIUtaKSssLV1URTxscWwuKWFDcmBuRFk7LGs0XnA3WkkwZTlkQ20vKlhXUSclZ2wpSDhRLF1YcypDZGxNJEhEMlxeY1ktW2IoN3UzITpLKUtmcDhHO3RmRSc+ZE5wb1xdSEg/PWRLLWxoYzchRkhQLUlFVDZ1anU6JWY2aVI7I3RvXFxWPzVrL1ZDQ1lxa1lhOGUxYS1Ca2lzQVhCbGdGOFtFZjlEXDozISxdNnQmbV9ZN1hOV1RbOiZYI2VTRmwnOGdsUUFraDVhXnA0PzYxR2RLcDw6SjVmIjZBNDpqUikvanI6ajYsSlUiSzctX1siSltnYiZSWm88Y0hVLT8xclFLNE8zPlRhOE5dRCZiZnRMYVsoWCZrNk5mO0coQUpfL09cP2Y8JlNpLmcyVkZoS2ssW1NXQHRIaSlONC1wS1dscytEMkhzXWwjTyNpJUtrWUJPZSYpND0+JVFpYUk7YT9gQXAsZ3FxIVJwSkxjRD9jOmhlVGVDaTRUXDZfUDtDcHRaJDdtL11pZCplUFsqXDNNSl49ISRISk0yKldAQyc0dVsrcGxyb1RFUGM0U3IuMWRYXF1LXjJPWVFnKmpBK3I+S1dtVkhaPislLnI7QSlwOnBaXVlgdDFaWD5MWmhTQG8rXm5nMCY+Iy80Xmc0U3NVQEJUXVhAbzxHcjNqa1lwOGNUQ2tOcmFVRi0hJjJUSUxYck5XXiVMI2dKXm4oVWFNLWMoPk0hdUkqSDkwKjVGY3I2ZDxGVGRFMUU+c11OV0E4NXAybVxCa3FAIXBeKF1uUHBeNnBkU3BTUmN1IyRCSTFxVFwjQVNsPC1RMjtzK0EvPjUnc1YsPG0oIkJqMEx0aC1pa15GXU5iYVpEW2IoODBOLD8zRUUyOShVWk0+aihFcVRqXyF1LUhlNz9SVUpvcSVQbD5JTFF1bkpsXkQ1QzZaSiZAdGsjUzFTdWtiLmMhODJnXlVGU2ksLTU9VlYqRFdnYXNSY0NXWEAhV3MocUAuLmt0IVYkb0NoYG9paXJtQWFjaUM9amA7KldlMHAhYC80Okw6QWtKJVlSR3E+SkZnIVUnWUJqNTQjKyplOF9vaipiR0kjYFhzb0M1L2wmZClQdSNOKiMkW1JEdXA8LG0tQDFWOEJHclYvVURtRyVqVzxUVVI+KD1nZldgY2ZfNHBnT1JPUUokRDVcOl1SPzI6Tjo3Tl8qOWFXazQsPDc7P0E5WT9PRjVXTW1fLWNZM1svcC4+cjA9K1ZbcXQwLD49TF9uMztSMzoyY0dIRm84ckIsUSw+RUc/S2pnIl0kJD1mRk9GOmg9bmpYKkBxR2xcO2FsOiVsaSFDPVpxamYtZy9ZSWtaJy9FcHJwSF5nQmxlTCRvX25pRGgpRGxvVzIoRlYwUSRGSEh1UyVBKTU1Im8kYVAkP1VDPFhCQ15FcGApPyhlS3JRLWEvZG9MSlguSXFhUnVbaD8tbWFOW2VLU2BYNCUqbjlFb09uY0tCIl1eXmMjdVxlYE0rbm0/OFlgYyh+PmVuZHN0cmVhbQplbmRvYmoKMzEgMCBvYmoKPDwKL0ZpbHRlciBbIC9BU0NJSTg1RGVjb2RlIC9GbGF0ZURlY29kZSBdIC9MZW5ndGggMjc4OQo+PgpzdHJlYW0KR2IiLyk5NjkuJyZcZFI0RkRnWmgiNjJ0J1dVYUpdaCs+Jlw4UE5mRWU6alZHTS1DXFkscTQyU1dWbEtJcF0pSU8sZzNKXy9sY2MhQTRmUHQlNV0iJUZha005TUxWYCcrIm1ab0gzWkFOKSkpUEUxTFFBOlxHSS5tXUdwZjFAYm02OiZlYkNBNjZJK1I7SkJzJltuLnRjZGZHT2FqOiRfZjwuUD5ZUGsuYTk7QnVONypuaTY0LDhrR2VWPDdPdF9dT2FpX3NAbU9CVkpZJkouajVuVFIpXjBwQDY1RzlMKCE2SzxYVTlRXEMpQSZfTkNUW2lsdUkwcWVXR2VPZWIvPUFHMEFTOHAhUDZhcTBhKU5YKTlYOjBUZ0xAMHVvISNnJ2coc1RjNiZTQExnKzstP1chOSdAckBwMVsuQFk+LyNkJFZwalJ1SzhgLDJickMmSi5CIi1vPFdwIiEmZE04NmwlOmpDSDdBVVNKSVJNM0VYWDhCcT5DZjwoUC9bUm9JZT1JdHFORW1JRl4+PDZHVylwPD9qWGRORV1wVmhLcFI0N2wpXCNtRD1AI2xtKHMqWzlMNFQ0NV9eIys1VTI7OSVpSjlKM3BSXm1qW2B1aFFcXlpWa1EmNFJQTHEnR19iaSwva10rK0szNyVwPUs3YWZhUmkoVidAZnA9UTwxXk0iPGlYUVVCJjJFV0IxSlxWODpFPDttO2Y0bVs4QWdIRlU/JCZmZ0FHaW5mV2lDMCxgX2k5QnE7Zl1JXCdHRzhvbiRXRUpMIkVRN2AjZTYkNDE/LShoPU0zblkyT2hLMGA3MEQ+R1skNmBVWVNZTnJPMU8wUCFXVSpaJF1LJ0spMFpHdVopZDMwPywzNEM6IUJEKWEqJ0pILEg2K29QSDAhX1InOShQKChYNXUvZS8hck48NlBkWEFQaChyWWMiIzlaYi1JaENUaDkndSRbPmpOZkVeOSotPFpKVy8hdTg3NmYhK3VbUk4hc10zRiJsKistVDAyIV1SPzJLZ1hvajE5ZmBqTEJyLlgxcm1jcGBLRzJNWURlZmNJVS9Xaz83QmZDIyxRUWJaRCUnYEdpJkBgbSJuVENPZ2pISEApRzBHIyhIV1FLZ3MtbXBJPmFZZShFVylxMVI7XmkqTnJyZE82Q1VSX1AuWFBwQypsY1Y1XzM4PihdUXNJRzBoTnEyT3B1L01TSk1eRmBgNzJnTWM+bjdoPmM4Rm0tL2tqMWklNVdMZEsqWV43Pjw4UjZQNSY9YitvbVhZLjk8VShlL0EuVjBzV0svMHAjUCoqZlw7LExUSiJaKUxbZSxrM1E8LWFWMVZsPzRANG9MXUBiKDVRNWUoPjdHY3JSSk1DVWQjYy1bKU81KktdOF1EWDBuJSZLIWZEO3FbWWRdRSw+Zi9qV2tdNClTbGwyTVptIy0+bGBCMCpEU1dCQl4sZGo1RiJZbCw8Zy85PWM9K1ZxZ01ZJ0dVQWVtSi5qTE9pX3JVXCVcMFxZJVovMTE/XGIsViJcbDg4TW5ddFpiJG1UZykwREVdS18+Q2lqZipqN2hBX3M6VCVKLTErcCRdczZXJ1wmcU5zTlFYUl5cWSI9QDFUKGROYUI4ZkY7RCE7LCVOMyM3WXJiPDdFYWJYbl81KVkqcW87OCJIU20rTmRfMkolYyhyJVo8cSw5PGNDKEIyTFtxNmRgKEUycm5dY3VOTWppMHJtRC9dWG44cmg8Rkg6WmJPN3BNIXFdbz5DSmgkblZhQ1BAW21hJilmOVI6ZmVIRV0kZi8hW1khXjo9J1thSCtOZSYkOTVSM0pDXz9KLGNBS2ElN0c2SixDTGQ5KWIkXDc+RUVmM1BDaSFbPSVLbiFGMmAxNDlmZVlcY2ZgT1dwRGIycl5AXVdnYT50JjwrJ0AmSTdsMS0iKFY9Nj0wJ2UjJFFkTVVDIzpQWTw5P3BZSnVHcmpfQlksXF1DXy9DcVZsbTxKXj0mRzhIIjBQPSRnbnVtXi1aUV5jTzFvYl5JMVkqTSwuVGE3bm9bVmRIO1REbTksQlVXNGVOcSJnOTslUD5AY0xeSFYvaS9FI1htbjVCQmZCXl4wW0E9cik2TmtwcFJyRGdBVG5bQklCTyNFcWpXOkB1OzVVYkFcT1IzXVUwJUJIYHQ/YC4+J2AxcGIzYmJKVTtOIjRbbDYwa0FvcyM+Miw4Y05SO3BTcSRoXT8rcltgMiE+cTFIRlIyUkpMZ2NUXzUsUV5YTWtJb2AjKmtoPEYtUUFYQFkycm9ZWixzNDdyWmBoMGpbSDFUSnIwIycnZ0hFZzAvMWQ6VW01Wig1RjJpXCExbSVoWiZFbj1JMHBrUFk/YiU3ImhuP2JgajVWOmAzSkU0MXAxO1cjVmI+Y0NeMnM2b2chQUxaYlNqJD1pK0crPHEtOFlGLjxScE1yalNcKjJBL249SEouYTM+OzdjXkVNZSRjaG9qZzIoLV1WYmEzVy9bXkQ3cjZSRF0vYzhoZDwsdTRIQjxQaio1Zi87MGNHYUZlZ1guXm1LZWo+PzQlK3B1SlUtX2sqSDZCbS0/cE4jUTZ1NDBlNHQtbUdLQjRvZDlIOF5VP0NDYmRkaWQ/TClOOW0uLzE5bTNnbjltLl5Bb0xdQGJRYyRDQVJbbTNvXGhmIW9gNCJVS1g/MmxRaU8rJ2FdcEorb2g1MFlPYGo7dT1cMG0nLFlaJT09WiNyI2Y0LmVwRlhTWTIyTDQnZkUjTylJMVE+MCg3Wi1zVGFyQlUsbnEhaj1zVW9cSlRecnQzPFA4ZFcsWjkhRVRkY0I3KzdSVUE/azkjLktiJG1wMWNuQyxjI0I3J1BDVCtHY0xdLil0cDBBPmNsIzolZk9hK1I7XVBGQnRjPnI+MWhsQk0kTWJxZ1cqQ0I1aVQ/L2wnZGpjZGddZmIuaTVBZ3Q6Km0zSmsoIl5cTDZWaUYhMlxrQltcc1ZUQFY/cSkwOTM+VUpdam5IJ2M6ai5CIU9GMldNbTxFLWBIazhGLkBSRksqQW0mQmUyaycmSkU3USJTcyNEUVBmM0E1Y0AwX1lJZkhmUGY+az9XP1hXcjhYIUYwOzpVLjFsL1VWT1tfXGUrXk04TVAxS1k9cC5cS291K0MlZlFXaEVsTU1xLU1lVVBDS25ebihaRlY6Rlg6YFJgRU80WGA3IlE9XSZVRD9maCRsaGw+NTZHKSklckRhVk41TnFZNmpDZ0otZSthZisyQyZNakZqKE8+YXBkXGUrbkk5XS01LjBZJEhabTdjLHNrUSloQjVqLmcuIWJoSWc0T1taWyNeSlhoVmJAOXEjVGZAY0pMXjQ1TyIxM3VRIUIyVXMzWzJaYzBWTE86b1hyLFk7OD9NT1dvIXVEZTdWJ1hjMipXIjBwJERSNzcmbVpfTnBcQGxpMDwtbjlGT1tHV0NlImVdKkk2QzgqdCk+czdFXF9NSl9vKyo/PWdoPEYrUm9zR1BiOzAtPlVpQD1OLXNhXT1sTTtTMFpUXllCVHQ1OGAzTWI0WE5hTD9Vak1nU1VKb0ozQTQvJTc4Q2RuOlx0VWVFK1JAXyVHLTZWZiY8Z3I5Kk0sZmsuU0whYmtCUmk2RlZqYSprKTJLRmx0Ri84R0Q0dTFELSVRb2pUZClCc0RCIm9zSnAsTGQwZmVpZTRHc3FIQkBnI2ImYGI/S1wocVZeUlJhO25mRXQ7YCU5SCYlWWZPazAsT1U1OCVSXjkpfj5lbmRzdHJlYW0KZW5kb2JqCjMyIDAgb2JqCjw8Ci9GaWx0ZXIgWyAvQVNDSUk4NURlY29kZSAvRmxhdGVEZWNvZGUgXSAvTGVuZ3RoIDM1NjUKPj4Kc3RyZWFtCkdiIi8qPkYzZXUmcTgwMWQrYTVBN2QrVT9tLi5xI1lmZVhRQ2o1UykwNWE6TkdoOTI+Z1MqanByOmhsPiwwPlwqOjU5I2BGNjdFYThfTCpuPEwnU3VPcCIyVnJtOWZiQTwicz4xXEJgQzc/ak0hJ3F0YTsxamFqXWM2YVZbWyFQXmAqIVFFWS4kLC1hLlVhL1ZgSz9mbSJVSVUxVUplcSslKVJPaUVdTTVoJmRMX0AsL1toUCZIVGQ7LWpEbWtwYFZAJFdWSVw9S2JZJUJAVFtabU0vajpsNSssTGskaytIQDs4XTMtS2ZCREMmITpHKC4kY1tzLCVSTlI5JmVAK1p0czMqPjhoS3RNM0ZCJUxmNWdWKypPPVVpazU/I1NaRi8+NT5Oc1pebSQjb2kuSFtnMUlZZ2tbVXJ1Lmo8Pi4kQGpaLDEyR29rM0o7InRsS1w0Qi8kO28iSydoSTozRydsJ00xc2VBY048TSNAMiIyV09OLFc9XGc8JmNPLF1SUkVCIVQ5OjFLaDApOFBMLEhGUThAS2xwMUhlSGJsLiJwSiYrSV5YVkl0L15PR1RfJVBUJSkwXk1hPnRnXGVidG5PZDEhPyQ+QVVQW0JAOCtHc0AwI0phJSQ8QSEjK2ErV05NXD9uYFR1aGBLLiRJPjIjQGZQckc0R09VJy0+bDYnKlJCNiVNVDwnJmVALkpxLHJhZm10VF8sbVloPjBhL15dJjJeIkM4JiNmKUZjaUguQnBCQlhVOUVtaWFRSlVIXFZIbzFScVFjSSYtQyUyODtZbmdhOVhURSFfOkdcS3BWL20pI0wvU0Z0PkRzZC5aWEEyWGlYXigxMlxfVWJSVmpQLF4/Ll8jaUJxKDdFdSRRc1dqMygtOFdyPlY3dEhIQV5qRG5WXCluTUFVXTc6ZzBQZVYmKFBfOnFiPEBBIjdCbS5ddVRYSjElUE0lZW80MXBMbVh0J1chZl5pW2libllxXWEyRnQvc2dgTWRUdGAjNl1WbFV0TW06Z0JbVjxNY2FycEM6cCI9S2ZzRzBZSz9mJzc2Pko9OC1AL2AvInRfJjVpajtJSW1bZCtrQylAb2dNRCsuM14wKDBJQzhrMUxzYiFmaTo6KkZVUUE8Ii0xIVhkakJeLzknUmMrI1hoIUprUWxAQVFPQEk0SCZgTyJrNWxQNiRqITtnaltwYz0/aWFjWSRGUSw6Qms7ISpcW0pkcU0pX1pWI3JTXXQlVz9FKDJtMyZNKmtNS0wkbGA6aStkWF9tbjdhR2xScTNlNFYicHBacUxmYHRRdEpCdCkmKEYqYCJpZjgsNVtbVCJGODRlJ3JoNyM1c0ApPW0hVyJOPSs5J0xualQlUiojZXMlVitrJyJeQmUwMjhdLHBlIzY2WHFTQ0BBMy8oKksvXjpWckxNSlFlUjNDWWVxNVEqJmkpJCJcVjszajhyPWplTmVkL140dEc8J2IlOypLXyswYnEiOFVsOFdrVDctRS8iXGtJW3EkXzc6IlVoL0FzLihxaWQ8cXJZSyJkXjZiQVBfODAlNDlsLT4uImc5bk1hZ2ZfZ2wiY1daWVI/QWU+PC4xLlNQKUlIajxgTVtoNiUrbi4xO2NGUjJBXldASy1jbFNiY3Mlcyo1a1JqJigtMkphKTduLFE2cyJUZTM8W0Q4JC03YDA8aV8wYDgzZSMvZTdxO20xIlBbdWQ6cV47b2I8WickTlJfak9idCZhSkloO3FJcEQ7W1NgWD5FSGpTKSMxcGwrXEQlbW87SStaQV9TXnNjcGRddEZzUU1sW1w0OjAhUFBmdVMtOV5BXGokMEpyJ3A/NitSLTdlXVcoN3AhKWpcZDA0X2JjRXBqYzUidTpwJ1spSnMjUUIjbSJqU1EnUWhcVlkwP0AtMm4rMUshK0Q2MS8iWV8hL0U9OCgxamJNXmBcdVFrVEBibmM/JlclU2BaY1JfNDAqLG1iNjsjOmA5TT1ARV0zUCRkP0I1TWgrbDpKVD0oXWdpP0NdKi5ZPm5mI11DOzU2LGU+STwsUjZZXFtTQSNbc3JiTjFZO3Eoa0EtVzlmQjthNVZqN0tWKGUxMT1DNiIzUUg+bEotPHJmMCJzK2ZNV1BWSlNIQz1nNllxJ1slLU8tWmpvcWpobDYiLEduXkRlLSJrVV00Yj9gKEFncGJbMGNZYShWJ0E9Zy8mLmBNSj9BSThoRDAuPXMlJ0klb2IlLCE3Z0kvdEgwYllzaj47L1Nuc0pKKzdOJi1iTkI7PTUiIW0yUEdaW2Y+JzZmYFhRUyJzbiJLQXRwQDonNENccTRXUkE9PElOVShIQj8pMi5rUUxbMV81V3EqXSsvO1ZeUDVCNzZINz9UWU4nSFEmZWIvYC5YUE1gR2xFLWVDX2UqY3IzJltAVkg9Rz07I1VZTSVhVjhNVWExbGkoQm9TQVJPXS9AaEIrOCUjMDwzIzkhakJCJ2E0bVhPYEVfRjEqbDA6Tyg2b1BbNkduK2hMVjVkczBBYm5oOi5lNnBgcWxBWFo6RE5SPW5JYjwtXUFiKD5eImJGT0ttNVpvKllgUzd1Llp0czMqPkZKUj1FZCphUyNIdVViOUpdMkY5XlMyJmY9YDJUYGxfUjM5a2dzJzMrYTBcVW8lNUttW0NybDFdbUNRSEElLlU5Rk03OltYNypcXEkiLCciQHRLNHBBNDFSaHA1cl1ocCdPRm9BQUg/NEowPDlIJURSJUhcJ0lMXjN0SjBjXG9MMGJjT0AvVFY9a3NzKUtEIiJAaEEsKEteWjQkJGI/WkZkVFVRXWNfY3QpJiRAcSstOk5vLz50alFfMT5mVVY7JScpPmlCKHArKEhhK1BaWEJgKyhLJCdZcEUwMVdWXzRNbGxrNzAvPGtcJyFdPzY4WmEnMjJbSy5mbklGbVEtIW9uUmdbSzVjI0c6aGZrIisiIWddNlYsVTNqdXN1SUYpZ3IvJCVELyombSEyaCQqXVdVW0hKXWk4LyxlZ0I5P00+aTQjJSI0QVV0JFhPTyJeMzZcTVtXXlhZP2wwJilkLDBcZFpvcEtqZC1MbDQ8LHJEISlrQHU0ayF0IWpobS90Mz1POTtoXnFjaDQhKkpHbUdoNm1EaUAlJDJGP1A0X2JFNyNDQSU9VXRfI1pPSTRVUT9TbTVDU0MwRFdSajBndVVkN0YlP05DZmVjV21sa3FQVDpcJEdCajEpKkhgTnRQNHQoYE9gSHVlNGhmMFtvSSUmPiY1cjlWRlpYPF02PGVrdEhWbVxcYmBFUkUxIVAnPEQ3cVskLTdZRWJWZjlpMm9SLzssPyVUVmora1QkcW5uaXBDcVkocldqa1VGNmE7JTFmQCIoKi5zOz5XSTVCKV0lbUY/QidNM2tlJUxESz9AKFYqRj50cGomKzpaI2kpVG1STi1BTkwwRjVfWClmaSRwNjU5bU47RSZOb0FwXUIrUVROZW06ajhbX21xNCg+MGV1Jl9NRy5kJUBUQS9TIU9aXz9uLFArbmovKnFvR083OEQ6VCJnUzZEdSFQRVwnXj1QT0tNKGlqJFxpOlU+PUcwImMqPnQtaDRbZEhZYUVpYSRPbkNRRyxPOSdeWXBFMDFPMFQ4clddLWkxNSlHY0I2WjNkNlRCV0xBcio5OzgsTTEwOjJKVGM4LytSLUMhLiU1b0V0QDNMTW1zI0giLE0zLi1lUjslR3VyTVgoKGBXQyRRb2o0ZnRORFRCaClJSyktIz0/Mi5wbDVLY0RsPGkhZiVgbT02ITZZRCtFQyM4Nj1DOFwqXnVoZklqVUtra0w0UlwpS1dIdFZLa1UyRV5wL08kLCUzUnJjIjhUVS5lTzQ9MTVRcXJkOGhqbWA9U2NWYGZEbVtlVUxLZWlcNCQ7UWAhcFlcWzo8alZoPE10Kz82Vj1TbE9pRUN1aXQ6XFgzcUQuaCh1UEU+XnBOYl5PQiV1SUEjUHE7OmxWYT5nZGI/IktDMSFHYyJnVTZOM2ZXYmVPWVNrZTlHYGVuUjhRP2k3RWU1OnVUZTA/IVhBNDhCaTBWWlZhTSlgP2VcKG4tKnBhaytMQV41Wj9QWUpYTDprR3VBSSFGKVw1Xk5kXm84JEBJImVZUDQ3ZWFOWm1YZ1A2Q1s+cjhUIy8vUl8+M0M5Zz9tPihLcVZtNE51KHRPLkdkWTxsYCFKLzEmX1ddIlhDMFs9dE1EJzFsa0NaOlgiIWNTN1slYzA2Jl5ZWyJQSS9iTyVKL0E+cUN0QXJgLE03b1clclleJS9nbFFsXzYvZCIxIlBSTSNpM1dAKEU3QCZQIiRTYitNdU9ATHBIWW9JQFxWMFVIJHNMaVI3NWMjaGs+LVMvLlRKRHU0YixJa0xgZSgldFdtajtlOl0vJ2hfJT5QLVQybjhcKm8pKTNOZCdFM21oSUZQU15ePl0mOUlZRiUvbkRhSz9eOWRBIzM7O2BFUDhAVm9CQG1rcDdYcUFXVDArQkZTaz0nLW5tV1VLYEo7ITwjNDtMI0g0MFVgbVg8Wjk3K09mcyctKlJfMylFLms6dS84NF02ZUwjMF5HPShxaFRfTyYsdXFBVy83aUkoPSJAZSIrdCRvPUNcXVRDczMoJl1xak0rXUZENUpCMGx1YVQtUCptI0lGLykuJmpbPDlvNSQxXzg0YEA6USolSCM2OS9RWUYuZT5pTi1DMlNMMSZxYlwwSj09QFJvLT89TzZOPkdSU04qU1o/MWNuOG8xSWcibmNNTWpjNW44UUsxXklcTXEqNENmOVBzfj5lbmRzdHJlYW0KZW5kb2JqCjMzIDAgb2JqCjw8Ci9GaWx0ZXIgWyAvQVNDSUk4NURlY29kZSAvRmxhdGVEZWNvZGUgXSAvTGVuZ3RoIDM1NjAKPj4Kc3RyZWFtCkdiIi8qRDArSUEmY1NxP1ovPVBHRCQ5O1FuKWdMMihUMGhQOkA7cSg0NmNNSi9eWklwLXJOUTVHISdYQUhQW2UyUCouNjokN0c0NycyTihYIVVNRl5UM1ZGKUwmbzc4QillRFIhKyZDWWBFTlAqX3Q0azcsU0hzcmksaCRVQSZATiYqW1NQTzlTKmBrZDdQZixMV3RLTGpuZyMnZSdiITAjUy88azF1cFRaRjxWI21wXyFRU141dU41PUE1TStgJy00Y0ppI29EVkg/S1RnKjdaZiQ3LC5wQiJVTSQjZCJmLzljVC42VS00UV9RPC1GUEtRPkRDRTgzO1dHZWFIaDNdKigoOChXS105R2tVZjhBP0l1UTdIZytjNmZwSy5fdXEhWnQmJVZbOiwzTmpFPlNCX2g8OGwjRWtlWlxBMEolOkxBMUhaRDEyMCduUGo+JlpxJD5CTGViUURsPjY+UjBdRVVrJmtBXis8JWtjZjE3JCsrQjsnUzlQNSMvaXNiU2dIbyRcSEw4bzpdJFpPbjMsVyhUPCEya0lFYlpcOW0vWFxUV05vaCR0Z2ZtQ0dfZWU9R05iUXFpKilsVTlnImZNPy5wSkJeQCpISm0mNzM2b09jTV8/Q1tCQ0pTdFEwZUpGNnRnU1lNOmdGOStuZ0YtdXE6ZGlaZjRWZjdpVyNVUDJnRjFfNTdtLU5qMEI9UiRkbEtQb1pxIldVc1g0KS4icGo9ZVo0Ykl0STpYPEM+Xk9HcGYsUDUoOGZiVGplLCVyZkFVMmxuLy0lYCw0RyclbFVeLHJAPjBXdS5OLVw9XSwhRiIrImdcLWM4ZHRjRGAlbWM7SGk/VjUqRHVqIVInXTRsL25rbVs1NUNnI0pGXG4uJjNlWF1wZ1tsZitCNm4hISlZYi46LGsvPDFmXkJlSlhcMS5yZk9SWi1ZNHRJOTxrc3MkKjQ2NWphUFZOazVWbSg2KiprWkBBW0U6QjtQOGhZO0FiZEtbPV5EKUExUjhqPFMkWSc4ZDsrR0pUNSdBbzhqaVtJTC1oNixVcyMvRiVrKUIsKHBIYnJcOyE+cFtdZWRwTSQlLm9ANUNcJWdpcUEnLGJKLE9KI3RPbG1kaS1uQGpSNi9AakxIWlFvNXIxO2xwdW5DaTY2VzpmJE0uXVUzN19LKG9zJCUsdTBZK2c9ImktUFI2YFJHYC5dbS1UKTh1PlhrWzgrPiIyaTtWLTElOFphYS1hOTZnJm04LiNecjhHZFA9UjlwNDIzUG8lbXNQWVImXF9hS0J1UUFuQ01xOypkaE0jVixpUDJHOWU3Kz9HNlAsPSQ+YmUnTVUnOnFBI0I3aFBUWS4qcGlCLiVKV0QxOzhZaFNqcyg+byY5MDhqLkpnWTpLIWlnTCYpXlg4Jz0iRTpiIlMjWlNbIiUnLmY+ZCg3ajY3YVhWPjM7amJWZW0zNCU/ZnBKMCNTaURBKS1IKWAuXGV0VXBAcWJLLD9saGZHWUddQF0yRCdxQyleRk0+SkdMWzNxQUElQSg/NFQwaktmJElVUFFUYz8nVFtwLylyMlomYWpTVCcmaXQ+ZWNzZ0o5Vj1sImooYU5VU1ZMZkQsQW9FWmQtQnIlNURqOzFcWWtJW2lhPGIhMGJmR0I+N1s2WCReWF8mbls4WD1KWkQuVV1Oc20xLGBFckQ5bWRgbl1tKnQpLkM5Pi1lM0ZTPyxsXXRLM3UjXV1DQkh0I08raFQna2k7XEBFNG4rM3BjdVZHXCtXIj9ral8pTydfZCgjZFpgdVgmZzMlWlMrOmBgS2p0aEVEclU5K2lbVlFwJjY8TE02TGkpR2JoJmNsUSguVj9DSWQsOSdsLG5AMGkrPmJCSmJyP2BTVE1wYEBgZVdsYilkSEsoKDglZ0I0ZFdMamJoXkprSHVYOy41VzNSX19fLmdhZGBwVmIoaCNvNnAvLEc+XD4+YjpMWFI0VS1uNklDOCpNLm50I3BibmJmSl5WPFIjKE1OKzA1XlpMLlFoXT11NjQjWE9iQ2g6UkdHV01QPkUoR0IkIWMrMGcyM0tHMUA5Mk1GUDROZUUkbjYiPzNianA9SVE3Jlt1JVJnIVVtSlQ+TFZPJylTRUxFb2JwZmErRjRLa0JhQUFtL2sxP2JkYSFtWz1vbTxgXTlmc3NGJmpJMFsoRFs1PnByYD5fUi1xQVZaIyw/SyFsKjNYVVNMPD0uXzFrOEojaS9SLlFnV0xiaStHKCQ8aGdfLF49Qz9wJSUpTzk8M1paL0NNOC1DZkNcZUhXQlMuTT1GSC9yLTxGaTNeV0ZRbiJyazJCMl1UWzhgXXM2KFFmWiw2UEkjaCJVNm9YdWc2W1BKMXJvWkNVVz4zYiJSaC5yK2tMM29fV2YmPUFzT2M2bWJPUDdYLCVDRmY1YEAuWnVeUjlwN18zWG9gMjp0V1h1ZnQzIUNiZDFsRjZhPTNQVTlbbzZkY2E9cUAjQGI5alYrZidIc3RjTF8+ZSFbXzVwRG9PUUgnXk82MUMlOCcvRVRIXSROTmdTQGI7MiRUTVFDL29UVShKTltTTDNYZ1RiOksyIzpoQzhlXzlHXkZKPS9JOCEoMDJUXjgsMV5fUGc3dEJLMG4sbFtfbUtGTmspcFpSPyVIVTVgYDNsX1w1YD9kSTwrP2AxcGtTKUlUdEUpbE0+KjUiQ3Q8MD9HZXE+NmBYcEgucEZbbFxTWmUzITNQVD9iX0dJPiQpQG8yIk5jMGA7LC1zN1leVVMmXUhfNz1gTyM0ckMlU0duUihARWImcWprNG9kc2MlUjREXTE7Kzc+TSh0JTsmZCE3OmVWOUVocTNIajR1NGovXUZmaTo6P2x1cUEkLEZZP0FvTDkhOFUxN2dCZy9vRSw3TzU8YCpnNipNbkFxN25ZMShcPi5IOy9UJT5ROyFlQW9ENytOdFNJVGJGa11FTTdiZ1tOIjlLWlEhMj45aSVFMCpKMENXbWxrcSE0YC1RQTJ0TG84LGZeVitJRSosM0BJZ2FfbVBYZXVJN1RQN3VlLztwQ1c6O0o0UTkvaklmY0NcUTM/aTY3Ri85dClSZHJhJyFKUUw6Uj4qSSFjNzA6RSRtbSRhPT08LERqXV0sP1IkKmtxMiJQdEBeTCgwL1olKCg4cFVTRT4qTyleaHM6bEsiRj9jNFA1KGRQQ0tEQFVQJlUvLzhfNlFiL1xzMkFodHVLYz9fTT1dO2FLL3QrcElxRjEyM0BzVyZXYlohcVM1cTw8TyhQWm8rQl1hczpGSHMlQSY4bTJrXXMpPTBjVjBVNCptTlw1UixEUWlUYyhKKixeSGhgYW5zUyohYl5WVUAmUTtCV0U/WSZcIypyOXBzR3BHSEBxPnFtSGkwTlMncDdtIj9yWmxtN2FrWVVsPWs1UzstMSNyN0RYJFpRKldMcDgzbGgxRUkiTUVWUWpUazpVIT9YK2JmTj9VNnJCayhpaGxuKlI8WTUjUls6K087ZklpLXBSMEZ1YkhLRSlfQFooPm1jaGBzNkQnMW9gKEAzQFxBX3BZZUk/Nz8jOWlxImdacF81ZGomQjZdKSVfUDRoOCJSSTJuJFpMYTgwSV5wK1Q8KFdzTFl0bm5OQWtwcz5oWCtrV2pDbDplajNPMVhoWjs8YV86LG5MND1SOm1icUBcTy1qMkJFRXQpZWpQIihOcGIwNERfazVsWEJSJzBrLEp1MSxVTFdRZ1NtcyhLKyw2Kmo3XTspSE1tJDU9ZUQ/NUpyLlRvXClFLSZiQG8sOEE4IkZTLyxARTo1LCk3ViM5P1wyWkUzVjphK2FaYzlrKls3aiZML0FhO2NiSDA5YkVlITU1dHBqcUwzSS1mNSkkT05KUU4xYDdGVV9JOWJRLDBRdWRpXD9BJ1sqVVtATFt0al46Sk0kbFcsNm1qM2BOJzVKMFV1Xz1TYldhKF1sQlNoOFRsMyMrXGxJLidkV29vKls9M1ZCb0YiISt0YXRBcEY3Zz9GNFYsJ1ticG1xKmlHQE5OdDJVb3BwZ29vSitnVjRyJjRaUmMna2M5aFY1ND9YLTA9NDQtaUUxbGQmdGokQ05hXyMzbGFuQ1o8R1ZBSGpfWGQhVD10SG9zWl0hcEdbKGtKMUJRT0VgKC1QXUdnRFYhVDkrZjQhRStfX29VMVxRO2RGWDBUKWFsLU1yZzFUS24rY3MxTVwkbHBETkUjK2JLNz8sXWlJb1g1YDopP1BrNiZvLmouKkBoTjg/Zj1pMkM3Q00odVl1bz5UQ1g8PkBwSE1vNUcqQiQhNU1BUUZbVSc6XG0qXmY3XU0mYDlUQWIlSVRYZnBEJycqLHI8InJbIT9DaUdpMC9jNEgrI004UUVRMTFvRilfbWZzT0pqLXJDYCptQkgvai8xX2JMTC9jK0lqY2AjJ09BPkJFLko9JVJkdHRoQ01wVVolcE4pJ1hiS3E3O2NjQzRnQUc6XFVWLXBtREpQKGxNNW1zPlkrKi1BQlFLPyZRLyQyQGNHU3AvKipoUzFEVkZFVzBdKi1HTHAjaV9Ral9zclFxWihAclsnI145LTJxWTsqKiNqXDNUNjY8XTpESTozWTtBWGdILjdjP3VXPiRqSiQpM1gsVkZBb0NvSmtHOiM3YkpsK2U3bC5lbTk2Y144SyM5Xy84dDxtbG82ZmRyNnVNI1RHJy03NUN1K2wkUyk8dTpxTGVZWC1aIm4hUSJuImpZODkoMUFwMCcrQXQ4RytTNnMuJiNqITI5SmZeOmZuZk8qYEFnQH4+ZW5kc3RyZWFtCmVuZG9iagozNCAwIG9iago8PAovRmlsdGVyIFsgL0FTQ0lJODVEZWNvZGUgL0ZsYXRlRGVjb2RlIF0gL0xlbmd0aCAxMTEyCj4+CnN0cmVhbQpHYXUwQmFfb2llJkFAcmtrMyohVWMkZCw7Pm9eNEdNbzYzKCdaYF8nalglLi08Z0pxQjVKQkwiWi9kMmBKY25QME0pNDQ+SSdaV1guL20/REolbCdbJkFfYnFKOHBDQl5hLCRSPyw+XiZwU1olXTpJQnVoUlJ0bFcmMWFRckZfRSpzMTFpP1NWbU90VTdrNGFoamcvOU5sXCM+PSU1Q08sXEE0Rm5KYSQ8dUwtPHFcTDg9cDptdCM0XVZTa2JyZW8yQm02KnBeMExmJSZoUztBVENvImdFP3AjW1w3N1s6QSQ3a0cwPU1WTShrMXViNnJZLl90aHJVXyp1Jisub3Q0VCVtbWxVP3A9RioqLmxrXlhsMyl1UildZj4/JTlKaHM1RCZFUGArW1E4UXMvSC1vJCI8MTEqN3FKMl0uP3U+OnFOTGkkKl46dUMzbHRrZT44NlxSUW41T3Q7OmcvVSZgXUJAbWIiakRFXnFOWnAvUnAkbFE9UzI4c1tSTU8mbGVgMCdtVENZRnFqPjY7alhxOWFlNyEjMUddSzBCMihNY2RIOWJqSyNlWFk4X0I4ImFmJTdFNVg0Vjo8QDdZSC9mPjNRIzM4PzMsKzwpIV4wPFYyJWwvZDc7XDZlbXRbYTRfYi87RSpDNzxfSGI+JFtgKW43VihETTRRWWdnPWJUTzYsaSZVM2lSIistUjcubklldGsyIUs+NlZdZ1ZxL1NnJGclK0FlW0o1LWdeUDxqYixwKWJvYExYcnBFaE5WcC9wbDcoVEJhXzdnQGYtKz5KYjUyZC5UVGg5W2crTmJAPyNAK3AmJFtcaCU0V2UlQE1BRSQ8QGxvXUc7NDBhZ0VDOzgnTWNXUVs6XyZTVHVxKjdcLT0jTkRyaTUxTC0pM0A5LzYxYUQ1KEc7O2pYK1tRaUtGcF5hdTM1WWFWU10/YFxxOjM3PyRCJ2dfJTk0LS4+bTpsKiEkSHJ1czBpc0o1MzJwTVMmUHJJTWZeakFMV2YkPWFqWDdRKEBYJV9AX1lVcGdIPFRNaV1LRFs7Pl8hL01nOmhhQSEwUyZFS15yPmVrSko9Lk4zZFdIY0Zib187S3ByOlVQbTxLPyhmRU9kdEVKL3RIJmo+ZysxYG9WWWBbZl1tNGspIzghYkNIYyJuS0EjSSc5anRKSiRbS1NZTmhrKS4lZV0wMTxoajdKVyE1KjNQVF9AR1FiW1VTZ09OIjcxJHNmMThzWyE/LUNyKW8sInBPTDlqczgvTEVFIzkzNkJxNWVKQ2M0WHM6TnBEL0NuRUdBIWA5RExPIVdFNXNbNS1dYFZjMypZUHBUPEo8WzVdblY6Z1VVLW9zMV1BWS1scVRWWzkjMElwU3NIM0FKIVk/K3M9LUZpUl5xP0NhWnIkQ0BUaUpcNiIqKkdPMiZFLytMRD1GNSpXOiQ4KUhrNUwob0NTWUYxNi8lXl5cKkZpZUVUM0FDXWJnPzRsNXFJcSp+PmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDM1CjAwMDAwMDAwMDAgNjU1MzUgZiAKMDAwMDAwMDA2MSAwMDAwMCBuIAowMDAwMDAwMTY1IDAwMDAwIG4gCjAwMDAwMDAyNzIgMDAwMDAgbiAKMDAwMDAwMDM4NCAwMDAwMCBuIAowMDAwMDAwNDkyIDAwMDAwIG4gCjAwMDAwMDA2MDIgMDAwMDAgbiAKMDAwMDAwMDcxMSAwMDAwMCBuIAowMDAwMDAwNzk0IDAwMDAwIG4gCjAwMDAwMDA4NzEgMDAwMDAgbiAKMDAwMDAwMDk4NSAwMDAwMCBuIAowMDAwMDAxMTY4IDAwMDAwIG4gCjAwMDAwMDEzNTQgMDAwMDAgbiAKMDAwMDAwMTU1MCAwMDAwMCBuIAowMDAwMDAxNzQyIDAwMDAwIG4gCjAwMDAwMDE5ODYgMDAwMDAgbiAKMDAwMDAwMjIzMCAwMDAwMCBuIAowMDAwMDAyNDc0IDAwMDAwIG4gCjAwMDAwMDI3MTggMDAwMDAgbiAKMDAwMDAwMjk2MiAwMDAwMCBuIAowMDAwMDAzMjA2IDAwMDAwIG4gCjAwMDAwMDM0NTAgMDAwMDAgbiAKMDAwMDAwMzY5NCAwMDAwMCBuIAowMDAwMDAzOTc4IDAwMDAwIG4gCjAwMDAwMDQwNDggMDAwMDAgbiAKMDAwMDAwNDQyNyAwMDAwMCBuIAowMDAwMDA0NTQ0IDAwMDAwIG4gCjAwMDAwMDc5MjYgMDAwMDAgbiAKMDAwMDAxMTIwNyAwMDAwMCBuIAowMDAwMDE0MjExIDAwMDAwIG4gCjAwMDAwMTgyODkgMDAwMDAgbiAKMDAwMDAyMjcwMSAwMDAwMCBuIAowMDAwMDI1NTgyIDAwMDAwIG4gCjAwMDAwMjkyMzkgMDAwMDAgbiAKMDAwMDAzMjg5MSAwMDAwMCBuIAp0cmFpbGVyCjw8Ci9JRCAKWzwzOTg4NmE0NDU1MzY0OGIzNGY3MDRmZDZiNjAyZGM5OT48Mzk4ODZhNDQ1NTM2NDhiMzRmNzA0ZmQ2YjYwMmRjOTk+XQolIFJlcG9ydExhYiBnZW5lcmF0ZWQgUERGIGRvY3VtZW50IC0tIGRpZ2VzdCAob3BlbnNvdXJjZSkKCi9JbmZvIDI0IDAgUgovUm9vdCAyMyAwIFIKL1NpemUgMzUKPj4Kc3RhcnR4cmVmCjM0MDk1CiUlRU9GCg=="
     download="foundations-real-numbers-fractalfrontiermaths.pdf"
     title="Download academic PDF notes">
    <span class="pi">&#x1F4D6;</span>
    <span class="pt">
      <span class="pt1">Download Academic PDF Notes</span>
      <span class="pt2">Foundations of Real Numbers &mdash; Fractal Frontier Maths</span>
    </span>
  </a>
</div>
