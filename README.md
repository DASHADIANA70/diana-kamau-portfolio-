<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Diana Kamau | Product & Visual Designer</title>
<style>
:root {
  --blue: #295689;
  --ivory: #FBF9F0;
  --dark: #14355A;
  --accent: #F7BB3B;
}
* {
  box-sizing: border-box;
  margin: 0; padding: 0;
}
body {
  font-family: 'Rubik', sans-serif;
  background: var(--ivory);
  color: var(--dark);
  line-height: 1.6;
  scroll-behavior: smooth;
}

/* NAVIGATION */
nav {
  background: var(--blue);
  display: flex;
  justify-content: center;
  padding: 15px;
  position: sticky;
  top: 0;
  z-index: 100;
}
nav a {
  color: var(--ivory);
  text-decoration: none;
  margin: 0 16px;
  font-weight: 500;
}
nav a:hover {
  color: var(--accent);
}

/* HERO */
header {
  text-align: center;
  padding: 100px 20px 60px;
}
header h1 {
  font-size: 2.8rem;
  color: var(--dark);
}
header p {
  font-size: 1.2rem;
  color: var(--blue);
  margin: 10px 0 25px;
}
.btn {
  display: inline-block;
  background: var(--blue);
  color: var(--ivory);
  padding: 12px 28px;
  border-radius: 30px;
  text-decoration: none;
  transition: background 0.3s ease;
}
.btn:hover { background: var(--dark); }

/* PROJECTS */
section {
  max-width: 1100px;
  margin: auto;
  padding: 60px 20px;
}
h2.section-title {
  text-align: center;
  font-size: 2rem;
  border-bottom: 2px solid var(--blue);
  display: inline-block;
  margin-bottom: 40px;
}
.projects {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
  gap: 25px;
}
.card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 6px 16px rgba(0,0,0,0.1);
  overflow: hidden;
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.6s ease;
}
.card.visible {
  opacity: 1;
  transform: translateY(0);
}
.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
}
.card-body {
  padding: 20px;
}
.card-body h3 {
  color: var(--dark);
  margin-bottom: 10px;
}
.card-body p {
  color: var(--blue);
  font-size: 0.95rem;
  margin-bottom: 10px;
}
.card-body button {
  background: var(--blue);
  color: var(--ivory);
  border: none;
  padding: 10px 18px;
  border-radius: 20px;
  cursor: pointer;
  font-weight: 500;
}
.card-body button:hover {
  background: var(--dark);
}

/* MODAL */
.modal {
  display: none;
  position: fixed;
  z-index: 200;
  left: 0; top: 0;
  width: 100%; height: 100%;
  overflow-y: auto;
  background: rgba(0,0,0,0.6);
}
.modal-content {
  background: var(--ivory);
  margin: 80px auto;
  padding: 30px;
  border-radius: 10px;
  max-width: 800px;
  animation: fadeIn 0.4s ease;
}
@keyframes fadeIn { from {opacity: 0;} to {opacity: 1;} }
.close {
  color: var(--dark);
  float: right;
  font-size: 24px;
  font-weight: bold;
  cursor: pointer;
}
.close:hover { color: var(--accent); }

/* ABOUT */
.about {
  background: var(--blue);
  color: var(--ivory);
  text-align: center;
  padding: 80px 20px;
}
.about h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}
.about p {
  max-width: 700px;
  margin: 10px auto;
}

/* CONTACT */
footer {
  background: var(--dark);
  color: var(--ivory);
  text-align: center;
  padding: 60px 20px;
}
footer a {
  color: var(--accent);
  text-decoration: none;
}
footer a:hover {
  text-decoration: underline;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  header h1 { font-size: 2.2rem; }
  h2.section-title { font-size: 1.6rem; }
}
</style>
</head>

<body>

<nav>
  <a href="#projects">Work</a>
  <a href="#about">About</a>
  <a href="#contact">Contact</a>
</nav>

<header>
  <h1>DIANA KAMAU</h1>
  <p>Product & Visual Designer</p>
  <p>Blending creativity and usability to craft human-centered digital experiences.</p>
  <a href="#projects" class="btn">View My Work</a>
</header>

