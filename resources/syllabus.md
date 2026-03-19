---
layout: default
title: "Competitive Exam Syllabi"
permalink: /resources/syllabus/
---

<style>
  .sub-hero {
    background: linear-gradient(135deg, #7c3aed, #a855f7);
    border-radius: 16px; padding: 40px 35px; color: white; margin-bottom: 40px;
  }
  .sub-hero h1 { font-size: 2rem; font-weight: 800; color: white; margin: 0 0 10px; }
  .sub-hero p  { opacity: 0.9; margin: 0; font-size: 0.95rem; max-width: 650px; line-height: 1.7; }
  .breadcrumb  { font-size: 0.82rem; opacity: 0.8; margin-bottom: 12px; }
  .breadcrumb a { color: white; text-decoration: none; }
  .breadcrumb a:hover { text-decoration: underline; }

  .exam-section { margin-bottom: 50px; }
  .exam-header {
    border-radius: 14px; padding: 24px 28px; margin-bottom: 22px;
    color: white; display: flex; align-items: center; gap: 18px;
  }
  .exam-header.csir   { background: linear-gradient(135deg, #d97706, #f59e0b); }
  .exam-header.gate   { background: linear-gradient(135deg, #1e3c72, #2a5298); }
  .exam-header.jam    { background: linear-gradient(135deg, #7c3aed, #a855f7); }
  .exam-header.uni    { background: linear-gradient(135deg, #059669, #10b981); }
  .exam-header-icon {
    width: 56px; height: 56px; background: rgba(255,255,255,0.2);
    border-radius: 14px; display: flex; align-items: center; justify-content: center;
    font-size: 1.6rem; flex-shrink: 0;
  }
  .exam-header h2 { font-size: 1.3rem; font-weight: 800; color: white; margin: 0 0 4px; }
  .exam-header p  { opacity: 0.88; margin: 0; font-size: 0.85rem; }

  .syllabus-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px; margin-bottom: 16px;
  }
  .syllabus-unit {
    background: white; border-radius: 13px; padding: 20px 22px;
    box-shadow: 0 3px 12px rgba(0,0,0,0.07);
    border-top: 4px solid #7c3aed;
  }
  .syllabus-unit.csir  { border-top-color: #d97706; }
  .syllabus-unit.gate  { border-top-color: #1e3c72; }
  .syllabus-unit.jam   { border-top-color: #7c3aed; }
  .syllabus-unit.uni   { border-top-color: #059669; }
  .unit-label {
    font-size: 0.7rem; font-weight: 700; text-transform: uppercase;
    letter-spacing: 0.5px; color: #888; margin-bottom: 6px;
  }
  .syllabus-unit h3 { font-size: 0.98rem; font-weight: 800; color: #1e3c72; margin: 0 0 12px; }
  .syllabus-unit ul { list-style: none; padding: 0; margin: 0; }
  .syllabus-unit ul li {
    font-size: 0.83rem; color: #555; padding: 4px 0;
    border-bottom: 1px solid #f1f5f9;
    display: flex; align-items: center; gap: 8px;
  }
  .syllabus-unit ul li:last-child { border-bottom: none; }
  .syllabus-unit ul li::before {
    content: '▸'; font-size: 0.65rem; flex-shrink: 0;
  }
  .syllabus-unit.csir ul li::before { color: #d97706; }
  .syllabus-unit.gate ul li::before { color: #1e3c72; }
  .syllabus-unit.jam  ul li::before { color: #7c3aed; }
  .syllabus-unit.uni  ul li::before { color: #059669; }

  .exam-meta {
    background: #f8faff; border-radius: 12px; padding: 16px 20px;
    margin-bottom: 18px; display: flex; flex-wrap: wrap; gap: 20px; font-size: 0.85rem;
  }
  .meta-item { display: flex; align-items: center; gap: 8px; color: #444; }
  .meta-item i { color: #1e3c72; width: 16px; }
  .meta-item strong { color: #1e3c72; }

  .official-btn {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 9px 20px; border-radius: 30px; font-weight: 700; font-size: 0.85rem;
    text-decoration: none; transition: all 0.2s; margin-right: 10px; margin-top: 14px;
  }
  .btn-csir { background: #fffbeb; color: #d97706; border: 1px solid #fde68a; }
  .btn-csir:hover { background: #d97706; color: white; text-decoration: none; }
  .btn-gate { background: #eff6ff; color: #1e3c72; border: 1px solid #bfdbfe; }
  .btn-gate:hover { background: #1e3c72; color: white; text-decoration: none; }
  .btn-jam  { background: #f5f3ff; color: #7c3aed; border: 1px solid #ddd6fe; }
  .btn-jam:hover  { background: #7c3aed; color: white; text-decoration: none; }
  .btn-uni  { background: #ecfdf5; color: #059669; border: 1px solid #a7f3d0; }
  .btn-uni:hover  { background: #059669; color: white; text-decoration: none; }

  .back-link {
    display: inline-flex; align-items: center; gap: 8px;
    color: #7c3aed; text-decoration: none; font-size: 0.88rem; font-weight: 600;
    margin-top: 10px; padding: 8px 18px; border-radius: 30px;
    background: #f5f3ff; border: 1px solid #ddd6fe; transition: all 0.2s;
  }
  .back-link:hover { background: #7c3aed; color: white; text-decoration: none; }
</style>

<div class="sub-hero">
  <p class="breadcrumb"><a href="/resources/">← Resources Hub</a> / Exam Syllabi</p>
  <h1><i class="fas fa-list-alt"></i> Competitive Exam Syllabi</h1>
  <p>Official and detailed syllabi for CSIR NET, GATE, IIT JAM and university examinations — know exactly what to study.</p>
</div>

<!-- CSIR NET -->
<div class="exam-section">
  <div class="exam-header csir">
    <div class="exam-header-icon">🔬</div>
    <div>
      <h2>CSIR NET — Mathematical Sciences</h2>
      <p>Three parts: Part A (General Aptitude) + Part B (Core MSc level) + Part C (Advanced Research level)</p>
    </div>
  </div>

  <div class="exam-meta">
    <div class="meta-item"><i class="fas fa-calendar"></i> <span>Conducted: <strong>June & December</strong></span></div>
    <div class="meta-item"><i class="fas fa-clock"></i> <span>Duration: <strong>3 hours</strong></span></div>
    <div class="meta-item"><i class="fas fa-star"></i> <span>Marks: <strong>200 (Part A: 30 + Part B: 70 + Part C: 100)</strong></span></div>
    <div class="meta-item"><i class="fas fa-award"></i> <span>Qualifies for: <strong>JRF / Lectureship</strong></span></div>
  </div>

  <div class="syllabus-grid">
    <div class="syllabus-unit csir">
      <div class="unit-label">Unit 1</div>
      <h3>Analysis</h3>
      <ul>
        <li>Elementary set theory, countable & uncountable sets</li>
        <li>Real number system, sequences & series</li>
        <li>Continuity, differentiability, mean value theorems</li>
        <li>Riemann integration, sequences of functions</li>
        <li>Uniform convergence, power series, Fourier series</li>
        <li>Functions of several variables, metric spaces</li>
      </ul>
    </div>
    <div class="syllabus-unit csir">
      <div class="unit-label">Unit 2</div>
      <h3>Linear Algebra & Abstract Algebra</h3>
      <ul>
        <li>Vector spaces, subspaces, linear maps</li>
        <li>Matrices, eigenvalues, eigenvectors</li>
        <li>Inner product spaces, orthonormal basis</li>
        <li>Groups, subgroups, normal subgroups</li>
        <li>Rings, fields, polynomial rings</li>
      </ul>
    </div>
    <div class="syllabus-unit csir">
      <div class="unit-label">Unit 3</div>
      <h3>Complex Analysis & ODE</h3>
      <ul>
        <li>Analytic functions, Cauchy-Riemann equations</li>
        <li>Cauchy's theorem, Taylor & Laurent series</li>
        <li>Residues & poles, conformal mappings</li>
        <li>First order ODEs, singular points</li>
        <li>Sturm-Liouville problems</li>
      </ul>
    </div>
    <div class="syllabus-unit csir">
      <div class="unit-label">Unit 4</div>
      <h3>Topology, Functional Analysis & PDE</h3>
      <ul>
        <li>Topological spaces, continuity, compactness</li>
        <li>Connectedness, separation axioms</li>
        <li>Normed & Banach spaces, Hilbert spaces</li>
        <li>Second order linear PDEs</li>
        <li>Numerical Analysis fundamentals</li>
      </ul>
    </div>
  </div>

  <a href="https://csirnet.nta.ac.in/syllabus" target="_blank" rel="noopener" class="official-btn btn-csir"><i class="fas fa-external-link-alt"></i> Official CSIR NET Syllabus</a>
</div>

<!-- GATE -->
<div class="exam-section">
  <div class="exam-header gate">
    <div class="exam-header-icon">🏛️</div>
    <div>
      <h2>GATE — Mathematics (MA)</h2>
      <p>Graduate Aptitude Test in Engineering — Mathematics paper for M.Tech / Ph.D. / PSU admissions</p>
    </div>
  </div>

  <div class="exam-meta">
    <div class="meta-item"><i class="fas fa-calendar"></i> <span>Conducted: <strong>February</strong></span></div>
    <div class="meta-item"><i class="fas fa-clock"></i> <span>Duration: <strong>3 hours</strong></span></div>
    <div class="meta-item"><i class="fas fa-star"></i> <span>Marks: <strong>100 (65 questions)</strong></span></div>
    <div class="meta-item"><i class="fas fa-award"></i> <span>Qualifies for: <strong>M.Tech / Ph.D. / PSU Jobs</strong></span></div>
  </div>

  <div class="syllabus-grid">
    <div class="syllabus-unit gate">
      <div class="unit-label">Section 1</div>
      <h3>Calculus & Real Analysis</h3>
      <ul>
        <li>Sequences, series, convergence tests</li>
        <li>Limits, continuity, differentiability</li>
        <li>Mean value theorems, L'Hôpital's rule</li>
        <li>Riemann integration, improper integrals</li>
        <li>Functions of two variables, maxima/minima</li>
      </ul>
    </div>
    <div class="syllabus-unit gate">
      <div class="unit-label">Section 2</div>
      <h3>Linear Algebra</h3>
      <ul>
        <li>Finite-dimensional vector spaces</li>
        <li>Linear transformations, matrix representation</li>
        <li>Eigenvalues, eigenvectors, diagonalization</li>
        <li>Quadratic forms, inner product spaces</li>
        <li>Systems of linear equations</li>
      </ul>
    </div>
    <div class="syllabus-unit gate">
      <div class="unit-label">Section 3</div>
      <h3>Complex Analysis & ODE</h3>
      <ul>
        <li>Analytic functions, Cauchy integral formula</li>
        <li>Laurent series, singularities, residue theorem</li>
        <li>First and second order ODEs</li>
        <li>Systems of ODEs, Laplace transforms</li>
        <li>Boundary value problems</li>
      </ul>
    </div>
    <div class="syllabus-unit gate">
      <div class="unit-label">Section 4</div>
      <h3>Algebra, Topology & Numerical Analysis</h3>
      <ul>
        <li>Groups, rings, fields, ideals</li>
        <li>Metric spaces, topological spaces</li>
        <li>Numerical methods — bisection, Newton-Raphson</li>
        <li>Numerical integration — Simpson's, Trapezoidal</li>
        <li>Probability & Statistics basics</li>
      </ul>
    </div>
  </div>

  <a href="https://gate2025.iitr.ac.in/syllabus_ma.html" target="_blank" rel="noopener" class="official-btn btn-gate"><i class="fas fa-external-link-alt"></i> Official GATE MA Syllabus</a>
</div>

<!-- IIT JAM -->
<div class="exam-section">
  <div class="exam-header jam">
    <div class="exam-header-icon">🎓</div>
    <div>
      <h2>IIT JAM — Mathematics (MA)</h2>
      <p>Joint Admission Test for M.Sc. programmes at IITs and IISc — Mathematics paper</p>
    </div>
  </div>

  <div class="exam-meta">
    <div class="meta-item"><i class="fas fa-calendar"></i> <span>Conducted: <strong>February</strong></span></div>
    <div class="meta-item"><i class="fas fa-clock"></i> <span>Duration: <strong>3 hours</strong></span></div>
    <div class="meta-item"><i class="fas fa-star"></i> <span>Marks: <strong>100 (60 questions)</strong></span></div>
    <div class="meta-item"><i class="fas fa-award"></i> <span>Qualifies for: <strong>M.Sc. at IITs / IISc</strong></span></div>
  </div>

  <div class="syllabus-grid">
    <div class="syllabus-unit jam">
      <div class="unit-label">Section 1</div>
      <h3>Real Analysis</h3>
      <ul>
        <li>Sequences and series of real numbers</li>
        <li>Limits, continuity, uniform continuity</li>
        <li>Differentiability, Rolle's & MVT theorems</li>
        <li>Riemann integrability, fundamental theorem</li>
        <li>Sequences and series of functions</li>
      </ul>
    </div>
    <div class="syllabus-unit jam">
      <div class="unit-label">Section 2</div>
      <h3>Multivariable Calculus & Linear Algebra</h3>
      <ul>
        <li>Functions of two variables, partial derivatives</li>
        <li>Double integrals, change of variables</li>
        <li>Vector calculus — Green's, Stokes', Divergence</li>
        <li>Matrices, determinants, rank</li>
        <li>Eigenvalues, eigenvectors, orthogonality</li>
      </ul>
    </div>
    <div class="syllabus-unit jam">
      <div class="unit-label">Section 3</div>
      <h3>Differential Equations & Complex Numbers</h3>
      <ul>
        <li>First order ODEs — exact, linear, Bernoulli</li>
        <li>Second order ODEs — constant coefficients</li>
        <li>Systems of linear ODEs</li>
        <li>Complex numbers, complex functions</li>
        <li>Power series, analytic functions basics</li>
      </ul>
    </div>
    <div class="syllabus-unit jam">
      <div class="unit-label">Section 4</div>
      <h3>Abstract Algebra & Probability</h3>
      <ul>
        <li>Groups, subgroups, cyclic groups</li>
        <li>Normal subgroups, quotient groups</li>
        <li>Rings, integral domains, fields</li>
        <li>Random variables, probability distributions</li>
        <li>Mean, variance, standard distributions</li>
      </ul>
    </div>
  </div>

  <a href="https://jam.iitd.ac.in/syllabus.html" target="_blank" rel="noopener" class="official-btn btn-jam"><i class="fas fa-external-link-alt"></i> Official IIT JAM Syllabus</a>
</div>

<!-- University -->
<div class="exam-section">
  <div class="exam-header uni">
    <div class="exam-header-icon">🏫</div>
    <div>
      <h2>University Syllabi — B.Sc. & M.Sc.</h2>
      <p>Rajasthan University and affiliated college syllabi for undergraduate and postgraduate mathematics</p>
    </div>
  </div>

  <div class="syllabus-grid">
    <div class="syllabus-unit uni">
      <div class="unit-label">B.Sc. Year 1 & 2</div>
      <h3>Core Mathematics</h3>
      <ul>
        <li>Calculus — differential and integral</li>
        <li>Coordinate geometry</li>
        <li>Abstract algebra — groups and rings</li>
        <li>Ordinary differential equations</li>
        <li>Vector calculus</li>
      </ul>
    </div>
    <div class="syllabus-unit uni">
      <div class="unit-label">B.Sc. Year 3</div>
      <h3>Advanced Mathematics</h3>
      <ul>
        <li>Real analysis</li>
        <li>Linear algebra</li>
        <li>Partial differential equations</li>
        <li>Numerical methods</li>
        <li>Mechanics / Operations Research</li>
      </ul>
    </div>
    <div class="syllabus-unit uni">
      <div class="unit-label">M.Sc. Semesters 1–2</div>
      <h3>Postgraduate Core</h3>
      <ul>
        <li>Real and complex analysis</li>
        <li>Abstract algebra (advanced)</li>
        <li>Topology</li>
        <li>Functional analysis</li>
        <li>Advanced linear algebra</li>
      </ul>
    </div>
    <div class="syllabus-unit uni">
      <div class="unit-label">M.Sc. Semesters 3–4</div>
      <h3>Electives & Specialisation</h3>
      <ul>
        <li>Measure theory & integration</li>
        <li>Differential geometry</li>
        <li>Operations research</li>
        <li>Mathematical statistics</li>
        <li>Dissertation / Project</li>
      </ul>
    </div>
  </div>

  <a href="https://www.uniraj.ac.in/syllabus.php" target="_blank" rel="noopener" class="official-btn btn-uni"><i class="fas fa-external-link-alt"></i> University of Rajasthan Syllabus</a>
</div>

<a href="/resources/" class="back-link"><i class="fas fa-arrow-left"></i> Back to Resources Hub</a>
