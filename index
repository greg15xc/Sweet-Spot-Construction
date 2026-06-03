<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sweet Spot Construction</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --black: #0a0a0a;
    --off-black: #111111;
    --charcoal: #1a1a1a;
    --gold: #c9a84c;
    --gold-light: #e8d5a3;
    --white: #f5f4f0;
    --gray: #888;
    --border: rgba(201,168,76,0.2);
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--black);
    color: var(--white);
    font-family: 'Montserrat', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 28px 60px;
    background: linear-gradient(to bottom, rgba(10,10,10,0.95), transparent);
  }

  .nav-logo {
    display: flex;
    align-items: center;
    gap: 14px;
  }

  .logo-badge {
    width: 44px;
    height: 56px;
    border: 2px solid var(--white);
    border-radius: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1px;
  }

  .logo-badge span {
    font-family: 'Cormorant Garamond', serif;
    font-size: 14px;
    font-weight: 600;
    line-height: 1;
    letter-spacing: 1px;
  }

  .logo-dot {
    width: 3px;
    height: 3px;
    background: var(--white);
    border-radius: 50%;
  }

  .logo-text {
    display: flex;
    flex-direction: column;
  }

  .logo-text .name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-weight: 600;
    letter-spacing: 4px;
    text-transform: uppercase;
  }

  .logo-text .sub {
    font-size: 9px;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--gray);
    margin-top: 1px;
  }

  .nav-links {
    display: flex;
    gap: 40px;
    list-style: none;
  }

  .nav-links a {
    color: var(--white);
    text-decoration: none;
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    opacity: 0.7;
    transition: opacity 0.3s;
  }

  .nav-links a:hover { opacity: 1; }

  .nav-cta {
    background: transparent;
    border: 1px solid var(--gold);
    color: var(--gold);
    padding: 10px 24px;
    font-family: 'Montserrat', sans-serif;
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    cursor: pointer;
    transition: all 0.3s;
  }

  .nav-cta:hover {
    background: var(--gold);
    color: var(--black);
  }

  /* HERO */
  .hero {
    height: 100vh;
    position: relative;
    display: flex;
    align-items: flex-end;
    overflow: hidden;
  }

  .hero-bg {
    position: absolute;
    inset: 0;
    background:
      linear-gradient(135deg, #1a1a1a 0%, #0a0a0a 50%, #111 100%);
  }

  .hero-grid {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(201,168,76,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(201,168,76,0.04) 1px, transparent 1px);
    background-size: 80px 80px;
  }

  .hero-accent {
    position: absolute;
    top: 15%;
    right: 8%;
    width: 340px;
    height: 480px;
    border: 1px solid rgba(201,168,76,0.15);
    border-radius: 2px;
  }

  .hero-accent::before {
    content: '';
    position: absolute;
    top: 20px; left: 20px; right: -20px; bottom: -20px;
    border: 1px solid rgba(201,168,76,0.07);
  }

  .hero-img-placeholder {
    position: absolute;
    top: 12%;
    right: 6%;
    width: 360px;
    height: 500px;
    background: linear-gradient(160deg, #1e1e1e, #2a2a2a);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .hero-img-placeholder::after {
    content: 'PROJECT PHOTO';
    font-size: 9px;
    letter-spacing: 4px;
    color: rgba(255,255,255,0.15);
  }

  /* Diagonal line decoration */
  .hero-line {
    position: absolute;
    top: 0;
    left: 38%;
    width: 1px;
    height: 100%;
    background: linear-gradient(to bottom, transparent, rgba(201,168,76,0.2), transparent);
    transform: rotate(12deg);
    transform-origin: top center;
  }

  .hero-content {
    position: relative;
    z-index: 2;
    padding: 0 60px 80px;
    max-width: 680px;
  }

  .hero-eyebrow {
    font-size: 9px;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .hero-eyebrow::before {
    content: '';
    display: block;
    width: 40px;
    height: 1px;
    background: var(--gold);
  }

  .hero-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(52px, 7vw, 88px);
    font-weight: 300;
    line-height: 1.0;
    letter-spacing: -1px;
    margin-bottom: 28px;
  }

  .hero-title em {
    font-style: italic;
    color: var(--gold-light);
  }

  .hero-desc {
    font-size: 12px;
    letter-spacing: 1px;
    line-height: 2;
    color: rgba(245,244,240,0.6);
    max-width: 420px;
    margin-bottom: 44px;
  }

  .hero-actions {
    display: flex;
    align-items: center;
    gap: 32px;
  }

  .btn-primary {
    background: var(--gold);
    color: var(--black);
    border: none;
    padding: 16px 36px;
    font-family: 'Montserrat', sans-serif;
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
  }

  .btn-primary:hover { background: var(--gold-light); }

  .btn-ghost {
    background: transparent;
    border: none;
    color: var(--white);
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 10px;
    opacity: 0.6;
    transition: opacity 0.3s;
  }

  .btn-ghost:hover { opacity: 1; }

  .btn-ghost::after {
    content: '→';
    font-size: 14px;
  }

  .hero-roc {
    position: absolute;
    bottom: 80px;
    right: 60px;
    font-size: 9px;
    letter-spacing: 3px;
    color: rgba(255,255,255,0.3);
    text-transform: uppercase;
  }

  /* STATS BAR */
  .stats-bar {
    background: var(--charcoal);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    display: flex;
  }

  .stat {
    flex: 1;
    padding: 36px 40px;
    border-right: 1px solid var(--border);
    text-align: center;
  }

  .stat:last-child { border-right: none; }

  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 42px;
    font-weight: 300;
    color: var(--gold);
    line-height: 1;
    margin-bottom: 8px;
  }

  .stat-label {
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gray);
  }

  /* ABOUT */
  .section {
    padding: 120px 60px;
  }

  .section-tag {
    font-size: 9px;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .section-tag::before {
    content: '';
    display: block;
    width: 30px;
    height: 1px;
    background: var(--gold);
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 4vw, 54px);
    font-weight: 300;
    line-height: 1.15;
    margin-bottom: 28px;
  }

  .section-title em {
    font-style: italic;
    color: var(--gold-light);
  }

  /* ABOUT LAYOUT */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .about-text p {
    font-size: 13px;
    line-height: 2.2;
    color: rgba(245,244,240,0.65);
    margin-bottom: 20px;
  }

  .about-img {
    height: 520px;
    background: linear-gradient(160deg, #1e1e1e, #2a2a2a);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    color: rgba(255,255,255,0.1);
    font-size: 9px;
    letter-spacing: 4px;
  }

  .about-img::before {
    content: '';
    position: absolute;
    top: -16px;
    left: -16px;
    right: 16px;
    bottom: 16px;
    border: 1px solid var(--border);
    z-index: -1;
  }

  /* SERVICES */
  .services-section {
    background: var(--charcoal);
    padding: 120px 60px;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    margin-top: 60px;
  }

  .service-card {
    background: var(--charcoal);
    padding: 48px 40px;
    transition: background 0.3s;
    position: relative;
    overflow: hidden;
  }

  .service-card::before {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    width: 0; height: 2px;
    background: var(--gold);
    transition: width 0.4s ease;
  }

  .service-card:hover { background: #1f1f1f; }
  .service-card:hover::before { width: 100%; }

  .service-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px;
    font-weight: 300;
    color: rgba(201,168,76,0.15);
    line-height: 1;
    margin-bottom: 20px;
  }

  .service-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 400;
    margin-bottom: 14px;
    letter-spacing: 1px;
  }

  .service-desc {
    font-size: 11px;
    line-height: 2;
    color: rgba(245,244,240,0.5);
    letter-spacing: 0.5px;
  }

  /* PROJECTS */
  .projects-section { padding: 120px 60px; }

  .projects-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    margin-bottom: 60px;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    grid-template-rows: 300px 300px;
    gap: 2px;
  }

  .project-card {
    background: #1a1a1a;
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: flex-end;
    cursor: pointer;
  }

  .project-card:first-child {
    grid-row: 1 / 3;
  }

  .project-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(to top, rgba(10,10,10,0.9) 0%, transparent 50%);
    opacity: 0;
    transition: opacity 0.4s;
  }

  .project-card:hover .project-overlay { opacity: 1; }

  .project-info {
    position: relative;
    z-index: 2;
    padding: 28px;
    transform: translateY(20px);
    opacity: 0;
    transition: all 0.4s;
  }

  .project-card:hover .project-info {
    transform: translateY(0);
    opacity: 1;
  }

  .project-type {
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 8px;
  }

  .project-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px;
    font-weight: 300;
  }

  .project-placeholder {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 9px;
    letter-spacing: 3px;
    color: rgba(255,255,255,0.1);
    text-transform: uppercase;
  }

  /* PROCESS */
  .process-section {
    background: var(--charcoal);
    padding: 120px 60px;
  }

  .process-steps {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0;
    margin-top: 70px;
    position: relative;
  }

  .process-steps::before {
    content: '';
    position: absolute;
    top: 28px;
    left: 14%;
    right: 14%;
    height: 1px;
    background: var(--border);
  }

  .process-step {
    padding: 0 30px;
    text-align: center;
  }

  .step-num {
    width: 56px;
    height: 56px;
    border: 1px solid var(--gold);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 28px;
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px;
    color: var(--gold);
    background: var(--charcoal);
    position: relative;
    z-index: 1;
  }

  .step-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-weight: 400;
    margin-bottom: 14px;
    letter-spacing: 1px;
  }

  .step-desc {
    font-size: 11px;
    line-height: 2;
    color: rgba(245,244,240,0.5);
  }

  /* CONTACT */
  .contact-section {
    padding: 120px 60px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 100px;
    align-items: start;
  }

  .contact-info h2 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px;
    font-weight: 300;
    line-height: 1.15;
    margin-bottom: 28px;
  }

  .contact-info p {
    font-size: 12px;
    line-height: 2.2;
    color: rgba(245,244,240,0.55);
    margin-bottom: 40px;
  }

  .contact-details {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .contact-item {
    display: flex;
    flex-direction: column;
    gap: 4px;
  }

  .contact-item label {
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
  }

  .contact-item span {
    font-size: 14px;
    font-family: 'Cormorant Garamond', serif;
  }

  .contact-form {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .form-group label {
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: rgba(245,244,240,0.4);
  }

  .form-group input,
  .form-group textarea,
  .form-group select {
    background: var(--charcoal);
    border: 1px solid var(--border);
    color: var(--white);
    padding: 14px 18px;
    font-family: 'Montserrat', sans-serif;
    font-size: 12px;
    font-weight: 300;
    outline: none;
    transition: border-color 0.3s;
    appearance: none;
  }

  .form-group input:focus,
  .form-group textarea:focus,
  .form-group select:focus {
    border-color: var(--gold);
  }

  .form-group textarea { height: 120px; resize: none; }

  .form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .submit-btn {
    background: var(--gold);
    color: var(--black);
    border: none;
    padding: 18px;
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.3s;
    margin-top: 8px;
  }

  .submit-btn:hover { background: var(--gold-light); }

  /* FOOTER */
  footer {
    background: var(--off-black);
    border-top: 1px solid var(--border);
    padding: 48px 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-copy {
    font-size: 10px;
    letter-spacing: 2px;
    color: rgba(255,255,255,0.25);
    text-transform: uppercase;
  }

  .footer-roc {
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--gold);
    opacity: 0.6;
  }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-eyebrow { animation: fadeUp 0.8s ease 0.2s both; }
  .hero-title { animation: fadeUp 0.8s ease 0.4s both; }
  .hero-desc { animation: fadeUp 0.8s ease 0.6s both; }
  .hero-actions { animation: fadeUp 0.8s ease 0.8s both; }

  /* SCROLL INDICATOR */
  .scroll-indicator {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    opacity: 0.3;
    animation: fadeUp 1s ease 1.2s both;
  }

  .scroll-line {
    width: 1px;
    height: 50px;
    background: linear-gradient(to bottom, transparent, var(--white));
    animation: scrollPulse 2s ease infinite;
  }

  @keyframes scrollPulse {
    0%, 100% { opacity: 0.3; transform: scaleY(0.8); }
    50% { opacity: 1; transform: scaleY(1); }
  }

  .scroll-text {
    font-size: 8px;
    letter-spacing: 3px;
    text-transform: uppercase;
    writing-mode: vertical-rl;
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">
    <div class="logo-badge">
      <span>S</span>
      <div class="logo-dot"></div>
      <span>S</span>
    </div>
    <div class="logo-text">
      <span class="name">Sweet Spot</span>
      <span class="sub">Construction</span>
    </div>
  </div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <button class="nav-cta">Start a Project</button>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-line"></div>
  <div class="hero-accent"></div>

  <div class="hero-img-placeholder"></div>

  <div class="hero-content">
    <div class="hero-eyebrow">Scottsdale, Arizona</div>
    <h1 class="hero-title">Where<br><em>Precision</em><br>Meets Results</h1>
    <p class="hero-desc">Architecturally driven construction and design-build services for discerning clients across the greater Phoenix–Scottsdale area.</p>
    <div class="hero-actions">
      <button class="btn-primary">View Our Work</button>
      <button class="btn-ghost">Get a Quote</button>
    </div>
  </div>

  <div class="hero-roc">ROC #361611 · Licensed · Bonded · Insured</div>

  <div class="scroll-indicator">
    <div class="scroll-line"></div>
    <span class="scroll-text">Scroll</span>
  </div>
</section>

<!-- STATS -->
<div class="stats-bar">
  <div class="stat">
    <div class="stat-num">15+</div>
    <div class="stat-label">Years Experience</div>
  </div>
  <div class="stat">
    <div class="stat-num">100%</div>
    <div class="stat-label">Licensed & Insured</div>
  </div>
  <div class="stat">
    <div class="stat-num">AZ</div>
    <div class="stat-label">ROC #361611</div>
  </div>
  <div class="stat">
    <div class="stat-num">5★</div>
    <div class="stat-label">Client Satisfaction</div>
  </div>
</div>

<!-- ABOUT -->
<section class="section" id="about">
  <div class="about-grid">
    <div class="about-text">
      <div class="section-tag">Our Philosophy</div>
      <h2 class="section-title">Built with<br><em>intention.</em><br>Finished with precision.</h2>
      <p>Sweet Spot Construction is a Scottsdale-based design-build firm operating at the intersection of architectural vision and master craftsmanship. We believe the best projects happen when every detail is considered from the first sketch to the final finish.</p>
      <p>Whether it's a complete home transformation, a luxury addition, or a commercial build-out, our approach is the same — meticulous planning, relentless communication, and results that exceed expectations.</p>
      <button class="btn-primary" style="margin-top: 16px;">About the Team</button>
    </div>
    <div class="about-img">PROJECT PHOTO</div>
  </div>
</section>

<!-- SERVICES -->
<section class="services-section" id="services">
  <div class="section-tag">What We Build</div>
  <h2 class="section-title">Our <em>Services</em></h2>
  <div class="services-grid">
    <div class="service-card">
      <div class="service-num">01</div>
      <div class="service-name">Architecture & Design</div>
      <div class="service-desc">Conceptual design, working drawings, and full design oversight from vision to permit-ready documents.</div>
    </div>
    <div class="service-card">
      <div class="service-num">02</div>
      <div class="service-name">General Contracting</div>
      <div class="service-desc">Full project management, subcontractor coordination, and site supervision for residential and commercial builds.</div>
    </div>
    <div class="service-card">
      <div class="service-num">03</div>
      <div class="service-name">Renovation & Remodeling</div>
      <div class="service-desc">Kitchen and bath transformations, home additions, expansions, and full-home renovations done right the first time.</div>
    </div>
    <div class="service-card">
      <div class="service-num">04</div>
      <div class="service-name">Commercial Projects</div>
      <div class="service-desc">Office, retail, mixed-use, and hospitality builds with the same precision and attention to detail as our residential work.</div>
    </div>
    <div class="service-card">
      <div class="service-num">05</div>
      <div class="service-name">Specialty Work</div>
      <div class="service-desc">Concrete, flooring, drywall, electrical, HVAC coordination, painting, and finish work handled by trusted specialists.</div>
    </div>
    <div class="service-card">
      <div class="service-num">06</div>
      <div class="service-name">Design-Build</div>
      <div class="service-desc">One team. One vision. We handle design and construction under one roof for a seamless, efficient project experience.</div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section class="projects-section" id="projects">
  <div class="projects-header">
    <div>
      <div class="section-tag">Portfolio</div>
      <h2 class="section-title">Recent <em>Work</em></h2>
    </div>
    <button class="btn-ghost">View All Projects</button>
  </div>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-placeholder">Featured Project Photo</div>
      <div class="project-overlay"></div>
      <div class="project-info">
        <div class="project-type">Full Renovation</div>
        <div class="project-name">North Scottsdale Estate</div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-placeholder">Photo</div>
      <div class="project-overlay"></div>
      <div class="project-info">
        <div class="project-type">Kitchen Remodel</div>
        <div class="project-name">Paradise Valley</div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-placeholder">Photo</div>
      <div class="project-overlay"></div>
      <div class="project-info">
        <div class="project-type">Commercial</div>
        <div class="project-name">Old Town Scottsdale</div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-placeholder">Photo</div>
      <div class="project-overlay"></div>
      <div class="project-info">
        <div class="project-type">Home Addition</div>
        <div class="project-name">DC Ranch</div>
      </div>
    </div>
    <div class="project-card">
      <div class="project-placeholder">Photo</div>
      <div class="project-overlay"></div>
      <div class="project-info">
        <div class="project-type">Bath Renovation</div>
        <div class="project-name">McCormick Ranch</div>
      </div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process-section">
  <div style="text-align: center; max-width: 500px; margin: 0 auto 0;">
    <div class="section-tag" style="justify-content: center;">How We Work</div>
    <h2 class="section-title">The Sweet Spot <em>Process</em></h2>
  </div>
  <div class="process-steps">
    <div class="process-step">
      <div class="step-num">1</div>
      <div class="step-title">Consultation</div>
      <div class="step-desc">We meet to understand your vision, scope, timeline, and budget before anything else.</div>
    </div>
    <div class="process-step">
      <div class="step-num">2</div>
      <div class="step-title">Design & Plan</div>
      <div class="step-desc">We develop detailed plans, drawings, and a transparent project proposal.</div>
    </div>
    <div class="process-step">
      <div class="step-num">3</div>
      <div class="step-title">Build</div>
      <div class="step-desc">Expert execution with weekly updates, clear milestones, and zero surprises.</div>
    </div>
    <div class="process-step">
      <div class="step-num">4</div>
      <div class="step-title">Deliver</div>
      <div class="step-desc">Final walkthrough, punch list completion, and a project you're proud to show off.</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <div class="contact-info">
    <div class="section-tag">Get in Touch</div>
    <h2>Let's build<br>something<br><em>remarkable.</em></h2>
    <p>Ready to start your project? We'd love to hear about your vision. Reach out and we'll schedule a complimentary consultation.</p>
    <div class="contact-details">
      <div class="contact-item">
        <label>Phone</label>
        <span>(602) 000-0000</span>
      </div>
      <div class="contact-item">
        <label>Email</label>
        <span>hello@sweetspotconstruction.com</span>
      </div>
      <div class="contact-item">
        <label>Service Area</label>
        <span>Scottsdale · Phoenix · Paradise Valley · North AZ</span>
      </div>
      <div class="contact-item">
        <label>License</label>
        <span>ROC #361611</span>
      </div>
    </div>
  </div>
  <div class="contact-form">
    <div class="form-row">
      <div class="form-group">
        <label>First Name</label>
        <input type="text" placeholder="Greg">
      </div>
      <div class="form-group">
        <label>Last Name</label>
        <input type="text" placeholder="Smith">
      </div>
    </div>
    <div class="form-group">
      <label>Email</label>
      <input type="email" placeholder="you@email.com">
    </div>
    <div class="form-group">
      <label>Project Type</label>
      <select>
        <option value="" disabled selected>Select a service</option>
        <option>Kitchen Remodel</option>
        <option>Bathroom Remodel</option>
        <option>Home Addition</option>
        <option>Full Renovation</option>
        <option>Commercial Project</option>
        <option>Other</option>
      </select>
    </div>
    <div class="form-group">
      <label>Tell Us About Your Project</label>
      <textarea placeholder="Describe your project, timeline, and budget range..."></textarea>
    </div>
    <button class="submit-btn">Send Message →</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-copy">© 2025 Sweet Spot Construction · All Rights Reserved</div>
  <div class="footer-roc">ROC #361611 · Licensed · Bonded · Insured · Scottsdale, AZ</div>
</footer>

</body>
</html>
