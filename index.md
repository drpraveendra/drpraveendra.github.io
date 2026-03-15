---
layout: default
---

<style>
  /* Core Styles */
  .profile-header {
    display: flex;
    align-items: center;
    gap: 30px;
    padding: 40px 20px;
    background: linear-gradient(135deg, #ffffff 0%, #f0f4f8 100%);
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.05);
    margin-bottom: 40px;
  }
  .profile-info h1 {
    font-size: 2.8rem;
    margin-bottom: 10px;
    background: linear-gradient(90deg, #1e3c72, #2a5298, #ff4b2b);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: 800;
  }
  .designation {
    font-size: 1.1rem;
    color: #444;
    line-height: 1.6;
    border-left: 4px solid #ff4b2b;
    padding-left: 15px;
  }
  
 /* Buttons */
  .hero-links {
    margin-top: 25px;
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }
  .hero-links a {
    padding: 10px 20px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.9rem;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 8px;
    border: 2px solid #ddd;
    background: white;
    color: #333;
  }
  .hero-links a:hover {
    transform: translateY(-3px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.15);
  }
  .hero-links a.email-btn       { border-color: #555; color: #555; }
  .hero-links a.email-btn:hover { background: #555; color: white; }

  .hero-links a.scholar-btn       { border-color: #4285F4; color: #4285F4; }
  .hero-links a.scholar-btn:hover { background: #4285F4; color: white; }

  .hero-links a.rgate-btn       { border-color: #40BA9B; color: #40BA9B; }
  .hero-links a.rgate-btn:hover { background: #40BA9B; color: white; }

  .hero-links a.youtube-btn       { border-color: #ff0000; color: #ff0000; }
  .hero-links a.youtube-btn:hover { background: #ff0000; color: white; }

  .hero-links a.telegram-btn       { border-color: #0088cc; color: #0088cc; }
  .hero-links a.telegram-btn:hover { background: #0088cc; color: white; }

  .hero-links a.instagram-btn       { border-color: #e1306c; color: #e1306c; }
  .hero-links a.instagram-btn:hover { background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888); color: white; border-color: transparent; }

  /* Grids & Cards */
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }
  .card {
    padding: 25px;
    border-radius: 15px;
    background: white;
    border-top: 5px solid #1e3c72;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    transition: transform 0.3s;
    text-align: center;
  }
  .card:hover { transform: translateY(-8px); }
  .card i { font-size: 2rem; margin-bottom: 15px; }
  
  .card:nth-child(1) { border-top-color: #ff4b2b; color: #ff4b2b; }
  .card:nth-child(2) { border-top-color: #1e3c72; color: #1e3c72; }
  .card:nth-child(3) { border-top-color: #00b894; color: #00b894; }
  .card:nth-child(4) { border-top-color: #0984e3; color: #0984e3; }
  
  .card h3 { color: #333; margin-top: 10px; }
  .card p { color: #666; font-size: 0.9rem; }

  /* Navigation */
  .nav-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 15px;
    margin-top: 30px;
  }
  .nav-card {
    background: #f8f9fa;
    padding: 20px;
    border-radius: 12px;
    text-align: center;
    font-weight: 600;
    color: #1e3c72;
    transition: all 0.3s;
    border: 1px solid transparent;
  }
  .nav-card:hover {
    background: #1e3c72;
    color: white !important;
    transform: scale(1.05);
  }
  .nav-grid a { text-decoration: none; }

  /* Specific Sections */
  .pub-card {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 15px;
    border-left: 5px solid #ff4b2b;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }
  .tools-badge {
    display: inline-block;
    padding: 8px 15px;
    margin: 5px;
    background: #e9ecef;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: 500;
    color: #495057;
  }
</style>

<div class="profile-header">
  <img src="/assets/images/profile1.png" class="profile-img" style="width: 200px; border-radius: 50%; border: 5px solid white; box-shadow: 0 5px 15px rgba(0,0,0,0.1);">
  <div class="profile-info">
    <h1>Dr. Praveendra Singh</h1>
    <p class="designation">
      Assistant Professor of Mathematics<br>
      Government College Kherwara, Rajasthan, India
    </p>

<div class="hero-links">
  <a href="mailto:drpraveendra.singh@gmail.com" class="email-btn"><i class="fas fa-envelope"></i> Email</a>
  <a href="#" class="scholar-btn" target="_blank"><i class="fas fa-graduation-cap"></i> Google Scholar</a>
  <a href="#" class="rgate-btn" target="_blank"><i class="fas fa-flask"></i> ResearchGate</a>
  <a href="https://www.youtube.com/@FractalFrontierMaths" class="youtube-btn" target="_blank"><i class="fab fa-youtube"></i> Fractal Frontier Maths</a>
  <a href="https://t.me/fractalfrontiermaths" class="telegram-btn" target="_blank"><i class="fab fa-telegram-plane"></i> Telegram</a>
  <a href="https://www.instagram.com/mathsworld007" class="instagram-btn" target="_blank"><i class="fab fa-instagram"></i> Instagram</a>
</div>
</div>
</div>

---

## 👨‍🏫 About Me
I am an **Assistant Professor of Mathematics** specializing in **inventory control, supply chain optimization, and metaheuristic algorithms**. Alongside my academic research into nature-inspired optimization techniques, I am deeply passionate about making higher mathematics accessible to B.Sc. and M.Sc. students, as well as those preparing for competitive exams like CSIR NET, GATE, and IIT JAM.

---

## 🔬 Research Areas

<div class="card-grid">
  <div class="card">
    <i class="fas fa-box"></i>
    <h3>Inventory Control</h3>
    <p>Mathematical models for deteriorating items and optimal policies.</p>
  </div>
  <div class="card">
    <i class="fas fa-truck"></i>
    <h3>Supply Chain</h3>
    <p>Optimization of production and distribution systems.</p>
  </div>
  <div class="card">
    <i class="fas fa-brain"></i>
    <h3>Metaheuristics</h3>
    <p>Differential Evolution, Bat Algorithm and hybrid methods.</p>
  </div>
  <div class="card">
    <i class="fas fa-leaf"></i>
    <h3>Sustainability</h3>
    <p>Integration of green practices in supply chain models.</p>
  </div>
</div>

---

## 💻 Computational Tools & Skills
Mathematics today is heavily supported by computation. I actively utilize various tools for research modeling and creating engaging educational content.
<br><br>
<span class="tools-badge"><i class="fab fa-python"></i> Python</span>
<span class="tools-badge"><i class="fas fa-shapes"></i> Manim (Mathematical Animations)</span>
<span class="tools-badge"><i class="fas fa-chart-line"></i> Scilab</span>
<span class="tools-badge"><i class="fas fa-file-code"></i> LaTeX</span>

---

## 📚 Featured Publications

<div class="pub-card">
  <strong>Singh, P. & Jain, M. (2025)</strong><br>
  Intelligent optimization and inventory control of deteriorating items <br>
  <em>Knowledge and Information Systems</em>
</div>

<div class="pub-card">
  <strong>Jain, M. & Singh, P. (2024)</strong><br>
  Pricing and preservation strategy for inventory models <br>
  <em>Soft Computing</em>
</div>

---

## 🧭 Explore the Website

<div class="nav-grid">
  <a href="about"><div class="nav-card"><i class="fas fa-user"></i><br>About</div></a>
  <a href="research"><div class="nav-card"><i class="fas fa-flask"></i><br>Research</div></a>
  <a href="publications"><div class="nav-card"><i class="fas fa-book"></i><br>Publications</div></a>
  <a href="teaching"><div class="nav-card"><i class="fas fa-chalkboard-teacher"></i><br>Teaching</div></a>
  <a href="resources"><div class="nav-card"><i class="fas fa-file-pdf"></i><br>Notes & PDFs</div></a>
  <a href="videos"><div class="nav-card"><i class="fas fa-video"></i><br>Video Lectures</div></a>
  <a href="blog"><div class="nav-card"><i class="fas fa-pen"></i><br>Blog</div></a>
  <a href="contact"><div class="nav-card"><i class="fas fa-envelope"></i><br>Contact</div></a>
</div>

---

## ✍️ Latest Blog Post
{% for post in site.posts limit:1 %}
### [{{ post.title }}]({{ post.url }})
*{{ post.date | date: "%B %d, %Y" }}*
{% endfor %}
