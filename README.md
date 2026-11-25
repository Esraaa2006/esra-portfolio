
<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#f6f4ec">
<meta name="description" content="Israa Al-Hetari — Cybersecurity and Networks student, creative thinker and aspiring developer.">
<title>Esraa Al-Hetari — Personal Portfolio</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=IBM+Plex+Sans+Arabic:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #f6f4ec;
  --surface: #fffefa;
  --olive: #596348;
  --olive-dark: #333d2d;
  --gold: #b39a6a;
  --text: #292e25;
  --muted: #77796e;
  --line: #e7e3d8;
  --soft: #eeede2;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 90px;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: "DM Sans", "IBM Plex Sans Arabic", sans-serif;
  line-height: 1.8;
  overflow-x: hidden;
}

body[dir="rtl"] {
  font-family: "IBM Plex Sans Arabic", sans-serif;
}

a {
  text-decoration: none;
  color: inherit;
}

button {
  font: inherit;
}

.container {
  width: min(1120px, 89%);
  margin-inline: auto;
}

::selection {
  background: var(--olive);
  color: white;
}

/* Navigation */

header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(246,244,236,.93);
  backdrop-filter: blur(14px);
  border-bottom: 1px solid var(--line);
}

nav {
  min-height: 78px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}

.logo {
  font-size: 21px;
  font-weight: 700;
  color: var(--olive);
  letter-spacing: -1px;
  white-space: nowrap;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 29px;
  list-style: none;
  font-size: 13px;
  font-weight: 500;
}

.nav-links a {
  transition: color .25s;
}

