---
layout: post
title: "वास्तविक संख्याओं की नींव: संख्या प्रणाली की समझ"
date: 2026-03-21
category: maths
lang: hi
lang_pair: "/blog/foundations-of-real-numbers-understanding-the-number-system/"
permalink: /blog/vastvik-sankhyaon-ki-neenv-sankhya-pranali-ki-samajh/
listed: false
description: "एक सरल और प्रभावी मार्गदर्शिका — संख्या प्रणाली का विकास ℕ से ℝ तक, इतिहास, उदाहरण, और परिमेय-अपरिमेय संख्याओं की समझ।"
---

<link href="https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
  .math-post-hi { font-family: 'Hind', 'Noto Sans Devanagari', sans-serif; font-size: 1.05rem; line-height: 1.95; color: #2d2d2d; max-width: 860px; margin: 0 auto; }
  .post-hero { background: linear-gradient(135deg, #1e3c72 0%, #2a5298 50%, #7c3aed 100%); border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px; position: relative; overflow: hidden; }
  .post-hero::before { content: "ℝ"; position: absolute; right: 20px; top: -10px; font-size: 8rem; color: rgba(255,255,255,0.06); font-family: serif; }
  .post-hero h1 { font-size: 1.75rem; font-weight: 800; color: white; margin: 0 0 10px; line-height: 1.35; font-family: 'Hind', sans-serif; }
  .post-hero p { font-size: 1rem; opacity: 0.9; margin: 0 0 14px; }
  .lang-switch { display: inline-flex; align-items: center; gap: 8px; background: rgba(255,255,255,0.15); border: 1px solid rgba(255,255,255,0.35); border-radius: 50px; padding: 7px 18px; font-size: 0.85rem; color: white; text-decoration: none; transition: background 0.2s; }
  .lang-switch:hover { background: rgba(255,255,255,0.28); color: white; text-decoration: none; }
  .stats-strip { background: linear-gradient(135deg, #1e3c72, #7c3aed); border-radius: 14px; padding: 22px 28px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 16px; margin-bottom: 35px; text-align: center; color: white; }
  .stat-item .num { font-size: 1.9rem; font-weight: 900; display: block; line-height: 1; }
  .stat-item .lbl { font-size: 0.7rem; opacity: 0.8; margin-top: 4px; display: block; text-transform: uppercase; letter-spacing: 0.5px; }
  .section-title { display: flex; align-items: center; gap: 12px; font-size: 1.35rem; font-weight: 800; color: #1e3c72; margin: 42px 0 20px; padding-bottom: 10px; border-bottom: 3px solid transparent; border-image: linear-gradient(to right, #1e3c72, #7c3aed, #ff4b2b, transparent) 1; }
  .sec-icon { width: 38px; height: 38px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .sub-title { font-size: 1.05rem; font-weight: 700; color: #2a5298; margin: 28px 0 12px; display: flex; align-items: center; gap: 8px; }
  .sub-title::before { content: ''; width: 4px; height: 18px; background: linear-gradient(to bottom, #ff4b2b, #fbbf24); border-radius: 2px; flex-shrink: 0; }
  .info-card { background: white; border-radius: 13px; padding: 22px 26px; margin: 18px 0; box-shadow: 0 4px 14px rgba(0,0,0,0.07); border-left: 5px solid #1e3c72; }
  .info-card.gold { border-left-color: #d97706; background: #fffbeb; }
  .info-card.green { border-left-color: #059669; background: #ecfdf5; }
  .info-card-header { display: flex; align-items: center; gap: 8px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 10px; color: #1e3a5f; }
  .info-card.gold .info-card-header { color: #92400e; }
  .info-card.green .info-card-header { color: #065f46; }
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
  .floor-body h4 { margin: 0 0 5px; font-size: 1rem; font-weight: 800; color: #1e3c72; font-family: 'Hind', sans-serif; }
  .floor-body .floor-set { font-size: 0.82rem; color: #7c3aed; font-weight: 700; font-family: monospace; margin-bottom: 8px; }
  .floor-body p { margin: 0 0 8px; font-size: 0.93rem; color: #444; line-height: 1.75; }
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
  @media (max-width: 640px) { .compare-grid { grid-template-columns: 1fr; } .post-hero { padding: 26px 18px; } .post-hero h1 { font-size: 1.4rem; } .stats-strip { flex-direction: column; align-items: center; } .spotlight { flex-direction: column; } }
</style>

<div class="math-post-hi">

<div class="post-hero">
  <h1>अनन्त स्थापत्य: वास्तविक संख्याओं की नींव</h1>
  <p>प्राचीन गिनती से सम्पूर्ण संख्या रेखा तक — वे पाँच मंजिलें जो तीन हज़ार वर्षों में बनीं और जिन पर आज का समस्त गणित टिका है।</p>
  <a class="lang-switch" href="/blog/foundations-of-real-numbers-understanding-the-number-system/">
    <span>🇬🇧</span> Read in English
  </a>
</div>

<div class="stats-strip">
  <div class="stat-item"><span class="num">5</span><span class="lbl">संख्या प्रणालियाँ</span></div>
  <div class="stat-item"><span class="num">3000+</span><span class="lbl">वर्षों का इतिहास</span></div>
  <div class="stat-item"><span class="num">4</span><span class="lbl">हल किए उदाहरण</span></div>
  <div class="stat-item"><span class="num">★★☆</span><span class="lbl">सरल भाषा</span></div>
  <div class="stat-item"><span class="num">ℝ</span><span class="lbl">अन्तिम प्रणाली</span></div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-building"></i></span> इमारत का रूपक</h2>

<p>क्या आपने कभी सोचा है — <em>"संख्या वास्तव में होती क्या है?"</em> आम लोगों के लिए संख्याएँ बस उपकरण हैं — बैंक बैलेंस, खाना पकाने की सामग्री, दूरी। लेकिन एक गणितज्ञ के नज़रिये से संख्या प्रणाली एक भव्य <strong>ऊँची इमारत</strong> है जो तीन हज़ार वर्षों में मंजिल दर मंजिल बनाई गई।</p>

<div class="pull-quote">
  जब भी मनुष्यता किसी दीवार से टकराई — कोई ऐसी समस्या जिसे "हल नहीं किया जा सकता" कहा गया — हमने हार नहीं मानी। हमने एक नई मंजिल बना दी।
  <cite>— गणितीय प्रगति की भावना</cite>
</div>

<p>यह समझना ज़रूरी है कि <strong>हर नए प्रकार की संख्या एक वास्तविक जरूरत से पैदा हुई</strong> — एक ऐसी समस्या जो पुरानी संख्याएँ हल नहीं कर सकती थीं। जो भेड़ों की गिनती से शुरू हुआ, वह बन गया — <strong>वास्तविक संख्या प्रणाली ($\mathbb{R}$)</strong>।</p>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-layer-group"></i></span> पाँच मंजिलें: इतिहास की एक यात्रा</h2>

<div class="floor-stack">

  <div class="floor-item">
    <div class="floor-badge n">ℕ</div>
    <div class="floor-body">
      <h4>मंजिल 1 — प्राकृत संख्याएँ $\mathbb{N}$</h4>
      <div class="floor-set">$\mathbb{N} = \{1,\, 2,\, 3,\, 4,\, \ldots\}$</div>
      <p>गणित का सबसे पहला काम था — <strong>गिनना</strong>। प्राचीन लोग मवेशियों, दिनों और फसलों को गिनते थे। इन्हें प्राकृत संख्याएँ कहते हैं क्योंकि ये स्वाभाविक रूप से मिलती हैं — जब आप पूछते हैं "कितने?" तो ये संख्याएँ खुद-ब-खुद सामने आती हैं।</p>
      <p>इनमें जोड़ ($3 + 5 = 8$) और गुणा ($3 \times 4 = 12$) हमेशा हो सकता है, और उत्तर भी प्राकृत संख्या ही आता है। लेकिन घटाव (बड़े में से छोटा घटाने पर) मुश्किल पैदा कर देता है।</p>
      <span class="problem-badge">❌ कमी: $3 - 5 = ?$ कोई प्राकृत संख्या उत्तर नहीं। नई मंजिल चाहिए।</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge w">𝕎</div>
    <div class="floor-body">
      <h4>मंजिल 2 — सम्पूर्ण संख्याएँ $\mathbb{W}$</h4>
      <div class="floor-set">$\mathbb{W} = \{0,\, 1,\, 2,\, 3,\, \ldots\}$</div>
      <p>हम बस एक नया विचार जोड़ते हैं: <strong>शून्य</strong>। यह मामूली लग सकता है, लेकिन यह मानव इतिहास की सबसे महत्त्वपूर्ण खोजों में से एक है। शून्य केवल "कुछ नहीं" नहीं है — यह एक संख्या है जो स्थान रखती है और हमारी पूरी दशमलव प्रणाली को संभव बनाती है।</p>

      <div class="spotlight">
        <div class="spotlight-icon">🏛️</div>
        <div>
          <h4>आर्यभट और शून्य की शक्ति — आर्यभटीय (499 ई.)</h4>
          <p>भारतीय गणितज्ञ आर्यभट ने अपनी रचना <em>आर्यभटीय</em> (499 ई.) में दशमलव स्थानीय-मान प्रणाली का उपयोग किया जिसने शून्य को एक काम करने वाला अंक बनाया — केवल खाली जगह नहीं। उनकी प्रणाली से 42, 402 और 420 को स्पष्ट रूप से अलग दिखाना सम्भव हुआ। रोमन अंकों जैसी पुरानी प्रणालियों में यह बताना बहुत कठिन था। यह योगदान अरबी अनुवादों के ज़रिये दुनिया भर में फैला और हम सबके अंकगणित का आधार बना।</p>
        </div>
      </div>

      <span class="problem-badge">❌ कमी: $5 - 8 = ?$ अभी भी उत्तर नहीं। शून्य से नीचे की संख्याएँ चाहिए।</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge z">ℤ</div>
    <div class="floor-body">
      <h4>मंजिल 3 — पूर्णांक $\mathbb{Z}$</h4>
      <div class="floor-set">$\mathbb{Z} = \{\ldots,\, -3,\, -2,\, -1,\, 0,\, 1,\, 2,\, 3,\, \ldots\}$</div>
      <p><strong>ऋणात्मक संख्याएँ</strong> जोड़कर हम संख्या रेखा को दोनों दिशाओं में फैला देते हैं। अब घटाव का हमेशा उत्तर मिलता है। $\mathbb{Z}$ प्रतीक जर्मन शब्द <em>Zahlen</em> से आया है, जिसका अर्थ है "संख्याएँ।"</p>
      <p>ऋणात्मक संख्याओं ने गणित को <strong>दिशा</strong> (बायाँ-दायाँ, समुद्र तल से ऊपर-नीचे), <strong>ऋण</strong> (किसी को पैसे देने हैं) और <strong>शून्य से नीचे तापमान</strong> जैसी अवधारणाएँ दीं। भारतीय गणितज्ञ <strong>ब्रह्मगुप्त</strong> ने अपनी रचना <em>ब्रह्मस्फुटसिद्धान्त</em> (628 ई.) में ऋणात्मक संख्याओं और शून्य के अंकगणित के पहले स्पष्ट नियम दिए।</p>
      <span class="problem-badge">❌ कमी: $1 \div 2 = ?$ कोई पूर्णांक उत्तर नहीं। भिन्न चाहिए।</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge q">ℚ</div>
    <div class="floor-body">
      <h4>मंजिल 4 — परिमेय संख्याएँ $\mathbb{Q}$</h4>
      <div class="floor-set">$\mathbb{Q} = \left\{\dfrac{p}{q} : p,\, q \in \mathbb{Z},\ q \neq 0\right\}$</div>
      <p><em>परिमेय</em> शब्द लैटिन <em>ratio</em> (अनुपात) से आया है। परिमेय संख्याएँ वे सभी भिन्न हैं जिनके अंश और हर (ऊपर और नीचे का भाग) दोनों पूर्णांक हों और हर शून्य न हो। हर वह दशमलव जो या तो रुक जाए ($0.75$) या एक निश्चित पैटर्न में हमेशा दोहराता रहे ($0.\overline{3} = \frac{1}{3}$) — परिमेय है।</p>
      <p>परिमेय संख्याओं में जोड़, घटाव, गुणा और भाग (शून्य से भाग को छोड़कर) हमेशा सम्भव है और उत्तर भी परिमेय ही आता है। प्राचीन यूनानी गणितज्ञ यहाँ तक आकर संतुष्ट थे — जब तक एक सरल-से वर्ग ने उनकी दुनिया हिला नहीं दी।</p>
      <span class="problem-badge">❌ कमी: कौन-सी संख्या का वर्ग ठीक 2 होगा? यह कोई भिन्न नहीं है। संख्या रेखा में अभी भी छिद्र हैं!</span>
    </div>
  </div>

  <div class="floor-item">
    <div class="floor-badge r">ℝ</div>
    <div class="floor-body">
      <h4>मंजिल 5 — वास्तविक संख्याएँ $\mathbb{R}$ &nbsp;<em>(सम्पूर्ण मंजिल)</em></h4>
      <div class="floor-set">$\mathbb{R} = \mathbb{Q} \cup \mathbb{Q}^c \quad$ (सभी परिमेय + सभी अपरिमेय)</div>
      <p>वास्तविक संख्याएँ संख्या रेखा के <strong>हर एक बिन्दु को भर देती हैं</strong> — कोई अन्तराल नहीं, कोई छिद्र नहीं, कुछ भी नहीं छूटता। हर भिन्न एक वास्तविक संख्या है। $\sqrt{2}$, $\pi$, $e$ जैसी अपरिमेय संख्याएँ भी वास्तविक हैं। मिलकर ये एक निरन्तर (बिना किसी टूट-फूट के, बहती हुई) संख्या रेखा बनाते हैं।</p>
      <p>यही वह संख्या प्रणाली है जिसका उपयोग Calculus, भौतिकी और सभी उच्च गणित में होता है।</p>
      <span class="solved-badge">✓ सम्पूर्ण: संख्या रेखा पर रखी जाने वाली हर संख्या एक वास्तविक संख्या है।</span>
    </div>
  </div>

</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-exclamation-circle"></i></span> वह संकट जिसने अपरिमेय संख्याओं को जन्म दिया</h2>

<p>प्राचीन यूनानी पाइथागोरस-सम्प्रदाय का दृढ़ विश्वास था: <em>प्रकृति की हर मात्रा को एक भिन्न के रूप में लिखा जा सकता है।</em> उनके लिए परिमेय संख्याएँ ही सब कुछ थीं — जब तक उनके ही एक सदस्य ने एक ऐसी खोज की जिसने उनके पूरे दर्शन को हिला दिया।</p>

<div class="compare-grid">
  <div class="compare-card blue">
    <h4>📐 समस्या: एक साधारण वर्ग</h4>
    <ul>
      <li>एक वर्ग बनाइए जिसकी हर भुजा ठीक 1 इकाई लम्बी हो</li>
      <li>पाइथागोरस प्रमेय से, विकर्ण (कोने से कोने तक की रेखा) की लम्बाई $\sqrt{2}$ है</li>
      <li>पाइथागोरसियों ने पूछा: क्या $\sqrt{2}$ को $\frac{p}{q}$ के रूप में लिखा जा सकता है?</li>
      <li>उन्हें यकीन था — हाँ। और उन्होंने इसे सिद्ध करने की कोशिश की।</li>
    </ul>
  </div>
  <div class="compare-card green">
    <h4>✗ चौंकाने वाला सच: यह कोई भिन्न नहीं हो सकती</h4>
    <ul>
      <li>मान लीजिए $\sqrt{2} = \frac{p}{q}$ सबसे सरल रूप में है (कोई उभयनिष्ठ गुणनखण्ड नहीं)</li>
      <li>$p^2 = 2q^2$, तो $p$ सम होना चाहिए — $p = 2m$ लिखें</li>
      <li>$4m^2 = 2q^2$, तो $q$ भी सम होना चाहिए</li>
      <li>लेकिन अब $p$ और $q$ दोनों सम हैं — उनमें 2 का उभयनिष्ठ गुणनखण्ड है। यह हमारी शुरुआती मान्यता का खण्डन (विरोधाभास) है!</li>
    </ul>
  </div>
</div>

<p>इसलिए $\sqrt{2}$ <strong>अपरिमेय</strong> है — यह एक वास्तविक संख्या है, लेकिन किसी भी भिन्न के बराबर नहीं। कहावत है कि जिस पाइथागोरियन ने यह खोज उजागर की (हिप्पेसस, लगभग 5वीं शताब्दी ईसापूर्व) उसे समुद्र में फेंक दिया गया। सच हो या न हो — गणितीय बात स्पष्ट है: परिमेय संख्याएँ संख्या रेखा भरने के लिए पर्याप्त नहीं हैं।</p>

<div class="info-card gold">
  <div class="info-card-header"><i class="fas fa-lightbulb"></i> अपरिमेय संख्याएँ क्या होती हैं?</div>
  <p>एक <strong>अपरिमेय संख्या</strong> वह वास्तविक संख्या है जिसे $\frac{p}{q}$ के रूप में <em>नहीं</em> लिखा जा सकता जहाँ $p$ और $q$ पूर्णांक हों। दशमलव रूप में, अपरिमेय संख्याएँ बिना किसी दोहराने वाले पैटर्न के अनन्त (हमेशा-हमेशा) चलती रहती हैं।</p>
  <ul style="margin:10px 0 0;padding-left:20px;color:#333;">
    <li>$\sqrt{2} = 1.41421356\ldots$ — कभी नहीं रुकती, कोई पैटर्न नहीं</li>
    <li>$\pi = 3.14159265\ldots$ — वृत्त की परिधि (पूरी सीमा की लम्बाई) और व्यास का अनुपात</li>
    <li>$e = 2.71828182\ldots$ — ऑयलर की संख्या, वृद्धि और क्षय के लिए उपयोग</li>
    <li>$\sqrt{3},\, \sqrt{5},\, \sqrt{7}$ — ऐसी संख्याओं के वर्गमूल जो पूर्ण वर्ग नहीं हैं</li>
  </ul>
  <p style="margin-top:10px;"><strong>ध्यान दें:</strong> हर वर्गमूल अपरिमेय नहीं होती। $\sqrt{4} = 2$ और $\sqrt{9} = 3$ परिमेय हैं — हमेशा पहले सरल करके देखें!</p>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#f5f3ff;color:#7c3aed;"><i class="fas fa-history"></i></span> संख्या प्रणाली का विकास — एक ऐतिहासिक कालक्रम</h2>

<p>यह एक बार का आविष्कार नहीं था। इसमें हज़ारों वर्ष और कई सभ्यताओं का योगदान लगा — हर पीढ़ी ने पिछली पीढ़ी की अनसुलझी समस्याएँ सुलझाईं।</p>

<table class="summary-table">
  <thead>
    <tr>
      <th>काल</th>
      <th>किसने</th>
      <th>योगदान</th>
      <th>कौन-सी प्रणाली तक पहुँचे</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>~3000 ईसापूर्व</td>
      <td>मेसोपोटामिया और मिस्र</td>
      <td>वस्तुओं की गिनती; तैली-मार्क और आरम्भिक अंक</td>
      <td>प्राकृत संख्याएँ $\mathbb{N}$</td>
    </tr>
    <tr>
      <td>~500 ईसापूर्व</td>
      <td>प्राचीन यूनान</td>
      <td>ज्यामिति में अनुपात और समानुपात का अध्ययन</td>
      <td>परिमेय संख्याएँ $\mathbb{Q}$</td>
    </tr>
    <tr>
      <td>~500 ईसापूर्व</td>
      <td>पाइथागोरसियन (यूनान)</td>
      <td>खोज: $\sqrt{2}$ किसी भिन्न के बराबर नहीं — पहली ज्ञात अपरिमेय संख्या</td>
      <td>अपरिमेय संख्याओं की ज़रूरत</td>
    </tr>
    <tr>
      <td>499 ई.</td>
      <td>आर्यभट (भारत)</td>
      <td><em>आर्यभटीय</em> — दशमलव स्थानीय-मान प्रणाली, शून्य एक काम करने वाले अंक के रूप में</td>
      <td>सम्पूर्ण संख्याएँ $\mathbb{W}$ औपचारिक</td>
    </tr>
    <tr>
      <td>628 ई.</td>
      <td>ब्रह्मगुप्त (भारत)</td>
      <td><em>ब्रह्मस्फुटसिद्धान्त</em> — शून्य और ऋणात्मक संख्याओं के अंकगणित के पहले स्पष्ट नियम</td>
      <td>पूर्णांक $\mathbb{Z}$ औपचारिक</td>
    </tr>
    <tr>
      <td>1872 ई.</td>
      <td>Richard Dedekind (जर्मनी)</td>
      <td>"Dedekind cuts" के माध्यम से वास्तविक संख्याओं की कठोर (तार्किक रूप से पूर्ण और सटीक) परिभाषा</td>
      <td>वास्तविक संख्याएँ $\mathbb{R}$ परिभाषित</td>
    </tr>
    <tr>
      <td>1874 ई.</td>
      <td>Georg Cantor (जर्मनी)</td>
      <td>सिद्ध किया: संख्या रेखा पर परिमेय की तुलना में अपरिमेय संख्याएँ कहीं अधिक हैं</td>
      <td>$\mathbb{R}$ का पूर्ण सिद्धान्त स्थापित</td>
    </tr>
  </tbody>
</table>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-pencil-alt"></i></span> हल किए गए उदाहरण</h2>

<div class="example-card">
  <div class="example-label">उदाहरण 1 — संख्या को पहचानें</div>
  <div class="example-num">1</div>
  <p>प्रत्येक संख्या के लिए बताइए कि वह <strong>सबसे छोटे</strong> किस समुच्चय में है: $\mathbb{N}$, $\mathbb{W}$, $\mathbb{Z}$, $\mathbb{Q}$, या अपरिमेय।</p>
  <p style="margin-top:8px;">$7, \quad -3, \quad \dfrac{5}{4}, \quad \sqrt{5}, \quad 0, \quad -\dfrac{2}{7}, \quad \sqrt{9}, \quad 0.\overline{6}$</p>
  <div class="solution-block">
    <strong>हल:</strong>
    <ul style="margin:8px 0 0;padding-left:20px;">
      <li>$7$ → <strong>प्राकृत</strong> $\mathbb{N}$ — सकारात्मक गणना-संख्या</li>
      <li>$0$ → <strong>सम्पूर्ण</strong> $\mathbb{W}$ — प्राकृत नहीं, पर सम्पूर्ण है</li>
      <li>$-3$ → <strong>पूर्णांक</strong> $\mathbb{Z}$ — ऋणात्मक है</li>
      <li>$\frac{5}{4}$ → <strong>परिमेय</strong> $\mathbb{Q}$ — दो पूर्णांकों की भिन्न, $= 1.25$</li>
      <li>$-\frac{2}{7}$ → <strong>परिमेय</strong> $\mathbb{Q}$ — ऋणात्मक भिन्न, फिर भी परिमेय</li>
      <li>$\sqrt{9} = 3$ → <strong>प्राकृत</strong> $\mathbb{N}$ — 3 में सरल होती है; अपरिमेय बिल्कुल नहीं!</li>
      <li>$0.\overline{6} = \frac{2}{3}$ → <strong>परिमेय</strong> $\mathbb{Q}$ — दोहराने वाला दशमलव भिन्न के बराबर</li>
      <li>$\sqrt{5}$ → <strong>अपरिमेय</strong> — 5 पूर्ण वर्ग नहीं, इसलिए $\sqrt{5}$ कोई भिन्न नहीं $\blacksquare$</li>
    </ul>
  </div>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 2 — सिद्ध करें: $\sqrt{2}$ अपरिमेय है</div>
  <div class="example-num">2</div>
  <p>सिद्ध करें कि $\sqrt{2}$ अपरिमेय है — अर्थात इसे $\frac{p}{q}$ के रूप में नहीं लिखा जा सकता जहाँ $p$ और $q$ पूर्णांक हों।</p>
  <p style="font-size:0.85rem;color:#666;margin-top:4px;"><em>सन्दर्भ: W. Rudin, Principles of Mathematical Analysis, 3rd ed. (McGraw-Hill, 1976), Example 1.1, पृ. 2</em></p>
  <div class="solution-block">
    <strong>हल — विरोधाभास द्वारा प्रमाण</strong> (हम विपरीत मान लेते हैं और दिखाते हैं कि यह असम्भवता (contradiction — ऐसी स्थिति जो खुद ही खुद से टकराए) की ओर ले जाता है):
    <p><strong>चरण 1.</strong> मान लीजिए $\sqrt{2} = \dfrac{p}{q}$, जहाँ $p$ और $q$ धनात्मक पूर्णांक हैं जिनका कोई उभयनिष्ठ (साझा) गुणनखण्ड नहीं (भिन्न अपने सरलतम रूप में है)।</p>
    <p><strong>चरण 2.</strong> दोनों पक्षों का वर्ग: $p^2 = 2q^2$। तो $p^2$ सम है। चूँकि किसी पूर्ण वर्ग के सम होने का अर्थ है उसका वर्गमूल सम है, $p$ सम होना चाहिए। $p = 2m$ लिखें।</p>
    <p><strong>चरण 3.</strong> $p = 2m$ प्रतिस्थापित करें: $(2m)^2 = 2q^2 \Rightarrow 4m^2 = 2q^2 \Rightarrow q^2 = 2m^2$। तो $q^2$ भी सम है, अर्थात $q$ भी सम है।</p>
    <p><strong>चरण 4.</strong> अब $p$ और $q$ दोनों सम हैं — यानी दोनों में 2 का गुणनखण्ड है। यह सीधे हमारी पहली मान्यता (भिन्न सरलतम रूप में है) का खण्डन करता है।</p>
    <p><strong>निष्कर्ष:</strong> हमारी मान्यता गलत थी। $\sqrt{2}$ के बराबर कोई ऐसी भिन्न $\frac{p}{q}$ नहीं है। अतः $\sqrt{2}$ अपरिमेय है। $\blacksquare$</p>
  </div>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 3 — परिमेय है या अपरिमेय?</div>
  <div class="example-num">3</div>
  <p>तय करें कि प्रत्येक व्यंजक परिमेय है या अपरिमेय, और संक्षिप्त कारण बताएँ।</p>
  <p style="margin-top:8px;">(a) $0.\overline{142857}$ &nbsp;&nbsp; (b) $\sqrt{2} + \sqrt{2}$ &nbsp;&nbsp; (c) $\sqrt{2} \times \sqrt{2}$ &nbsp;&nbsp; (d) $\pi - \pi$ &nbsp;&nbsp; (e) $2 + \sqrt{3}$</p>
  <div class="solution-block">
    <strong>हल:</strong>
    <p>(a) $0.\overline{142857}$ — <strong>परिमेय।</strong> कोई भी दोहराने वाले पैटर्न वाला दशमलव परिमेय होता है। वास्तव में $0.\overline{142857} = \dfrac{1}{7}$।</p>
    <p>(b) $\sqrt{2} + \sqrt{2} = 2\sqrt{2}$ — <strong>अपरिमेय।</strong> एक अपरिमेय संख्या को एक अशून्य परिमेय संख्या से गुणा करने पर हमेशा अपरिमेय ही मिलती है।</p>
    <p>(c) $\sqrt{2} \times \sqrt{2} = 2$ — <strong>परिमेय!</strong> यह सबसे महत्त्वपूर्ण जाल है: दो अपरिमेय संख्याओं का गुणनफल परिमेय हो सकता है। बिना जाँचे कभी न मान लें।</p>
    <p>(d) $\pi - \pi = 0$ — <strong>परिमेय।</strong> कोई भी संख्या अपने आप को घटाने पर शून्य देती है, जो परिमेय है ($= \frac{0}{1}$)।</p>
    <p>(e) $2 + \sqrt{3}$ — <strong>अपरिमेय।</strong> किसी परिमेय में अपरिमेय जोड़ने पर हमेशा अपरिमेय मिलता है। यदि $2 + \sqrt{3}$ परिमेय होती, तो $\sqrt{3} = (2 + \sqrt{3}) - 2$ भी परिमेय होती — लेकिन $\sqrt{3}$ परिमेय नहीं है। विरोधाभास! $\blacksquare$</p>
  </div>
</div>

<div class="example-card">
  <div class="example-label">उदाहरण 4 — एक आम भ्रान्ति</div>
  <div class="example-num">4</div>
  <p>एक विद्यार्थी कहता है: <em>"चूँकि $\frac{22}{7}$ का उपयोग $\pi$ के लिए किया जाता है, इसलिए $\pi$ एक परिमेय संख्या होनी चाहिए।"</em> क्या विद्यार्थी सही है? स्पष्ट करें।</p>
  <div class="solution-block">
    <strong>हल:</strong>
    <p>विद्यार्थी <strong>गलत</strong> है।</p>
    <p>$\frac{22}{7}$ केवल $\pi$ का एक <em>सन्निकटन</em> (एक निकट अनुमान, सटीक मान नहीं) है। दशमलव में $\frac{22}{7} = 3.142857142857\ldots$ — यह दोहराता है, इसलिए परिमेय है। लेकिन $\pi = 3.14159265\ldots$ — यह बिना किसी दोहराने वाले पैटर्न के हमेशा चलता रहता है, इसलिए अपरिमेय है।</p>
    <p>दोनों संख्याएँ केवल पहले दो दशमलव स्थानों तक मेल खाती हैं। उसके बाद वे अलग हो जाती हैं। गणनाओं में $\frac{22}{7}$ का उपयोग व्यावहारिक (काम के लिए आसान) है और अधिकांश रोज़मर्रा की समस्याओं के लिए काफी अच्छा उत्तर देता है। लेकिन इसका मतलब यह नहीं कि $\pi$ और $\frac{22}{7}$ एक ही संख्या हैं।</p>
    <p>$\pi$ को जर्मन गणितज्ञ Johann Heinrich Lambert ने 1761 में अपरिमेय सिद्ध किया था। यह एक वास्तविक संख्या है, लेकिन परिमेय नहीं। $\blacksquare$</p>
  </div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fffbeb;color:#d97706;"><i class="fas fa-graduation-cap"></i></span> याद रखने योग्य मुख्य बातें</h2>

<div class="tip-box">
  <div class="tip-box-header"><i class="fas fa-lightbulb"></i> ये बातें हमेशा काम आएंगी</div>
  <ul>
    <li><strong>क्रम एक शृंखला है:</strong> $\mathbb{N} \subset \mathbb{W} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$। हर प्राकृत संख्या, पूर्णांक, परिमेय और वास्तविक भी है।</li>
    <li><strong>हर वर्गमूल अपरिमेय नहीं:</strong> $\sqrt{4}=2$, $\sqrt{16}=4$, $\sqrt{25}=5$ परिमेय हैं। केवल ऐसी संख्याओं के वर्गमूल अपरिमेय होते हैं जो पूर्ण वर्ग नहीं ($\sqrt{2}$, $\sqrt{3}$, $\sqrt{5}$)।</li>
    <li><strong>दोहराने वाला दशमलव हमेशा परिमेय:</strong> $0.333\ldots = \frac{1}{3}$, $0.142857142857\ldots = \frac{1}{7}$। पैटर्न हो तो परिमेय है।</li>
    <li><strong>गुणन का जाल:</strong> $\sqrt{2} \times \sqrt{2} = 2$ परिमेय है, हालाँकि दोनों गुणनखण्ड अपरिमेय हैं। दो अपरिमेय का गुणनफल <em>हमेशा</em> अपरिमेय नहीं होता।</li>
    <li><strong>$\frac{22}{7}$, $\pi$ नहीं है:</strong> यह केवल सन्निकटन है। $\pi$ अपरिमेय है — Lambert ने 1761 में सिद्ध किया।</li>
    <li><strong>$e$ भी अपरिमेय है:</strong> ऑयलर की संख्या $e \approx 2.718$, जो चक्रवृद्धि ब्याज और वृद्धि दर में काम आती है, अपरिमेय है। Hermite ने 1873 में इसे सिद्ध किया।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#fff5f5;color:#dc2626;"><i class="fas fa-exclamation-triangle"></i></span> सामान्य गलतियाँ</h2>

<div class="warning-box">
  <div class="warning-box-header"><i class="fas fa-times-circle"></i> इन भूलों से बचें</div>
  <ul>
    <li><strong>"सभी दशमलव अपरिमेय होते हैं":</strong> गलत। $0.5 = \frac{1}{2}$ परिमेय है। केवल अनन्त और अनावर्ती (कोई पैटर्न नहीं दोहराता) दशमलव अपरिमेय होते हैं।</li>
    <li><strong>"हर वर्गमूल अपरिमेय है":</strong> $\sqrt{9} = 3 \in \mathbb{N}$। निर्णय से पहले हमेशा सरल करें।</li>
    <li><strong>"अपरिमेय + अपरिमेय = अपरिमेय":</strong> हमेशा नहीं। $\sqrt{2} + (-\sqrt{2}) = 0$, जो परिमेय है।</li>
    <li><strong>"अपरिमेय × अपरिमेय = अपरिमेय":</strong> हमेशा नहीं। $\sqrt{3} \times \sqrt{3} = 3$, जो परिमेय है।</li>
    <li><strong>"$\frac{22}{7} = \pi$":</strong> यह केवल सन्निकटन है। $\pi$ अपरिमेय है और किसी भी भिन्न के बराबर नहीं हो सकती।</li>
    <li><strong>"$\mathbb{N}$ में 0 शामिल है":</strong> अधिकांश गणित पाठ्यक्रमों में $\mathbb{N} = \{1, 2, 3, \ldots\}$। शून्य एक सम्पूर्ण संख्या है, प्राकृत नहीं — हालाँकि परम्परा देश के अनुसार भिन्न हो सकती है।</li>
  </ul>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#ecfdf5;color:#059669;"><i class="fas fa-globe"></i></span> वास्तविक संख्याएँ क्यों महत्त्वपूर्ण हैं?</h2>

<div class="app-grid">
  <div class="app-card">
    <div class="app-icon">📐</div>
    <strong>ज्यामिति</strong>
    <p>एक इकाई वर्ग का विकर्ण ($\sqrt{2}$) और वृत्त की परिधि-व्यास अनुपात ($\pi$) अपरिमेय हैं — केवल भिन्नों से इन्हें बिल्कुल सटीक नहीं मापा जा सकता।</p>
  </div>
  <div class="app-card">
    <div class="app-icon">⚙️</div>
    <strong>इंजीनियरिंग</strong>
    <p>कोण, तरंग और संकेत — सभी में $\pi$ और $\sqrt{2}$ जैसी अपरिमेय संख्याएँ लगती हैं। वास्तविक संख्याओं के बिना आधुनिक इंजीनियरिंग असम्भव होती।</p>
  </div>
  <div class="app-card">
    <div class="app-icon">📈</div>
    <strong>वित्त</strong>
    <p>चक्रवृद्धि ब्याज में $e \approx 2.718$ का उपयोग होता है। हर बैंक इसका उपयोग करता है — अक्सर बिना जाने भी।</p>
  </div>
  <div class="app-card">
    <div class="app-icon">⚛️</div>
    <strong>भौतिकी</strong>
    <p>गति, तापमान और दूरी प्रकृति में निरन्तर (बिना किसी अचानक छलाँग के) हैं। वास्तविक संख्याएँ हर भौतिक राशि के लिए सबसे उपयुक्त भाषा हैं।</p>
  </div>
</div>

<h2 class="section-title"><span class="sec-icon" style="background:#eff6ff;color:#1e3c72;"><i class="fas fa-table"></i></span> सारांश — संख्या प्रणाली एक नज़र में</h2>

<table class="summary-table">
  <thead>
    <tr>
      <th>प्रणाली</th>
      <th>प्रतीक</th>
      <th>उदाहरण</th>
      <th>नई अवधारणा</th>
      <th>किस समस्या का समाधान</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>प्राकृत संख्याएँ</td>
      <td>$\mathbb{N}$</td>
      <td>$1, 2, 3$</td>
      <td>गिनती</td>
      <td>कितनी चीजें हैं?</td>
    </tr>
    <tr>
      <td>सम्पूर्ण संख्याएँ</td>
      <td>$\mathbb{W}$</td>
      <td>$0, 1, 2$</td>
      <td>शून्य</td>
      <td>"कुछ नहीं" को कैसे दिखाएँ?</td>
    </tr>
    <tr>
      <td>पूर्णांक</td>
      <td>$\mathbb{Z}$</td>
      <td>$-3, 0, 5$</td>
      <td>ऋणात्मक संख्याएँ</td>
      <td>$3 - 5 = ?$</td>
    </tr>
    <tr>
      <td>परिमेय संख्याएँ</td>
      <td>$\mathbb{Q}$</td>
      <td>$\frac{1}{2}, -\frac{3}{4}, 0.\overline{3}$</td>
      <td>भिन्न और अनुपात</td>
      <td>$1 \div 2 = ?$</td>
    </tr>
    <tr>
      <td>अपरिमेय संख्याएँ</td>
      <td>$\mathbb{Q}^c$</td>
      <td>$\sqrt{2}, \pi, e$</td>
      <td>भिन्न-रहित लम्बाइयाँ</td>
      <td>इकाई वर्ग का विकर्ण क्या है?</td>
    </tr>
    <tr>
      <td><strong>वास्तविक संख्याएँ</strong></td>
      <td>$\mathbb{R}$</td>
      <td>उपरोक्त सभी</td>
      <td>अखण्ड संख्या रेखा</td>
      <td>रेखा का हर बिन्दु एक संख्या है</td>
    </tr>
  </tbody>
</table>

<div class="highlight-result">
  <p style="margin:0;font-size:1.1rem;font-weight:700;">$\mathbb{N} \subset \mathbb{W} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$</p>
  <p style="margin:8px 0 0;font-size:0.9rem;color:#4338ca;">हर संख्या प्रणाली अगली के अन्दर समाई है। वास्तविक संख्याएँ सबसे बड़ी हैं — वे उन सभी संख्याओं को सम्मिलित करती हैं जिन्हें एक सीधी संख्या रेखा पर रखा जा सके।</p>
</div>

</div>

<!-- ═══ PDF DOWNLOAD — jsPDF (Hindi post — PDF is English) ════════ -->
<style>
.pdf-section { text-align:center; margin:44px 0 28px; }
.pdf-btn {
  display:inline-flex; align-items:center; gap:14px;
  background:linear-gradient(135deg,#1e3c72,#7c3aed);
  color:white; border:none; cursor:pointer;
  padding:15px 34px; border-radius:50px;
  font-family:'Hind',sans-serif; font-size:1rem; font-weight:700;
  box-shadow:0 6px 22px rgba(30,60,114,0.38);
  transition:transform .2s, box-shadow .2s;
}
.pdf-btn:hover { transform:translateY(-3px); box-shadow:0 10px 30px rgba(30,60,114,0.48); color:white; }
.pdf-btn.generating { opacity:.65; pointer-events:none; }
.pdf-btn .pi { font-size:1.45rem; }
.pdf-btn .pt { display:flex; flex-direction:column; text-align:left; line-height:1.35; }
.pdf-btn .pt .pt1 { font-size:1rem; }
.pdf-btn .pt .pt2 { font-size:0.72rem; opacity:.82; font-weight:400; }
</style>

<div class="pdf-section">
  <button class="pdf-btn" id="pdfDownloadBtnHi" onclick="generatePDFHi()">
    <span class="pi">&#x1F4E5;</span>
    <span class="pt">
      <span class="pt1">PDF &#x928;&#x94B;&#x91F;&#x94D;&#x938; &#x921;&#x93E;&#x909;&#x928;&#x932;&#x94B;&#x921; &#x915;&#x930;&#x947;&#x902;</span>
      <span class="pt2">Foundations of Real Numbers &#8212; Fractal Frontier Maths</span>
    </span>
  </button>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script>
// Wrapper for Hindi button — delegates to same buildPDF logic
function generatePDFHi() {
  var btn = document.getElementById('pdfDownloadBtnHi');
  btn.classList.add('generating');
  btn.querySelector('.pt1').textContent = 'PDF &#x092C;&#x0928; &#x0930;&#x0939;&#x0940; &#x0939;&#x0948;…';
  setTimeout(function() {
    try {
      buildPDF(btn, 'PDF &#x0928;&#x094B;&#x091F;&#x094D;&#x0938; &#x0921;&#x093E;&#x0909;&#x0928;&#x0932;&#x094B;&#x0921; &#x0915;&#x0930;&#x0947;&#x0902;');
    } catch(e) {
      console.error(e);
      btn.classList.remove('generating');
      btn.querySelector('.pt1').textContent = 'PDF &#x0928;&#x094B;&#x091F;&#x094D;&#x0938; &#x0921;&#x093E;&#x0909;&#x0928;&#x0932;&#x094B;&#x0921; &#x0915;&#x0930;&#x0947;&#x0902;';
    }
  }, 80);
}

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

function buildPDF(btn, resetLabel) {
  if (!btn) { btn = document.getElementById('pdfDownloadBtn'); }
  if (!resetLabel) resetLabel = 'Download PDF Notes';
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
  btn.querySelector('.pt1').textContent = resetLabel;
}

</script>
