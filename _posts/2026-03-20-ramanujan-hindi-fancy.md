---
layout: post
title: "श्रीनिवास रामानुजन् — अनंत को जानने वाला महान गणितज्ञ"
date: 2026-03-20
category: history
lang: hi
lang_pair: "/blog/ramanujan-english/"
permalink: /blog/ramanujan-hindi/
description: "श्रीनिवास रामानुजन् के जीवन, संघर्षों, गणितीय खोजों और भारतीय संस्कृति से गहरे जुड़ाव की विस्तृत कहानी — हिंदी में।"
---

<link href="https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&family=Tiro+Devanagari+Hindi:ital@0;1&display=swap" rel="stylesheet">

<style>
  /* ── Base Hindi Typography ── */
  .ramanujan-post {
    font-family: 'Hind', 'Noto Sans Devanagari', sans-serif;
    font-size: 1.08rem;
    line-height: 1.9;
    color: #2d2d2d;
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── Opening Quote ── */
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
    font-family: 'Tiro Devanagari Hindi', serif;
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

  /* ── Section Headers ── */
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

  /* ── Info Cards ── */
  .info-card {
    background: white;
    border-radius: 14px;
    padding: 24px 28px;
    margin: 22px 0;
    box-shadow: 0 4px 16px rgba(0,0,0,0.07);
    border-left: 5px solid #1e3c72;
    position: relative;
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

  /* ── Timeline ── */
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

  /* ── Math Discovery Cards ── */
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
  .discovery-title {
    font-size: 1.1rem; font-weight: 700;
    color: #1e3c72; margin-bottom: 10px;
  }

  /* ── Formula Box ── */
  .formula-box {
    background: linear-gradient(135deg, #0f172a 0%, #1e3a5f 100%);
    border-radius: 12px;
    padding: 22px 24px;
    margin: 16px 0;
    text-align: center;
    overflow-x: auto;
  }
  .formula-box .MathJax, .formula-box .katex {
    color: #fff !important;
  }

  /* ── Applications Tags ── */
  .app-tags {
    display: flex; flex-wrap: wrap; gap: 8px;
    margin-top: 12px;
  }
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

  /* ── Highlight Quote ── */
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

  /* ── Contrast Quote (Hardy) ── */
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

  /* ── Personality Compare ── */
  .compare-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin: 20px 0;
  }
  .compare-card {
    border-radius: 12px;
    padding: 18px 20px;
  }
  .compare-card.hardy   { background: #eff6ff; border: 2px solid #93c5fd; }
  .compare-card.ramanu  { background: #fdf4ff; border: 2px solid #e9d5ff; }
  .compare-card h4 {
    margin: 0 0 10px;
    font-size: 1rem; font-weight: 700;
  }
  .compare-card.hardy h4  { color: #1e40af; }
  .compare-card.ramanu h4 { color: #6d28d9; }
  .compare-card ul { margin: 0; padding-left: 18px; font-size: 0.9rem; color: #444; }
  .compare-card ul li { margin-bottom: 4px; }

  /* ── Taxicab Special Box ── */
  .taxicab-box {
    background: linear-gradient(135deg, #fef9c3, #fde68a);
    border-radius: 16px;
    padding: 24px 28px;
    margin: 22px 0;
    border: 2px solid #fbbf24;
    text-align: center;
  }
  .taxicab-number {
    font-size: 3.5rem;
    font-weight: 900;
    color: #92400e;
    line-height: 1;
    margin-bottom: 8px;
  }
  .taxicab-proof {
    font-size: 1.1rem;
    color: #78350f;
    font-weight: 600;
  }

  /* ── Legacy Stats ── */
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

  /* ── Syllabus Table ── */
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

  /* ── Lessons List ── */
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

  /* ── Final Quote ── */
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
    font-family: 'Tiro Devanagari Hindi', serif;
    font-size: 1.15rem; font-style: italic;
    margin: 0 0 12px; line-height: 1.8;
    position: relative; z-index: 1;
  }
  .final-quote .attr { color: #fbbf24; font-weight: 700; font-size: 0.9rem; }

  /* ── Film Note ── */
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

<!-- ══════════════════════════════════════════ -->
<!-- OPENING QUOTE -->
<!-- ══════════════════════════════════════════ -->

<div class="opening-quote">
  <p>"गणित में एक समीकरण का तब तक कोई अर्थ नहीं जब तक वह ईश्वर के एक विचार को व्यक्त न करे।"</p>
  <span class="quote-attr">— श्रीनिवास रामानुजन्</span>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- STATS STRIP -->
<!-- ══════════════════════════════════════════ -->

<div class="stats-strip">
  <div class="stat-item"><span class="num">1887</span><span class="lbl">जन्म वर्ष</span></div>
  <div class="stat-item"><span class="num">32</span><span class="lbl">वर्ष की आयु में निधन</span></div>
  <div class="stat-item"><span class="num">3900+</span><span class="lbl">गणितीय परिणाम</span></div>
  <div class="stat-item"><span class="num">100</span><span class="lbl">पृष्ठ — खोई नोटबुक</span></div>
  <div class="stat-item"><span class="num">FRS</span><span class="lbl">पहले भारतीय</span></div>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 1: PRASTAVNA -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#eff6ff; color:#1e3c72;"><i class="fas fa-book-open"></i></span> प्रस्तावना</h2>

गणित के इतिहास में कुछ ऐसे नाम हैं जो केवल संख्याओं और सूत्रों से परे, एक प्रेरणा बन जाते हैं। श्रीनिवास रामानुजन् ऐसा ही एक नाम है — एक ऐसा व्यक्ति जिसने दक्षिण भारत के एक छोटे से शहर में, बिना किसी उचित शिक्षा के, बिना किसी प्रयोगशाला के, बिना किसी मार्गदर्शक के — ऐसे गणितीय सत्यों की खोज की जो आज भी विश्व के श्रेष्ठतम गणितज्ञों को चकित करते हैं।

रामानुजन् की कहानी केवल एक प्रतिभाशाली व्यक्ति की कहानी नहीं है। यह एक ऐसे इंसान की कहानी है जिसने अभाव में भी अनंत को पाया, जिसने भूख और बीमारी के बावजूद गणित से मुँह नहीं मोड़ा, जिसने अपनी माँ, अपनी पत्नी, अपनी संस्कृति और अपने देवी नामगिरि की भक्ति से अपनी प्रतिभा को पोषित किया।

यह लेख रामानुजन् के जीवन, उनके परिवार, उनके संघर्षों, उनकी गणितीय खोजों और उनकी विरासत का एक विस्तृत विवरण प्रस्तुत करता है।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 2: JANM -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-star-and-crescent"></i></span> जन्म और प्रारंभिक जीवन</h2>

<h3>जन्म</h3>

श्रीनिवास रामानुजन् अय्यंगार का जन्म <strong>22 दिसम्बर 1887</strong> को तमिलनाडु के <strong>इरोड</strong> नगर में हुआ था। उनके जन्म के समय उनकी माँ कोमलताम्मल अपने मायके आई हुई थीं। जन्म के कुछ ही दिनों बाद परिवार <strong>कुम्भकोणम</strong> नामक नगर में आ गया, जहाँ रामानुजन् का अधिकांश बचपन बीता।

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-map-marker-alt"></i> कुम्भकोणम — एक पवित्र नगर</div>
  कुम्भकोणम एक प्राचीन और धार्मिक नगर है, जो कावेरी नदी के किनारे बसा है। यह नगर अपने भव्य मंदिरों, विद्वान पुजारियों और शास्त्रीय संगीत के लिए प्रसिद्ध था। इस वातावरण ने रामानुजन् के व्यक्तित्व को गहराई से प्रभावित किया।
</div>

<h3>परिवार की पृष्ठभूमि</h3>

रामानुजन् का परिवार एक **ब्राह्मण परिवार** था जो आर्थिक दृष्टि से बहुत सम्पन्न नहीं था। उनके पिता **श्रीनिवास अय्यंगार** एक कपड़े की दुकान में मुनीम (लिपिक) का काम करते थे। उनकी मासिक आय अत्यंत सीमित थी — लगभग बीस रुपये प्रति माह — जो उस समय भी एक बड़े परिवार के लिए पर्याप्त नहीं थी।

उनकी माँ **कोमलताम्मल** एक धार्मिक, तेजस्वी और दृढ़ चरित्र की महिला थीं। वे स्थानीय नामगिरि मंदिर में भजन गाती थीं और देवी नामगिरि की परम भक्त थीं। रामानुजन् के जीवन पर उनकी माँ का प्रभाव अत्यंत गहरा था। माँ और पुत्र के बीच का सम्बंध असाधारण रूप से घनिष्ठ था।

रामानुजन् के अनेक भाई-बहन थे, परन्तु उनमें से अधिकांश शैशवावस्था में ही दिवंगत हो गए। इस दुःख ने परिवार को और भी अधिक रामानुजन् के इर्द-गिर्द केन्द्रित कर दिया।

<h3>देवी नामगिरि — रामानुजन् की आध्यात्मिक प्रेरणा</h3>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-om"></i> आध्यात्मिक स्रोत</div>
  रामानुजन् के जीवन में देवी <strong>नामगिरि</strong> का स्थान अत्यंत महत्त्वपूर्ण था। नामकोल स्थित नामगिरि मंदिर उनकी माँ का आराध्य स्थान था। रामानुजन् स्वयं भी इस देवी को अपनी गणितीय प्रतिभा का स्रोत मानते थे।
</div>

उन्होंने कई बार यह कहा कि उनके स्वप्न में देवी नामगिरि आती हैं और उनकी जीभ पर गणितीय सूत्र लिख देती हैं। जब वे प्रातःकाल जागते थे, तो वे उन सूत्रों को तुरंत अपनी नोटबुक में लिख लेते थे।

यह केवल आस्था की बात नहीं थी — यह रामानुजन् की अंतर्ज्ञान की अद्भुत शक्ति का प्रतीक था। उनका मस्तिष्क सोते हुए भी गणितीय समस्याओं पर काम करता रहता था और नींद में उन्हें उत्तर मिल जाते थे।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 3: BALYAKAL -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#ecfdf5; color:#059669;"><i class="fas fa-child"></i></span> बाल्यकाल में गणित की प्रतिभा</h2>

<h3>असाधारण बालक</h3>

रामानुजन् बहुत छोटी उम्र से ही असाधारण प्रतिभा के धनी थे। उनकी स्मृति अद्भुत थी — वे एक बार जो देख या सुन लेते, वह स्थायी रूप से उनके मन में बैठ जाता था।

<div class="timeline">
  <div class="timeline-item">
    <span class="timeline-year">5 वर्ष</span>
    <p>प्रारंभिक शिक्षा आरंभ। अध्यापकों को चकित करने वाले उत्तर देते थे।</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">10 वर्ष</span>
    <p>जिले की प्राथमिक परीक्षा में <strong>सर्वोच्च अंक</strong>। सबके आश्चर्य का विषय बने।</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">15 वर्ष</span>
    <p>जी.एस. कार की पुस्तक मिली — जीवन की दिशा बदल गई।</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">16 वर्ष</span>
    <p>कार की पुस्तक के सभी 5000 प्रमेयों को स्वयं सिद्ध कर नए सूत्र विकसित किए।</p>
  </div>
</div>

<h3>कार (Carr) की पुस्तक — एक जीवन बदलने वाला क्षण</h3>

<div class="info-card blue">
  <div class="info-card-header"><i class="fas fa-book"></i> वह महान पुस्तक</div>
  <strong>पन्द्रह वर्ष की आयु</strong> में रामानुजन् के जीवन में एक ऐसी घटना हुई जिसने उनकी दिशा सदा के लिए बदल दी। उन्हें <strong>जी.एस. कार</strong> की पुस्तक <em>"A Synopsis of Elementary Results in Pure and Applied Mathematics"</em> मिली — 5000 से अधिक गणितीय प्रमेयों और सूत्रों का संग्रह, जिसमें अधिकांश के प्रमाण नहीं दिए गए थे।
</div>

एक सामान्य विद्यार्थी इस पुस्तक को देखकर निराश हो जाता। परन्तु रामानुजन् ने इसे एक चुनौती के रूप में लिया। उन्होंने प्रत्येक सूत्र को स्वयं सिद्ध करने का प्रयास किया, और जहाँ उन्हें सूत्र अपूर्ण लगे, वहाँ उन्होंने नए सूत्र विकसित किए। यह पुस्तक उनके लिए **गणित का विश्वविद्यालय** बन गई।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 4: SHIKSHA -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fff5f5; color:#dc2626;"><i class="fas fa-times-circle"></i></span> शिक्षा में असफलता — एक दर्दनाक सत्य</h2>

<h3>महाविद्यालय में संघर्ष</h3>

रामानुजन् की गणित में इतनी अधिक रुचि थी कि वे अन्य विषयों पर ध्यान नहीं दे पाते थे।

<div class="timeline">
  <div class="timeline-item">
    <span class="timeline-year">1904</span>
    <p>कुम्भकोणम के <strong>गवर्नमेंट आर्ट्स कॉलेज</strong> में प्रवेश। गणित में छात्रवृत्ति मिली। परन्तु अन्य विषयों में अनुत्तीर्ण — छात्रवृत्ति वापस।</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">1905</span>
    <p>घर से भाग गए, विशाखापट्टनम पहुँचे। परिवार ने ढूँढकर वापस लाया।</p>
  </div>
  <div class="timeline-item">
    <span class="timeline-year">1906</span>
    <p>मद्रास के <strong>पचैयप्पा कॉलेज</strong> में प्रवेश। F.A. परीक्षा में <strong>दो बार अनुत्तीर्ण।</strong></p>
  </div>
</div>

<div class="info-card red">
  <div class="info-card-header"><i class="fas fa-pencil-alt"></i> डिग्री के बिना जीवन</div>
  बिना किसी औपचारिक डिग्री के रामानुजन् ने कई वर्षों तक संघर्षपूर्ण जीवन जिया। वे ट्यूशन पढ़ाते थे — कभी-कभी केवल भोजन के बदले में। <strong>कागज़ महँगा था</strong>, इसलिए वे स्लेट पर गणना करते और जो परिणाम महत्त्वपूर्ण होते उन्हें नोटबुक में लिख लेते।
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 5: VIVAH -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-heart"></i></span> विवाह और पारिवारिक जीवन</h2>

<h3>जानकी से विवाह</h3>

**1909 में**, जब रामानुजन् की आयु 21 वर्ष थी, उनका विवाह हुआ। उनकी पत्नी का नाम **जानकी अम्माल** था। विवाह के समय जानकी की आयु केवल **नौ वर्ष** थी (उस काल में बाल विवाह प्रचलित था)।

जानकी एक सीधी-सादी, शांत और समर्पित महिला थीं। वे रामानुजन् की गणितीय प्रतिभा को नहीं समझती थीं, परन्तु उन्होंने सदैव उनका साथ दिया। जब रामानुजन् इंग्लैंड गए, तो जानकी अपनी सास कोमलताम्मल के साथ रहीं।

रामानुजन् के इंग्लैंड जाने के बाद माँ और बहू के बीच तनाव की कुछ कहानियाँ भी हैं। कोमलताम्मल ने जानकी को इंग्लैंड जाने से रोका, और रामानुजन् के पत्रों को भी जानकी तक पहुँचने नहीं दिया। रामानुजन् को यह नहीं पता था कि जानकी को उनके पत्र मिल रहे हैं या नहीं।

<h3>माँ कोमलताम्मल — शक्ति और संघर्ष</h3>

रामानुजन् और उनकी माँ के बीच का सम्बंध बहुत जटिल और गहरा था। माँ ने ही उन्हें देवी नामगिरि की भक्ति सिखाई। माँ ने ही उन्हें संस्कृत के श्लोक याद कराए। माँ की लोरियों में संख्याएँ थीं, भजनों में गणित था।

<div class="highlight-quote">
  कोमलताम्मल एक प्रबल व्यक्तित्व की महिला थीं। परिवार के सभी महत्त्वपूर्ण निर्णय वही करती थीं। रामानुजन् का इंग्लैंड जाना उन्हें पसंद नहीं था — एक कट्टर ब्राह्मण परिवार के लिए समुद्र पार करना धर्म भ्रष्ट करना माना जाता था। परन्तु अंततः, देवी नामगिरि से स्वप्न में आदेश मिलने के बाद उन्होंने अनुमति दे दी।
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 6: MADRAS -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fff7ed; color:#d97706;"><i class="fas fa-city"></i></span> मद्रास में संघर्ष — पहचान की तलाश</h2>

<h3>रामचंद्र राव से मुलाकात</h3>

**1910-11 के आसपास** रामानुजन् मद्रास के जिला कलेक्टर **दीवान बहादुर रामचंद्र राव** से मिले। रामानुजन् ने अपनी नोटबुक दिखाई। राव आश्चर्यचकित रह गए।

<div class="highlight-quote">
  "मेरे सामने एक अर्धभूखा व्यक्ति बैठा था जिसके हाथों में एक नोटबुक थी। मैंने उसे खोला और देखा — ऐसे परिणाम जो मैंने कभी नहीं देखे थे, ऐसे सूत्र जो किसी भी ज्ञात ग्रंथ में नहीं थे।"
  <span class="quote-src">— दीवान बहादुर रामचंद्र राव</span>
</div>

<h3>मद्रास पोर्ट ट्रस्ट में नौकरी</h3>

**1912 में** रामानुजन् को **मद्रास पोर्ट ट्रस्ट** में क्लर्क की नौकरी मिली। मासिक वेतन था — **तीस रुपये**। यह उनके जीवन का पहला स्थायी आय-स्रोत था। उनके बॉस **एस. नारायण अय्यर** ने उनकी प्रतिभा को पहचाना और उन्हें गणित के लिए समय और प्रोत्साहन दिया।

<h3>इंडियन मैथमेटिकल सोसायटी से जुड़ाव</h3>

**1911 में** रामानुजन् का पहला शोध-पत्र प्रकाशित हुआ — *"बर्नोली संख्याओं के कुछ गुणों पर"* — **जर्नल ऑफ़ द इंडियन मैथमेटिकल सोसायटी** में। यह एक महत्त्वपूर्ण पड़ाव था। अब उनका नाम गणित जगत में जाना जाने लगा था।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 7: HARDY KO PATRA -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#eff6ff; color:#1e3c72;"><i class="fas fa-envelope-open-text"></i></span> हार्डी को पत्र — वह ऐतिहासिक क्षण</h2>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-calendar-day"></i> 16 जनवरी 1913 — इतिहास में अमर तारीख</div>
  इस दिन रामानुजन् ने कैम्ब्रिज विश्वविद्यालय के प्रोफेसर <strong>गॉडफ्रे हेरॉल्ड हार्डी</strong> को एक पत्र लिखा — साथ में <strong>120 से अधिक प्रमेयों और सूत्रों</strong> की एक लम्बी सूची थी, बिना किसी प्रमाण के।
</div>

<h3>पत्र लिखने का निर्णय</h3>

पत्र में रामानुजन् ने लिखा:

<div class="highlight-quote">
  "मैं मद्रास पोर्ट ट्रस्ट में एक क्लर्क हूँ। मेरी आयु 23 वर्ष है। मेरे पास कोई विश्वविद्यालय की शिक्षा नहीं है। परन्तु मैंने कुछ गणितीय परिणाम खोजे हैं जो शायद आपके लिए रुचिकर हों..."
  <span class="quote-src">— रामानुजन् का हार्डी को पत्र, 1913</span>
</div>

<h3>हार्डी की प्रतिक्रिया</h3>

हार्डी ने पहले पत्र को एक तरफ रख दिया। उन्हें लगा यह किसी विक्षिप्त व्यक्ति का पत्र है। परन्तु उस रात नींद नहीं आई। पत्र में लिखे सूत्र उनके मन में घूमते रहे। सुबह उठकर उन्होंने अपने सहयोगी **जॉन एडेन्सर लिटलवुड** को बुलाया।

दोनों ने घंटों तक सूत्रों की जाँच की। उन्होंने पाया:
- कुछ सूत्र पहले से ज्ञात थे — परन्तु रामानुजन् ने उन्हें स्वतंत्र रूप से खोजा था
- कुछ सूत्र **पूर्णतः नए** थे और उनकी सत्यता अद्भुत थी
- कुछ सूत्र इतने जटिल थे कि हार्डी और लिटलवुड भी उन्हें तत्काल सिद्ध नहीं कर सके

<div class="contrast-quote">
  "ये सूत्र किसी ऐसे व्यक्ति द्वारा लिखे जा सकते हैं जो उच्चतम श्रेणी का गणितज्ञ हो। वे निश्चित रूप से सत्य हैं क्योंकि यदि ये असत्य होते, तो कोई भी इनकी कल्पना करने में सक्षम नहीं होता।"
  <span class="quote-src">— प्रोफेसर जी.एच. हार्डी</span>
</div>

हार्डी ने तुरंत उत्तर लिखा और रामानुजन् को कैम्ब्रिज आने का निमंत्रण दिया।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 8: CAMBRIDGE -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#f0fdf4; color:#059669;"><i class="fas fa-university"></i></span> कैम्ब्रिज में — एक नई दुनिया</h2>

<h3>इंग्लैंड की यात्रा</h3>

इंग्लैंड जाना रामानुजन् के लिए आसान नहीं था। उनकी माँ धर्म-भ्रष्ट होने के भय से विरोध कर रही थीं। ब्राह्मण समाज में समुद्र पार जाना वर्जित माना जाता था।

अंततः **देवी नामगिरि ने माँ को स्वप्न में दर्शन दिए** और कहा कि रामानुजन् को जाने दो। इस स्वप्न के बाद माँ ने अनुमति दे दी।

**17 मार्च 1914** को रामानुजन् ने मद्रास से इंग्लैंड के लिए प्रस्थान किया। यात्रा लम्बी और कठिन थी। एक शाकाहारी ब्राह्मण के लिए जहाज़ पर भोजन की समस्या भी थी।

<h3>कैम्ब्रिज का जीवन</h3>

कैम्ब्रिज पहुँचकर रामानुजन् को एक नई दुनिया मिली — विशाल पुस्तकालय, अनुभवी प्राध्यापक, गणितीय चर्चाओं का वातावरण। परन्तु साथ ही कुछ कठिनाइयाँ भी थीं।

<div class="compare-grid">
  <div class="compare-card hardy">
    <h4><i class="fas fa-exclamation-triangle"></i> कठिनाइयाँ</h4>
    <ul>
      <li><strong>भोजन की समस्या:</strong> शाकाहारी भोजन मिलना कठिन था</li>
      <li><strong>जलवायु:</strong> ठंड और धुंध — दक्षिण भारत की धूप का अभाव</li>
      <li><strong>प्रथम विश्वयुद्ध:</strong> 1914 से जीवन और कठिन हो गया</li>
    </ul>
  </div>
  <div class="compare-card ramanu">
    <h4><i class="fas fa-check-circle"></i> उपलब्धियाँ</h4>
    <ul>
      <li>विशाल पुस्तकालय तक पहुँच</li>
      <li>हार्डी जैसे गुरु का मार्गदर्शन</li>
      <li>पाँच वर्षों में अनेक महान खोजें</li>
    </ul>
  </div>
</div>

<h3>हार्डी-रामानुजन् की जोड़ी</h3>

हार्डी और रामानुजन् की जोड़ी गणित के इतिहास की सबसे असाधारण जोड़ियों में से एक है।

<div class="compare-grid">
  <div class="compare-card hardy">
    <h4><i class="fas fa-calculator"></i> प्रोफेसर हार्डी</h4>
    <ul>
      <li>तर्कवादी, नास्तिक</li>
      <li>सुव्यवस्थित, अनुशासित</li>
      <li>कठोर प्रमाण में विश्वास</li>
    </ul>
  </div>
  <div class="compare-card ramanu">
    <h4><i class="fas fa-star"></i> रामानुजन्</h4>
    <ul>
      <li>आस्तिक, अंतर्ज्ञानवादी</li>
      <li>प्रायः बिना प्रमाण के परिणाम</li>
      <li>गहन भावनात्मक एवं आध्यात्मिक</li>
    </ul>
  </div>
</div>

परन्तु दोनों में एक बात समान थी — **गणित के प्रति अदम्य प्रेम।** हार्डी ने रामानुजन् को औपचारिक गणित की भाषा सिखाई। रामानुजन् ने हार्डी को वह अंतर्दृष्टि दी जो किसी पाठ्यपुस्तक में नहीं मिलती।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 9: KHOJEIN -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-atom"></i></span> महान गणितीय खोजें</h2>

<div class="discovery-card">
  <div class="discovery-number">१</div>
  <div class="discovery-title">संख्या विभाजन (Partition of Numbers) — $p(n)$</div>
  रामानुजन् की सबसे प्रसिद्ध खोजों में से एक है <strong>संख्या विभाजन का सिद्धांत।</strong> किसी धनात्मक पूर्णांक $n$ को धनात्मक पूर्णांकों के योग के रूप में लिखने के तरीकों की संख्या $p(n)$ कहलाती है।

  उदाहरण — $n = 4$ के विभाजन:
  $$4 = 4 \qquad 4 = 3+1 \qquad 4 = 2+2 \qquad 4 = 2+1+1 \qquad 4 = 1+1+1+1$$
  अतः $p(4) = 5$।

  हार्डी और रामानुजन् ने मिलकर महान **असम्प्रदायिक सूत्र** विकसित किया:
  $$p(n) \sim \frac{1}{4n\sqrt{3}} \cdot e^{\pi\sqrt{\frac{2n}{3}}} \quad \text{जब } n \to \infty$$

  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-atom"></i> भौतिकी — ऊर्जा स्तर</span>
    <span class="app-tag purple"><i class="fas fa-project-diagram"></i> स्ट्रिंग सिद्धांत</span>
    <span class="app-tag green"><i class="fas fa-chart-bar"></i> सांख्यिकीय यांत्रिकी</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">२</div>
  <div class="discovery-title">रामानुजन् का $\pi$ का अद्भुत सूत्र</div>
  $$\frac{1}{\pi} = \frac{2\sqrt{2}}{9801} \sum_{k=0}^{\infty} \frac{(4k)!\,(1103 + 26390k)}{(k!)^4 \cdot 396^{4k}}$$
  इस सूत्र की प्रत्येक पद $\pi$ के मान में <strong>आठ दशमलव स्थान</strong> जोड़ती है। आज के सुपरकम्प्यूटर इसी सूत्र से $\pi$ के <strong>खरबों दशमलव स्थान</strong> की गणना करते हैं।
  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-desktop"></i> सुपरकम्प्यूटर</span>
    <span class="app-tag purple"><i class="fas fa-infinity"></i> संख्यात्मक विधियाँ</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">३</div>
  <div class="discovery-title">टैक्सीकैब संख्या — 1729</div>

<div class="taxicab-box">
  <div class="taxicab-number">1729</div>
  <div class="taxicab-proof">$1729 = 1^3 + 12^3 = 9^3 + 10^3$</div>
  <p style="font-size:0.85rem; color:#78350f; margin-top:8px;">सबसे छोटी संख्या जो दो घनों के योग के रूप में दो तरीकों से लिखी जा सकती है</p>
</div>

  रामानुजन् अस्पताल में थे और हार्डी उनसे मिलने आए। हार्डी ने बताया कि उनकी टैक्सी का नम्बर 1729 था और यह संख्या उबाऊ लगी। रामानुजन् ने तुरंत इस संख्या का रहस्य बता दिया। यह घटना उनके अद्भुत **संख्या-बोध** का प्रमाण है।
</div>

<div class="discovery-card">
  <div class="discovery-number">४</div>
  <div class="discovery-title">अनंत श्रृंखला — एक विचित्र परिणाम</div>
  $$1 + 2 + 3 + 4 + 5 + \cdots = -\frac{1}{12}$$
  यह देखने में पूर्णतः असम्भव लगता है! परन्तु यह सूत्र <strong>रीमान जीटा फ़ंक्शन</strong> के माध्यम से सत्य है।
  <div class="app-tags">
    <span class="app-tag purple"><i class="fas fa-atom"></i> क्वाण्टम भौतिकी</span>
    <span class="app-tag orange"><i class="fas fa-project-diagram"></i> स्ट्रिंग सिद्धांत</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">५</div>
  <div class="discovery-title">रामानुजन् प्राइम (Ramanujan Primes)</div>
  रामानुजन् ने अभाज्य संख्याओं के बारे में महत्त्वपूर्ण खोजें कीं। <strong>रामानुजन् प्राइम</strong> $R_n$ वह संख्या है जो <strong>बर्ट्रांड-चेबिशेव प्रमेय</strong> का एक विशेष रूप है। उन्होंने सिद्ध किया कि $x$ और $2x$ के बीच कम से कम $n$ अभाज्य संख्याएँ होती हैं, यदि $x \geq R_n$।
</div>

<div class="discovery-card">
  <div class="discovery-number">६</div>
  <div class="discovery-title">रामानुजन् थीटा फ़ंक्शन</div>
  $$f(a,b) = \sum_{n=-\infty}^{\infty} a^{n(n+1)/2} \cdot b^{n(n-1)/2}$$
  यह फ़ंक्शन <strong>मॉड्यूलर फ़ॉर्म्स</strong> के सिद्धांत की नींव है।
  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-lock"></i> क्रिप्टोग्राफी</span>
    <span class="app-tag green"><i class="fas fa-wifi"></i> डिजिटल संचार</span>
    <span class="app-tag purple"><i class="fas fa-microchip"></i> क्वाण्टम कम्प्यूटिंग</span>
  </div>
</div>

<div class="discovery-card">
  <div class="discovery-number">७</div>
  <div class="discovery-title">मॉक थीटा फ़ंक्शन — रहस्यमय अंतिम खोज</div>
  <div class="info-card purple" style="margin:10px 0;">
    <div class="info-card-header"><i class="fas fa-envelope"></i> अंतिम पत्र — 1920</div>
    मृत्यु से कुछ सप्ताह पहले रामानुजन् ने हार्डी को अंतिम पत्र लिखा जिसमें <strong>मॉक थीटा फ़ंक्शन</strong> की अवधारणा प्रस्तुत की। हार्डी सहित सभी गणितज्ञ इन्हें <strong>80 वर्षों तक</strong> पूर्णतः नहीं समझ पाए।
  </div>
  <strong>2002 में</strong> गणितज्ञ शैंड ग्रिफ़ीथ ने इन्हें हार्मोनिक माएस्ट्रोम फ़ॉर्म्स से जोड़ा।
  <div class="app-tags">
    <span class="app-tag"><i class="fas fa-black-circle"></i> काले छिद्रों की भौतिकी</span>
    <span class="app-tag purple"><i class="fas fa-atom"></i> कण भौतिकी</span>
  </div>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 10: FELLOWSHIP -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fff7ed; color:#d97706;"><i class="fas fa-award"></i></span> फ़ेलोशिप — भारत का गौरव</h2>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-trophy"></i> 1918 — ऐतिहासिक सम्मान</div>
  रामानुजन् को <strong>रॉयल सोसायटी (F.R.S.)</strong> का फ़ेलो चुना गया — इस सम्मान को पाने वाले <strong>पहले भारतीय।</strong> उसी वर्ष <strong>ट्रिनिटी कॉलेज, कैम्ब्रिज</strong> का फ़ेलो भी।
</div>

**1918 में** रामानुजन् को **रॉयल सोसायटी** (Royal Society, London) का **फ़ेलो** (F.R.S.) चुना गया। उस समय रॉयल सोसायटी का फ़ेलो बनना विज्ञान और गणित की सर्वोच्च मान्यता थी। रामानुजन् इस सम्मान को पाने वाले **पहले भारतीय** थे।

यह समाचार भारत में एक उत्सव की तरह मनाया गया। एक क्लर्क जिसके पास कोई डिग्री नहीं थी, जो गरीब घर से था, जो किसी मेट्रोपॉलिटन शहर का नहीं था — उसने विश्व के सर्वोच्च गणितीय सम्मान प्राप्त किए।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 11: BIMARI -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fff5f5; color:#dc2626;"><i class="fas fa-heartbeat"></i></span> बीमारी और वापसी</h2>

<h3>क्षय रोग का आक्रमण</h3>

इंग्लैंड में रहते हुए रामानुजन् का स्वास्थ्य धीरे-धीरे गिरता गया। **1917 में** उन्हें गंभीर रूप से बीमार होने के कारण **मेथवॉल्ड सेनेटोरियम** में भर्ती कराया गया। उन्हें **क्षय रोग** (Tuberculosis) होने की सम्भावना थी।

<div class="info-card red">
  <div class="info-card-header"><i class="fas fa-book-medical"></i> अस्पताल में भी गणित</div>
  अस्पताल में भी रामानुजन् गणित करते रहे। बुखार की अवस्था में भी वे नोटबुक खोलकर सूत्र लिखते रहते थे। यहीं हार्डी ने उनसे मिलने आकर टैक्सीकैब नम्बर 1729 का ज़िक्र किया।
</div>

<h3>भारत वापसी</h3>

**27 फरवरी 1919** को रामानुजन् इंग्लैंड से भारत के लिए रवाना हुए। पाँच वर्ष बाद वे वापस आ रहे थे — परन्तु अब वे एक प्रसिद्ध गणितज्ञ थे। भारत पहुँचने पर उनकी स्थिति अत्यंत कमज़ोर थी। वे मद्रास और फिर **कोडुमुंडी** में इलाज के लिए गए।

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 12: ANTIM DIN -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#1e3c72; color:white;"><i class="fas fa-star"></i></span> अंतिम दिन और विरासत</h2>

<h3>मृत्यु</h3>

<div class="info-card red">
  <div class="info-card-header"><i class="fas fa-calendar-times"></i> 26 अप्रैल 1920</div>
  केवल <strong>32 वर्ष की आयु</strong> में, श्रीनिवास रामानुजन् का निधन हो गया। मृत्यु से कुछ दिन पहले भी वे गणित कर रहे थे। उनकी पत्नी जानकी ने बताया कि अपने अंतिम दिनों में भी वे रात को जागकर स्लेट पर कुछ लिखते रहते थे।
</div>

<div class="contrast-quote">
  "गणित ने अपना एक सबसे बड़ा रहस्यमय प्रतिभावान खो दिया।"
  <span class="quote-src">— प्रोफेसर जी.एच. हार्डी</span>
</div>

<h3>खोई हुई नोटबुक — एक अद्भुत खोज</h3>

<div class="info-card purple">
  <div class="info-card-header"><i class="fas fa-book"></i> 1976 — खोई नोटबुक मिली</div>
  गणितज्ञ <strong>जॉर्ज एंड्रयूज़</strong> कैम्ब्रिज के <strong>रेन पुस्तकालय</strong> में रामानुजन् की एक <strong>100 पृष्ठों की खोई हुई नोटबुक</strong> मिली — जिसे <strong>"Lost Notebook"</strong> कहते हैं। इस पर शोध करने में <strong>30 से अधिक वर्ष</strong> लगे।
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 13: AADHUNIK YOAGDAN -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#ecfdf5; color:#059669;"><i class="fas fa-laptop-code"></i></span> आधुनिक गणित में रामानुजन् का योगदान</h2>

रामानुजन् की खोजें आज के विज्ञान और प्रौद्योगिकी में जीवित हैं:

<div class="lessons-grid">
  <div class="lesson-card">
    <div class="lesson-icon">💻</div>
    <strong>कम्प्यूटर विज्ञान</strong>
    <p>$\pi$ के सूत्र का उपयोग सुपरकम्प्यूटर में खरबों दशमलव स्थान की गणना के लिए।</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">🔐</div>
    <strong>क्रिप्टोग्राफी</strong>
    <p>मॉड्यूलर फ़ॉर्म्स सिद्धांत आधुनिक डेटा सुरक्षा में उपयोग होता है।</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">⚛️</div>
    <strong>भौतिकी</strong>
    <p>स्ट्रिंग सिद्धांत और क्वाण्टम गुरुत्वाकर्षण में रामानुजन् के कार्य का उपयोग।</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">📊</div>
    <strong>सांख्यिकी</strong>
    <p>विभाजन सिद्धांत का उपयोग सांख्यिकीय यांत्रिकी और ऊष्मागतिकी में।</p>
  </div>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 14: BHARTIYA SANSKRITI -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fff7ed; color:#d97706;"><i class="fas fa-om"></i></span> भारतीय संस्कृति में रामानुजन्</h2>

रामानुजन् केवल एक गणितज्ञ नहीं थे — वे **भारतीय आध्यात्मिकता और गणितीय प्रतिभा के संगम** का प्रतीक हैं।

उन्होंने यह सिद्ध किया कि गणित और आध्यात्म एक-दूसरे के विरोधी नहीं हैं। जब वे कहते थे कि *"सूत्र देवी ने दिए"*, तो वे अपने अंतर्ज्ञान की शक्ति की बात कर रहे थे — उस गहन एकाग्रता की, जिसे हम ध्यान या साधना कहते हैं।

<div class="lessons-grid">
  <div class="lesson-card">
    <div class="lesson-icon">🌱</div>
    <strong>प्रतिभा जन्मजात होती है</strong>
    <p>किसी विश्वविद्यालय की मोहताज नहीं।</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">💪</div>
    <strong>संघर्ष से निखार</strong>
    <p>अभाव ने रामानुजन् को तोड़ा नहीं, बल्कि और मज़बूत किया।</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">🏠</div>
    <strong>परिवार की जड़ें</strong>
    <p>माँ की भक्ति और संस्कृति ने उनकी प्रेरणा को जीवित रखा।</p>
  </div>
  <div class="lesson-card">
    <div class="lesson-icon">🌍</div>
    <strong>गणित सार्वभौमिक है</strong>
    <p>यह न जाति देखता है, न देश, न धर्म।</p>
  </div>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- SECTION 15: SYLLABUS TABLE -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#eff6ff; color:#1e3c72;"><i class="fas fa-graduation-cap"></i></span> CSIR NET, GATE और IIT JAM के लिए प्रासंगिकता</h2>

रामानुजन् का कार्य सीधे आपके परीक्षा-पाठ्यक्रम से जुड़ा है:

<table class="syllabus-table">
  <thead>
    <tr><th>विषय</th><th>रामानुजन् का योगदान</th></tr>
  </thead>
  <tbody>
    <tr><td>संख्या सिद्धांत</td><td>विभाजन फ़ंक्शन, अभाज्य संख्याएँ, टैक्सीकैब संख्याएँ</td></tr>
    <tr><td>अनंत श्रृंखलाएँ</td><td>अभिसरण परीक्षण, विशेष श्रृंखलाएँ</td></tr>
    <tr><td>जटिल विश्लेषण</td><td>थीटा फ़ंक्शन, मॉड्यूलर फ़ॉर्म्स</td></tr>
    <tr><td>वास्तविक विश्लेषण</td><td>अनंत श्रृंखलाएँ, सतत भिन्न</td></tr>
    <tr><td>अनुप्रयुक्त गणित</td><td>$\pi$ की गणना, संख्यात्मक विधियाँ</td></tr>
  </tbody>
</table>

<!-- ══════════════════════════════════════════ -->
<!-- CLOSING -->
<!-- ══════════════════════════════════════════ -->

<h2><span class="sec-icon" style="background:#fdf4ff; color:#7c3aed;"><i class="fas fa-infinity"></i></span> उपसंहार</h2>

श्रीनिवास रामानुजन् की कहानी समाप्त नहीं होती — वह निरंतर आगे बढ़ती रहती है। उनकी नोटबुक के सूत्र आज भी नए शोध की प्रेरणा देते हैं। उनके द्वारा की गई खोजें आज भी गणित और विज्ञान की नींव को मज़बूत कर रही हैं।

वे एक ऐसे व्यक्ति थे जिन्होंने अभाव को अवसर में बदला, संघर्ष को साधना में बदला और एक छोटे से कस्बे की मिट्टी से निकलकर अनंत के द्वार खोले।

<div class="info-card gold" style="text-align:center; margin:25px 0;">
  <div class="info-card-header" style="justify-content:center;"><i class="fas fa-calendar-check"></i> राष्ट्रीय गणित दिवस</div>
  <strong>22 दिसम्बर</strong> को <strong>भारत में राष्ट्रीय गणित दिवस</strong> के रूप में मनाया जाता है — रामानुजन् के जन्मदिन के उपलक्ष्य में।
</div>

जब भी आप गणित पढ़ें, जब भी कोई समस्या कठिन लगे, जब भी लगे कि आगे नहीं बढ़ सकते — तो रामानुजन् को याद करें। एक ऐसा व्यक्ति जिसने भूख में भी, बीमारी में भी, अकेलेपन में भी — **अनंत को जाना।**

<div class="final-quote">
  <p>"गणित के इतिहास में ऐसे प्रतिभाशाली व्यक्ति अत्यंत विरले हैं जिनसे रामानुजन् की तुलना की जा सके।"</p>
  <span class="attr">— प्रोफेसर जी.एच. हार्डी</span>
</div>

<div class="film-note">
  <i class="fas fa-film"></i> <strong>अनुशंसा:</strong> यदि आप रामानुजन् के बारे में और जानना चाहते हैं, तो 2015 की फ़िल्म <strong>"The Man Who Knew Infinity"</strong> (हिंदी में: अनंत को जानने वाला) अवश्य देखें — यह उनके जीवन पर आधारित एक अत्यंत प्रेरणादायक फ़िल्म है।
</div>

</div>