.nav-links a:hover {
  color: var(--gold);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.lang-btn {
  border: 1px solid var(--line);
  background: transparent;
  color: var(--olive);
  border-radius: 30px;
  padding: 8px 15px;
  cursor: pointer;
  font-size: 12px;
  font-weight: 700;
  transition: .3s;
}

.lang-btn:hover {
  background: var(--olive);
  color: white;
}

.menu-btn {
  display: none;
  border: 0;
  background: none;
  font-size: 24px;
  color: var(--olive);
  cursor: pointer;
}

/* Hero */

.hero {
  min-height: 650px;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding: 95px 0 80px;
}

.hero::before {
  content: "";
  position: absolute;
  width: 500px;
  height: 500px;
  border-radius: 50%;
  background: #e9e9dc;
  top: 65px;
  right: -180px;
  z-index: -1;
}

.hero::after {
  content: "";
  position: absolute;
  width: 230px;
  height: 230px;
  border: 1px solid #d8d1bd;
  border-radius: 50%;
  bottom: -130px;
  left: -60px;
  z-index: -1;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.3fr .7fr;
  align-items: center;
  gap: 65px;
}

.eyebrow {
  color: var(--gold);
  font-size: 11px;
  letter-spacing: 3px;
  font-weight: 700;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.hero h1 {
  font-size: clamp(42px, 6.5vw, 76px);
  line-height: 1.12;
  letter-spacing: -3px;
  margin-bottom: 22px;
  font-weight: 600;
}

.hero h1 span {
  display: block;
  color: var(--olive);
}

.hero-description {
  max-width: 550px;
  color: var(--muted);
  font-size: 16px;
  margin-bottom: 30px;
}

.hero-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 13px;
}

.btn {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  gap: 9px;
  padding: 12px 25px;
  border-radius: 40px;
  font-size: 13px;
  font-weight: 600;
  transition: .3s;
  cursor: pointer;
}

.btn-primary {
  background: var(--olive);
  color: white;
}

.btn-primary:hover {
  background: var(--olive-dark);
  transform: translateY(-3px);
}

.btn-outline {
  border: 1px solid var(--olive);
  color: var(--olive);
}

.btn-outline:hover {
  background: var(--olive);
  color: white;
}

.hero-visual {
  display: flex;
  justify-content: center;
  align-items: center;
}

.profile-art {
  width: 290px;
  height: 350px;
  background: var(--olive);
  border-radius: 145px 145px 12px 12px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 18px 18px 0 #e4dfd0;
  overflow: hidden;
}

.profile-art::before,
.profile-art::after {
  content: "";
  position: absolute;
  border: 1px solid rgba(255,255,255,.25);
  border-radius: 50%;
}

.profile-art::before {
  width: 250px;
  height: 250px;
}

.profile-art::after {
  width: 190px;
  height: 190px;
}

.initials {
  font-family: "DM Sans", sans-serif;
  font-size: 91px;
  font-weight: 500;
  color: #f6f4ec;
  letter-spacing: -8px;
  z-index: 1;
}

.art-label {
  position: absolute;
  bottom: 25px;
  color: #e4ddc8;
  font-size: 10px;
  letter-spacing: 3px;
  z-index: 2;
}

.hero-caption {
  margin-top: 48px;
  font-size: 11px;
  letter-spacing: 3px;
  color: var(--gold);
}

/* General sections */

section {
  padding: 100px 0;
}

.section-top {
  margin-bottom: 45px;
}

.section-label {
  color: var(--gold);
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 3px;
  margin-bottom: 10px;
}

.section-title {
  font-size: clamp(29px, 4vw, 42px);
  font-weight: 600;
  letter-spacing: -1px;
}

.section-title span {
  color: var(--olive);
}

.section-description {
  color: var(--muted);
  max-width: 600px;
  font-size: 14px;
  margin-top: 12px;
}

/* About */

.about {
  background: var(--surface);
}

.about-grid {
  display: grid;
  grid-template-columns: 1.2fr .8fr;
  gap: 65px;
  align-items: center;
}

.about-copy p {
  color: var(--muted);
  font-size: 15px;
  margin-bottom: 17px;
}

.about-note {
  background: var(--olive);
  color: white;
  padding: 38px;
  border-radius: 4px 45px 4px 45px;
}

.about-note .quote-mark {
  font-family: Georgia, serif;
  color: #d5c49b;
  font-size: 55px;
  line-height: 1;
}

.about-note h3 {
  font-size: 22px;
  margin: 12px 0;
}

.about-note p {
  font-size: 13px;
  color: #e1e3d7;
}

/* Focus */

.focus {
  background: var(--bg);
}

.focus-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

.focus-card {
  background: var(--surface);
  border: 1px solid var(--line);
  padding: 29px;
  transition: .3s;
}

.focus-card:hover {
  transform: translateY(-6px);
  border-color: var(--gold);
}

.card-icon {
  font-size: 26px;
  color: var(--gold);
  margin-bottom: 15px;
}

.focus-card h3 {
  font-size: 17px;
  margin-bottom: 8px;
}

.focus-card p {
  color: var(--muted);
  font-size: 13px;
}

/* Skills */

.skills {
  background: var(--surface);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}

.skill-item {
  padding: 22px 24px;
  border: 1px solid var(--line);
  background: var(--bg);
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  transition: .3s;
}

.skill-item:hover {
  border-color: var(--gold);
  transform: translateY(-3px);
}

.skill-name {
  font-size: 14px;
  font-weight: 600;
}

.skill-type {
  font-size: 10px;
  color: var(--gold);
  letter-spacing: 1px;
  white-space: nowrap;
}

/* Projects */

.projects {
  background: var(--bg);
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 22px;
}

.project-card {
  background: var(--surface);
  border: 1px solid var(--line);
  padding: 32px;
  transition: .3s;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 35px rgba(45,50,35,.06);
}

.project-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 25px;
}

.project-number {
  font-size: 11px;
  letter-spacing: 2px;
  color: var(--gold);
  font-weight: 700;
}

.project-symbol {
  width: 45px;
  height: 45px;
  background: var(--soft);
  border-radius: 50%;
  display: grid;
  place-items: center;
  color: var(--olive);
  font-size: 20px;
}

.project-card h3 {
  font-size: 21px;
  margin-bottom: 10px;
}

.project-card p {
  font-size: 13px;
  color: var(--muted);
  margin-bottom: 22px;
}

.project-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}

.project-tag {
  font-size: 10px;
  color: var(--olive);
  letter-spacing: 1px;
  font-weight: 700;
}

.project-link {
  color: var(--gold);
  font-size: 12px;
  font-weight: 700;
}

/* Learning */

.learning {
  background: var(--surface);
}

.learning-box {
  border: 1px solid var(--line);
  padding: 34px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 25px;
  background: var(--bg);
}

.learning-box h3 {
  font-size: 19px;
  margin-bottom: 7px;
}

.learning-box p {
  color: var(--muted);
  font-size: 13px;
}

