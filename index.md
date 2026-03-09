---
layout: default
---

<style>
  /* 1. Header & Typography */
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

  /* 2. Professional Animated Buttons */
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
    border: 1px solid #ddd;
    background: white;
    color: #333;
  }

  .hero-links a:hover {
    transform: translateY(-3px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    border-color: #1e3c72;
    color: #1e3c72;
  }

  /* 3. Colorful Research Cards */
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
  
  /* Different colors for cards */
  .card:nth-child(1) { border-top-color: #ff4b2b; color: #ff4b2b; }
  .card:nth-child(2) { border-top-color: #1e3c72; color: #1e3c72; }
  .card:nth-child(3) { border-top-color: #00b894; color: #00b894; }
  .card:nth-child(4) { border-top-color: #0984e3; color: #0984e3; }
  .card h3 { color: #333; margin-top: 10px; }
  .card p { color: #666; font-size: 0.9rem; }

  /* 4. Navigation Grid - Modern Look */
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

  /* 5. Publication Styling */
  .pub-card {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 15px;
    border-left: 5px solid #ff4b2b;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }
</style>

<div class="profile-header">
  <img src="/assets/images/profile1.png" class="profile-img" style="width: 200px; border-radius: 50%; border: 5px solid white; shadow: 0 5px 15px rgba(0,0,0,0.1);">
  <div class="profile-info">
    <h1>Dr. Praveendra Singh</h1>
    <p class="designation">
      Assistant Professor<br>
      Department of Mathematics<br>
      Government College Kherwara, Rajasthan, India
    </p>
    <div class="hero-links">
      <a href="mailto:drpraveendra.singh@gmail.com"><i class="fas fa-envelope"></i> Email</a>
      <a href="#"><i class="fas fa-graduation-cap"></i> Google Scholar</a>
      <a href="#"><i class="fab fa-orcid"></i> ORCID</a>
      <a href="#"><i class="fab fa-researchgate"></i> ResearchGate</a>
    </div>
  </div>
</div>

---

## 👋 About Me
I am an **Assistant Professor of Mathematics** specializing in **inventory control, supply chain optimization, and metaheuristic algorithms**. My research focus involves **nature-inspired optimization techniques** for real-world decision systems involving deteriorating inventory and sustainable supply chains.

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

## 🚀 Explore the Website

<div class="nav-grid">
  <a href="about"><div class="nav-card"><i class="fas fa-user"></i><br>About</div></a>
  <a href="research"><div class="nav-card"><i class="fas fa-flask"></i><br>Research</div></a>
  <a href="publications"><div class="nav-card"><i class="fas fa-book"></i><br>Publications</div></a>
  <a href="teaching"><div class="nav-card"><i class="fas fa-chalkboard-teacher"></i><br>Teaching</div></a>
  <a href="resources"><div class="nav-card"><i class="fas fa-square-root-variable"></i><br>Resources</div></a>
  <a href="videos"><div class="nav-card"><i class="fas fa-video"></i><br>Videos</div></a>
  <a href="blog"><div class="nav-card"><i class="fas fa-pen"></i><br>Blog</div></a>
  <a href="contact"><div class="nav-card"><i class="fas fa-envelope"></i><br>Contact</div></a>
</div>

---

## 📝 Latest Blog Post
{% for post in site.posts limit:1 %}
### [{{ post.title }}]({{ post.url }})
*{{ post.date | date: "%B %d, %Y" }}*
{% endfor %}
