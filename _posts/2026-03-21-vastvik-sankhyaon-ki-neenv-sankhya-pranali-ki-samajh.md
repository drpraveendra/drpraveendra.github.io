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

<!-- ═══════════════════════════════════════════════════════════
     PDF GENERATION — html2pdf.js (client-side)
     Uses the same English-content #pdf-content div as the EN post.
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

<!-- Hindi download button -->
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
  <button class="pdf-btn" id="pdfDownloadBtnHi" onclick="generatePDF()">
    <span class="pi">📥</span>
    <span class="pt">
      <span class="pt1">PDF नोट्स डाउनलोड करें</span>
      <span class="pt2">Foundations of Real Numbers — Fractal Frontier Maths</span>
    </span>
  </button>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>

<script>
function generatePDF() {
  var btn = document.getElementById('pdfDownloadBtnHi');
  btn.classList.add('generating');
  btn.querySelector('.pt1').textContent = 'PDF बन रही है…';

  var source = document.getElementById('pdf-content');
  var clone = source.cloneNode(true);
  clone.removeAttribute('id');

  var overlay = document.createElement('div');
  overlay.style.cssText = [
    'position:fixed','top:0','left:0',
    'width:210mm','min-height:100vh',
    'background:#fff','z-index:99999',
    'overflow:visible','padding:0','margin:0','box-sizing:border-box'
  ].join(';');

  overlay.appendChild(clone);
  document.body.appendChild(overlay);

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
        jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait', compress: true },
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
            pdf.saveGraphicsState();
            pdf.setGState(new pdf.GState({ opacity: 0.07 }));
            pdf.setFont('helvetica', 'bold');
            pdf.setFontSize(28);
            pdf.setTextColor(30, 60, 114);
            pdf.text('Fractal Frontier Maths', pw/2, ph/2, { align:'center', angle:45 });
            pdf.restoreGraphicsState();
            pdf.setDrawColor(220, 220, 220);
            pdf.setLineWidth(0.3);
            pdf.line(14, ph-11, pw-14, ph-11);
            pdf.setFont('helvetica','normal');
            pdf.setFontSize(7);
            pdf.setTextColor(120,120,120);
            pdf.text('drpraveendra.github.io  |  Fractal Frontier Maths', 14, ph-7.5);
            pdf.text('Page ' + i + ' of ' + totalPages, pw-14, ph-7.5, { align:'right' });
          }
        })
        .save()
        .then(function() {
          document.body.removeChild(overlay);
          btn.classList.remove('generating');
          btn.querySelector('.pt1').textContent = 'PDF नोट्स डाउनलोड करें';
        })
        .catch(function(err) {
          console.error('PDF error:', err);
          document.body.removeChild(overlay);
          btn.classList.remove('generating');
          btn.querySelector('.pt1').textContent = 'PDF नोट्स डाउनलोड करें';
        });

    });
  });
}
</script>
