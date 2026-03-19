---
layout: default
title: "Previous Year Question Papers"
permalink: /resources/previous-papers/
---

<style>
  .sub-hero {
    background: linear-gradient(135deg, #d97706, #f59e0b);
    border-radius: 16px; padding: 40px 35px; color: white; margin-bottom: 40px;
  }
  .sub-hero h1 { font-size: 2rem; font-weight: 800; color: white; margin: 0 0 10px; }
  .sub-hero p  { opacity: 0.9; margin: 0; font-size: 0.95rem; max-width: 650px; line-height: 1.7; }
  .breadcrumb  { font-size: 0.82rem; opacity: 0.8; margin-bottom: 12px; }
  .breadcrumb a { color: white; text-decoration: none; }
  .breadcrumb a:hover { text-decoration: underline; }

  .exam-tabs {
    display: flex; gap: 12px; flex-wrap: wrap; margin-bottom: 35px;
  }
  .exam-tab {
    padding: 10px 24px; border-radius: 30px; font-size: 0.9rem; font-weight: 700;
    cursor: pointer; transition: all 0.2s; border: 2px solid transparent;
  }
  .tab-csir   { background: #fffbeb; color: #d97706; border-color: #fde68a; }
  .tab-gate   { background: #eff6ff; color: #1e3c72; border-color: #bfdbfe; }
  .tab-jam    { background: #f5f3ff; color: #7c3aed; border-color: #ddd6fe; }
  .tab-csir:hover   { background: #d97706; color: white; border-color: #d97706; }
  .tab-gate:hover   { background: #1e3c72; color: white; border-color: #1e3c72; }
  .tab-jam:hover    { background: #7c3aed; color: white; border-color: #7c3aed; }

  .exam-section { margin-bottom: 50px; }
  .exam-header {
    border-radius: 14px; padding: 24px 28px; margin-bottom: 22px; color: white;
    display: flex; align-items: center; gap: 18px;
  }
  .exam-header.csir   { background: linear-gradient(135deg, #d97706, #f59e0b); }
  .exam-header.gate   { background: linear-gradient(135deg, #1e3c72, #2a5298); }
  .exam-header.jam    { background: linear-gradient(135deg, #7c3aed, #a855f7); }
  .exam-header-icon {
    width: 56px; height: 56px; background: rgba(255,255,255,0.2);
    border-radius: 14px; display: flex; align-items: center; justify-content: center;
    font-size: 1.6rem; flex-shrink: 0;
  }
  .exam-header h2 { font-size: 1.3rem; font-weight: 800; color: white; margin: 0 0 4px; }
  .exam-header p  { opacity: 0.88; margin: 0; font-size: 0.88rem; }

  .papers-table {
    width: 100%; border-collapse: collapse;
    border-radius: 12px; overflow: hidden;
    box-shadow: 0 4px 14px rgba(0,0,0,0.07);
    margin-bottom: 16px;
  }
  .papers-table th {
    padding: 13px 16px; text-align: left;
    font-size: 0.82rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px;
    color: white;
  }
  .papers-table.csir th { background: #d97706; }
  .papers-table.gate th { background: #1e3c72; }
  .papers-table.jam  th { background: #7c3aed; }
  .papers-table td {
    padding: 12px 16px; font-size: 0.88rem; color: #333;
    border-bottom: 1px solid #e5e7eb;
  }
  .papers-table tr:nth-child(even) td { background: #fafafa; }
  .papers-table tr:last-child td { border-bottom: none; }
  .papers-table td:first-child { font-weight: 700; color: #1e3c72; }
  .btn-download, .btn-solution {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 0.78rem; font-weight: 700; padding: 5px 14px;
    border-radius: 16px; text-decoration: none; transition: all 0.2s; margin-right: 6px;
  }
  .btn-download { background: #eff6ff; color: #1e3c72; border: 1px solid #bfdbfe; }
  .btn-download:hover { background: #1e3c72; color: white; text-decoration: none; }
  .btn-solution { background: #ecfdf5; color: #059669; border: 1px solid #a7f3d0; }
  .btn-solution:hover { background: #059669; color: white; text-decoration: none; }
  .btn-soon {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 0.78rem; font-weight: 600; padding: 5px 14px;
    border-radius: 16px; background: #f1f5f9; color: #94a3b8;
    border: 1px solid #e2e8f0;
  }
  .official-link {
    display: inline-flex; align-items: center; gap: 7px;
    font-size: 0.85rem; font-weight: 700;
    padding: 9px 20px; border-radius: 30px; text-decoration: none; transition: all 0.2s;
    margin-right: 10px; margin-top: 10px;
  }
  .link-csir { background: #fffbeb; color: #d97706; border: 1px solid #fde68a; }
  .link-csir:hover { background: #d97706; color: white; text-decoration: none; }
  .link-gate { background: #eff6ff; color: #1e3c72; border: 1px solid #bfdbfe; }
  .link-gate:hover { background: #1e3c72; color: white; text-decoration: none; }
  .link-jam  { background: #f5f3ff; color: #7c3aed; border: 1px solid #ddd6fe; }
  .link-jam:hover  { background: #7c3aed; color: white; text-decoration: none; }

  .notice-box {
    background: #fffbeb; border: 1px solid #fde68a; border-radius: 12px;
    padding: 16px 20px; font-size: 0.86rem; color: #92400e;
    display: flex; align-items: flex-start; gap: 10px; margin-bottom: 20px;
  }
  .notice-box i { margin-top: 2px; flex-shrink: 0; }
  .back-link {
    display: inline-flex; align-items: center; gap: 8px;
    color: #d97706; text-decoration: none; font-size: 0.88rem; font-weight: 600;
    margin-top: 10px; padding: 8px 18px; border-radius: 30px;
    background: #fffbeb; border: 1px solid #fde68a; transition: all 0.2s;
  }
  .back-link:hover { background: #d97706; color: white; text-decoration: none; }
</style>

<div class="sub-hero">
  <p class="breadcrumb"><a href="/resources/">← Resources Hub</a> / Previous Year Papers</p>
  <h1><i class="fas fa-file-alt"></i> Previous Year Question Papers</h1>
  <p>Past question papers with solutions for CSIR NET, GATE, and IIT JAM — the most effective exam preparation strategy.</p>
</div>

<div class="notice-box">
  <i class="fas fa-info-circle"></i>
  <span>Papers and solutions are being added progressively. For the most recent papers, always check the official examination authority websites linked below. This page will be updated regularly.</span>
</div>

<!-- CSIR NET -->
<div class="exam-section">
  <div class="exam-header csir">
    <div class="exam-header-icon">🔬</div>
    <div>
      <h2>CSIR NET — Mathematical Sciences</h2>
      <p>Council of Scientific & Industrial Research — National Eligibility Test &nbsp;|&nbsp; Conducted twice a year (June & December)</p>
    </div>
  </div>

  <table class="papers-table csir">
    <thead><tr><th>Year</th><th>Session</th><th>Question Paper</th><th>Solutions</th></tr></thead>
    <tbody>
      <tr><td>2024</td><td>June</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2023</td><td>December</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2023</td><td>June</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2022</td><td>December</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
    </tbody>
  </table>
  <a href="https://csirnet.nta.ac.in/" target="_blank" rel="noopener" class="official-link link-csir"><i class="fas fa-external-link-alt"></i> Official CSIR NET Website</a>
  <a href="https://www.nta.ac.in/previous-year-papers" target="_blank" rel="noopener" class="official-link link-csir"><i class="fas fa-download"></i> NTA Previous Papers</a>
</div>

<!-- GATE -->
<div class="exam-section">
  <div class="exam-header gate">
    <div class="exam-header-icon">🏛️</div>
    <div>
      <h2>GATE — Mathematics (MA)</h2>
      <p>Graduate Aptitude Test in Engineering — Mathematics &nbsp;|&nbsp; Conducted annually (February)</p>
    </div>
  </div>

  <table class="papers-table gate">
    <thead><tr><th>Year</th><th>Set</th><th>Question Paper</th><th>Solutions</th></tr></thead>
    <tbody>
      <tr><td>2025</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2024</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2023</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2022</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
    </tbody>
  </table>
  <a href="https://gate2025.iitr.ac.in/" target="_blank" rel="noopener" class="official-link link-gate"><i class="fas fa-external-link-alt"></i> Official GATE Website</a>
  <a href="https://gate.iitkgp.ac.in/gate_old_qp.php" target="_blank" rel="noopener" class="official-link link-gate"><i class="fas fa-download"></i> GATE Old Papers</a>
</div>

<!-- IIT JAM -->
<div class="exam-section">
  <div class="exam-header jam">
    <div class="exam-header-icon">🎓</div>
    <div>
      <h2>IIT JAM — Mathematics (MA)</h2>
      <p>Joint Admission Test for M.Sc. — Mathematics &nbsp;|&nbsp; Conducted annually (February)</p>
    </div>
  </div>

  <table class="papers-table jam">
    <thead><tr><th>Year</th><th>Paper</th><th>Question Paper</th><th>Solutions</th></tr></thead>
    <tbody>
      <tr><td>2025</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2024</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2023</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
      <tr><td>2022</td><td>MA</td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td><td><span class="btn-soon"><i class="fas fa-clock"></i> Coming Soon</span></td></tr>
    </tbody>
  </table>
  <a href="https://jam.iitd.ac.in/" target="_blank" rel="noopener" class="official-link link-jam"><i class="fas fa-external-link-alt"></i> Official IIT JAM Website</a>
  <a href="https://jam.iitm.ac.in/previous_qp.php" target="_blank" rel="noopener" class="official-link link-jam"><i class="fas fa-download"></i> JAM Old Papers</a>
</div>

<a href="/resources/" class="back-link"><i class="fas fa-arrow-left"></i> Back to Resources Hub</a>
