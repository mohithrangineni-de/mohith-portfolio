<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohith Rangineni — Senior Data & AI Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0b0b0c;
    --surface: #0f1115;
    --gray-50: #15171c;
    --gray-100: #1f2229;
    --gray-200: #2a2e36;
    --gray-400: #8b92a1;
    --gray-600: #c9d1d9;
    --accent: #4f46e5;
    --accent-light: #6366f1;
    --green: #00ff9f;
    --green-light: #00ff9f22;
    --mono: 'DM Mono', monospace;
    --serif: 'DM Serif Display', serif;
    --sans: 'Instrument Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--sans);
    background: var(--bg);
    color: var(--gray-600);
    line-height: 1.6;
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
    padding: 1.25rem 3rem;
    background: rgba(11,11,12,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--gray-100);
  }

  .nav-logo {
    font-family: var(--mono);
    font-size: 0.8rem;
    color: var(--gray-600);
    letter-spacing: 0.08em;
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .nav-links a {
    font-size: 0.85rem;
    color: var(--gray-600);
    text-decoration: none;
    letter-spacing: 0.04em;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--gray-600); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 8rem 3rem 4rem;
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
  }

  .hero-label {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--gray-400);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .hero-label::before {
    content: '';
    display: block;
    width: 2rem;
    height: 1px;
    background: var(--gray-400);
  }

  .hero-name {
    font-family: var(--serif);
    font-size: clamp(3.5rem, 8vw, 7rem);
    line-height: 1.0;
    color: var(--gray-600);
    margin-bottom: 0.5rem;
  }

  .hero-name em {
    font-style: italic;
    color: var(--gray-400);
  }

  .hero-title {
    font-family: var(--mono);
    font-size: clamp(0.85rem, 1.5vw, 1rem);
    color: var(--gray-400);
    letter-spacing: 0.06em;
    margin-bottom: 0.75rem;
  }

  .hero-differentiator {
    font-size: 0.95rem;
    color: var(--green);
    margin-bottom: 2rem;
    font-family: var(--mono);
    letter-spacing: 0.03em;
  }

  .hero-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 3rem;
  }

  .tag {
    font-family: var(--mono);
    font-size: 0.75rem;
    padding: 0.35rem 0.85rem;
    border: 1px solid var(--gray-200);
    border-radius: 2px;
    color: var(--gray-400);
    letter-spacing: 0.04em;
    transition: border-color 0.2s, color 0.2s;
    cursor: default;
  }

  .tag:hover { border-color: var(--green); color: var(--green); }

  .hero-meta {
    font-size: 0.85rem;
    color: var(--gray-400);
    margin-bottom: 2.5rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .available-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--green);
    display: inline-block;
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  .hero-ctas {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--accent);
    color: #fff;
    text-decoration: none;
    font-size: 0.85rem;
    font-family: var(--sans);
    font-weight: 500;
    padding: 0.75rem 1.5rem;
    border-radius: 2px;
    letter-spacing: 0.03em;
    transition: background 0.2s, transform 0.15s;
  }

  .btn-primary:hover { background: var(--accent-light); transform: translateY(-1px); }

  .btn-secondary {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: transparent;
    color: var(--gray-600);
    text-decoration: none;
    font-size: 0.85rem;
    font-family: var(--sans);
    font-weight: 500;
    padding: 0.75rem 1.5rem;
    border: 1px solid var(--gray-200);
    border-radius: 2px;
    letter-spacing: 0.03em;
    transition: border-color 0.2s, transform 0.15s;
  }

  .btn-secondary:hover { border-color: var(--gray-400); transform: translateY(-1px); }

  .btn-hire {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--green);
    color: #0b0b0c;
    text-decoration: none;
    font-size: 0.8rem;
    font-family: var(--mono);
    font-weight: 500;
    padding: 0.6rem 1.2rem;
    border-radius: 2px;
    letter-spacing: 0.05em;
    transition: opacity 0.2s, transform 0.15s;
  }

  .btn-hire:hover { opacity: 0.85; transform: translateY(-1px); }

  .hero-scroll {
    position: absolute;
    bottom: 3rem;
    right: 3rem;
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    letter-spacing: 0.1em;
    writing-mode: vertical-rl;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .hero-scroll::after {
    content: '';
    display: block;
    width: 1px;
    height: 3rem;
    background: var(--gray-200);
  }

  /* SECTIONS */
  section {
    padding: 6rem 3rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .section-divider {
    width: 100%;
    height: 1px;
    background: var(--gray-100);
    max-width: 1200px;
    margin: 0 auto;
  }

  .section-label {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    letter-spacing: 0.14em;
    text-transform: uppercase;
    margin-bottom: 3rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .section-label span {
    color: var(--gray-200);
    font-size: 0.65rem;
  }

  /* ABOUT */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem;
    align-items: start;
  }

  .about-heading {
    font-family: var(--serif);
    font-size: clamp(2rem, 4vw, 3.2rem);
    line-height: 1.15;
    color: var(--gray-600);
    margin-bottom: 2rem;
  }

  .about-heading em {
    font-style: italic;
    color: var(--gray-400);
  }

  .about-body {
    font-size: 1.05rem;
    color: var(--gray-600);
    line-height: 1.8;
    margin-bottom: 1.5rem;
  }

  .about-pillars {
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
    margin-top: 1rem;
  }

  .pillar {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
    padding: 1.25rem;
    border: 1px solid var(--gray-100);
    border-radius: 4px;
    background: var(--gray-50);
  }

  .pillar-icon {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    padding-top: 0.15rem;
    min-width: 1.5rem;
  }

  .pillar-text {
    font-size: 0.9rem;
    color: var(--gray-600);
    line-height: 1.6;
  }

  .pillar-text strong {
    display: block;
    color: var(--gray-600);
    font-weight: 600;
    font-size: 0.85rem;
    margin-bottom: 0.2rem;
  }

  /* STATS */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1px;
    background: var(--gray-100);
    border: 1px solid var(--gray-100);
    border-radius: 4px;
    overflow: hidden;
    margin-top: 3rem;
  }

  .stat {
    background: var(--surface);
    padding: 2rem 1.5rem;
    text-align: center;
  }

  .stat-num {
    font-family: var(--serif);
    font-size: 2.2rem;
    color: var(--green);
    display: block;
    margin-bottom: 0.35rem;
  }

  .stat-label {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
  }

  .project-card {
    border: 1px solid var(--gray-100);
    border-radius: 4px;
    padding: 2rem;
    background: var(--surface);
    transition: border-color 0.2s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--accent);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }

  .project-card:hover::before { transform: scaleX(1); }
  .project-card:hover { border-color: var(--gray-200); transform: translateY(-2px); box-shadow: 0 10px 30px rgba(0,255,159,0.08); }

  .project-number {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-200);
    letter-spacing: 0.1em;
    margin-bottom: 1.25rem;
  }

  .project-title {
    font-family: var(--serif);
    font-size: 1.6rem;
    color: var(--gray-600);
    margin-bottom: 0.75rem;
    line-height: 1.2;
  }

  .project-desc {
    font-size: 0.9rem;
    color: var(--gray-600);
    line-height: 1.7;
    margin-bottom: 1.5rem;
  }

  .project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-bottom: 1.75rem;
  }

  .tech-tag {
    font-family: var(--mono);
    font-size: 0.7rem;
    padding: 0.25rem 0.6rem;
    background: var(--gray-50);
    border: 1px solid var(--gray-100);
    border-radius: 2px;
    color: var(--gray-600);
  }

  .project-links {
    display: flex;
    gap: 1rem;
    align-items: center;
  }

  .project-link {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--gray-600);
    text-decoration: none;
    letter-spacing: 0.05em;
    display: flex;
    align-items: center;
    gap: 0.4rem;
    border-bottom: 1px solid var(--gray-200);
    padding-bottom: 1px;
    transition: border-color 0.2s, color 0.2s;
  }

  .project-link:hover { border-color: var(--green); color: var(--green); }

  /* EXPERIENCE */
  .exp-list {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .exp-item {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 3rem;
    padding: 2.5rem 0;
    border-bottom: 1px solid var(--gray-100);
    align-items: start;
  }

  .exp-item:first-child { border-top: 1px solid var(--gray-100); }

  .exp-period {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--gray-400);
    letter-spacing: 0.06em;
    padding-top: 0.2rem;
  }

  .exp-company {
    font-weight: 600;
    font-size: 1rem;
    color: var(--gray-600);
    margin-bottom: 0.2rem;
  }

  .exp-role {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--gray-400);
    letter-spacing: 0.05em;
    margin-bottom: 0.75rem;
  }

  .exp-highlight {
    font-size: 0.9rem;
    color: var(--gray-600);
    line-height: 1.7;
  }

  /* SKILLS */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1px;
    background: var(--gray-100);
    border: 1px solid var(--gray-100);
    border-radius: 4px;
    overflow: hidden;
  }

  .skill-group {
    background: var(--surface);
    padding: 2rem;
  }

  .skill-group-label {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1.25rem;
    display: flex;
    align-items: center;
    gap: 0.6rem;
  }

  .skill-group-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--gray-100);
  }

  .skill-items {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .skill-item {
    font-family: var(--mono);
    font-size: 0.78rem;
    padding: 0.4rem 0.8rem;
    border-radius: 2px;
    color: var(--gray-400);
    background: var(--gray-50);
    border: 1px solid var(--gray-100);
    letter-spacing: 0.02em;
  }

  /* CONTACT */
  .contact-inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6rem;
    align-items: center;
  }

  .contact-heading {
    font-family: var(--serif);
    font-size: clamp(2.5rem, 5vw, 4rem);
    line-height: 1.1;
    color: var(--gray-600);
    margin-bottom: 1.5rem;
  }

  .contact-heading em {
    font-style: italic;
    color: var(--green);
  }

  .contact-body {
    font-size: 1rem;
    color: var(--gray-600);
    line-height: 1.8;
    margin-bottom: 2rem;
  }

  .contact-links {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .contact-link {
    display: flex;
    align-items: center;
    gap: 1rem;
    text-decoration: none;
    padding: 1.25rem 1.5rem;
    border: 1px solid var(--gray-100);
    border-radius: 4px;
    background: var(--gray-50);
    transition: border-color 0.2s, background 0.2s;
  }

  .contact-link:hover {
    border-color: var(--gray-200);
    background: var(--surface);
  }

  .contact-link-label {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .contact-link-value {
    font-size: 0.9rem;
    color: var(--gray-600);
    font-weight: 500;
  }

  .contact-link-icon {
    margin-left: auto;
    color: var(--gray-200);
    font-size: 1rem;
    transition: color 0.2s;
  }

  .contact-link:hover .contact-link-icon { color: var(--gray-400); }

  /* FOOTER */
  footer {
    border-top: 1px solid var(--gray-100);
    padding: 2rem 3rem;
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-copy {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    letter-spacing: 0.06em;
  }

  .footer-back {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--gray-400);
    text-decoration: none;
    letter-spacing: 0.06em;
    transition: color 0.2s;
  }

  .footer-back:hover { color: var(--gray-600); }

  /* ANIMATIONS */
  .fade-in {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }

  .fade-in.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    section { padding: 4rem 1.5rem; }
    .hero { padding: 7rem 1.5rem 4rem; }
    .about-grid { grid-template-columns: 1fr; gap: 3rem; }
    .projects-grid { grid-template-columns: 1fr; }
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .skills-grid { grid-template-columns: 1fr; }
    .contact-inner { grid-template-columns: 1fr; gap: 3rem; }
    .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
    .hero-scroll { display: none; }
    footer { flex-direction: column; gap: 1rem; text-align: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">MR.DEV</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#contact" class="btn-hire">Hire Me</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-label">Senior Data & AI Engineer</div>
  <h1 class="hero-name">Mohith<br><em>Rangineni</em></h1>
  <p class="hero-title">RAG Systems &nbsp;·&nbsp; Multi-Agent AI &nbsp;·&nbsp; LLM Pipelines &nbsp;·&nbsp; Production ML &nbsp;·&nbsp; Cloud Platforms</p>
  <p class="hero-differentiator">→ Production AI Engineer — not prototypes, real systems at scale</p>
  <p style="font-size:0.8rem; color:#8b92a1; font-family:var(--mono); margin-bottom:2rem; letter-spacing:0.03em;">→ Building scalable AI systems that reduce latency, cost, and complexity</p>
  <div class="hero-tags">
    <span class="tag">LangChain</span>
    <span class="tag">Vector DBs</span>
    <span class="tag">AWS · Azure · GCP</span>
    <span class="tag">Apache Spark</span>
    <span class="tag">Python</span>
    <span class="tag">MLOps</span>
  </div>
  <p class="hero-meta">
    <span class="available-dot"></span>
    Irving, TX &nbsp;·&nbsp; Open to Contract / C2C &nbsp;·&nbsp; Immediate
  </p>
  <div class="hero-ctas">
    <a href="#projects" class="btn-primary">View Projects →</a>
    <a href="https://github.com/mohithrangineni-de" target="_blank" class="btn-secondary">GitHub ↗</a>
    <a href="https://www.linkedin.com/in/mohith-data-engineer/" target="_blank" class="btn-secondary">LinkedIn ↗</a>
    <a href="/cdn-cgi/l/email-protection#f88a99969f91969d9691959790918c90c1ceb89f95999194d69b9795" class="btn-secondary">Email ↗</a>
  </div>
  <div style="margin-top:2.5rem; font-family:var(--mono); font-size:0.68rem; color:var(--gray-200); letter-spacing:0.12em;">
    TRUSTED EXPERIENCE &nbsp;·&nbsp; CARDINAL HEALTH &nbsp;·&nbsp; PAYPAL &nbsp;·&nbsp; COSTCO &nbsp;·&nbsp; STATE FARM
  </div>
  <div class="hero-scroll">Scroll down</div>
</div>

<div class="section-divider"></div>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">01 <span>———</span> About</div>
  <div class="about-grid fade-in">
    <div>
      <h2 class="about-heading">I build AI systems<br>that work <em>in production</em></h2>
      <p class="about-body">Senior Data & AI Engineer with 10+ years leading design and deployment of large-scale data platforms and AI systems across AWS, Azure, and GCP.</p>
      <p class="about-body">I specialize in RAG pipelines, multi-agent orchestration, and LLM systems — built for enterprise scale, not just demos.</p>
      <p class="about-body">Currently open to Contract / C2C engagements. I bring production AI expertise to teams building the next generation of intelligent systems.</p>
    </div>
    <div class="about-pillars">
      <div class="pillar">
        <span class="pillar-icon">01</span>
        <div class="pillar-text">
          <strong>Production AI Systems</strong>
          RAG, LLM pipelines, multi-agent workflows — built for scale, observability, and reliability.
        </div>
      </div>
      <div class="pillar">
        <span class="pillar-icon">02</span>
        <div class="pillar-text">
          <strong>Enterprise Data Engineering</strong>
          500M+ daily transactions, 80+ pipelines, 100x query performance improvements.
        </div>
      </div>
      <div class="pillar">
        <span class="pillar-icon">03</span>
        <div class="pillar-text">
          <strong>Cloud Architecture</strong>
          AWS, Azure, GCP — FinOps strategies that reduced cloud costs by 25–40%.
        </div>
      </div>
      <div class="pillar">
        <span class="pillar-icon">04</span>
        <div class="pillar-text">
          <strong>AI Governance & MLOps</strong>
          HIPAA/GDPR compliance, bias detection, LLM observability, prompt evaluation frameworks.
        </div>
      </div>
    </div>
  </div>

  <div class="stats-row fade-in">
    <div class="stat">
      <span class="stat-num">10+</span>
      <span class="stat-label">Years Experience</span>
    </div>
    <div class="stat">
      <span class="stat-num">500M+</span>
      <span class="stat-label">Daily Transactions</span>
    </div>
    <div class="stat">
      <span class="stat-num">100x</span>
      <span class="stat-label">Query Performance</span>
    </div>
    <div class="stat">
      <span class="stat-num">40%</span>
      <span class="stat-label">Cloud Cost Reduction</span>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-label">02 <span>———</span> Featured Projects</div>
  <div class="projects-grid">

    <div class="project-card fade-in">
      <div class="project-number">PROJECT · 001</div>
      <h3 class="project-title">Enterprise RAG System</h3>
      <p class="project-desc">Production-grade Retrieval-Augmented Generation pipeline with semantic search, vector DB optimization, and LLM observability. Built for enterprise-scale document retrieval and question answering with evaluation metrics and HIPAA-compliant data handling.
        <span style="display:block; margin-top:10px; font-family:'DM Mono',monospace; font-size:0.78rem; color:#00ff9f; letter-spacing:0.03em;">→ 60% retrieval latency reduction &nbsp;·&nbsp; 35% accuracy improvement</span>
      </p>
      <div class="project-tech">
        <span class="tech-tag">LangChain</span>
        <span class="tech-tag">FAISS</span>
        <span class="tech-tag">OpenAI</span>
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Vector DB</span>
        <span class="tech-tag">Pinecone</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/mohithrangineni-de/enterprise-rag-system" target="_blank" class="project-link">GitHub ↗</a>
        <a href="https://github.com/mohithrangineni-de/enterprise-rag-system#architecture" target="_blank" class="project-link">Architecture ↗</a>
        <a href="https://github.com/mohithrangineni-de/enterprise-rag-system#readme" target="_blank" class="project-link">Case Study ↗</a>
      </div>
    </div>

    <div class="project-card fade-in">
      <div class="project-number">PROJECT · 002</div>
      <h3 class="project-title">AI Agent Platform</h3>
      <p class="project-desc">Multi-agent orchestration platform with planner, executor, and response agents. Tool-based reasoning with SQL, Python, and RAG integrations. Stateful workflows enabling complex, multi-step AI task execution at enterprise scale.
        <span style="display:block; margin-top:10px; font-family:'DM Mono',monospace; font-size:0.78rem; color:#00ff9f; letter-spacing:0.03em;">→ Multi-step task automation &nbsp;·&nbsp; Tool-integrated reasoning pipeline</span>
      </p>
      <div class="project-tech">
        <span class="tech-tag">LangChain</span>
        <span class="tech-tag">OpenAI</span>
        <span class="tech-tag">Python</span>
        <span class="tech-tag">FastAPI</span>
        <span class="tech-tag">Docker</span>
        <span class="tech-tag">PostgreSQL</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/mohithrangineni-de/enterprise-ai-agent-platform" target="_blank" class="project-link">GitHub ↗</a>
        <a href="https://github.com/mohithrangineni-de/enterprise-ai-agent-platform#architecture" target="_blank" class="project-link">Architecture ↗</a>
        <a href="https://github.com/mohithrangineni-de/enterprise-ai-agent-platform#readme" target="_blank" class="project-link">Case Study ↗</a>
      </div>
    </div>

  </div>
</section>

<div class="section-divider"></div>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-label">03 <span>———</span> Experience</div>
  <div class="exp-list fade-in">
    <div class="exp-item">
      <div class="exp-period">Jan 2024 — Present</div>
      <div>
        <div class="exp-company">Cardinal Health</div>
        <div class="exp-role">SENIOR DATA & AI ENGINEER · Dublin, OH</div>
        <p class="exp-highlight">Architected enterprise RAG systems using LangChain, FAISS, and OpenAI embeddings. Led AI governance initiatives enforcing HIPAA compliance and bias detection. Delivered 100x query performance improvement — Redshift load times from 4+ minutes to under 3 seconds. Managed AWS data platform processing 2–5 TB/day across 80+ pipelines.</p>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-period">Nov 2021 — Dec 2023</div>
      <div>
        <div class="exp-company">PayPal</div>
        <div class="exp-role">DATA & AI ENGINEER · San Jose, CA</div>
        <p class="exp-highlight">Directed predictive fraud pipelines processing 5–10 TB/day with Azure Databricks. Built vector-based semantic search achieving >90% accuracy. Standardized 100+ pipelines with Airflow DAGs, reducing team onboarding from 2 weeks to 2 days.</p>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-period">Jan 2020 — Oct 2021</div>
      <div>
        <div class="exp-company">Costco Wholesale</div>
        <div class="exp-role">SPARK & CLOUD DATA ENGINEER · Issaquah, WA</div>
        <p class="exp-highlight">Spearheaded migration to GCP BigQuery & Dataproc, improving processing efficiency by ~60%. Built real-time streaming pipelines with Cloud Pub/Sub + Dataflow for sub-hour inventory analytics.</p>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-period">Dec 2017 — Dec 2019</div>
      <div>
        <div class="exp-company">State Farm</div>
        <div class="exp-role">BIG DATA ENGINEER · Bloomington, IL</div>
        <p class="exp-highlight">Architected Hadoop/Spark analytics platform processing 500GB–2TB/day. Migrated legacy MapReduce to Spark, reducing processing time by 40%. Built real-time Kafka + Elasticsearch streaming pipelines.</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">04 <span>———</span> Tech Stack</div>
  <div class="skills-grid fade-in">
    <div class="skill-group">
      <div class="skill-group-label">AI / ML / LLM</div>
      <div class="skill-items">
        <span class="skill-item">RAG</span>
        <span class="skill-item">LangChain</span>
        <span class="skill-item">LLM Pipelines</span>
        <span class="skill-item">OpenAI APIs</span>
        <span class="skill-item">Hugging Face</span>
        <span class="skill-item">FAISS</span>
        <span class="skill-item">Pinecone</span>
        <span class="skill-item">Weaviate</span>
        <span class="skill-item">Prompt Engineering</span>
        <span class="skill-item">MLflow</span>
        <span class="skill-item">Vector Embeddings</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Cloud Platforms</div>
      <div class="skill-items">
        <span class="skill-item">AWS</span>
        <span class="skill-item">Azure</span>
        <span class="skill-item">GCP</span>
        <span class="skill-item">Redshift</span>
        <span class="skill-item">SageMaker</span>
        <span class="skill-item">Databricks</span>
        <span class="skill-item">Snowflake</span>
        <span class="skill-item">BigQuery</span>
        <span class="skill-item">Synapse</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Data Engineering</div>
      <div class="skill-items">
        <span class="skill-item">Apache Spark</span>
        <span class="skill-item">PySpark</span>
        <span class="skill-item">Kafka</span>
        <span class="skill-item">Airflow</span>
        <span class="skill-item">dbt</span>
        <span class="skill-item">Delta Lake</span>
        <span class="skill-item">Hadoop</span>
        <span class="skill-item">Hive</span>
        <span class="skill-item">NiFi</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-label">Languages & DevOps</div>
      <div class="skill-items">
        <span class="skill-item">Python</span>
        <span class="skill-item">SQL</span>
        <span class="skill-item">Scala</span>
        <span class="skill-item">Docker</span>
        <span class="skill-item">Kubernetes</span>
        <span class="skill-item">Terraform</span>
        <span class="skill-item">GitHub Actions</span>
        <span class="skill-item">FastAPI</span>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label">05 <span>———</span> Contact</div>
  <div class="contact-inner fade-in">
    <div>
      <h2 class="contact-heading">Let's build production <em>AI systems</em></h2>
      <p class="contact-body">I'm currently open to Contract and C2C engagements. If you're looking for a senior AI/data engineer who ships production systems — not prototypes — let's talk.</p>
      <p class="contact-body">Available immediately · Irving, TX · Remote friendly</p>
    </div>
    <div class="contact-links">
      <a href="/cdn-cgi/l/email-protection#7e0c1f101917101b1017131116170a1647483e19131f1712501d1113" class="contact-link">
        <div>
          <div class="contact-link-label">Email</div>
          <div class="contact-link-value"><span class="__cf_email__" data-cfemail="a3d1c2cdc4cacdc6cdcacecccbcad7cb9a95e3c4cec2cacf8dc0ccce">[email&#160;protected]</span></div>
        </div>
        <span class="contact-link-icon">→</span>
      </a>
      <a href="https://www.linkedin.com/in/mohith-data-engineer/" target="_blank" class="contact-link">
        <div>
          <div class="contact-link-label">LinkedIn</div>
          <div class="contact-link-value">mohith-data-engineer</div>
        </div>
        <span class="contact-link-icon">↗</span>
      </a>
      <a href="https://github.com/mohithrangineni-de" target="_blank" class="contact-link">
        <div>
          <div class="contact-link-label">GitHub</div>
          <div class="contact-link-value">mohithrangineni-de</div>
        </div>
        <span class="contact-link-icon">↗</span>
      </a>
    </div>
  </div>
</section>

<footer>
  <span class="footer-copy">© 2026 Mohith Rangineni · Built with purpose</span>
  <a href="#" class="footer-back">Back to top ↑</a>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  const observer = new IntersectionObserv
