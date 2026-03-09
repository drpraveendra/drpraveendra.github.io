<div class="profile-header">

<img src="/assets/images/profile1.png" class="profile-img">

<div class="profile-info">

<h1>Dr. Praveendra Singh</h1>

<p class="designation">
Assistant Professor<br>
Department of Mathematics<br>
Government College Kherwara<br>
Rajasthan, India
</p>

</div>

</div>
</p>

<div class="hero-links">

<a href="mailto:drpraveendra.singh@gmail.com">
<i class="fas fa-envelope"></i> Email
</a>

<a href="#">
<i class="fas fa-graduation-cap"></i> Google Scholar
</a>

<a href="#">
<i class="fab fa-orcid"></i> ORCID
</a>

<a href="#">
<i class="fab fa-researchgate"></i> ResearchGate
</a>

</div>

</div>

</div>

---

## About Me

I am an **Assistant Professor of Mathematics** specializing in **inventory control, supply chain optimization, and metaheuristic algorithms**.

My research focuses on **nature-inspired optimization techniques for real-world decision systems involving deteriorating inventory and sustainable supply chains.**

---

## Research Areas

<div class="card-grid">

<div class="card">

<i class="fas fa-box"></i>

<h3>Inventory Control</h3>

Mathematical models for deteriorating items and optimal policies.

</div>

<div class="card">

<i class="fas fa-truck"></i>

<h3>Supply Chain Systems</h3>

Optimization of production and distribution systems.

</div>

<div class="card">

<i class="fas fa-brain"></i>

<h3>Metaheuristic Algorithms</h3>

Differential Evolution, Bat Algorithm, and hybrid optimization methods.

</div>

<div class="card">

<i class="fas fa-leaf"></i>

<h3>Sustainable Systems</h3>

Sustainability integration in supply chain decision models.

</div>

</div>

---

## Featured Publications

<div class="pub-card">

<strong>Singh, P. & Jain, M. (2025)</strong>
Intelligent optimization and inventory control of deteriorating items <em>Knowledge and Information Systems</em>

</div>

<div class="pub-card">

<strong>Jain, M. & Singh, P. (2024)</strong>
Pricing and preservation strategy for inventory models <em>Soft Computing</em>

</div>

---

## Explore the Website

<div class="nav-grid">

<a href="about">
<div class="nav-card">
<i class="fas fa-user"></i> About
</div>
</a>

<a href="research">
<div class="nav-card">
<i class="fas fa-flask"></i> Research
</div>
</a>

<a href="publications">
<div class="nav-card">
<i class="fas fa-book"></i> Publications
</div>
</a>

<a href="teaching">
<div class="nav-card">
<i class="fas fa-chalkboard-teacher"></i> Teaching
</div>
</a>

<a href="resources">
<div class="nav-card">
<i class="fas fa-square-root-variable"></i> Math Resources
</div>
</a>

<a href="videos">
<div class="nav-card">
<i class="fas fa-video"></i> Lecture Videos
</div>
</a>

<a href="projects">
<div class="nav-card">
<i class="fas fa-diagram-project"></i> Projects
</div>
</a>

<a href="blog">
<div class="nav-card">
<i class="fas fa-pen"></i> Blog
</div>
</a>

<a href="problems">
<div class="nav-card">
<i class="fas fa-infinity"></i> Problems
</div>
</a>

<a href="contact">
<div class="nav-card">
<i class="fas fa-envelope"></i> Contact
</div>
</a>

</div>

---

## Latest Blog Post

{% for post in site.posts limit:1 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%B %d, %Y" }}

{% endfor %}