.learning-status {
  border: 1px solid var(--gold);
  color: var(--olive);
  border-radius: 30px;
  padding: 8px 16px;
  font-size: 11px;
  white-space: nowrap;
}

/* Contact */

.contact {
  background: var(--olive-dark);
  color: white;
  text-align: center;
}

.contact .section-label {
  color: #d4c19a;
}

.contact .section-title {
  color: white;
}

.contact .section-title span {
  color: #d8c7a3;
}

.contact .section-description {
  color: #d7dbd0;
  margin: 14px auto 28px;
}

.contact .btn {
  background: var(--bg);
  color: var(--olive-dark);
}

.contact .btn:hover {
  transform: translateY(-3px);
  background: white;
}

.email {
  display: block;
  direction: ltr;
  font-size: 14px;
  color: #e1d2b2;
  margin-top: 22px;
}

/* Footer */

footer {
  background: #252b22;
  color: #d2d1c7;
  padding: 24px 0;
}

.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  font-size: 11px;
}

.footer-brand {
  font-weight: 700;
  letter-spacing: 1px;
}

/* Scroll reveal */

.reveal {
  opacity: 0;
  transform: translateY(22px);
  transition: opacity .7s ease, transform .7s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Arabic mode */

body[dir="rtl"] .hero h1 {
  letter-spacing: 0;
  line-height: 1.45;
}

body[dir="rtl"] .section-title {
  letter-spacing: 0;
}

body[dir="rtl"] .eyebrow,
body[dir="rtl"] .section-label,
body[dir="rtl"] .project-number,
body[dir="rtl"] .skill-type,
body[dir="rtl"] .project-tag {
  letter-spacing: 1px;
}

/* Mobile */

@media(max-width: 850px) {
  .hero-grid {
    grid-template-columns: 1fr;
    gap: 55px;
  }

  .hero-visual {
    order: -1;
  }

  .profile-art {
    width: 230px;
    height: 280px;
  }

  .initials {
    font-size: 75px;
  }

  .hero {
    text-align: center;
    padding-top: 65px;
  }

  .hero-description {
    margin-inline: auto;
  }

  .hero-buttons {
    justify-content: center;
  }

  .hero-caption {
    text-align: center;
  }

  .about-grid {
    grid-template-columns: 1fr;
  }

  .focus-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media(max-width: 650px) {
  nav {
    min-height: 68px;
  }

  .menu-btn {
    display: block;
  }

  .nav-links {
    display: none;
    position: absolute;
    top: 68px;
    left: 0;
    right: 0;
    padding: 25px 6%;
    background: var(--surface);
    border-bottom: 1px solid var(--line);
    flex-direction: column;
    align-items: flex-start;
    gap: 17px;
  }

  .nav-links.open {
    display: flex;
  }

  .hero h1 {
    font-size: 48px;
  }

  section {
    padding: 72px 0;
  }

  .focus-grid,
  .skills-grid,
  .project-grid {
    grid-template-columns: 1fr;
  }

  .learning-box {
    align-items: flex-start;
    flex-direction: column;
  }

  .footer-inner {
    flex-direction: column;
    text-align: center;
  }
}

@media(prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    scroll-behavior: auto !important;
    animation-duration: .01ms !important;
    transition-duration: .01ms !important;
  }
}
</style>
</head>

<body>

<header>
  <div class="container">
    <nav>
      <a href="#home" class="logo">ISRAA.</a>

      <ul class="nav-links" id="navLinks">
        <li><a href="#home" data-i18n="navHome">Home</a></li>
        <li><a href="#about" data-i18n="navAbout">About</a></li>
        <li><a href="#focus" data-i18n="navFocus">Interests</a></li>
        <li><a href="#skills" data-i18n="navSkills">Skills</a></li>
        <li><a href="#projects" data-i18n="navProjects">Projects</a></li>
        <li><a href="#contact" data-i18n="navContact">Contact</a></li>
      </ul>

      <div class="nav-actions">
        <button class="lang-btn" id="langToggle" type="button" aria-label="Switch language">العربية</button>
        <button class="menu-btn" id="menuBtn" type="button" aria-label="Open menu">☰</button>
      </div>
    </nav>
  </div>
</header>

<main>

<section class="hero" id="home">
  <div class="container">
    <div class="hero-grid">

      <div class="hero-content reveal">
        <div class="eyebrow" data-i18n="eyebrow">PERSONAL PORTFOLIO · 2026</div>

        <h1>
          <span data-i18n="heroHello">Hello, I'm</span>
          <span>Israa Al-Hetari.</span>
        </h1>

        <p class="hero-description" data-i18n="heroDesc">
          Cybersecurity and Networks student with a passion for technology, creativity and continuous learning. Exploring the digital world one project at a time.
        </p>

        <div class="hero-buttons">
          <a href="#projects" class="btn btn-primary" data-i18n="heroButton">Explore my work ↗</a>
          <a href="#contact" class="btn btn-outline" data-i18n="heroContact">Get in touch</a>
        </div>

        <div class="hero-caption" data-i18n="heroCaption">
          LEARN · CREATE · GROW
        </div>
      </div>

      <div class="hero-visual reveal">
        <div class="profile-art" aria-label="Israa monogram">
          <div class="initials">IH.</div>
          <div class="art-label">ISRAA AL-HETARI</div>
        </div>
      </div>

    </div>
  </div>
</section>

<section class="about" id="about">
  <div class="container">
    <div class="section-top reveal">
      <div class="section-label" data-i18n="aboutLabel">01 — ABOUT ME</div>
      <h2 class="section-title" data-i18n="aboutTitle">A little about <span>my journey.</span></h2>
    </div>

    <div class="about-grid">
      <div class="about-copy reveal">
        <p data-i18n="aboutP1">
          I'm Israa Al-Hetari, a Cybersecurity and Networks student interested in technology, web development and digital creativity.
        </p>
        <p data-i18n="aboutP2">
          I enjoy exploring new tools, learning practical skills and turning ideas into digital projects. My journey is built around curiosity, consistency and a willingness to grow.
        </p>
        <p data-i18n="aboutP3">
          My goal is to keep developing my technical knowledge and creative perspective while building a meaningful career in technology.
        </p>
      </div>

      <div class="about-note reveal">
        <div class="quote-mark">“</div>
        <h3 data-i18n="quoteTitle">Curiosity leads to growth.</h3>
        <p data-i18n="quoteDesc">
          Every new skill is another step toward becoming the person I aspire to be.
        </p>
      </div>
    </div>
  </div>
</section>

<section class="focus" id="focus">
  <div class="container">
    <div class="section-top reveal">
      <div class="section-label" data-i18n="focusLabel">02 — WHAT I EXPLORE</div>
      <h2 class="section-title" data-i18n="focusTitle">Areas of <span>interest.</span></h2>
      <p class="section-description" data-i18n="focusDesc">
        A combination of technical curiosity and creative expression.
      </p>
    </div>

    <div class="focus-grid">
      <article class="focus-card reveal">
        <div class="card-icon">⌘</div>
        <h3 data-i18n="focus1Title">Cybersecurity</h3>
        <p data-i18n="focus1Desc">Exploring information security, networks and digital protection.</p>
      </article>

      <article class="focus-card reveal">
        <div class="card-icon">⌨</div>
        <h3 data-i18n="focus2Title">Web Development</h3>
        <p data-i18n="focus2Desc">Learning how to build and structure useful websites.</p>
      </article>

      <article class="focus-card reveal">
        <div class="card-icon">✧</div>
        <h3 data-i18n="focus3Title">Creative Design</h3>
        <p data-i18n="focus3Desc">Creating visual experiences with thoughtful details.</p>
      </article>
    </div>
  </div>
</section>

<section class="skills" id="skills">
  <div class="container">
    <div class="section-top reveal">
      <div class="section-label" data-i18n="skillsLabel">03 — MY TOOLKIT</div>
      <h2 class="section-title" data-i18n="skillsTitle">Skills & <span>capabilities.</span></h2>
      <p class="section-description" data-i18n="skillsDesc">
        Skills I'm developing and tools I enjoy working with.
      </p>
    </div>

    <div class="skills-grid">
      <div class="skill-item reveal">
        <span class="skill-name">HTML</span>
        <span class="skill-type">WEB</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">CSS</span>
        <span class="skill-type">WEB</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">Programming Fundamentals</span>
        <span class="skill-type">TECH</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">Cybersecurity Fundamentals</span>
        <span class="skill-type">SECURITY</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">Microsoft Office</span>
        <span class="skill-type">PRODUCTIVITY</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">Content Creation</span>
        <span class="skill-type">CREATIVE</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">Photo & Video Editing</span>
        <span class="skill-type">CREATIVE</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">Digital Design</span>
        <span class="skill-type">DESIGN</span>
      </div>
      <div class="skill-item reveal">
        <span class="skill-name">English Communication</span>
        <span class="skill-type">LANGUAGE</span>
      </div>
    </div>
  </div>
</section>

<section class="projects" id="projects">
  <div class="container">
    <div class="section-top reveal">
      <div class="section-label" data-i18n="projectsLabel">04 — SELECTED WORK</div>
      <h2 class="section-title" data-i18n="projectsTitle">Projects & <span>experiments.</span></h2>
      <p class="section-description" data-i18n="projectsDesc">
        A growing collection of projects and practical learning experiences.
      </p>
    </div>

    <div class="project-grid">

      <article class="project-card reveal">
        <div class="project-top">
          <span class="project-number">PROJECT 01</span>
          <span class="project-symbol">⌘</span>
        </div>
        <h3 data-i18n="project1Title">Personal Portfolio</h3>
        <p data-i18n="project1Desc">
          A personal website showcasing my background, skills, interests and digital journey.
        </p>
        <div class="project-footer">
          <span class="project-tag">HTML · CSS · JAVASCRIPT</span>
          <a class="project-link" href="https://github.com/Esraaa2006/esra-portfolio" target="_blank" rel="noopener noreferrer" data-i18n="viewCode">View code ↗</a>
        </div>
      </article>

      <article class="project-card reveal">
        <div class="project-top">
          <span class="project-number">PROJECT 02</span>
          <span class="project-symbol">✧</span>
        </div>
        <h3 data-i18n="project2Title">Taif Tourism Website</h3>
        <p data-i18n="project2Desc">
          A web project introducing selected tourist attractions and destinations in Taif.
        </p>
        <div class="project-footer">
          <span class="project-tag">HTML · CSS · WEB DESIGN</span>
          <a class="project-link" href="https://github.com/Esraaa2006/final-project" target="_blank" rel="noopener noreferrer" data-i18n="viewCode">View code ↗</a>
        </div>
      </article>

    </div>
  </div>
</section>

<section class="learning" id="learning">
  <div class="container">
    <div class="section-top reveal">
      <div class="section-label" data-i18n="learningLabel">05 — CONTINUOUS GROWTH</div>
      <h2 class="section-title" data-i18n="learningTitle">Always <span>learning.</span></h2>
    </div>

    <div class="learning-box reveal">
      <div>
        <h3 data-i18n="learningHeading">Currently building my skills</h3>
        <p data-i18n="learningDesc">
          Developing my knowledge in cybersecurity, networking and web technologies through study and practical projects.
        </p>
      </div>
      <div class="learning-status" data-i18n="learningStatus">IN PROGRESS</div>
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="container">
    <div class="section-label" data-i18n="contactLabel">06 — GET IN TOUCH</div>
    <h2 class="section-title" data-i18n="contactTitle">Let's create something <span>meaningful.</span></h2>
    <p class="section-description" data-i18n="contactDesc">
      Open to learning opportunities, collaborations and meaningful connections.
    </p>

    <a class="btn" href="mailto:esraalhtary@gmail.com" data-i18n="contactButton">
      Send me an email ↗
    </a>

    <a class="email" href="mailto:esraalhtary@gmail.com">
      esraalhtary@gmail.com
    </a>
  </div>
</section>

</main>

<footer>
  <div class="container footer-inner">
    <div class="footer-brand">ESRAA AL-HETARI.</div>
    <div data-i18n="footerText">Designed with intention · © 2026</div>
  </div>
</footer>

<script>
const translations = {
  en: {
    title: "Esraa Al-Hetari — Personal Portfolio",
    description: "Israa Al-Hetari — Cybersecurity and Networks student, creative thinker and aspiring developer.",
    navHome: "Home",
    navAbout: "About",
    navFocus: "Interests",
    navSkills: "Skills",
    navProjects: "Projects",
    navContact: "Contact",
    eyebrow: "PERSONAL PORTFOLIO · 2026",
    heroHello: "Hello, I'm",
    heroDesc: "Cybersecurity and Networks student with a passion for technology, creativity and continuous learning. Exploring the digital world one project at a time.",
    heroButton: "Explore my work ↗",
    heroContact: "Get in touch",
    heroCaption: "LEARN · CREATE · GROW",
    aboutLabel: "01 — ABOUT ME",
    aboutTitle: 'A little about <span>my journey.</span>',
    aboutP1: "I'm Israa Al-Hetari, a Cybersecurity and Networks student interested in technology, web development and digital creativity.",
    aboutP2: "I enjoy exploring new tools, learning practical skills and turning ideas into digital projects. My journey is built around curiosity, consistency and a willingness to grow.",
    aboutP3: "My goal is to keep developing my technical knowledge and creative perspective while building a meaningful career in technology.",
    quoteTitle: "Curiosity leads to growth.",
    quoteDesc: "Every new skill is another step toward becoming the person I aspire to be.",
    focusLabel: "02 — WHAT I EXPLORE",
    focusTitle: 'Areas of <span>interest.</span>',
    focusDesc: "A combination of technical curiosity and creative expression.",
    focus1Title: "Cybersecurity",
    focus1Desc: "Exploring information security, networks and digital protection.",
    focus2Title: "Web Development",
    focus2Desc: "Learning how to build and structure useful websites.",
    focus3Title: "Creative Design",
    focus3Desc: "Creating visual experiences with thoughtful details.",
    skillsLabel: "03 — MY TOOLKIT",
    skillsTitle: 'Skills & <span>capabilities.</span>',
    skillsDesc: "Skills I'm developing and tools I enjoy working with.",
    projectsLabel: "04 — SELECTED WORK",
    projectsTitle: 'Projects & <span>experiments.</span>',
    projectsDesc: "A growing collection of projects and practical learning experiences.",
    project1Title: "Personal Portfolio",
    project1Desc: "A personal website showcasing my background, skills, interests and digital journey.",
    project2Title: "Taif Tourism Website",
    project2Desc: "A web project introducing selected tourist attractions and destinations in Taif.",
    viewCode: "View code ↗",
    learningLabel: "05 — CONTINUOUS GROWTH",
    learningTitle: 'Always <span>learning.</span>',
    learningHeading: "Currently building my skills",
    learningDesc: "Developing my knowledge in cybersecurity, networking and web technologies through study and practical projects.",
    learningStatus: "IN PROGRESS",
    contactLabel: "06 — GET IN TOUCH",
    contactTitle: 'Let\'s create something <span>meaningful.</span>',
    contactDesc: "Open to learning opportunities, collaborations and meaningful connections.",
    contactButton: "Send me an email ↗",
    footerText: "Designed with intention · © 2026"
  },

  ar: {
    title: "إسراء الهتاري — الموقع الشخصي",
    description: "الموقع الشخصي لإسراء الهتاري، طالبة الأمن السيبراني والشبكات.",
    navHome: "الرئيسية",
    navAbout: "نبذة عني",
    navFocus: "اهتماماتي",
    navSkills: "مهاراتي",
    navProjects: "مشاريعي",
    navContact: "تواصل معي",
    eyebrow: "الموقع الشخصي · ٢٠٢٦",
    heroHello: "مرحباً، أنا",
    heroDesc: "طالبة أمن سيبراني وشبكات، شغوفة بالتقنية والإبداع والتعلم المستمر. أستكشف العالم الرقمي مشروعاً بعد مشروع.",
    heroButton: "استكشف أعمالي ↗",
    heroContact: "تواصل معي",
    heroCaption: "تعلّم · ابتكر · تطوّر",
    aboutLabel: "٠١ — نبذة عني",
    aboutTitle: 'قليل من <span>رحلتي.</span>',
    aboutP1: "أنا إسراء الهتاري، طالبة في تخصص الأمن السيبراني والشبكات، أهتم بالتقنية وتطوير المواقع والإبداع الرقمي.",
    aboutP2: "أستمتع باستكشاف الأدوات الجديدة واكتساب المهارات العملية وتحويل الأفكار إلى مشاريع رقمية. تقوم رحلتي على الفضول والاستمرارية والرغبة في التطور.",
    aboutP3: "أطمح إلى تطوير معرفتي التقنية وتوسيع رؤيتي الإبداعية وبناء مسيرة مهنية مميزة في عالم التقنية.",
    quoteTitle: "الفضول يقود إلى التطور.",
    quoteDesc: "كل مهارة جديدة هي خطوة إضافية نحو الشخص الذي أطمح أن أكونه.",
    focusLabel: "٠٢ — مجالات أهتم بها",
    focusTitle: 'مساحات <span>استكشافي.</span>',
    focusDesc: "مزيج بين الفضول التقني والتعبير الإبداعي.",
    focus1Title: "الأمن السيبراني",
    focus1Desc: "استكشاف أمن المعلومات والشبكات والحماية الرقمية.",
    focus2Title: "تطوير المواقع",
    focus2Desc: "تعلم بناء المواقع الإلكترونية وتنظيم صفحاتها.",
    focus3Title: "التصميم الإبداعي",
    focus3Desc: "ابتكار تجارب بصرية بتفاصيل مدروسة.",
    skillsLabel: "٠٣ — أدواتي ومهاراتي",
    skillsTitle: 'مهاراتي <span>وقدراتي.</span>',
    skillsDesc: "مهارات أعمل على تطويرها وأدوات أستمتع باستخدامها.",
    projectsLabel: "٠٤ — أعمال مختارة",
    projectsTitle: 'مشاريعي <span>وتجاربي.</span>',
    projectsDesc: "مجموعة متنامية من المشاريع والتجارب التعليمية العملية.",
    project1Title: "الموقع الشخصي",
    project1Desc: "موقع شخصي يعرض خلفيتي ومهاراتي واهتماماتي ورحلتي في العالم الرقمي.",
    project2Title: "موقع سياحي عن الطائف",
    project2Desc: "مشروع ويب للتعريف بمجموعة من المعالم والوجهات السياحية في الطائف.",
    viewCode: "عرض الكود ↗",
    learningLabel: "٠٥ — التطور المستمر",
    learningTitle: 'دائماً في <span>مرحلة تعلم.</span>',
    learningHeading: "أعمل حالياً على تطوير مهاراتي",
    learningDesc: "أطوّر معرفتي في الأمن السيبراني والشبكات وتقنيات الويب من خلال الدراسة والمشاريع العملية.",
    learningStatus: "قيد التطوير",
    contactLabel: "٠٦ — لنتواصل",
    contactTitle: 'لنصنع شيئاً <span>ذا معنى.</span>',
    contactDesc: "أرحب بفرص التعلم والتعاون وبناء العلاقات المهنية الهادفة.",
    contactButton: "راسليني عبر البريد ↗",
    footerText: "صُمم بكل اهتمام · © ٢٠٢٦"
  }
};

let currentLang = "en";

const langToggle = document.getElementById("langToggle");
const menuBtn = document.getElementById("menuBtn");
const navLinks = document.getElementById("navLinks");

function setLanguage(lang) {
  currentLang = lang;

  document.documentElement.lang = lang;
  document.documentElement.dir = lang === "ar" ? "rtl" : "ltr";
  document.body.dir = lang === "ar" ? "rtl" : "ltr";

  document.title = translations[lang].title;
  document.querySelector('meta[name="description"]').content =
    translations[lang].description;

  document.querySelectorAll("[data-i18n]").forEach(element => {
    const key = element.dataset.i18n;
    if (translations[lang][key]) {
      element.innerHTML = translations[lang][key];
    }
  });

  langToggle.textContent = lang === "en" ? "العربية" : "English";
  langToggle.setAttribute(
    "aria-label",
    lang === "en" ? "Switch to Arabic" : "Switch to English"
  );

  localStorage.setItem("israa-portfolio-language", lang);
}

langToggle.addEventListener("click", () => {
  setLanguage(currentLang === "en" ? "ar" : "en");
});

menuBtn.addEventListener("click", () => {
  navLinks.classList.toggle("open");
  menuBtn.textContent = navLinks.classList.contains("open") ? "×" : "☰";
});

document.querySelectorAll(".nav-links a").forEach(link => {
  link.addEventListener("click", () => {
    navLinks.classList.remove("open");
    menuBtn.textContent = "☰";
  });
});

// Reveal sections as they enter the screen.
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.12 });

document.querySelectorAll(".reveal").forEach(element => {
  observer.observe(element);
});

// Restore the visitor's language preference.
const savedLanguage = localStorage.getItem("israa-portfolio-language");
setLanguage(savedLanguage === "ar" ? "ar" : "en");
</script>

</body>
</html>
