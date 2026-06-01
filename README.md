index.html
# benedettaobert.github.io
title: Benedetta Obert Portfolio
description: Bookmark this to keep an eye on my project updates!
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Benedetta Obert — Senior Freelance PM · Global Events & Operations</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --navy: #1B2B4B;
    --gold: #C9973A;
    --gold-light: #E8C97A;
    --cream: #FAF8F4;
    --white: #FFFFFF;
    --grey: #6B7280;
    --light: #F0EDE8;
    --text: #2D2D2D;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--text);
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(27,43,75,0.97);
    backdrop-filter: blur(12px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 48px; height: 64px;
    border-bottom: 1px solid rgba(201,151,58,0.3);
  }
  nav .logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px; font-weight: 600; color: var(--white);
    letter-spacing: 0.05em;
  }
  nav .logo span { color: var(--gold); }
  nav .nav-links { display: flex; gap: 36px; }
  nav .nav-links a {
    color: rgba(255,255,255,0.7); text-decoration: none;
    font-size: 13px; letter-spacing: 0.08em; text-transform: uppercase;
    font-weight: 500; transition: color 0.2s;
  }
  nav .nav-links a:hover { color: var(--gold); }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: var(--navy);
    display: flex; align-items: center;
    position: relative; overflow: hidden;
    padding: 100px 0 80px;
  }
  .hero::before {
    content: '';
    position: absolute; top: 0; right: 0;
    width: 50%; height: 100%;
    background: linear-gradient(135deg, transparent 40%, rgba(201,151,58,0.07) 100%);
  }
  .hero::after {
    content: '';
    position: absolute; bottom: -1px; left: 0; right: 0; height: 80px;
    background: linear-gradient(to bottom, transparent, var(--cream));
  }
  .hero-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 80px; align-items: center;
    max-width: 1200px; margin: 0 auto; padding: 0 48px;
    width: 100%;
  }
  .hero-label {
    font-size: 11px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 24px;
    display: flex; align-items: center; gap: 12px;
  }
  .hero-label::before {
    content: ''; width: 32px; height: 1px; background: var(--gold);
  }
  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(52px, 6vw, 80px);
    font-weight: 300; line-height: 1.05;
    color: var(--white); margin-bottom: 8px;
  }
  .hero h1 em { font-style: italic; color: var(--gold-light); }
  .hero-title {
    font-size: 14px; letter-spacing: 0.12em; text-transform: uppercase;
    color: rgba(255,255,255,0.5); margin-bottom: 32px; font-weight: 400;
  }
  .hero-text {
    font-size: 17px; line-height: 1.75; color: rgba(255,255,255,0.75);
    max-width: 520px; margin-bottom: 48px;
  }
  .hero-cta {
    display: inline-flex; align-items: center; gap: 12px;
    background: var(--gold); color: var(--navy);
    padding: 14px 32px; font-size: 13px;
    letter-spacing: 0.1em; text-transform: uppercase; font-weight: 600;
    text-decoration: none; transition: all 0.25s;
  }
  .hero-cta:hover { background: var(--gold-light); transform: translateY(-2px); }
  .hero-cta svg { width: 16px; height: 16px; }
  .hero-right { display: flex; flex-direction: column; gap: 20px; }
  .stat-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(201,151,58,0.25);
    padding: 28px 32px;
    position: relative; overflow: hidden;
    animation: fadeUp 0.7s ease both;
  }
  .stat-card::before {
    content: ''; position: absolute; left: 0; top: 0; bottom: 0;
    width: 3px; background: var(--gold);
  }
  .stat-card:nth-child(2) { animation-delay: 0.1s; }
  .stat-card:nth-child(3) { animation-delay: 0.2s; }
  .stat-card:nth-child(4) { animation-delay: 0.3s; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 44px; font-weight: 300; color: var(--gold); line-height: 1;
    margin-bottom: 6px;
  }
  .stat-label { font-size: 13px; color: rgba(255,255,255,0.6); line-height: 1.4; }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* SECTION BASE */
  section { padding: 100px 0; }
  .container { max-width: 1200px; margin: 0 auto; padding: 0 48px; }
  .section-label {
    font-size: 11px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 16px;
    display: flex; align-items: center; gap: 12px;
  }
  .section-label::before { content: ''; width: 32px; height: 1px; background: var(--gold); }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 4vw, 54px); font-weight: 300;
    color: var(--navy); line-height: 1.15; margin-bottom: 60px;
  }
  .section-title em { font-style: italic; color: var(--gold); }

  /* EXPERTISE */
  #expertise { background: var(--white); }
  .expertise-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2px; }
  .exp-card {
    background: var(--cream);
    padding: 40px 32px;
    transition: all 0.3s;
    cursor: default;
    position: relative; overflow: hidden;
  }
  .exp-card::after {
    content: ''; position: absolute; bottom: 0; left: 0; right: 0;
    height: 3px; background: var(--gold);
    transform: scaleX(0); transform-origin: left;
    transition: transform 0.3s ease;
  }
  .exp-card:hover { background: var(--navy); }
  .exp-card:hover .exp-title { color: var(--white); }
  .exp-card:hover .exp-text { color: rgba(255,255,255,0.65); }
  .exp-card:hover .exp-icon { color: var(--gold); }
  .exp-card:hover::after { transform: scaleX(1); }
  .exp-icon { font-size: 28px; margin-bottom: 20px; color: var(--gold); }
  .exp-title { font-size: 17px; font-weight: 600; color: var(--navy); margin-bottom: 12px; line-height: 1.3; }
  .exp-text { font-size: 14px; color: var(--grey); line-height: 1.7; }

  /* PROJECTS */
  #projects { background: var(--cream); }
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 32px; }
  .project-card {
    background: var(--white);
    border: 1px solid rgba(27,43,75,0.1);
    padding: 40px;
    position: relative; overflow: hidden;
    transition: all 0.3s; cursor: default;
  }
  .project-card:hover { transform: translateY(-4px); box-shadow: 0 20px 60px rgba(27,43,75,0.12); }
  .project-card.featured {
    grid-column: 1 / -1;
    display: grid; grid-template-columns: 1fr 1fr; gap: 40px; align-items: start;
    background: var(--navy);
  }
  .project-card.featured .proj-label { color: var(--gold); }
  .project-card.featured .proj-title { color: var(--white); }
  .project-card.featured .proj-text { color: rgba(255,255,255,0.7); }
  .project-card.featured .proj-tag { background: rgba(201,151,58,0.2); color: var(--gold-light); border-color: rgba(201,151,58,0.3); }
  .project-card.featured .proj-detail-label { color: rgba(255,255,255,0.5); }
  .project-card.featured .proj-detail-val { color: var(--white); }
  .proj-label {
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 16px;
  }
  .proj-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px; font-weight: 400; color: var(--navy);
    margin-bottom: 16px; line-height: 1.2;
  }
  .proj-text { font-size: 15px; color: var(--grey); line-height: 1.75; margin-bottom: 24px; }
  .proj-tags { display: flex; flex-wrap: wrap; gap: 8px; }
  .proj-tag {
    font-size: 11px; padding: 4px 12px; letter-spacing: 0.06em;
    border: 1px solid rgba(27,43,75,0.15); color: var(--navy);
    text-transform: uppercase; font-weight: 500;
  }
  .proj-details { display: flex; flex-direction: column; gap: 20px; justify-content: center; }
  .proj-detail { border-left: 2px solid var(--gold); padding-left: 16px; }
  .proj-detail-label { font-size: 10px; letter-spacing: 0.15em; text-transform: uppercase; color: var(--grey); margin-bottom: 4px; }
  .proj-detail-val { font-size: 15px; font-weight: 500; color: var(--navy); line-height: 1.4; }

  /* BACKGROUND TIMELINE */
  #background { background: var(--white); }
  .timeline { position: relative; padding-left: 32px; }
  .timeline::before {
    content: ''; position: absolute; left: 0; top: 8px; bottom: 0;
    width: 1px; background: linear-gradient(to bottom, var(--gold), rgba(201,151,58,0.1));
  }
  .tl-item { position: relative; margin-bottom: 56px; }
  .tl-item::before {
    content: ''; position: absolute; left: -38px; top: 6px;
    width: 10px; height: 10px;
    background: var(--gold); border-radius: 50%;
    box-shadow: 0 0 0 4px var(--white), 0 0 0 5px var(--gold);
  }
  .tl-date { font-size: 11px; letter-spacing: 0.15em; text-transform: uppercase; color: var(--gold); margin-bottom: 8px; font-weight: 600; }
  .tl-role { font-size: 20px; font-weight: 600; color: var(--navy); margin-bottom: 4px; }
  .tl-company { font-size: 14px; color: var(--grey); margin-bottom: 16px; }
  .tl-points { list-style: none; display: flex; flex-direction: column; gap: 8px; }
  .tl-points li {
    font-size: 14px; color: #4B5563; line-height: 1.65;
    padding-left: 16px; position: relative;
  }
  .tl-points li::before {
    content: '—'; position: absolute; left: 0; color: var(--gold); font-size: 12px;
  }

  /* SKILLS */
  #skills { background: var(--navy); }
  #skills .section-title { color: var(--white); }
  .skills-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px; }
  .skill-block { }
  .skill-category {
    font-size: 11px; letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 16px;
    padding-bottom: 12px; border-bottom: 1px solid rgba(201,151,58,0.3);
  }
  .skill-list { list-style: none; display: flex; flex-direction: column; gap: 10px; }
  .skill-list li { font-size: 14px; color: rgba(255,255,255,0.75); line-height: 1.4; padding-left: 12px; position: relative; }
  .skill-list li::before { content: '·'; position: absolute; left: 0; color: var(--gold); }

  /* CONTACT */
  #contact { background: var(--cream); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: start; }
  .contact-text { font-size: 16px; color: var(--grey); line-height: 1.8; margin-bottom: 40px; }
  .contact-items { display: flex; flex-direction: column; gap: 20px; }
  .contact-item { display: flex; align-items: center; gap: 16px; }
  .contact-icon {
    width: 44px; height: 44px; background: var(--navy);
    display: flex; align-items: center; justify-content: center; flex-shrink: 0;
  }
  .contact-icon svg { width: 18px; height: 18px; color: var(--gold); fill: currentColor; }
  .contact-info { font-size: 15px; color: var(--text); font-weight: 500; }
  .contact-info small { display: block; font-size: 12px; color: var(--grey); font-weight: 400; margin-top: 2px; }
  .avail-box {
    background: var(--navy); padding: 40px;
  }
  .avail-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px; font-weight: 300; color: var(--white); margin-bottom: 24px; line-height: 1.2;
  }
  .avail-title em { font-style: italic; color: var(--gold-light); }
  .avail-types { display: flex; flex-direction: column; gap: 12px; margin-bottom: 32px; }
  .avail-type {
    display: flex; align-items: center; gap: 12px;
    font-size: 14px; color: rgba(255,255,255,0.8);
  }
  .avail-type::before {
    content: ''; width: 20px; height: 1px; background: var(--gold); flex-shrink: 0;
  }
  .avail-cta {
    display: inline-flex; align-items: center; gap: 10px;
    background: var(--gold); color: var(--navy);
    padding: 12px 28px; font-size: 12px;
    letter-spacing: 0.1em; text-transform: uppercase; font-weight: 600;
    text-decoration: none; transition: all 0.25s;
  }
  .avail-cta:hover { background: var(--gold-light); }

  /* FOOTER */
  footer {
    background: var(--navy); padding: 32px 48px;
    display: flex; align-items: center; justify-content: space-between;
    border-top: 1px solid rgba(201,151,58,0.2);
  }
  footer .logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px; color: var(--white); font-weight: 400;
  }
  footer .logo span { color: var(--gold); }
  footer p { font-size: 13px; color: rgba(255,255,255,0.4); }

  @media (max-width: 900px) {
    nav { padding: 0 24px; }
    .hero-grid, .projects-grid, .contact-grid, .skills-grid { grid-template-columns: 1fr; }
    .project-card.featured { grid-column: 1; display: block; }
    .expertise-grid { grid-template-columns: 1fr 1fr; }
    .container { padding: 0 24px; }
    footer { flex-direction: column; gap: 12px; text-align: center; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">B.<span>Obert</span></div>
  <div class="nav-links">
    <a href="#expertise">Expertise</a>
    <a href="#projects">Projects</a>
    <a href="#background">Background</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-grid">
    <div class="hero-left">
      <div class="hero-label">Available for Freelance Mandates</div>
      <h1>Benedetta<br/><em>Obert</em></h1>
      <div class="hero-title">Senior Freelance Project Manager ·&nbsp;<br/>
      Global Events &amp; Operations Consultant</div>
      <p class="hero-text">
        Complex projects. Multiple stakeholders. Zero room for failure.<br/>
        <br/>
        I help brands, agencies, and international organizations deliver large-scale events, market launches, operational programs, and transformation initiatives. From strategic planning to on-site execution.
      </p>
      <a href="#contact" class="hero-cta">
        Let's Work Together
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
      </a>
    </div>
    <div class="hero-right">
      <div class="stat-card">
        <div class="stat-num">7+</div>
        <div class="stat-label">Years leading and delivering complex international programs</div>
      </div>
       <div class="stat-card">
        <div class="stat-num">5</div>
        <div class="stat-label">Industries mastered: Events & Sponsorship· Luxury · Publishing & Media · FMCG · Payments</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">2026</div>
        <div class="stat-label">Recent project, lasting impact<br/> Olympic & Paralympic Winter Games Milano Cortina — Visa’s Global Sponsorship Team</div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERTISE -->
<section id="expertise">
  <div class="container">
    <div class="section-label">What I Do</div>
    <div class="section-title">Areas of <em>Expertise</em></div>
    <div class="expertise-grid">
      <div class="exp-card">
        <div class="exp-icon">🎯</div>
        <div class="exp-title">Event & Sponsorship Operations</div>
        <div class="exp-text">End-to-end program management of large-scale international events (sport and high-profile business), brand experiences and sponsorship programs. From strategic planning and venue readiness to live operations and post-event execution.</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">🏪</div>
        <div class="exp-title">Brand Activations & Retail Expansion</div>
        <div class="exp-text">Strategy and execution for new market launches, retail openings, in-store activations, local partnesrhips, B2B events, OOH, and integrated campigns.</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">🌍</div>
        <div class="exp-title">Multi-Stakeholder Coordination</div>
        <div class="exp-text">The bridge between clients, agencies, creative teams, suppliers, local partners, and global HQs — clear briefs, no silos, zero dropped balls.</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">⚙️</div>
        <div class="exp-title">Operations & Supply Chain</div>
        <div class="exp-text">Deep expertise in supply chain, demand forecasting, inventory management, logiscs and distribution — built within multinational environments including FMCG industry in roles at Lavazza and Nestlé across European markets.</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">💻</div>
        <div class="exp-title">Digital Transformation</div>
        <div class="exp-text">Support organizations in turning fragmented systems and workflows into integrated, scalable operating models. Lead cross-functional digital transformation programs across CRM, ERP, BI, marketing automation, editorial, and e-commerce ecosystems bridging business and technology.</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">📋</div>
        <div class="exp-title">Agile Program Delivery</div>
        <div class="exp-text">Certified Scrum Master & Product Owner. Structured delivery in ambiguous, fast-moving environments — on scope, on time, on budget.</div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="container">
    <div class="section-label">Selected Work</div>
    <div class="section-title">Key <em>Projects</em></div>
    <div class="projects-grid">

      <!-- FEATURED -->
      <div class="project-card featured">
        <div>
          <div class="proj-label">🏅 Winter Olympic & Paralympic Games · 2025-26 </div>
          <div class="proj-title">Visa Sponsorships & Payment Operations — Milano Cortina 2026</div>
          <div class="proj-text">
            Senior Operations Project Manager within Visa’s Global Sponsorship Team, delivering payment infrastructure and operational readiness across Olympic and Paralympic venues. Orchestrated multi-stakeholder execution from planning to Games-time operations and decommissioning, enabling seamless payment experiences, effective brand activation, and frictionless fan journeys in one of the world’s most complex live-event environments.
          </div>
          <div class="proj-tags">
            <span class="proj-tag">Event Operations</span>
            <span class="proj-tag">Payments Infrastructure</span>
            <span class="proj-tag">Retail Management</span>
            <span class="proj-tag">Stakeholder Coordination</span>
            <span class="proj-tag">Multi-venue Logistics</span>
            <span class="proj-tag">Live Operations</span>
          </div><br/>
        </div>
        <div class="proj-details">
          <div class="proj-detail">
            <div class="proj-detail-label">Scale</div>
            <div class="proj-detail-val">Multiple spread venues across Northern Italy</div>
          </div>
          <div class="proj-detail">
            <div class="proj-detail-label">Stakeholders</div>
            <div class="proj-detail-val">Visa Global, IOC, OCOG, local acquiring banks, retail partners, logistics suppliers and marketing agencies</div>
          </div>
          <div class="proj-detail">
            <div class="proj-detail-label">Scope</div>
            <div class="proj-detail-val">Payment acceptance · Retail operations · Venue readiness · Brand presence · Fan experience · Operational delivery</div>
          </div>
          <div class="proj-detail">
            <div class="proj-detail-label">Environment</div>
            <div class="proj-detail-val">Fixed deadline · Live venue operations & events · Zero-downtime requirement</div>
          </div>
        </div>
      </div>

      <!-- CARD 2 -->
      <div class="project-card">
        <div class="proj-label">🌟 Brand Experience, Activation & Market Expansion Strategy · 2025–Present</div>
        <div class="proj-title">International Premium Brand Activations & Market Expansion — EU / UAE</div>
        <div class="proj-text">
          Collaborating as freelance Senior Project Manager with international media and event partners to support premium brands in expansion and activation projects across new markets. Store openings, in-store activations, B2B launch events, PR and influencer strategy, OOH and media activities, local partnerships with hospitality and lifestyle brands including hotels, gyms, and cafés. Single point of contact between clients, production and media agencies, creative teams and local stakeholders — coordinating all project phases from strategic planning to execution.
        </div>
        <div class="proj-tags">
          <span class="proj-tag">Retail Expansion</span>
          <span class="proj-tag">Brand Launch</span>
          <span class="proj-tag">B2B Events</span>
          <span class="proj-tag">Integrated Campaign Coordination</span>
          <span class="proj-tag">Market Entry</span>
        </div>
      </div>

      <!-- CARD 3 -->
      <div class="project-card">
        <div class="proj-label">📱 Operations & Digital Transformation · 2022–2025</div>
        <div class="proj-title">Hearst Italia — Full Digital and Operational Redesign</div>
        <div class="proj-text">
          Led cross-functional digital and organizational transformation initiatives, redesigning processes and coordinating technology implementation across marketing, editorial, sales, finance, and events teams: Salesforce CRM & Marketing Cloud, Zucchetti ERP, WoodWing editorial platform, Magento e-commerce, and integrated operational workflows. Also coordinated logistics for fashion productions and supported the launch of the French subsidiary. Coordinated 15+ vendors, agencies, and technology partners over a multi-year transformation roadmap.
        </div>
        <div class="proj-tags">
          <span class="proj-tag">Smart Operations</span>
          <span class="proj-tag">CRM & Marketing Automation</span>
          <span class="proj-tag">E-commerce</span>
          <span class="proj-tag">Change Management</span>
          <span class="proj-tag">Vendor Management</span>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- BACKGROUND -->
<section id="background">
  <div class="container">
    <div class="section-label">Experience</div>
    <div class="section-title">Professional <em>Background</em></div>
    <div class="timeline">

   <div class="tl-item">
        <div class="tl-date">2025 – Present</div>
        <div class="tl-role">Freelance Head of Project Management</div>
        <div class="tl-company">International Brand Activations, Events & Market Expansion · Freelance</div>
        <ul class="tl-points">
          <li>Supporting agencies and premium brands in the planning and execution of events, retail activations, store openings, and market-entry initiatives</li>
          <li>Brand Activations, Retail Expansion, B2B & Consumer Events, Partnership Development</li>
          <li>Multi-stakeholder coordination across clients, agencies, production teams, and local partners</li>
          <li>From strategy and client briefing to on-the-ground execution</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="tl-date">2025 – Apr 2026</div>
        <div class="tl-role">Senior Acceptance Project Manager — Olympic & Paralympic Winter Games</div>
        <div class="tl-company">Visa · Global Sponsorship Team · Freelance</div>
        <ul class="tl-points">
          <li>End-to-end payment acceptance operations across all Milano Cortina 2026 venues</li>
          <li>Payment Operations (POS/ATM deployment), Retail & Merchant Ecosystem, Fan Experience</li>
          <li>Multi-stakeholder coordination</li>
          <li>Games-time escalation point for real-time operational decisions</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="tl-date">2022 – 2025</div>
        <div class="tl-role">Head of Project Management & Digital Transformation</div>
        <div class="tl-company">Hearst Italia (Hearst Corporation) · Full-time</div>
        <ul class="tl-points">
          <li>Salesforce CRM, Marketing Cloud, Magento membership & e-commerce, centralised BI platform built from scratch — full lifecycle PM</li>
          <li>Operations: French subsidiary launch including location scouting, Luxury fashion shoot and production logistics</li>
          <li>15+ agencies and vendors coordinated</li>
          <li>Change management across marketing, editorial, events, sales, and finance</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="tl-date">2021 – 2022</div>
        <div class="tl-role">Project Manager — Operations & Supply Chain</div>
        <div class="tl-company">Nestlé · Confectionery Business</div>
        <ul class="tl-points">
          <li>Demand forecasting accuracy improvements and inventory optimisation across European markets</li>
          <li>Cross-functional projects coordinating supply, planning, and sales teams</li>
          <li>Standardised processes across international markets</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="tl-date">2020 – 2021</div>
        <div class="tl-role">Distribution & Supply Planner — Logistics & Supply Chain</div>
        <div class="tl-company">Lavazza Group · France & Italy</div>
        <ul class="tl-points">
          <li>End-to-end distribution and logistics across France and Italy</li>
          <li>Demand forecasting, stock planning and inventory level optimisation, transport efficiency</li>
          <li>Distribution and logistics system implementation projects</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="container">
    <div class="section-label">Capabilities</div>
    <div class="section-title">Skills &amp; <em>Tools</em></div>
    <div class="skills-grid">
      <div class="skill-block">
        <div class="skill-category">Project Delivery</div>
        <ul class="skill-list">
          <li>Event & Sponsorship Operations</li>
          <li>Retail & Brand Activation</li>
          <li>Program & Portfolio Management</li>
          <li>Agile (Scrum / Kanban)</li>
          <li>Budget & Cost Management</li>
          <li>Risk & Issue Management</li>
        </ul>
      </div>
      <div class="skill-block">
        <div class="skill-category">Operations & Logistics</div>
        <ul class="skill-list">
          <li>Supply Chain & Logistics</li>
          <li>Demand Forecasting</li>
          <li>Inventory Optimisation</li>
          <li>Vendor & Supplier Management</li>
          <li>Contract Negotiation</li>
          <li>Procurement</li>
        </ul>
      </div>
      <div class="skill-block">
        <div class="skill-category">Digital & Platforms</div>
        <ul class="skill-list">
          <li>Salesforce CRM & Marketing Cloud</li>
          <li>Zucchetti ERP</li>
          <li>Magento / Shopify</li>
          <li>Woodwing Studio</li>
          <li>PowerBI / QlikView</li>
          <li>Adobe Suite</li>
        </ul>
      </div>
      <div class="skill-block">
        <div class="skill-category">Languages & Credentials</div>
        <ul class="skill-list">
          <li>Italian — Native</li>
          <li>English — Proficient</li>
          <li>Spanish — Intermediate</li>
          <li>French — Basic (in progress)</li>
          <li>Scrum Master & Product Owner</li>
          <li>Executive Programme — Digital Transformation (PoliMi)</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="section-label">Get In Touch</div>
    <div class="section-title">Let's Build Something <em>Exceptional</em></div>
    <div class="contact-grid">
      <div>
        <p class="contact-text">
          I partner with agencies, brands, and organisations that need a senior lead who can move between strategy and execution — and make it look seamless. Based in Milan, available for mandates across Europe, the Middle East and globally.
        </p>
        <div class="contact-items">
          <div class="contact-item">
            <div class="contact-icon">
              <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
            </div>
            <div class="contact-info">
              obert.benedetta@gmail.com
              <small>Email — preferred for project enquiries</small>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <svg viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
            </div>
            <div class="contact-info">
              +39 334 810 3387
              <small>Phone / WhatsApp</small>
            </div>
          </div>
            
        


        </div>
      </div>
      <div>
        <div class="avail-box">
          <div class="avail-title">Currently open to <em>new mandates</em></div>
          <div class="avail-types">
            <div class="avail-type">Event & Sponsorship Operations PM</div>
            <div class="avail-type">Brand Activation & Market Entry Lead</div>
            <div class="avail-type">Senior Project Consultant — Global Programs</div>
            <div class="avail-type">Digital Transformation Project Lead</div>
            <div class="avail-type">Retail & Operations Program Manager</div>
          </div>
          <a href="mailto:obert.benedetta@gmail.com" class="avail-cta">
            Send a Brief
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="logo">Benedetta <span>Obert</span></div>
  <p>Senior Freelance Project Manager · Global Events & Operations Consultant · Milan, Italy</p>
</footer>

</body>
</html>
