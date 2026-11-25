# esra-portfolio


<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="الموقع الشخصي لإسراء الهتاري - طالبة الأمن السيبراني والشبكات ومهتمة بالتقنية والإبداع.">
  <title>Esraa Al-Hetari | Personal Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=IBM+Plex+Sans+Arabic:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --cream: #f7f5ee;
      --white: #fffefa;
      --olive: #586044;
      --dark: #292e25;
      --muted: #77796d;
      --gold: #b69a66;
      --line: #e7e3d8;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--cream);
      color: var(--dark);
      font-family: 'IBM Plex Sans Arabic', sans-serif;
      line-height: 1.8;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1100px, 90%);
      margin: auto;
    }

    /* Navigation */

    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(247,245,238,.92);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--line);
    }

    nav {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      font-family: 'DM Sans', sans-serif;
      font-size: 21px;
      font-weight: 700;
      direction: ltr;
      color: var(--olive);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
      list-style: none;
      font-size: 14px;
    }

    .nav-links a:hover {
      color: var(--gold);
    }

    .contact-nav {
      border: 1px solid var(--olive);
      padding: 8px 19px;
      border-radius: 30px;
      transition: .3s;
    }

    .contact-nav:hover {
      background: var(--olive);
      color: white;
    }

    /* Hero */

    .hero {
      min-height: 620px;
      display: flex;
      align-items: center;
      padding: 85px 0;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 430px;
      height: 430px;
      border-radius: 50%;
      background: #e9e8d9;
      left: -130px;
      top: 70px;
      z-index: -1;
    }

    .hero-content {
      max-width: 760px;
    }

    .eyebrow {
      color: var(--olive);
      font-family: 'DM Sans', sans-serif;
      font-size: 13px;
      letter-spacing: 3px;
      direction: ltr;
      text-align: right;
      margin-bottom: 18px;
    }

    .hero h1 {
      font-size: clamp(42px, 8vw, 76px);
      line-height: 1.25;
      font-weight: 600;
      margin-bottom: 20px;
    }

    .hero h1 span {
      color: var(--olive);
      font-family: 'DM Sans', sans-serif;
      direction: ltr;
      display: inline-block;
    }

    .hero p {
      color: var(--muted);
      max-width: 580px;
      font-size: 17px;
      margin-bottom: 32px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .btn {
      padding: 12px 27px;
      border-radius: 35px;
      font-size: 14px;
      font-weight: 600;
      transition: .3s;
      display: inline-block;
    }

    .btn-primary {
      background: var(--olive);
      color: white;
    }

    .btn-primary:hover {
      background: var(--dark);
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

    .hero-note {
      margin-top: 55px;
      color: var(--gold);
      font-family: 'DM Sans', sans-serif;
      font-size: 12px;
      letter-spacing: 2px;
      direction: ltr;
      text-align: right;
    }

    /* Sections */

    section {
      padding: 90px 0;
    }

    .section-heading {
      margin-bottom: 42px;
    }

    .section-heading small {
      color: var(--gold);
      font-family: 'DM Sans', sans-serif;
      letter-spacing: 3px;
      direction: ltr;
      display: block;
      text-align: right;
      margin-bottom: 8px;
    }

    .section-heading h2 {
      font-size: 36px;
      font-weight: 600;
    }

    .section-heading h2 span {
      color: var(--olive);
    }

    /* About */

    .about {
      background: var(--white);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 50px;
      align-items: center;
    }

    .about-text p {
      color: var(--muted);
      margin-bottom: 17px;
      font-size: 16px;
    }

    .about-card {
      background: var(--olive);
      color: white;
      padding: 38px;
      border-radius: 5px 55px 5px 55px;
    }

    .about-card .number {
      font-family: 'DM Sans', sans-serif;
      font-size: 55px;
      color: #e2d4ad;
      line-height: 1.3;
    }

    .about-card h3 {
      font-size: 21px;
      margin: 8px 0;
    }

    .about-card p {
      color: #e1e1d5;
      font-size: 14px;
    }

    /* Skills */

    .skills {
      background: var(--cream);
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .skill {
      background: var(--white);
      padding: 27px;
      border: 1px solid var(--line);
      transition: .3s;
    }

    .skill:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }

    .skill .icon {
      font-size: 26px;
      margin-bottom: 12px;
    }

    .skill h3 {
      font-size: 17px;
      margin-bottom: 7px;
    }

    .skill p {
      color: var(--muted);
      font-size: 13px;
    }

    /* Projects */

    .projects {
      background: var(--white);
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 22px;
    }

    .project {
      border: 1px solid var(--line);
      padding: 30px;
      transition: .3s;
      background: var(--cream);
    }

    .project:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 30px rgba(0,0,0,.05);
    }

    .project-number {
      color: var(--gold);
      font-family: 'DM Sans', sans-serif;
      font-size: 14px;
      direction: ltr;
    }

    .project h3 {
      margin: 13px 0 8px;
      font-size: 21px;
    }

    .project p {
      color: var(--muted);
      font-size: 14px;
    }

    .project-tag {
      display: inline-block;
      margin-top: 20px;
      color: var(--olive);
      font-family: 'DM Sans', sans-serif;
      font-size: 12px;
      direction: ltr;
    }

    /* Contact */

    .contact {
      background: var(--olive);
      color: white;
      text-align: center;
    }

    .contact .section-heading small {
      color: #d6c49b;
      text-align: center;
    }

    .contact .section-heading h2 {
      color: white;
    }

    .contact p {
      color: #e5e5da;
      margin-bottom: 28px;
    }

    .contact .btn {
      background: var(--cream);
      color: var(--olive);
    }

    .email {
      display: block;
      direction: ltr;
      font-family: 'DM Sans', sans-serif;
      font-size: 15px;
      margin-top: 22px;
      color: #e2d4ad;
    }

    /* Footer */

    footer {
      padding: 23px 0;
      background: var(--dark);
      color: #d4d3c9;
      text-align: center;
      font-size: 12px;
    }

    footer span {
      font-family: 'DM Sans', sans-serif;
      direction: ltr;
      display: inline-block;
    }

    /* Responsive */

    @media (max-width: 750px) {
      .nav-links {
        gap: 12px;
        font-size: 12px;
      }

      .contact-nav {
        display: none;
      }

      .hero {
        min-height: 540px;
      }

      .about-grid {
        grid-template-columns: 1fr;
      }

      .skills-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .project-grid {
        grid-template-columns: 1fr;
      }

      section {
        padding: 65px 0;
      }

      .section-heading h2 {
        font-size: 29px;
      }
    }

    @media (max-width: 430px) {
      .nav-links {
        gap: 9px;
        font-size: 11px;
      }

      .logo {
        font-size: 17px;
      }

      .skills-grid {
        grid-template-columns: 1fr;
      }

      .hero p {
        font-size: 15px;
      }
    }

    /* Smooth entrance */

    .hero-content,
    .section-heading,
    .about-grid,
    .skill,
    .project {
      animation: appear .8s ease both;
    }

    @keyframes appear {
      from {
        opacity: 0;
        transform: translateY(18px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="container">
      <nav>
        <a href="#home" class="logo">ESRAA.</a>

        <ul class="nav-links">
          <li><a href="#home">الرئيسية</a></li>
          <li><a href="#about">عني</a></li>
          <li><a href="#skills">مهاراتي</a></li>
          <li><a href="#projects">أعمالي</a></li>
        </ul>

        <a href="#contact" class="contact-nav">تواصلي معي</a>
      </nav>
    </div>
  </header>

  <main>

    <section class="hero" id="home">
      <div class="container">
        <div class="hero-content">
          <div class="eyebrow">WELCOME TO MY PORTFOLIO</div>

          <h1>
            مرحباً، أنا<br>
            <span>Esraa Al-Hetari.</span>
          </h1>

          <p>
            طالبة أمن سيبراني وشبكات، أؤمن بأن التقنية
            مساحة لا نهائية للتعلم والإبداع وصناعة الأفكار.
            أعمل على تطوير مهاراتي وبناء تجارب رقمية تجمع
            بين البساطة والابتكار.
          </p>

          <div class="hero-buttons">
            <a href="#projects" class="btn btn-primary">استكشف أعمالي</a>
            <a href="#about" class="btn btn-outline">تعرف عليّ</a>
          </div>

          <div class="hero-note">
            LEARN · CREATE · INSPIRE
          </div>
        </div>
      </div>
    </section>

    <section class="about" id="about">
      <div class="container">
        <div class="section-heading">
          <small>01 — ABOUT ME</small>
          <h2>قصة <span>طموح وشغف</span></h2>
        </div>

        <div class="about-grid">
          <div class="about-text">
            <p>
              أنا إسراء الهتاري، طالبة في تخصص الأمن السيبراني
              والشبكات، مهتمة بعالم التقنية والبرمجة والتصميم.
            </p>

            <p>
              أحب استكشاف الأدوات الرقمية وتعلم مهارات جديدة،
              وأستمتع بتحويل الأفكار إلى مشاريع عملية تجمع
              بين الجانب التقني واللمسة الإبداعية.
            </p>

            <p>
              أطمح إلى تطوير خبرتي باستمرار والمساهمة في
              بناء مستقبل رقمي أكثر ابتكاراً وأماناً.
            </p>
          </div>

          <div class="about-card">
            <div class="number">01.</div>
            <h3>Always learning</h3>
            <p>
              أؤمن أن كل تجربة جديدة هي فرصة لاكتساب معرفة
              ومهارة تقربني من أهدافي.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section class="skills" id="skills">
      <div class="container">
        <div class="section-heading">
          <small>02 — MY SKILLS</small>
          <h2>مهاراتي <span>واهتماماتي</span></h2>
        </div>

        <div class="skills-grid">

          <div class="skill">
            <div class="icon">⌘</div>
            <h3>Cybersecurity</h3>
            <p>التعلم والاستكشاف في مجال الأمن السيبراني وحماية المعلومات.</p>
          </div>

          <div class="skill">
            <div class="icon">⌨</div>
            <h3>Web Development</h3>
            <p>أساسيات HTML وCSS والبرمجة وتطوير صفحات الويب.</p>
          </div>

          <div class="skill">
            <div class="icon">✧</div>
            <h3>Creative Design</h3>
            <p>تصميم المحتوى والأعمال البصرية باستخدام الأدوات الرقمية.</p>
          </div>

          <div class="skill">
            <div class="icon">◈</div>
            <h3>Content Creation</h3>
            <p>صناعة المحتوى والتصوير وتحرير الصور والفيديو.</p>
          </div>

          <div class="skill">
            <div class="icon">▤</div>
            <h3>Microsoft Office</h3>
            <p>استخدام تطبيقات Office والأدوات المكتبية الرقمية.</p>
          </div>

          <div class="skill">
            <div class="icon">文</div>
            <h3>Languages</h3>
            <p>اللغة العربية واللغة الإنجليزية.</p>
          </div>

        </div>
      </div>
    </section>

    <section class="projects" id="projects">
      <div class="container">
        <div class="section-heading">
          <small>03 — SELECTED WORK</small>
          <h2>مشاريعي <span>وأعمالي</span></h2>
        </div>

        <div class="project-grid">

          <article class="project">
            <div class="project-number">PROJECT 01</div>
            <h3>Personal Portfolio</h3>
            <p>
              موقع شخصي للتعريف بي وبمهاراتي واهتماماتي
              باستخدام HTML وCSS.
            </p>
            <div class="project-tag">HTML · CSS · WEB DESIGN</div>
          </article>

          <article class="project">
            <div class="project-number">PROJECT 02</div>
            <h3>Web Design</h3>
            <p>
              تجربة تصميم وتطوير صفحات ويب تهتم بالتنسيق
              وتجربة المستخدم والهوية البصرية.
            </p>
            <div class="project-tag">DESIGN · FRONTEND</div>
          </article>

        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="container">
        <div class="section-heading">
          <small>04 — GET IN TOUCH</small>
          <h2>لنبقَ على <span>تواصل</span></h2>
        </div>

        <p>
          لديك فرصة أو فكرة أو ترغب بالتواصل؟
          يسعدني أن أسمع منك.
        </p>

        <a
          class="btn"
          href="mailto:esraalhtary@gmail.com">
          أرسل لي رسالة
        </a>

        <a class="email" href="mailto:esraalhtary@gmail.com">
          esraalhtary@gmail.com
        </a>
      </div>
    </section>

  </main>

  <footer>
    © 2026 <span>Esraa Al-Hetari</span> — جميع الحقوق محفوظة.
  </footer>

</body>
</html>
