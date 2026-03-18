---
layout: post
title: "Srinivasa Ramanujan — The Man Who Knew Infinity"
date: 2026-03-20
category: history
lang: en
lang_pair: "/blog/ramanujan-hindi/"
permalink: /blog/ramanujan-english/
description: "A detailed account of Ramanujan's life, mathematical genius, family bonds, spiritual roots, struggles, and his lasting legacy in modern mathematics."
---

<style>
  .ramanujan-post {
    font-family: Georgia, 'Times New Roman', serif;
    font-size: 1.08rem;
    line-height: 1.9;
    color: #2d2d2d;
    max-width: 860px;
    margin: 0 auto;
  }

  .opening-quote {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 50%, #6b21a8 100%);
    border-radius: 18px;
    padding: 38px 40px;
    margin-bottom: 45px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .opening-quote::before {
    content: "❝";
    position: absolute;
    top: -10px; left: 20px;
    font-size: 8rem;
    color: rgba(255,255,255,0.08);
    font-family: Georgia, serif;
    line-height: 1;
  }
  .opening-quote p {
    font-size: 1.25rem;
    color: #fff;
    font-style: italic;
    margin: 0 0 12px;
    line-height: 1.8;
    position: relative;
    z-index: 1;
  }
  .opening-quote .quote-attr {
    font-size: 0.9rem;
    color: #fbbf24;
    font-weight: 600;
    font-style: normal;
  }

  .ramanujan-post h2 {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 1.5rem;
    font-weight: 700;
    color: #1e3c72;
    margin: 50px 0 22px;
    padding-bottom: 12px;
    border-bottom: 3px solid transparent;
    border-image: linear-gradient(to right, #1e3c72, #6b21a8, #ff4b2b, transparent) 1;
  }
  .ramanujan-post h2 .sec-icon {
    width: 40px; height: 40px;
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem; flex-shrink: 0;
  }
  .ramanujan-post h3 {
    font-size: 1.15rem;
    font-weight: 700;
    color: #2a5298;
    margin: 30px 0 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .ramanujan-post h3::before {
    content: '';
    width: 4px; height: 20px;
    background: linear-gradient(to bottom, #ff4b2b, #fbbf24);
    border-radius: 2px;
    flex-shrink: 0;
  }

  .info-card {
    background: white;
    border-radius: 14px;
    padding: 24px 28px;
    margin: 22px 0;
    box-shadow: 0 4px 16px rgba(0,0,0,0.07);
    border-left: 5px solid #1e3c72;
  }
  .info-card.gold   { border-left-color: #d97706; background: #fffbeb; }
  .info-card.purple { border-left-color: #7c3aed; background: #f5f3ff; }
  .info-card.green  { border-left-color: #059669; background: #ecfdf5; }
  .info-card.red    { border-left-color: #dc2626; background: #fff5f5; }
  .info-card.blue   { border-left-color: #1e3c72; background: #eff6ff; }
  .info-card-header {
    display: flex; align-items: center; gap: 10px;
    font-size: 0.8rem; font-weight: 700;
    text-transform: uppercase; letter-spacing: 0.8px;
    margin-bottom: 10px;
  }
  .info-card.gold   .info-card-header { color: #92400e; }
  .info-card.purple .info-card-header { color: #5b21b6; }
  .info-card.green  .info-card-header { color: #065f46; }
  .info-card.red    .info-card-header { color: #991b1b; }
  .info-card.blue   .info-card-header { color: #1e3a5f; }

  .timeline {
    position: relative;
    margin: 25px 0;
    padding-left: 28px;
  }
  .timeline::before {
    content: '';
    position: absolute;
    left: 8px; top: 0; bottom: 0;
    width: 2px;
    background: linear-gradient(to bottom, #1e3c72, #7c3aed, #ff4b2b);
    border-radius: 2px;
  }
  .timeline-item {
    position: relative;
    margin-bottom: 22px;
    padding: 16px 18px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.06);
  }
  .timeline-item::before {
    content: '';
    position: absolute;
    left: -24px; top: 18px;
    width: 14px; height: 14px;
    border-radius: 50%;
    border: 3px solid #1e3c72;
    background: white;
  }
  .timeline-year {
    display: inline-block;
    background: #1e3c72;
    color: white;
    font-size: 0.75rem;
    font-weight: 700;
    padding: 2px 10px;
    border-radius: 20px;
    margin-bottom: 6px;
  }
  .timeline-item p { margin: 0; font-size: 0.95rem; color: #444; }

  .discovery-card {
    background: white;
    border-radius: 16px;
    padding: 26px 28px;
    margin: 24px 0;
    box-shadow: 0 4px 18px rgba(0,0,0,0.08);
    border-top: 5px solid #1e3c72;
    transition: transform 0.2s;
  }
  .discovery-card:hover { transform: translateY(-3px); }
  .discovery-card:nth-child(2) { border-top-color: #7c3aed; }
  .discovery-card:nth-child(3) { border-top-color: #d97706; }
  .discovery-card:nth-child(4) { border-top-color: #dc2626; }
  .discovery-card:nth-child(5) { border-top-color: #059669; }
  .discovery-card:nth-child(6) { border-top-color: #0891b2; }
  .discovery-card:nth-child(7) { border-top-color: #9333ea; }

  .discovery-number {
    display: inline-flex; align-items: center; justify-content: center;
    width: 36px; height: 36px;
    background: linear-gradient(135deg, #1e3c72, #7c3aed);
    color: white; border-radius: 50%;
    font-size: 0.9rem; font-weight: 800;
    margin-bottom: 12px;
  }
  .discovery-title { font-size: 1.1rem; font-weight: 700; color: #1e3c72; margin-bottom: 10px; }

  .app-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 12px; }
  .app-tag {
    display: inline-flex; align-items: center; gap: 5px;
    background: #eff6ff; color: #1e3c72;
    border: 1px solid #bfdbfe;
    border-radius: 20px; padding: 4px 12px;
    font-size: 0.78rem; font-weight: 600;
  }
  .app-tag.purple { background: #f5f3ff; color: #6d28d9; border-color: #ddd6fe; }
  .app-tag.green  { background: #ecfdf5; color: #065f46; border-color: #a7f3d0; }
  .app-tag.orange { background: #fff7ed; color: #92400e; border-color: #fed7aa; }

  .highlight-quote {
    background: linear-gradient(135deg, #fef3c7, #fde68a);
    border-left: 5px solid #d97706;
    border-radius: 0 12px 12px 0;
    padding: 18px 22px;
    margin: 20px 0;
    font-style: italic;
    color: #78350f;
    font-size: 1rem;
    line-height: 1.7;
  }
  .highlight-quote .quote-src {
    display: block; margin-top: 8px;
    font-style: normal; font-weight: 700;
    font-size: 0.85rem; color: #92400e;
  }

  .contrast-quote {
    background: linear-gradient(135deg, #1e3c72, #2a5298);
    border-radius: 12px;
    padding: 20px 24px;
    margin: 20px 0;
    color: white;
    font-style: italic;
    font-size: 1rem;
    line-height: 1.7;
  }
  .contrast-quote .quote-src {
    display: block; margin-top: 8px;
    font-style: normal; font-weight: 700;
    font-size: 0.85rem; color: #fbbf24;
  }

  .compare-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 20px 0; }
  .compare-card { border-radius: 12px; padding: 18px 20px; }
  .compare-card.hardy  { background: #eff6ff; border: 2px solid #93c5fd; }
  .compare-card.ramanu { background: #fdf4ff; border: 2px solid #e9d5ff; }
  .compare-card h4 { margin: 0 0 10px; font-size: 1rem; font-weight: 700; }
  .compare-card.hardy h4  { color: #1e40af; }
  .compare-card.ramanu h4 { color: #6d28d9; }
  .compare-card ul { margin: 0; padding-left: 18px; font-size: 0.9rem; color: #444; }
  .compare-card ul li { margin-bottom: 4px; }

  .taxicab-box {
    background: linear-gradient(135deg, #fef9c3, #fde68a);
    border-radius: 16px;
    padding: 24px 28px;
    margin: 22px 0;
    border: 2px solid #fbbf24;
    text-align: center;
  }
  .taxicab-number { font-size: 3.5rem; font-weight: 900; color: #92400e; line-height: 1; margin-bottom: 8px; }
  .taxicab-proof  { font-size: 1.1rem; color: #78350f; font-weight: 600; }

  .stats-strip {
    background: linear-gradient(135deg, #1e3c72, #7c3aed);
    border-radius: 16px;
    padding: 28px 30px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    gap: 20px;
    margin: 30px 0;
    text-align: center;
    color: white;
  }
  .stat-item .num { font-size: 2.2rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.78rem; opacity: 0.8; margin-top: 5px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }

  .syllabus-table {
    width: 100%; border-collapse: collapse; margin: 20px 0;
    border-radius: 12px; overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.07);
  }
  .syllabus-table th {
    background: linear-gradient(135deg, #1e3c72, #2a5298);
    color: white; padding: 14px 18px;
    text-align: left; font-size: 0.9rem;
  }
  .syllabus-table td {
    padding: 12px 18px; font-size: 0.9rem; color: #333;
    border-bottom: 1px solid #e5e7eb;
  }
  .syllabus-table tr:nth-child(even) td { background: #f8faff; }
  .syllabus-table tr:last-child td { border-bottom: none; }
  .syllabus-table td:first-child { font-weight: 700; color: #1e3c72; }

  .lessons-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 14px;
    margin: 20px 0;
  }
  .lesson-card {
    background: white;
    border-radius: 12px;
    padding: 18px 16px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.06);
    border-top: 4px solid #1e3c72;
    text-align: center;
  }
  .lesson-card:nth-child(2) { border-top-color: #7c3aed; }
  .lesson-card:nth-child(3) { border-top-color: #d97706; }
  .lesson-card:nth-child(4) { border-top-color: #059669; }
  .lesson-card .lesson-icon { font-size: 1.8rem; margin-bottom: 8px; }
  .lesson-card p { font-size: 0.88rem; color: #555; margin: 0; line-height: 1.5; }
  .lesson-card strong { color: #1e3c72; display: block; margin-bottom: 4px; font-size: 0.92rem; }

  .final-quote {
    background: linear-gradient(135deg, #0f172a, #1e3c72, #6b21a8);
    border-radius: 18px;
    padding: 38px 40px;
    margin: 40px 0 20px;
    text-align: center;
    color: white;
    position: relative;
    overflow: hidden;
  }
  .final-quote::after {
    content: "∞";
    position: absolute;
    right: 20px; bottom: -20px;
    font-size: 8rem;
    color: rgba(255,255,255,0.05);
    font-family: serif;
  }
  .final-quote p {
    font-size: 1.15rem; font-style: italic;
    margin: 0 0 12px; line-height: 1.8;
    position: relative; z-index: 1;
  }
  .final-quote .attr { color: #fbbf24; font-weight: 700; font-size: 0.9rem; }

  .film-note {
    background: #f0fdf4;
    border: 2px dashed #86efac;
    border-radius: 12px;
    padding: 18px 22px;
    margin-top: 25px;
    font-size: 0.92rem;
    color: #166534;
  }

  @media (max-width: 640px) {
    .compare-grid { grid-template-columns: 1fr; }
    .stats-strip { flex-direction: column; align-items: center; }
    .opening-quote { padding: 28px 20px; }
    .opening-quote p { font-size: 1.05rem; }
  }
</style>

<div class="ramanujan-post">

<!-- OPENING QUOTE -->
<div class="opening-quote">
  <p>"An equation for me has no meaning unless it expresses a thought of God."</p>
  <span class="quote-attr">— Srinivasa Ramanujan</span>
</div>

<!-- STATS STRIP -->
<div class="stats-strip">
  <div class="stat-item"><span class="num">1887</span><span class="lbl">Year of Birth</span></div>
  <div class="stat-item"><span class="num">32</span><span class="lbl">Age at Death</span></div>
  <div class="stat-item"><span class="num">3900+</span><span class="lbl">Mathematical Results</span></div>
  <div class="stat-item"><span class="num">100</span><span class="lbl">Pages — Lost Notebook</span></div>
  <div class="stat-item"><span class="num">FRS</span><span class="lbl">First Indian Fellow</span></div>
</div>

<!-- SECTION 1: INTRODUCTION -->
<h2><span class="sec-icon" style="background:#eff6ff; color:#1e3c72;"><i class="fas fa-book-open"></i></span> Introduction</h2>

In the history of mathematics, a few names rise above mere numbers and formulas to become enduring symbols of inspiration. Srinivasa Ramanujan is one such name — a man who, from a small town in South India, without formal training, without a laboratory, without any mentor, discovered mathematical truths that still astonish the world's greatest mathematicians today.

Ramanujan's story is not merely the story of a prodigy. It is the story of a man who found infinity in poverty, who refused to abandon mathematics despite hunger and illness, who nourished his genius through devotion to his mother, his wife, his culture, and his goddess Namagiri.

This article presents a detailed account of Ramanujan's life, his family, his struggles, his mathematical discoveries, and his enduring legacy.

<!-- SECTION 2: BIRTH AND EARLY LIFE -->
<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-star-and-crescent"></i></span> Birth and Early Life</h2>

<h3>Birth</h3>

Srinivasa Ramanujan Iyengar was born on <strong>22 December 1887</strong> in <strong>Erode</strong>, Tamil Nadu. His mother, Komalatammal, had come to her parents' home for the delivery. Within days, the family returned to <strong>Kumbakonam</strong>, where Ramanujan spent most of his childhood.

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-map-marker-alt"></i> Kumbakonam — A Sacred Town</div>
  Kumbakonam is an ancient, deeply religious town on the banks of the Kaveri river. Famous for its magnificent temples, learned priests and classical music, this environment shaped Ramanujan's personality in profound ways.
</div>

<h3>Family Background</h3>

Ramanujan's family was a <strong>Brahmin family</strong> of modest means. His father, <strong>Srinivasa Iyengar</strong>, worked as a clerk in a cloth merchant's shop, earning around twenty rupees a month — barely enough even then for a large family.

His mother, <strong>Komalatammal</strong>, was a religious, spirited, and strong-willed woman. She sang devotional songs at the local Namagiri temple and was a devoted follower of the goddess Namagiri. Her influence on Ramanujan's life was immense. The bond between mother and son was extraordinarily close.

Ramanujan had several siblings, but most died in infancy. This grief made the family centre itself even more deeply around Ramanujan.

<h3>Goddess Namagiri — His Spiritual Inspiration</h3>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-om"></i> Spiritual Source</div>
  The goddess <strong>Namagiri</strong> held a place of supreme importance in Ramanujan's life. The Namagiri temple at Namakkal was his mother's place of worship. Ramanujan himself attributed his mathematical gift to the goddess.
</div>

He often said that the goddess Namagiri would appear in his dreams and write mathematical formulas on his tongue. Upon waking each morning, he would immediately record those formulas in his notebook.

This was not mere superstition — it was a symbol of Ramanujan's extraordinary power of intuition. His mind continued working on mathematical problems even in sleep, and answers came to him in dreams.

<!-- SECTION 3: MATHEMATICAL TALENT IN CHILDHOOD -->
<h2><span class="sec-icon" style="background:#ecfdf5; color:#059669;"><i class="fas fa-child"></i></span> Mathematical Talent in Childhood</h2>

<h3>An Extraordinary Child</h3>

Ramanujan displayed exceptional talent from a very early age. His memory was phenomenal — once he saw or heard something, it was permanently etched into his mind.

<div class="timeline">
  <div class="timeline-item">
    <span class="timeline-year">Age 5</span>
    <p>Began formal schooling. Stunned teachers with answers they had never seen before.</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">Age 10</span>
    <p>Scored <strong>top marks in the district</strong> primary examination. Left everyone astonished.</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">Age 15</span>
    <p>Obtained G. S. Carr's book — a moment that changed the direction of his life forever.</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">Age 16</span>
    <p>Independently proved all 5000 theorems in Carr's book and extended many of them with new results.</p>
  </div>
</div>

<h3>Carr's Book — A Life-Changing Moment</h3>

<div class="info-card blue">
  <div class="info-card-header"><i class="fas fa-book"></i> That Great Book</div>
  At <strong>age fifteen</strong>, Ramanujan obtained a copy of <strong>G. S. Carr's</strong> <em>"A Synopsis of Elementary Results in Pure and Applied Mathematics"</em> — a collection of over 5000 mathematical theorems and formulas, most without proofs.
</div>

An ordinary student would have been discouraged. But Ramanujan took it as a challenge. He attempted to prove every single formula himself, and wherever he found them incomplete, he developed entirely new formulas. This book became his <strong>university of mathematics</strong>.

<!-- SECTION 4: FAILURE IN FORMAL EDUCATION -->
<h2><span class="sec-icon" style="background:#fff5f5; color:#dc2626;"><i class="fas fa-times-circle"></i></span> Failure in Formal Education — A Painful Truth</h2>

<h3>Struggle in College</h3>

Ramanujan's obsession with mathematics meant he could not pay attention to any other subject.

<div class="timeline">
  <div class="timeline-item">
    <span class="timeline-year">1904</span>
    <p>Entered <strong>Government Arts College, Kumbakonam</strong>. Won a mathematics scholarship. But failed in all other subjects — scholarship revoked.</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">1905</span>
    <p>Ran away from home, reached Visakhapatnam. Family brought him back.</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">1906</span>
    <p>Entered <strong>Pachaiyappa's College, Madras</strong>. Failed the F.A. examination <strong>twice</strong>.</p>
  </div>
</div>

<div class="info-card red">
  <div class="info-card-header"><i class="fas fa-pencil-alt"></i> Life Without a Degree</div>
  Without any formal degree, Ramanujan spent years in a hand-to-mouth struggle. He gave private tuitions — sometimes in exchange for meals. <strong>Paper was expensive</strong>, so he worked on a slate, transferring only the most important results to his notebooks.
</div>

<!-- SECTION 5: MARRIAGE AND FAMILY LIFE -->
<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-heart"></i></span> Marriage and Family Life</h2>

<h3>Marriage to Janaki</h3>

In <strong>1909</strong>, when Ramanujan was 21, he was married. His wife's name was <strong>Janaki Ammal</strong>. At the time of their marriage, Janaki was only <strong>nine years old</strong> (child marriage was common in that era).

Janaki was a quiet, gentle, and devoted woman. She did not understand Ramanujan's mathematical genius, but she stood by him always. When Ramanujan left for England, Janaki stayed behind with her mother-in-law Komalatammal.

After Ramanujan's departure, there arose tension between mother and daughter-in-law. Komalatammal prevented Janaki from going to England and also withheld Ramanujan's letters from her. Ramanujan did not know whether his letters were reaching Janaki at all.

<h3>Mother Komalatammal — Strength and Conflict</h3>

The relationship between Ramanujan and his mother was complex and deep. It was she who instilled in him devotion to goddess Namagiri. She who taught him Sanskrit verses. Her lullabies held numbers in them; her devotional songs were threaded with mathematics.

<div class="highlight-quote">
  Komalatammal was a woman of strong personality. All important family decisions were hers. She was deeply opposed to Ramanujan crossing the seas — in a strict Brahmin family, travelling across the ocean was considered a transgression of faith. But ultimately, after Goddess Namagiri appeared to her in a dream and gave her blessing, she granted her permission.
</div>

<!-- SECTION 6: STRUGGLES IN MADRAS -->
<h2><span class="sec-icon" style="background:#fff7ed; color:#d97706;"><i class="fas fa-city"></i></span> Struggles in Madras — In Search of Recognition</h2>

<h3>Meeting Ramachandra Rao</h3>

<strong>Around 1910–11</strong>, Ramanujan met <strong>Diwan Bahadur Ramachandra Rao</strong>, District Collector of Madras, and showed him his notebook. Rao was astounded.

<div class="highlight-quote">
  "Before me sat a half-starved man holding a notebook. I opened it and saw — results I had never seen before, formulas that existed in no known text."
  <span class="quote-src">— Diwan Bahadur Ramachandra Rao</span>
</div>

<h3>Clerk at Madras Port Trust</h3>

In <strong>1912</strong>, Ramanujan was appointed as a clerk at <strong>Madras Port Trust</strong>. Monthly salary — <strong>thirty rupees</strong>. This was his first stable income. His supervisor <strong>S. Narayana Iyer</strong> recognised his talent and gave him time and encouragement for mathematics, eventually presenting him to the Indian Mathematical Society.

<h3>Connection with the Indian Mathematical Society</h3>

In <strong>1911</strong>, Ramanujan's first research paper was published — *"On Some Properties of Bernoulli Numbers"* — in the <strong>Journal of the Indian Mathematical Society</strong>. This was an important milestone. His name was now known in the world of mathematics.

<!-- SECTION 7: THE LETTER TO HARDY -->
<h2><span class="sec-icon" style="background:#eff6ff; color:#1e3c72;"><i class="fas fa-envelope-open-text"></i></span> The Letter to Hardy — That Historic Moment</h2>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-calendar-day"></i> 16 January 1913 — A Date Immortalised in History</div>
  On this day, Ramanujan wrote a letter to Professor <strong>Godfrey Harold Hardy</strong> of Cambridge University — enclosing a list of <strong>over 120 theorems and formulas</strong>, without any proofs.
</div>

<h3>The Decision to Write</h3>

In his letter, Ramanujan wrote:

<div class="highlight-quote">
  "I am a clerk in the Madras Port Trust. I am 23 years of age. I have had no university education. But I have found some mathematical results that might be of interest to you..."
  <span class="quote-src">— Ramanujan's letter to Hardy, 1913</span>
</div>

<h3>Hardy's Reaction</h3>

Hardy initially set the letter aside, thinking it the work of a crank. But that night he could not sleep. The formulas in the letter kept circling in his mind. In the morning he called his colleague <strong>John Edensor Littlewood</strong>.

Together they examined the formulas for hours. They found:
- Some formulas were already known — but Ramanujan had discovered them independently
- Some formulas were <strong>entirely new</strong> and of astounding validity
- Some formulas were so complex that even Hardy and Littlewood could not immediately prove them

<div class="contrast-quote">
  "They must be true because, if they were not true, no one would have had the imagination to invent them."
  <span class="quote-src">— Professor G. H. Hardy</span>
</div>

Hardy wrote back immediately and invited Ramanujan to Cambridge.

<!-- SECTION 8: CAMBRIDGE -->
<h2><span class="sec-icon" style="background:#f0fdf4; color:#059669;"><i class="fas fa-university"></i></span> Cambridge — A New World</h2>

<h3>The Journey to England</h3>

Travelling to England was not easy for Ramanujan. His mother strongly objected, fearing spiritual transgression. In strict Brahmin tradition, crossing the seas was considered religiously forbidden.

Eventually, <strong>Goddess Namagiri appeared to his mother in a dream</strong> and told her to let Ramanujan go. After this dream, she gave her blessing.

On <strong>17 March 1914</strong>, Ramanujan departed Madras for England. The journey was long and difficult. For a strict vegetarian Brahmin, finding suitable food on board the ship was itself a challenge.

<h3>Life at Cambridge</h3>

Arriving at Cambridge, Ramanujan found a new world — vast libraries, eminent professors, an environment of mathematical discussion. But there were hardships too.

<div class="compare-grid">
  <div class="compare-card hardy">
    <h4><i class="fas fa-exclamation-triangle"></i> Hardships</h4>
    <ul>
      <li><strong>Food:</strong> Vegetarian food was almost impossible to find</li>
      <li><strong>Climate:</strong> Cold and fog — a stark contrast to South India's warmth</li>
      <li><strong>World War I:</strong> Life became even harder from 1914 onwards</li>
    </ul>
  </div>
  <div class="compare-card ramanu">
    <h4><i class="fas fa-check-circle"></i> Achievements</h4>
    <ul>
      <li>Access to vast libraries and resources</li>
      <li>Mentorship from Hardy — the finest mathematician of his time</li>
      <li>Five years of extraordinary discoveries</li>
    </ul>
  </div>
</div>

<h3>The Hardy–Ramanujan Partnership</h3>

The Hardy–Ramanujan partnership is one of the most remarkable in the history of mathematics.

<div class="compare-grid">
  <div class="compare-card hardy">
    <h4><i class="fas fa-calculator"></i> Professor Hardy</h4>
    <ul>
      <li>Rationalist, atheist</li>
      <li>Systematic, disciplined</li>
      <li>Believed in rigorous proof</li>
    </ul>
  </div>
  <div class="compare-card ramanu">
    <h4><i class="fas fa-star"></i> Ramanujan</h4>
    <ul>
      <li>Deeply religious, intuitive</li>
      <li>Results often arrived without proof</li>
      <li>Deeply emotional and spiritual</li>
    </ul>
  </div>
</div>

But both shared one thing — <strong>an indomitable love of mathematics.</strong> Hardy taught Ramanujan the formal language of mathematics. Ramanujan gave Hardy the insight that no textbook could ever provide.

<!-- SECTION 9: MATHEMATICAL DISCOVERIES -->
<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-atom"></i></span> The Great Mathematical Discoveries</h2>

<div class="discovery-card">
  <div class="discovery-number">1</div>
  <div class="discovery-title">Partition of Numbers — $p(n)$</div>
  One of Ramanujan's most celebrated contributions is the <strong>theory of number partitions</strong>. The partition function $p(n)$ counts the number of ways a positive integer $n$ can be written as a sum of positive integers.

  For example, the partitions of $n = 4$ are:
  $$4 = 4 \qquad 4 = 3+1 \qquad 4 = 2+2 \qquad 4 = 2+1+1 \qquad 4 = 1+1+1+1$$
  So $p(4) = 5$.

  Together, Hardy and Ramanujan developed the famous <strong>Hardy–Ramanujan asymptotic formula</strong>:
  $$p(n) \sim \frac{1}{4n\sqrt{3}} \cdot e^{\pi\sqrt{\frac{2n}{3}}} \quad \text{as } n \to \infty$$

  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-atom"></i> Physics — Energy Levels</span>
    <span class="app-tag purple"><i class="fas fa-project-diagram"></i> String Theory</span>
    <span class="app-tag green"><i class="fas fa-chart-bar"></i> Statistical Mechanics</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">2</div>
  <div class="discovery-title">Ramanujan's Remarkable Formula for $\pi$</div>
  $$\frac{1}{\pi} = \frac{2\sqrt{2}}{9801} \sum_{k=0}^{\infty} \frac{(4k)!\,(1103 + 26390k)}{(k!)^4 \cdot 396^{4k}}$$
  Each term of this series adds approximately <strong>eight correct decimal places</strong> of $\pi$. Today's supercomputers use this very formula to compute $\pi$ to <strong>trillions of decimal places</strong>.
  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-desktop"></i> Supercomputing</span>
    <span class="app-tag purple"><i class="fas fa-infinity"></i> Numerical Methods</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">3</div>
  <div class="discovery-title">The Taxicab Number — 1729</div>

<div class="taxicab-box">
  <div class="taxicab-number">1729</div>
  <div class="taxicab-proof">$1729 = 1^3 + 12^3 = 9^3 + 10^3$</div>
  <p style="font-size:0.85rem; color:#78350f; margin-top:8px;">The smallest number expressible as the sum of two cubes in two different ways</p>
</div>

  Hardy was visiting Ramanujan in hospital and mentioned his taxi's number was 1729, which seemed dull. Ramanujan instantly replied with the number's remarkable property. This anecdote is the most celebrated demonstration of Ramanujan's extraordinary <strong>number sense</strong>.
</div>

<div class="discovery-card">
  <div class="discovery-number">4</div>
  <div class="discovery-title">Infinite Series — A Startling Result</div>
  $$1 + 2 + 3 + 4 + 5 + \cdots = -\frac{1}{12}$$
  This appears utterly impossible — yet it is true in the framework of the <strong>Riemann Zeta Function</strong>. Today this result plays a crucial role in <strong>quantum physics</strong> and <strong>string theory</strong>.
  <div class="app-tags">
    <span class="app-tag purple"><i class="fas fa-atom"></i> Quantum Physics</span>
    <span class="app-tag orange"><i class="fas fa-project-diagram"></i> String Theory</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">5</div>
  <div class="discovery-title">Ramanujan Primes</div>
  Ramanujan made important contributions to the theory of prime numbers. A <strong>Ramanujan prime</strong> $R_n$ is a special case of the <strong>Bertrand–Chebyshev theorem</strong>. He proved that there are at least $n$ prime numbers between $x$ and $2x$, whenever $x \geq R_n$.
</div>

<div class="discovery-card">
  <div class="discovery-number">6</div>
  <div class="discovery-title">Ramanujan Theta Function</div>
  $$f(a,b) = \sum_{n=-\infty}^{\infty} a^{n(n+1)/2} \cdot b^{n(n-1)/2}$$
  This function is the foundation of the theory of <strong>Modular Forms</strong>.
  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-lock"></i> Cryptography</span>
    <span class="app-tag green"><i class="fas fa-wifi"></i> Digital Communications</span>
    <span class="app-tag purple"><i class="fas fa-microchip"></i> Quantum Computing</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">7</div>
  <div class="discovery-title">Mock Theta Functions — His Most Mysterious Legacy</div>
  <div class="info-card purple" style="margin:10px 0;">
    <div class="info-card-header"><i class="fas fa-envelope"></i> The Final Letter — 1920</div>
    A few weeks before his death, Ramanujan wrote a final letter to Hardy introducing the concept of <strong>Mock Theta Functions</strong>. Mathematicians, including Hardy, could not fully understand these functions for <strong>80 years</strong>.
  </div>
  In <strong>2002</strong>, mathematician Sander Zwegers connected them to <strong>Harmonic Maass Forms</strong> — a landmark achievement of modern mathematics.
  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-circle"></i> Black Hole Physics</span>
    <span class="app-tag purple"><i class="fas fa-atom"></i> Particle Physics</span>
  </div>
</div>

<!-- SECTION 10: FELLOWSHIP -->
<h2><span class="sec-icon" style="background:#fff7ed; color:#d97706;"><i class="fas fa-award"></i></span> Fellowship — India's Pride</h2>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-trophy"></i> 1918 — A Historic Honour</div>
  Ramanujan was elected <strong>Fellow of the Royal Society (F.R.S.)</strong> — the <strong>first Indian</strong> ever to receive this honour. In the same year he was also elected Fellow of <strong>Trinity College, Cambridge</strong>.
</div>

In <strong>1918</strong>, Ramanujan was elected Fellow of the <strong>Royal Society</strong> (London) — the highest recognition in science and mathematics at the time, and he was the <strong>first Indian</strong> to receive it.

The news was celebrated across India like a festival. A clerk without a degree, from a poor family, from no metropolitan city — had received the world's highest mathematical honour.

<!-- SECTION 11: ILLNESS AND RETURN -->
<h2><span class="sec-icon" style="background:#fff5f5; color:#dc2626;"><i class="fas fa-heartbeat"></i></span> Illness and Return</h2>

<h3>The Attack of Tuberculosis</h3>

While in England, Ramanujan's health gradually deteriorated. In <strong>1917</strong>, he was admitted to <strong>Matlock Sanatorium</strong> with serious illness, suspected to be <strong>tuberculosis</strong>.

<div class="info-card red">
  <div class="info-card-header"><i class="fas fa-book-medical"></i> Mathematics Even in Hospital</div>
  Even in hospital, Ramanujan continued doing mathematics. Even in fever, he would open his notebook and write formulas. It was here that Hardy came to visit him and mentioned the taxicab number 1729.
</div>

<h3>Return to India</h3>

On <strong>27 February 1919</strong>, Ramanujan left England for India. Five years had passed — and he was returning as a celebrated mathematician. But his condition on arrival was extremely weak. He went to Madras and then to <strong>Chetput</strong> for treatment.

<!-- SECTION 12: FINAL DAYS AND LEGACY -->
<h2><span class="sec-icon" style="background:#1e3c72; color:white;"><i class="fas fa-star"></i></span> Final Days and Legacy</h2>

<h3>Death</h3>

<div class="info-card red">
  <div class="info-card-header"><i class="fas fa-calendar-times"></i> 26 April 1920</div>
  At only <strong>32 years of age</strong>, Srinivasa Ramanujan passed away. Even in his final days he was doing mathematics. His wife Janaki recalled that until the very end he would wake at night and write on his slate.
</div>

<div class="contrast-quote">
  "Mathematics has lost its most romantic figure."
  <span class="quote-src">— Professor G. H. Hardy</span>
</div>

<h3>The Lost Notebook — A Miraculous Discovery</h3>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-book"></i> 1976 — The Lost Notebook Found</div>
  Mathematician <strong>George Andrews</strong> discovered Ramanujan's <strong>100-page lost notebook</strong> in the <strong>Wren Library, Cambridge</strong> — now known as the <strong>"Lost Notebook"</strong>. It took mathematicians <strong>over 30 years</strong> of research to fully explore it.
</div>

<!-- SECTION 13: MODERN APPLICATIONS -->
<h2><span class="sec-icon" style="background:#ecfdf5; color:#059669;"><i class="fas fa-laptop-code"></i></span> Ramanujan's Contributions in Modern Mathematics</h2>

Ramanujan's discoveries live on vibrantly in today's science and technology:

<div class="lessons-grid">
  <div class="lesson-card">
    <div class="lesson-icon">💻</div>
    <strong>Computer Science</strong>
    <p>His formula for $\pi$ is used in supercomputers to compute trillions of decimal places.</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">🔐</div>
    <strong>Cryptography</strong>
    <p>His Modular Forms theory underpins modern data security and encryption.</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">⚛️</div>
    <strong>Physics</strong>
    <p>His work appears in String Theory and Quantum Gravity.</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">📊</div>
    <strong>Statistics</strong>
    <p>Partition theory is used in Statistical Mechanics and Thermodynamics.</p>
  </div>
</div>

<!-- SECTION 14: INDIAN CULTURE -->
<h2><span class="sec-icon" style="background:#fff7ed; color:#d97706;"><i class="fas fa-om"></i></span> Ramanujan and Indian Culture</h2>

Ramanujan was not merely a mathematician — he was the embodiment of the <strong>meeting point between Indian spirituality and mathematical genius</strong>.

He demonstrated that mathematics and spirituality are not opposites. When he said *"the goddess gave me the formulas,"* he was speaking of the power of his intuition — that deep concentration which we call meditation or *sadhana*.

<div class="lessons-grid">
  <div class="lesson-card">
    <div class="lesson-icon">🌱</div>
    <strong>Talent is Innate</strong>
    <p>It does not depend on any university or institution.</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">💪</div>
    <strong>Struggle Refines Genius</strong>
    <p>Hardship did not break Ramanujan — it made him stronger.</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">🏠</div>
    <strong>Family as Foundation</strong>
    <p>His mother's devotion and culture kept his inspiration alive.</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">🌍</div>
    <strong>Mathematics is Universal</strong>
    <p>It sees no caste, no country, no religion.</p>
  </div>
</div>

<!-- SECTION 15: SYLLABUS RELEVANCE -->
<h2><span class="sec-icon" style="background:#eff6ff; color:#1e3c72;"><i class="fas fa-graduation-cap"></i></span> Relevance to CSIR NET, GATE and IIT JAM</h2>

Ramanujan's work connects directly to your examination syllabus:

<table class="syllabus-table">
  <thead>
    <tr><th>Topic</th><th>Ramanujan's Contribution</th></tr>
  </thead>
  <tbody>
    <tr><td>Number Theory</td><td>Partition function, prime numbers, taxicab numbers</td></tr>
    <tr><td>Infinite Series</td><td>Convergence tests, special series</td></tr>
    <tr><td>Complex Analysis</td><td>Theta functions, Modular Forms</td></tr>
    <tr><td>Real Analysis</td><td>Infinite series, continued fractions</td></tr>
    <tr><td>Applied Mathematics</td><td>Computation of $\pi$, numerical methods</td></tr>
  </tbody>
</table>

<!-- CLOSING -->
<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-infinity"></i></span> Conclusion</h2>

Ramanujan's story does not end — it continues to grow. The formulas in his notebooks continue to inspire new research. His discoveries continue to strengthen the foundations of mathematics and science.

He was a man who turned poverty into opportunity, struggle into devotion, and from the soil of a small Indian town, flung open the doors of infinity.

<div class="info-card gold" style="text-align:center; margin:25px 0;">
  <div class="info-card-header" style="justify-content:center;"><i class="fas fa-calendar-check"></i> National Mathematics Day</div>
  <strong>22 December</strong> is celebrated as <strong>National Mathematics Day in India</strong> — in honour of Ramanujan's birthday.
</div>

Whenever you study mathematics, whenever a problem seems too difficult, whenever you feel you cannot go on — remember Ramanujan. A man who, through hunger, through illness, through loneliness — <strong>knew infinity</strong>.

<div class="final-quote">
  <p>"I have never met his equal, and I can compare him only with Euler or Jacobi."</p>
  <span class="attr">— Professor G. H. Hardy</span>
</div>

<div class="film-note">
  <i class="fas fa-film"></i> <strong>Recommendation:</strong> To learn more about Ramanujan's life, watch the 2015 film <strong>"The Man Who Knew Infinity"</strong> — a deeply inspiring portrayal of his extraordinary journey.
</div>

</div>