<section id="projects">
  <h2 class="section-title">Selected Projects</h2>
  <div class="projects">

    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2017/08/30/07/51/website-2696489_1280.jpg" alt="HAYDN Project">
      <div class="card-body">
        <h3>HAYDN — Brand & UI System</h3>
        <p>Collaborative visual identity defining brand colors, typography, and digital UI.</p>
        <button onclick="openModal('haydnModal')">Read More</button>
      </div>
    </div>

    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2016/11/19/14/00/web-1833038_1280.jpg" alt="Osiepe Portal">
      <div class="card-body">
        <h3>Osiepe Savings Group Portal</h3>
        <p>UX/UI case study improving transparency in community savings systems.</p>
        <button onclick="openModal('osiepeModal')">Read More</button>
      </div>
    </div>

    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2015/09/05/22/46/id-924887_1280.jpg" alt="Student ID Design">
      <div class="card-body">
        <h3>Student ID Card Design</h3>
        <p>Graphic design exploration focused on layout, color harmony, and branding.</p>
        <button onclick="openModal('idModal')">Read More</button>
      </div>
    </div>

    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2015/01/08/18/27/ux-593357_1280.jpg" alt="UX Research">
      <div class="card-body">
        <h3>UX Research Case Study</h3>
        <p>Understanding how students manage group projects to improve teamwork.</p>
        <button onclick="openModal('uxModal')">Read More</button>
      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="about">
  <h2>About Me</h2>
  <p>Hi, I’m <strong>Diana Kamau</strong> — a Product & Visual Designer based in Nairobi, Kenya. I combine UX research, design thinking, and visual systems to craft intuitive, human-centered experiences.</p>
  <p>Skilled in Figma, Canva, Photoshop, and UI prototyping for both web and mobile. I studied Computer Science at The Co-operative University of Kenya and Product Design at Moringa School.</p>
</section>

<!-- CONTACT -->
<footer id="contact">
  <h2>Let’s Connect</h2>
  <p>📧 <a href="mailto:wanguidiana075@gmail.com">wanguidiana075@gmail.com</a></p>
  <p>🔗 <a href="http://www.linkedin.com/in/diana-wangui-59aba1352" target="_blank">LinkedIn Profile</a></p>
  <p>📍 Nairobi, Kenya</p>
  <p style="margin-top:20px;">© 2025 | Designed by <strong>Diana Kamau</strong></p>
</footer>

<!-- MODALS -->
<div id="haydnModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('haydnModal')">&times;</span>
    <h2>HAYDN — Brand & UI System</h2>
    <p><strong>Problem:</strong> HAYDN needed a visual identity that could scale from marketing to UI design while staying approachable.</p>
    <p><strong>Research:</strong> Analyzed competitor brands and user tone preferences. Key insight: people trust simplicity and contrast.</p>
    <p><strong>Solution:</strong> Created a cohesive color palette led by Nomus Blue, defined typography, and built UI mockups in Figma.</p>
    <p><strong>Outcome:</strong> Delivered a complete style guide and responsive screens for handoff.</p>
  </div>
</div>

<div id="osiepeModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('osiepeModal')">&times;</span>
    <h2>Osiepe Savings Group Portal</h2>
    <p><strong>Problem:</strong> Savings groups lacked transparent, easy-to-access financial records.</p>
    <p><strong>Research:</strong> Conducted user interviews and surveys to find common frustrations and feature gaps.</p>
    <p><strong>Solution:</strong> Designed a dashboard that summarizes member savings, transactions, and notifications.</p>
    <p><strong>Outcome:</strong> The design improved trust and clarity; received 86% in project evaluation.</p>
  </div>
</div>

<div id="idModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('idModal')">&times;</span>
    <h2>Student ID Card Design</h2>
    <p><strong>Goal:</strong> Create a clean, modern ID card design for The Co-operative University of Kenya.</p>
    <p><strong>Process:</strong> Studied existing layouts, applied a modular grid, and used vector icons for clarity.</p>
    <p><strong>Outcome:</strong> A professional, print-ready ID card emphasizing readability and balance.</p>
  </div>
</div>

<div id="uxModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('uxModal')">&times;</span>
    <h2>UX Research Case Study</h2>
    <p><strong>Goal:</strong> Investigate how students coordinate group assignments to improve accountability.</p>
    <p><strong>Method:</strong> Conducted 5 interviews and 20 survey responses; synthesized data via affinity mapping.</p>
    <p><strong>Findings:</strong> Students use WhatsApp but struggle with task ownership and deadlines.</p>
    <p><strong>Recommendations:</strong> Introduce shared task boards and automated reminders for group projects.</p>
  </div>
</div>

<script>
// Scroll animation for cards
const cards = document.querySelectorAll('.card');
const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
},{threshold:0.1});
cards.forEach(card=>observer.observe(card));

// Modal functions
function openModal(id){document.getElementById(id).style.display='block';}
function closeModal(id){document.getElementById(id).style.display='none';}
window.onclick=function(e){
  document.querySelectorAll('.modal').forEach(m=>{
    if(e.target==m){m.style.display='none';}
  });
};
</script>

</body>
</html>
