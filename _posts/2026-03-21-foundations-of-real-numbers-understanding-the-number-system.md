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

<!-- ═══ PDF DOWNLOAD — jsPDF programmatic generation ══════════════ -->
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
    <span class="pi">&#x1F4E5;</span>
    <span class="pt">
      <span class="pt1">Download PDF Notes</span>
      <span class="pt2">Foundations of Real Numbers &#8212; Fractal Frontier Maths</span>
    </span>
  </button>
</div>

<!-- jsPDF from CDN — no html2canvas needed -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script>
// ─────────────────────────────────────────────────────────────────────────────
// Fractal Frontier Maths — jsPDF programmatic PDF generator
// Foundations of Real Numbers
// ─────────────────────────────────────────────────────────────────────────────

function generatePDF() {
  var btn = document.getElementById('pdfDownloadBtn');
  btn.classList.add('generating');
  btn.querySelector('.pt1').textContent = 'Building PDF\u2026';

  // Small timeout so the button state renders before heavy work starts
  setTimeout(function() {
    try {
      buildPDF();
    } catch(e) {
      console.error(e);
      btn.classList.remove('generating');
      btn.querySelector('.pt1').textContent = 'Download PDF Notes';
    }
  }, 80);
}

function buildPDF() {
  var btn = document.getElementById('pdfDownloadBtn');

  // ── jsPDF setup ────────────────────────────────────────────────────────────
  var { jsPDF } = window.jspdf;
  var doc = new jsPDF({ unit: 'mm', format: 'a4', orientation: 'portrait' });

  var PW = 210, PH = 297;        // A4 dimensions mm
  var ML = 14, MR = 14;          // left / right margin
  var MT = 14, MB = 18;          // top / bottom margin
  var CW = PW - ML - MR;         // content width = 182mm
  var y = MT;                    // current Y cursor

  // ── Colour palette ─────────────────────────────────────────────────────────
  var NAVY   = [30,  60, 114];
  var BLUE   = [42,  82, 152];
  var PURPLE = [124, 58, 237];
  var RED    = [220, 38,  38];
  var GOLD   = [217,119,   6];
  var GREEN  = [  5,150, 105];
  var TEXT   = [ 45, 45,  45];
  var GREY   = [107,114, 128];
  var LGREY  = [229,231, 235];
  var WHITE  = [255,255, 255];
  var LBLUE  = [239,246, 255];
  var LGREEN = [236,253, 245];
  var LYELL  = [255,251, 235];
  var LPUR   = [245,243, 255];
  var LRED   = [255,245, 245];
  var LINDIGO= [224,231, 255];

  // ── Helper utilities ───────────────────────────────────────────────────────
  function setFill(rgb)   { doc.setFillColor(rgb[0],rgb[1],rgb[2]); }
  function setStroke(rgb) { doc.setDrawColor(rgb[0],rgb[1],rgb[2]); }
  function setTxt(rgb)    { doc.setTextColor(rgb[0],rgb[1],rgb[2]); }

  function rect(x, yy, w, h, fill, stroke, radius) {
    if (fill)   setFill(fill);
    if (stroke) setStroke(stroke);
    var mode = fill && stroke ? 'FD' : fill ? 'F' : 'S';
    if (radius) doc.roundedRect(x, yy, w, h, radius, radius, mode);
    else        doc.rect(x, yy, w, h, mode);
  }

  // Wrap text to fit width, returns array of lines
  function wrapText(txt, maxWidth, fontSize, bold) {
    doc.setFontSize(fontSize);
    doc.setFont('helvetica', bold ? 'bold' : 'normal');
    return doc.splitTextToSize(txt, maxWidth);
  }

  // Draw wrapped text, return new Y after drawing
  function drawText(txt, x, yy, maxWidth, fontSize, bold, colour, align) {
    doc.setFontSize(fontSize);
    doc.setFont('helvetica', bold ? 'bold' : 'normal');
    setTxt(colour || TEXT);
    var lines = doc.splitTextToSize(txt, maxWidth);
    var lineH = fontSize * 0.4;  // ~mm per line
    doc.text(lines, x, yy, { align: align || 'left' });
    return yy + lines.length * lineH;
  }

  // Measure wrapped text height in mm
  function textH(txt, maxWidth, fontSize) {
    doc.setFontSize(fontSize);
    var lines = doc.splitTextToSize(String(txt), maxWidth);
    return lines.length * fontSize * 0.4;
  }

  // Check if we need a new page
  function checkPage(needed) {
    if (y + needed > PH - MB - 12) {
      addFooter();
      doc.addPage();
      y = MT;
    }
  }

  // ── Page footer (called on every page) ────────────────────────────────────
  function addFooter() {
    var pageNum = doc.internal.getCurrentPageInfo().pageNumber;
    var totalPages = doc.internal.getNumberOfPages();

    // Watermark — diagonal centre
    doc.saveGraphicsState();
    doc.setGState(doc.GState({ opacity: 0.06 }));
    doc.setFont('helvetica','bold');
    doc.setFontSize(28);
    setTxt(NAVY);
    doc.text('Fractal Frontier Maths', PW/2, PH/2, { align:'center', angle:45 });
    doc.restoreGraphicsState();

    // Footer line
    doc.setLineWidth(0.25);
    setStroke(LGREY);
    doc.line(ML, PH - MB + 2, PW - MR, PH - MB + 2);

    // Footer text
    doc.setFont('helvetica','normal');
    doc.setFontSize(7);
    setTxt(GREY);
    doc.text('drpraveendra.github.io  |  Fractal Frontier Maths', ML, PH - MB + 6);
    doc.text('Page ' + pageNum + ' of ' + totalPages, PW - MR, PH - MB + 6, { align:'right' });
  }

  // ── Gradient simulation (fill rect in two halves with avg colour) ──────────
  function gradRect(x, yy, w, h, c1, c2, radius) {
    // Simulate gradient with 40 thin vertical strips
    var steps = 40;
    for (var i = 0; i < steps; i++) {
      var t = i / (steps - 1);
      var r = Math.round(c1[0] + t*(c2[0]-c1[0]));
      var g = Math.round(c1[1] + t*(c2[1]-c1[1]));
      var b = Math.round(c1[2] + t*(c2[2]-c1[2]));
      doc.setFillColor(r,g,b);
      if (radius && (i === 0 || i === steps-1)) {
        // Just use plain rect for edge strips to avoid artefacts
        doc.rect(x + i*(w/steps), yy, w/steps + 0.5, h, 'F');
      } else {
        doc.rect(x + i*(w/steps), yy, w/steps + 0.5, h, 'F');
      }
    }
  }

  // ── Section header ─────────────────────────────────────────────────────────
  function sectionHeader(title) {
    checkPage(14);
    // Colour bar
    gradRect(ML, y, CW, 2.5, NAVY, PURPLE);
    y += 4;
    doc.setFont('helvetica','bold');
    doc.setFontSize(13);
    setTxt(NAVY);
    doc.text(title, ML, y + 4.5);
    y += 10;
    // Underline
    doc.setLineWidth(0.4);
    setStroke(NAVY);
    doc.line(ML, y - 1, ML + CW, y - 1);
    y += 3;
  }

  // ── Coloured box with title bar ────────────────────────────────────────────
  function infoBox(title, lines, titleBg, bodyBg, borderCol, startY) {
    var padding = 3;
    var titleH  = 7;
    var bodyLines = [];
    lines.forEach(function(l) {
      var wrapped = doc.splitTextToSize(l, CW - padding*2 - 4);
      wrapped.forEach(function(wl){ bodyLines.push(wl); });
    });
    var bodyH   = bodyLines.length * 4.2 + padding * 2;
    var totalH  = titleH + bodyH;
    checkPage(totalH + 4);
    var bx = ML, by = y;

    // Body bg
    if (borderCol) {
      doc.setLineWidth(0.4);
      setStroke(borderCol);
    }
    rect(bx, by, CW, totalH, bodyBg, borderCol, 2);

    // Title bar
    setFill(titleBg);
    doc.roundedRect(bx, by, CW, titleH, 2, 2, 'F');
    // Re-draw bottom of title bar as flat
    setFill(titleBg);
    doc.rect(bx, by + titleH - 2, CW, 2, 'F');

    doc.setFont('helvetica','bold');
    doc.setFontSize(8);
    setTxt(WHITE);
    doc.text(title, bx + 4, by + 4.8);

    // Body text
    doc.setFont('helvetica','normal');
    doc.setFontSize(9.5);
    setTxt(TEXT);
    var ty = by + titleH + padding + 3.5;
    bodyLines.forEach(function(line) {
      doc.text(line, bx + padding + 2, ty);
      ty += 4.2;
    });
    y = by + totalH + 4;
  }

  // ── Floor card ─────────────────────────────────────────────────────────────
  function floorCard(sym, symColour, title, setNotation, bodyText, badgeText, badgeType) {
    var wrapped = doc.splitTextToSize(bodyText, CW - 22);
    var cardH = 10 + wrapped.length * 4.2 + 8;
    checkPage(cardH + 4);

    var bx = ML, by = y;
    // Card background
    rect(bx, by, CW, cardH, WHITE, LGREY, 2);

    // Symbol circle
    var cx = bx + 7, cy = by + 7;
    setFill(symColour);
    doc.circle(cx, cy, 5, 'F');
    doc.setFont('helvetica','bold');
    doc.setFontSize(7.5);
    setTxt(WHITE);
    doc.text(sym, cx, cy + 2.5, { align:'center' });

    // Title
    doc.setFont('helvetica','bold');
    doc.setFontSize(9.5);
    setTxt(NAVY);
    doc.text(title, bx + 15, by + 5.5);

    // Set notation
    doc.setFont('courier','bold');
    doc.setFontSize(8);
    setTxt(PURPLE);
    doc.text(setNotation, bx + 15, by + 10.5);

    // Body text
    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt(TEXT);
    var ty = by + 16;
    wrapped.forEach(function(line) {
      doc.text(line, bx + 15, ty);
      ty += 4.2;
    });

    // Badge
    var badgeBg  = badgeType === 'problem' ? LRED   : LGREEN;
    var badgeFg  = badgeType === 'problem' ? RED     : GREEN;
    var badgeBor = badgeType === 'problem' ? [254,202,202] : [110,231,183];
    var bw = CW - 17, bh = 5.5;
    var badgeY = by + cardH - bh - 1.5;
    rect(bx + 15, badgeY, bw, bh, badgeBg, badgeBor, 1.5);
    doc.setFont('helvetica','bold');
    doc.setFontSize(7.5);
    setTxt(badgeFg);
    doc.text(badgeText, bx + 18, badgeY + 3.8);

    y = by + cardH + 3;
  }

  // ── Example card ───────────────────────────────────────────────────────────
  function exampleCard(num, label, questionLines, solutionLines, accentCol) {
    // Calculate height
    var qH = questionLines.length * 4.2 + 2;
    var sH = solutionLines.length * 4.2 + 6;
    var cardH = 8 + qH + sH + 6;
    checkPage(cardH + 6);

    var bx = ML, by = y;
    // Card outline
    rect(bx, by, CW, cardH, WHITE, LGREY, 2);
    // Top accent bar
    setFill(accentCol);
    doc.rect(bx, by, CW, 1.5, 'F');
    // Rounded top corners manually
    doc.roundedRect(bx, by, CW, 1.5, 2, 2, 'F');
    doc.rect(bx, by + 1, CW, 0.7, 'F');  // fill bottom of rounded to make it flat

    // Number circle
    setFill(accentCol);
    doc.circle(bx + 7, by + 8.5, 4.5, 'F');
    doc.setFont('helvetica','bold');
    doc.setFontSize(8.5);
    setTxt(WHITE);
    doc.text(String(num), bx + 7, by + 10.8, { align:'center' });

    // Label
    doc.setFont('helvetica','bold');
    doc.setFontSize(7.5);
    setTxt(GREY);
    doc.text(label.toUpperCase(), bx + 15, by + 6.5);

    // Question
    doc.setFont('helvetica','bold');
    doc.setFontSize(9.5);
    setTxt(TEXT);
    var ty = by + 12;
    questionLines.forEach(function(line) {
      doc.text(line, bx + 15, ty);
      ty += 4.5;
    });

    // Solution box
    var solY = ty + 1;
    var solH = sH;
    rect(bx + 4, solY, CW - 8, solH, LGREEN, null, 1.5);
    doc.setLineWidth(0.8);
    setStroke(GREEN);
    doc.line(bx + 4, solY, bx + 4, solY + solH);

    doc.setFont('helvetica','bold');
    doc.setFontSize(9);
    setTxt(GREEN);
    doc.text('Solution:', bx + 8, solY + 4.5);

    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt([26, 92, 56]);
    var sy = solY + 4.5;
    var isFirst = true;
    solutionLines.forEach(function(line) {
      if (isFirst) { isFirst = false; return; } // skip 'Solution:' placeholder
      doc.text(line, bx + 8, sy + 4.2);
      sy += 4.2;
    });

    y = by + cardH + 4;
  }

  // ── Two-column comparison ──────────────────────────────────────────────────
  function twoColBox(leftTitle, leftLines, rightTitle, rightLines) {
    var colW = (CW - 4) / 2;
    var leftWrapped = [], rightWrapped = [];
    leftLines.forEach(function(l) {
      doc.splitTextToSize(l, colW - 6).forEach(function(w){ leftWrapped.push(w); });
    });
    rightLines.forEach(function(l) {
      doc.splitTextToSize(l, colW - 6).forEach(function(w){ rightWrapped.push(w); });
    });
    var h = Math.max(leftWrapped.length, rightWrapped.length) * 4.2 + 14;
    checkPage(h + 6);

    var by = y;
    // Left box (blue)
    rect(ML, by, colW, h, LBLUE, [147,197,253], 2);
    doc.setFont('helvetica','bold');
    doc.setFontSize(9);
    setTxt([30,64,175]);
    doc.text(leftTitle, ML + 3, by + 5.5);
    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt(TEXT);
    var ty = by + 11;
    leftWrapped.forEach(function(line) {
      doc.text('\u2022 ' + line, ML + 4, ty);
      ty += 4.2;
    });

    // Right box (green)
    var rx = ML + colW + 4;
    rect(rx, by, colW, h, LGREEN, [110,231,183], 2);
    doc.setFont('helvetica','bold');
    doc.setFontSize(9);
    setTxt([6,95,70]);
    doc.text(rightTitle, rx + 3, by + 5.5);
    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt(TEXT);
    ty = by + 11;
    rightWrapped.forEach(function(line) {
      doc.text('\u2022 ' + line, rx + 4, ty);
      ty += 4.2;
    });

    y = by + h + 4;
  }

  // ── Bullet list box ────────────────────────────────────────────────────────
  function bulletBox(headerText, items, bg, borderCol, textCol) {
    var allLines = [];
    items.forEach(function(item) {
      var wrapped = doc.splitTextToSize(item, CW - 12);
      wrapped.forEach(function(w, i){ allLines.push({ text: w, first: i === 0 }); });
    });
    var boxH = allLines.length * 4.5 + 12;
    checkPage(boxH + 4);

    var by = y;
    rect(ML, by, CW, boxH, bg, borderCol, 2);
    doc.setLineWidth(1);
    setStroke(borderCol);
    doc.line(ML, by, ML, by + boxH);

    // Header
    doc.setFont('helvetica','bold');
    doc.setFontSize(8);
    setTxt(textCol || TEXT);
    doc.text(headerText.toUpperCase(), ML + 5, by + 5.5);

    // Items
    doc.setFont('helvetica','normal');
    doc.setFontSize(9.5);
    var ty = by + 11;
    allLines.forEach(function(line) {
      var prefix = line.first ? '\u2022 ' : '    ';
      doc.text(prefix + line.text, ML + 5, ty);
      ty += 4.5;
    });
    y = by + boxH + 4;
  }

  // ── Simple table ───────────────────────────────────────────────────────────
  function drawTable(headers, rows, colWidths) {
    var rowH = 7;
    var tableH = (rows.length + 1) * rowH;
    checkPage(tableH + 4);

    var by = y;
    var x = ML;

    // Header row
    gradRect(ML, by, CW, rowH, NAVY, PURPLE);
    doc.setFont('helvetica','bold');
    doc.setFontSize(8.5);
    setTxt(WHITE);
    var hx = ML;
    headers.forEach(function(h, i) {
      doc.text(String(h), hx + 2, by + 4.8);
      hx += colWidths[i];
    });
    by += rowH;

    // Data rows
    rows.forEach(function(row, ri) {
      var rowBg = ri % 2 === 0 ? WHITE : LBLUE;
      rect(ML, by, CW, rowH, rowBg, null);

      doc.setFont('helvetica','normal');
      var cx = ML;
      row.forEach(function(cell, ci) {
        if (ci === 0) {
          doc.setFont('helvetica','bolditalic');
          doc.setFontSize(8);
          setTxt(NAVY);
        } else {
          doc.setFont('helvetica','normal');
          doc.setFontSize(8.5);
          setTxt(TEXT);
        }
        var cellText = doc.splitTextToSize(String(cell), colWidths[ci] - 3);
        doc.text(cellText[0], cx + 2, by + 4.8); // show first line only (fits in rowH)
        cx += colWidths[ci];
      });
      by += rowH;
    });

    // Border
    doc.setLineWidth(0.3);
    setStroke([199,215,247]);
    doc.rect(ML, y, CW, tableH, 'S');
    // Column dividers
    var divX = ML;
    colWidths.slice(0,-1).forEach(function(w) {
      divX += w;
      doc.line(divX, y, divX, y + tableH);
    });
    // Row dividers
    for (var r = 1; r <= rows.length; r++) {
      doc.line(ML, y + r*rowH, ML + CW, y + r*rowH);
    }

    y = y + tableH + 4;
  }

  // ── Spotlight box (dark blue) ──────────────────────────────────────────────
  function spotlightBox(title, bodyLines) {
    var wrapped = [];
    bodyLines.forEach(function(l) {
      doc.splitTextToSize(l, CW - 20).forEach(function(w){ wrapped.push(w); });
    });
    var boxH = wrapped.length * 4.2 + 14;
    checkPage(boxH + 4);

    var by = y;
    gradRect(ML, by, CW, boxH, NAVY, BLUE);

    // Icon area
    doc.setFont('helvetica','normal');
    doc.setFontSize(20);
    setTxt(WHITE);
    doc.text('\uD83C\uDFDB', ML + 4, by + 12);

    // Title
    doc.setFont('helvetica','bold');
    doc.setFontSize(9.5);
    setTxt([251,191,36]); // gold
    doc.text(title, ML + 18, by + 7);

    // Body
    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt([226,232,240]);
    var ty = by + 13;
    wrapped.forEach(function(line) {
      doc.text(line, ML + 18, ty);
      ty += 4.2;
    });
    y = by + boxH + 4;
  }

  // ── Highlight result box ───────────────────────────────────────────────────
  function highlightBox(mainText, subText) {
    var subWrapped = doc.splitTextToSize(subText, CW - 16);
    var boxH = 10 + subWrapped.length * 4.2 + 6;
    checkPage(boxH + 4);

    var by = y;
    rect(ML, by, CW, boxH, LINDIGO, [129,140,248], 3);
    doc.setFont('helvetica','bold');
    doc.setFontSize(13);
    setTxt(NAVY);
    doc.text(mainText, PW/2, by + 8, { align:'center' });

    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt([67,56,202]);
    var ty = by + 14;
    subWrapped.forEach(function(line) {
      doc.text(line, PW/2, ty, { align:'center' });
      ty += 4.2;
    });
    y = by + boxH + 4;
  }

  // ═══════════════════════════════════════════════════════════════════════════
  // ── PAGE 1: HERO + STATS + SECTION 1 ──────────────────────────────────────
  // ═══════════════════════════════════════════════════════════════════════════

  // Hero banner
  gradRect(ML, y, CW, 52, NAVY, PURPLE);

  // Decorative R (approximated)
  doc.setFont('helvetica','bold');
  doc.setFontSize(70);
  doc.setTextColor(255,255,255);
  doc.setGState && doc.setGState(doc.GState({ opacity: 0.06 }));
  // Use R symbol
  doc.setFont('helvetica','bold');
  doc.setFontSize(55);
  setTxt([255,255,255]);
  doc.text('R', ML + CW - 22, y + 38, { align:'center' });

  doc.setGState && doc.setGState(doc.GState({ opacity: 1.0 }));

  // Hero text
  doc.setFont('helvetica','bold');
  doc.setFontSize(17);
  setTxt(WHITE);
  doc.text('The Infinite Architecture:', ML + 4, y + 13);
  doc.text('Foundations of Real Numbers', ML + 4, y + 21);

  doc.setFont('helvetica','normal');
  doc.setFontSize(9.5);
  setTxt([220,230,255]);
  doc.text('Understanding the Number System — from Ancient Counting to R', ML + 4, y + 29);

  doc.setFont('helvetica','normal');
  doc.setFontSize(8);
  setTxt([180,200,240]);
  doc.text('Author: Dr. Praveendra Singh  |  Fractal Frontier Maths  |  B.Sc./M.Sc. Mathematics  |  Real Analysis Unit 1', ML + 4, y + 37);

  // Red accent bar at bottom of hero
  setFill(RED);
  doc.rect(ML, y + 49, CW, 2, 'F');
  y += 56;

  // Stats strip
  gradRect(ML, y, CW, 14, NAVY, PURPLE);
  var stats = [
    { num:'5',     lbl:'Number Systems' },
    { num:'3000+', lbl:'Years of History' },
    { num:'4',     lbl:'Solved Examples' },
    { num:'★★☆',  lbl:'Beginner Friendly' },
    { num:'R',     lbl:'The Final System' }
  ];
  var sw = CW / stats.length;
  stats.forEach(function(s, i) {
    var sx = ML + i * sw + sw/2;
    doc.setFont('helvetica','bold');
    doc.setFontSize(11);
    setTxt(WHITE);
    doc.text(s.num, sx, y + 6, { align:'center' });
    doc.setFont('helvetica','normal');
    doc.setFontSize(6);
    setTxt([200,210,255]);
    doc.text(s.lbl.toUpperCase(), sx, y + 11, { align:'center' });
  });
  y += 18;

  // ── Section 1: Skyscraper Analogy ─────────────────────────────────────────
  sectionHeader('The Skyscraper Analogy');

  y = drawText(
    'Have you ever stopped to ask: what is a number, really? For most people, numbers are just tools. But to a mathematician, the number system is a magnificent skyscraper built floor by floor over three thousand years of human thought.',
    ML, y, CW, 10, false, TEXT
  ) + 3;

  // Pull quote
  var pqLines = doc.splitTextToSize(
    '"Every time humanity hit a wall — a problem that couldn\'t be solved — we didn\'t give up. We built a new floor."',
    CW - 12
  );
  var pqH = pqLines.length * 4.5 + 8;
  rect(ML, y, CW, pqH, LPUR, [167,139,250], 2);
  doc.setLineWidth(3);
  setStroke(PURPLE);
  doc.line(ML, y, ML, y + pqH);
  doc.setFont('helvetica','bolditalic');
  doc.setFontSize(10);
  setTxt([76,29,149]);
  var qy = y + 6;
  pqLines.forEach(function(l) { doc.text(l, ML + 6, qy); qy += 4.5; });
  y += pqH + 5;

  y = drawText(
    'Each new type of number was born out of a real need — a problem the existing numbers simply could not solve. What began as counting sheep eventually grew into the most powerful mathematical system we have: the Real Number System (R).',
    ML, y, CW, 10, false, TEXT
  ) + 5;

  // ── Section 2: Five Floors ─────────────────────────────────────────────────
  sectionHeader('The Five Floors: A Journey Through History');

  floorCard('N', NAVY, 'Floor 1 — Natural Numbers  N = {1, 2, 3, 4, ...}',
    'N = { 1, 2, 3, 4, ... }',
    'The first act of mathematics: counting. Ancient people counted cattle, days, and harvests. Addition and multiplication always stay within N. But subtraction quickly causes trouble.',
    'Gap: What is 3 - 5?  No natural number answer. We need a new floor.', 'problem');

  floorCard('W', GREEN, 'Floor 2 — Whole Numbers  W = {0, 1, 2, 3, ...}',
    'W = { 0, 1, 2, 3, ... }',
    'We add zero. Zero is not just "nothing" — it holds a place and makes our entire decimal system work. Aryabhata\'s Aryabhatiya (499 CE) established zero as a working digit.',
    'Gap: 5 - 8 = ?  Still no answer. We need numbers below zero.', 'problem');

  floorCard('Z', PURPLE, 'Floor 3 — Integers  Z = {..., -2, -1, 0, 1, 2, ...}',
    'Z = { ..., -3, -2, -1, 0, 1, 2, 3, ... }',
    'Negative numbers extend the line both ways. Now subtraction always works. Z comes from German Zahlen (numbers). Brahmagupta (628 CE) gave the first clear rules for arithmetic with negatives and zero.',
    'Gap: 1 / 2 = ?  No integer answer. We need fractions.', 'problem');

  floorCard('Q', GOLD, 'Floor 4 — Rational Numbers  Q = { p/q : p, q in Z, q not 0 }',
    'Q = { p/q : p, q integers, q not equal 0 }',
    'From Latin ratio. All fractions — every terminating or repeating decimal is rational. With Q we can add, subtract, multiply, and divide (except by 0) and always stay within Q. Ancient Greeks were satisfied here — until a simple square broke everything.',
    'Gap: No fraction squares to exactly 2. The number line has holes!', 'problem');

  floorCard('R', RED, 'Floor 5 — Real Numbers  R = Q union Q^c  (Rationals + Irrationals)',
    'R = Q union Q^c  (all rationals + all irrationals)',
    'Every single point on the number line is a real number. No gaps. No holes. sqrt(2), pi, e are all real. This is the number system used in all of calculus and physics.',
    'Complete: Every number that can be placed on a line is a real number.', 'solved');

  // ── Section 3: Irrational Crisis ──────────────────────────────────────────
  sectionHeader('The Crisis That Created Irrational Numbers');

  y = drawText(
    'The ancient Greek Pythagorean school had a firm belief: every quantity in nature can be written as a fraction. Then one of their own made a discovery that shook the foundations of their philosophy.',
    ML, y, CW, 10, false, TEXT
  ) + 4;

  twoColBox(
    'The Problem: A Simple Square',
    ['Draw a square with each side exactly 1 unit',
     'By Pythagoras, the diagonal = sqrt(2)',
     'Can sqrt(2) be written as p/q?',
     'Pythagoreans believed yes — until they tried to prove it.'],
    'The Shock: It Cannot Be a Fraction',
    ['Assume sqrt(2) = p/q in simplest form (no shared factors)',
     'p^2 = 2q^2  =>  p is even  =>  write p = 2m',
     'Then 4m^2 = 2q^2  =>  q is also even',
     'Both even => share factor 2 => contradicts simplest form!']
  );

  y = drawText(
    'So sqrt(2) is irrational — a real number that cannot be any fraction. The legend says Hippasus (~5th century BCE), who revealed this, was thrown into the sea. Mathematical point: rational numbers alone cannot fill the number line.',
    ML, y, CW, 10, false, TEXT
  ) + 4;

  infoBox(
    'WHAT ARE IRRATIONAL NUMBERS?',
    ['An irrational number is any real number that CANNOT be written as p/q where p and q are integers.',
     'In decimal form: they go on forever WITHOUT any repeating pattern.',
     '',
     'sqrt(2) = 1.41421356...   (never ends, never repeats)',
     'pi      = 3.14159265...   (ratio of a circle\'s circumference to its diameter)',
     'e       = 2.71828182...   (Euler\'s number — used in growth and decay)',
     'sqrt(3), sqrt(5), sqrt(7)  (square roots of non-perfect-squares)',
     '',
     'IMPORTANT: sqrt(4) = 2 and sqrt(9) = 3 are rational. Always simplify first!'],
    GOLD, LYELL, GOLD
  );

  // ── Section 4: Historical Timeline ────────────────────────────────────────
  sectionHeader('Historical Timeline — How the Number System Grew');

  y = drawText(
    'This took thousands of years and contributions from many civilisations — each generation solving the problems left by the previous one.',
    ML, y, CW, 10, false, TEXT
  ) + 4;

  drawTable(
    ['Period', 'Who', 'Contribution', 'System'],
    [
      ['~3000 BCE', 'Mesopotamia & Egypt',   'Counting; tally marks and early numerals',                       'N Natural'],
      ['~500 BCE',  'Ancient Greece',         'Study of ratios and proportions in geometry',                    'Q Rationals'],
      ['~500 BCE',  'Pythagoreans (Greece)',   'sqrt(2) cannot be a fraction — first known irrational',         'Irrationals needed'],
      ['499 CE',    'Aryabhata (India)',        'Aryabhatiya — decimal place-value, zero as working digit',      'W Whole Numbers'],
      ['628 CE',    'Brahmagupta (India)',      'Brahmasphutasiddhanta — rules for zero and negatives',          'Z Integers'],
      ['1872 CE',   'Dedekind (Germany)',       'Rigorous construction of reals via Dedekind cuts',              'R defined'],
      ['1874 CE',   'Cantor (Germany)',         'Proved irrationals far outnumber rationals on the line',        'R full theory'],
    ],
    [24, 38, 80, 40]
  );

  // ── Section 5: Solved Examples ─────────────────────────────────────────────
  sectionHeader('Solved Examples');

  exampleCard(1, 'Example 1 — Classify Each Number',
    doc.splitTextToSize('For each number, state the smallest set it belongs to  (N, W, Z, Q, or irrational):   7,  -3,  5/4,  sqrt(5),  0,  -2/7,  sqrt(9),  0.666...', CW - 18),
    ['Solution:',
     '7  =>  Natural N  (positive counting number)',
     '0  =>  Whole W  (not natural, but whole)',
     '-3  =>  Integer Z  (negative)',
     '5/4  =>  Rational Q  (fraction of integers = 1.25)',
     '-2/7  =>  Rational Q  (negative fraction)',
     'sqrt(9) = 3  =>  Natural N  (simplifies to 3 — rational!)',
     '0.666... = 2/3  =>  Rational Q  (repeating decimal = fraction)',
     'sqrt(5)  =>  Irrational  (5 is not a perfect square)'],
    NAVY);

  exampleCard(2, 'Example 2 — Prove that sqrt(2) is Irrational',
    doc.splitTextToSize('Prove that sqrt(2) is irrational — it cannot be written as p/q where p and q are integers.  [W. Rudin, Principles of Mathematical Analysis, 3rd ed., Example 1.1, p.2]', CW - 18),
    ['Solution — Proof by Contradiction:',
     'Step 1. Suppose sqrt(2) = p/q, where p, q are positive integers with no common factor (simplest form).',
     'Step 2. Squaring: p^2 = 2q^2.  So p^2 is even => p is even.  Write p = 2m.',
     'Step 3. Substituting: (2m)^2 = 2q^2  =>  4m^2 = 2q^2  =>  q^2 = 2m^2.  So q is also even.',
     'Step 4. Both p and q are even — they share factor 2. This contradicts simplest form.',
     'Conclusion: No fraction p/q can equal sqrt(2). Therefore sqrt(2) is irrational.'],
    PURPLE);

  exampleCard(3, 'Example 3 — Rational or Irrational?',
    doc.splitTextToSize('Decide whether each is rational or irrational, with a brief reason:  (a) 0.142857...   (b) sqrt(2)+sqrt(2)   (c) sqrt(2) x sqrt(2)   (d) pi - pi   (e) 2+sqrt(3)', CW - 18),
    ['Solution:',
     '(a) 0.142857142857... = 1/7  =>  Rational.  Any repeating decimal is rational.',
     '(b) sqrt(2)+sqrt(2) = 2*sqrt(2)  =>  Irrational.  Irrational x non-zero rational stays irrational.',
     '(c) sqrt(2) x sqrt(2) = 2  =>  Rational!  KEY TRAP: product of two irrationals CAN be rational.',
     '(d) pi - pi = 0  =>  Rational.  Any number minus itself = 0 = 0/1.',
     '(e) 2+sqrt(3)  =>  Irrational.  If rational r, then sqrt(3)=r-2 would be rational. Contradiction!'],
    GOLD);

  exampleCard(4, 'Example 4 — A Common Misconception about pi',
    doc.splitTextToSize('A student says: "Since 22/7 is used for pi in calculations, pi must be rational." Is the student correct?', CW - 18),
    ['Solution:  The student is incorrect.',
     '22/7 = 3.142857142857...  (repeating, hence rational) is only an approximation of pi.',
     'The actual value  pi = 3.14159265...  never repeats and never ends — making it irrational.',
     'The two numbers match only in the first two decimal places.',
     'pi was proved irrational by Johann Heinrich Lambert in 1761.'],
    RED);

  // ── Section 6: Key Points ──────────────────────────────────────────────────
  sectionHeader('Key Points to Remember');

  bulletBox('Things Worth Remembering',
    ['The hierarchy: N is-subset-of W is-subset-of Z is-subset-of Q is-subset-of R.  Every natural number is also whole, integer, rational, and real.',
     'Not every square root is irrational: sqrt(4)=2, sqrt(16)=4, sqrt(25)=5 are rational.  Only roots of non-perfect-squares are irrational.',
     'Repeating decimal = rational: 0.333...=1/3,  0.142857...=1/7.  A pattern that repeats means the number is rational.',
     'Product trap: sqrt(2) x sqrt(2) = 2 is rational.  Product of two irrationals is NOT always irrational.',
     '22/7 is not pi: Only an approximation. pi is irrational — proved by Lambert, 1761.',
     'e is also irrational: Euler\'s number e ≈ 2.718 is irrational — proved by Hermite, 1873.'],
    LYELL, GOLD, [146,64,14]
  );

  // ── Section 7: Common Mistakes ─────────────────────────────────────────────
  sectionHeader('Common Mistakes');

  bulletBox('Avoid These Errors',
    ['"All decimals are irrational": Not true.  0.5 = 1/2 is rational.  Only non-terminating, non-repeating decimals are irrational.',
     '"Every square root is irrational": sqrt(9)=3 is a natural number.  Always simplify before deciding.',
     '"Irrational + Irrational = Irrational": sqrt(2)+(-sqrt(2))=0 which is rational.',
     '"Irrational x Irrational = Irrational": sqrt(3) x sqrt(3) = 3 which is rational.',
     '"22/7 = pi": Only an approximation. pi is irrational and equals no fraction exactly.',
     '"N includes 0": Most courses define N={1,2,3,...}. Zero is whole, not natural.'],
    LRED, RED, [153,27,27]
  );

  // ── Section 8: Applications ────────────────────────────────────────────────
  sectionHeader('Why Do Real Numbers Matter?');

  var apps = [
    ['Geometry',     'The diagonal of a unit square (sqrt(2)) and the ratio pi are irrational — exact measurement requires R.'],
    ['Engineering',  'Angles, waves, and signals all use pi and sqrt(2). Without R, modern engineering is impossible.'],
    ['Finance',      'Compound interest uses Euler\'s number e ≈ 2.718 (irrational). Every bank uses it.'],
    ['Physics',      'Speed, temperature, and distance in nature are continuous. R is the natural language for every physical quantity.'],
  ];

  var appColW = (CW - 4) / 2;
  for (var ai = 0; ai < apps.length; ai += 2) {
    var app1 = apps[ai], app2 = apps[ai+1];
    var h1Lines = doc.splitTextToSize(app1[1], appColW - 8);
    var h2Lines = app2 ? doc.splitTextToSize(app2[1], appColW - 8) : [];
    var rowH = Math.max(h1Lines.length, h2Lines.length) * 4.2 + 13;
    checkPage(rowH + 4);

    var by = y;
    var accents = [NAVY, PURPLE, GOLD, GREEN];

    // Box 1
    rect(ML, by, appColW, rowH, WHITE, LGREY, 2);
    setFill(accents[ai]);
    doc.rect(ML, by, appColW, 2, 'F');
    doc.roundedRect(ML, by, appColW, 2, 2, 2, 'F');
    doc.setFont('helvetica','bold');
    doc.setFontSize(9.5);
    setTxt(NAVY);
    doc.text(app1[0], ML + 4, by + 8);
    doc.setFont('helvetica','normal');
    doc.setFontSize(9);
    setTxt(TEXT);
    var ty = by + 13;
    h1Lines.forEach(function(l){ doc.text(l, ML + 4, ty); ty += 4.2; });

    // Box 2
    if (app2) {
      var bx2 = ML + appColW + 4;
      rect(bx2, by, appColW, rowH, WHITE, LGREY, 2);
      setFill(accents[ai+1]);
      doc.rect(bx2, by, appColW, 2, 'F');
      doc.roundedRect(bx2, by, appColW, 2, 2, 2, 'F');
      doc.setFont('helvetica','bold');
      doc.setFontSize(9.5);
      setTxt(NAVY);
      doc.text(app2[0], bx2 + 4, by + 8);
      doc.setFont('helvetica','normal');
      doc.setFontSize(9);
      setTxt(TEXT);
      ty = by + 13;
      h2Lines.forEach(function(l){ doc.text(l, bx2 + 4, ty); ty += 4.2; });
    }
    y = by + rowH + 3;
  }

  // ── Section 9: Summary Table ───────────────────────────────────────────────
  sectionHeader('Summary — The Number System at a Glance');

  drawTable(
    ['System', 'Symbol', 'Examples', 'New Idea', 'Problem Solved'],
    [
      ['Natural Numbers', 'N',   '1, 2, 3',           'Counting',            'How many things?'],
      ['Whole Numbers',   'W',   '0, 1, 2',           'Zero',                'How to show "none"?'],
      ['Integers',        'Z',   '-3, 0, 5',          'Negative numbers',    'What is 3 - 5?'],
      ['Rational Numbers','Q',   '1/2, -3/4, 0.33...',  'Fractions',         'What is 1 / 2?'],
      ['Irrational Nos.', 'Q^c', 'sqrt(2), pi, e',    'Non-fraction lengths','Diagonal of unit square?'],
      ['Real Numbers',    'R',   'All of the above',  'Gapless number line', 'Every point has a number'],
    ],
    [34, 16, 38, 38, 56]
  );

  highlightBox(
    'N  ⊂  W  ⊂  Z  ⊂  Q  ⊂  R',
    'Every number system is contained inside the next. Real numbers include every number that can be placed on a straight line, with no gaps whatsoever.'
  );

  // ── Social footer ──────────────────────────────────────────────────────────
  checkPage(30);
  doc.setLineWidth(0.4);
  setStroke(LGREY);
  doc.line(ML, y, ML + CW, y);
  y += 5;

  doc.setFont('helvetica','bold');
  doc.setFontSize(10);
  setTxt(NAVY);
  doc.text('Fractal Frontier Maths  |  Empowering students in Real Analysis, Topology, and beyond', PW/2, y, { align:'center' });
  y += 6;

  // Clickable links
  var links = [
    { text: 'drpraveendra.github.io',           url: 'https://drpraveendra.github.io' },
    { text: 't.me/fractalfrontiermaths',         url: 'https://t.me/fractalfrontiermaths' },
    { text: 'YouTube: FractalFrontierMaths',     url: 'https://www.youtube.com/@FractalFrontierMaths' },
    { text: 'Instagram: mathsworld007',          url: 'https://www.instagram.com/mathsworld007' },
  ];
  var lw = CW / links.length;
  links.forEach(function(link, i) {
    var lx = ML + i * lw + lw/2;
    doc.setFont('helvetica','bold');
    doc.setFontSize(8.5);
    setTxt(BLUE);
    doc.textWithLink(link.text, lx, y, { url: link.url, align:'center' });
  });
  y += 5;

  doc.setFont('helvetica','normal');
  doc.setFontSize(7.5);
  setTxt(GREY);
  doc.text('© 2026 Fractal Frontier Maths  |  Dr. Praveendra Singh, Govt. College Kherwara, Rajasthan', PW/2, y, { align:'center' });

  // ── Add watermark + footer to ALL pages ────────────────────────────────────
  var totalPages = doc.internal.getNumberOfPages();
  for (var p = 1; p <= totalPages; p++) {
    doc.setPage(p);
    addFooter();
  }

  // ── Save ───────────────────────────────────────────────────────────────────
  doc.save('foundations-real-numbers-fractalfrontiermaths.pdf');

  btn.classList.remove('generating');
  btn.querySelector('.pt1').textContent = 'Download PDF Notes';
}

</script>
