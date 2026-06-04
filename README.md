<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zubair A — GitHub Profile README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&family=Orbitron:wght@700;900&family=Share+Tech+Mono&family=VT323&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #1c2128;
    --border: #30363d;
    --accent: #58a6ff;
    --accent2: #3fb950;
    --accent3: #d2a8ff;
    --amber: #e3b341;
    --coral: #ff7b72;
    --text: #e6edf3;
    --muted: #8b949e;
    --mono: 'Space Mono', monospace;
    --sans: 'Syne', sans-serif;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    min-height: 100vh;
    padding: 2rem;
  }
  .readme-wrap { max-width: 860px; margin: 0 auto; }

  .copy-hint {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 18px;
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 2rem;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .copy-hint span { color: var(--accent); font-family: var(--mono); font-size: 12px; }

  .readme {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }
  .readme-tab-bar {
    background: var(--bg);
    border-bottom: 1px solid var(--border);
    padding: 0 16px;
    display: flex;
  }
  .readme-tab {
    padding: 10px 16px;
    font-size: 13px;
    color: var(--muted);
    border-bottom: 2px solid transparent;
    font-family: var(--mono);
  }
  .readme-tab.active { color: var(--text); border-bottom-color: var(--coral); }
  .readme-body { padding: 2.5rem; }

  /* HERO */
  .hero {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 2rem;
    margin-bottom: 2.5rem;
    flex-wrap: wrap;
  }
  .hero-left { flex: 1; min-width: 260px; }
  .greeting {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--accent2);
    margin-bottom: 6px;
    letter-spacing: 1px;
  }
  .hero-name {
    font-family: 'VT323', monospace;
    font-size: 58px;
    font-weight: 400;
    line-height: 1.05;
    margin-bottom: 10px;
    letter-spacing: 6px;
    text-transform: uppercase;
    color: #00d9ff;
    text-shadow: 0 0 10px rgba(0,217,255,0.7), 0 0 30px rgba(0,217,255,0.3);
    -webkit-text-fill-color: #00d9ff;
  }
  .hero-title {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--coral);
    margin-bottom: 1rem;
    letter-spacing: 0.5px;
  }
  .hero-bio {
    font-size: 15px;
    color: var(--muted);
    line-height: 1.7;
    max-width: 480px;
    margin-bottom: 1.5rem;
  }
  .hero-bio strong { color: var(--text); }
  .badges { display: flex; flex-wrap: wrap; gap: 8px; }
  .badge {
    font-family: var(--mono);
    font-size: 11px;
    padding: 4px 12px;
    border-radius: 20px;
    border: 1px solid;
    letter-spacing: 0.3px;
  }
  .badge-blue   { color: var(--accent);  border-color: rgba(88,166,255,0.3);  background: rgba(88,166,255,0.08); }
  .badge-green  { color: var(--accent2); border-color: rgba(63,185,80,0.3);   background: rgba(63,185,80,0.08); }
  .badge-purple { color: var(--accent3); border-color: rgba(210,168,255,0.3); background: rgba(210,168,255,0.08); }
  .badge-amber  { color: var(--amber);   border-color: rgba(227,179,65,0.3);  background: rgba(227,179,65,0.08); }
  .badge-coral  { color: var(--coral);   border-color: rgba(255,123,114,0.3); background: rgba(255,123,114,0.08); }

  /* RIGHT STAT CARDS */
  .hero-right { display: flex; flex-direction: column; gap: 10px; min-width: 200px; }
  .stat-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .stat-icon { font-size: 18px; }
  .stat-label { font-size: 11px; color: var(--muted); font-family: var(--mono); }
  .stat-val   { font-size: 13px; color: var(--text); font-weight: 600; }

  .divider { border: none; border-top: 1px solid var(--border); margin: 2rem 0; }

  .section-heading {
    font-family: var(--mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 1.2rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-heading::after { content: ''; flex: 1; height: 1px; background: var(--border); }

  /* TECH STACK */
  .tech-grid { display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 2rem; }
  .tech-pill {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 6px 14px;
    font-size: 13px;
    font-family: var(--mono);
    color: var(--text);
    display: flex;
    align-items: center;
    gap: 6px;
    transition: border-color 0.2s;
  }
  .tech-pill:hover { border-color: var(--accent); }
  .tech-pill .dot { width: 6px; height: 6px; border-radius: 50%; }

  /* EXPERIENCE */
  .exp-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    border-radius: 10px;
    padding: 1.25rem 1.5rem;
    margin-bottom: 1rem;
  }
  .exp-header { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 6px; margin-bottom: 10px; }
  .exp-role { font-size: 15px; font-weight: 700; color: var(--text); }
  .exp-company { font-size: 13px; color: var(--accent); font-family: var(--mono); margin-top: 2px; }
  .exp-date {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent2);
    background: rgba(63,185,80,0.08);
    border: 1px solid rgba(63,185,80,0.25);
    border-radius: 20px;
    padding: 3px 10px;
    white-space: nowrap;
  }
  .exp-list { list-style: none; padding: 0; }
  .exp-list li {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.7;
    padding: 3px 0 3px 18px;
    position: relative;
  }
  .exp-list li::before { content: '▸'; position: absolute; left: 0; color: var(--accent2); }
  .exp-list li strong { color: var(--text); }
  .exp-metric {
    display: inline-block;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--amber);
    background: rgba(227,179,65,0.1);
    border: 1px solid rgba(227,179,65,0.25);
    border-radius: 4px;
    padding: 1px 6px;
    margin-left: 4px;
  }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 14px;
    margin-bottom: 2rem;
  }
  .project-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
    text-decoration: none;
    display: block;
    transition: border-color 0.2s, transform 0.15s;
    position: relative;
    overflow: hidden;
  }
  .project-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; }
  .project-card.blue::before   { background: var(--accent); }
  .project-card.green::before  { background: var(--accent2); }
  .project-card.purple::before { background: var(--accent3); }
  .project-card.amber::before  { background: var(--amber); }
  .project-card.coral::before  { background: var(--coral); }
  .project-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .project-card:hover .project-title { color: var(--accent); }
  .project-title {
    font-size: 14px; font-weight: 700; color: var(--text);
    margin-bottom: 6px; display: flex; align-items: center; gap: 6px;
    transition: color 0.2s;
  }
  .project-desc { font-size: 12px; color: var(--muted); line-height: 1.6; margin-bottom: 10px; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .project-tag {
    font-family: var(--mono); font-size: 10px; padding: 2px 8px;
    border-radius: 4px; background: rgba(88,166,255,0.08);
    border: 1px solid rgba(88,166,255,0.2); color: var(--accent);
  }
  .project-tag.green { background: rgba(63,185,80,0.08); border-color: rgba(63,185,80,0.2); color: var(--accent2); }
  .project-tag.purple { background: rgba(210,168,255,0.08); border-color: rgba(210,168,255,0.2); color: var(--accent3); }
  .project-tag.amber { background: rgba(227,179,65,0.08); border-color: rgba(227,179,65,0.2); color: var(--amber); }

  /* STATS */
  .stats-row { display: flex; flex-wrap: wrap; gap: 12px; margin-bottom: 2rem; align-items: center; justify-content: center; }
  .stats-img-placeholder {
    background: var(--surface2); border: 1px dashed var(--border); border-radius: 8px;
    padding: 20px 28px; font-family: var(--mono); font-size: 12px; color: var(--muted);
    text-align: center; flex: 1; min-width: 200px;
  }
  .stats-img-placeholder code { display: block; margin-top: 6px; color: var(--accent); font-size: 11px; }

  /* CONNECT */
  .connect-links { display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 2rem; }
  .connect-link {
    display: flex; align-items: center; gap: 8px;
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 8px; padding: 8px 16px; font-size: 13px;
    color: var(--text); text-decoration: none; font-family: var(--mono);
    transition: border-color 0.2s;
  }
  .connect-link:hover { border-color: var(--accent); color: var(--accent); }

  .readme-footer {
    font-family: var(--mono); font-size: 11px; color: var(--muted);
    text-align: center; padding: 1.5rem 0 0;
    border-top: 1px solid var(--border); line-height: 1.8;
  }

  /* MARKDOWN PANEL */
  .md-panel { margin-top: 2rem; background: var(--bg); border: 1px solid var(--border); border-radius: 12px; overflow: hidden; }
  .md-panel-header {
    background: var(--surface); border-bottom: 1px solid var(--border);
    padding: 10px 18px; display: flex; align-items: center; justify-content: space-between;
  }
  .md-panel-title { font-family: var(--mono); font-size: 12px; color: var(--muted); }
  .copy-btn {
    background: var(--surface2); border: 1px solid var(--border); border-radius: 6px;
    color: var(--accent); font-family: var(--mono); font-size: 11px;
    padding: 4px 12px; cursor: pointer; transition: background 0.15s;
  }
  .copy-btn:hover { background: rgba(88,166,255,0.1); }
  .md-code {
    padding: 1.5rem; font-family: var(--mono); font-size: 12px;
    color: var(--muted); line-height: 1.8; white-space: pre-wrap;
    word-break: break-word; max-height: 480px; overflow-y: auto;
  }
  .md-green  { color: var(--accent2); }
  .md-blue   { color: var(--accent); }
  .md-purple { color: var(--accent3); }
  .md-head   { color: var(--coral); font-weight: bold; }
</style>
</head>
<body>
<div class="readme-wrap">

  <div class="copy-hint">
    <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>
    Visual preview of your GitHub profile README. Scroll down → hit <span>Copy Markdown</span> → paste into your <span>zubair-2k/zubair-2k</span> repo's README.md
  </div>

  <div class="readme">
    <div class="readme-tab-bar">
      <div class="readme-tab active">README.md</div>
      <div class="readme-tab">Preview</div>
    </div>

    <div class="readme-body">

      <!-- HERO -->
      <div class="hero">
        <div class="hero-left">
          <div class="hero-name">Zubair A</div>
          <div class="hero-title">Frontend Developer · React.js</div>
          <p class="hero-bio">
            Frontend Developer building <strong>interactive web apps</strong> with React.js, GSAP animations, and REST APIs. Focused on <strong>clean components</strong> and fast, reliable UI.
          </p>
          <div class="badges">
            <span class="badge badge-green">🟢 Open to Work</span>
            <span class="badge badge-blue">⚛️ React.js</span>
            <span class="badge badge-purple">✨ GSAP Animations</span>
            <span class="badge badge-amber">🌐 REST APIs</span>
          </div>
        </div>
        <div class="hero-right">
          <div class="stat-card">
            <div class="stat-icon">💼</div>
            <div>
              <div class="stat-label">Experience</div>
              <div class="stat-val">1.5+ Years</div>
            </div>
          </div>
          <div class="stat-card">
            <div class="stat-icon">🚀</div>
            <div>
              <div class="stat-label">Projects Shipped</div>
              <div class="stat-val">5+ Live Apps</div>
            </div>
          </div>
          <div class="stat-card">
            <div class="stat-icon">📉</div>
            <div>
              <div class="stat-label">Dev Redundancy Cut</div>
              <div class="stat-val">25% Reduction</div>
            </div>
          </div>
          <div class="stat-card">
            <div class="stat-icon">⚡</div>
            <div>
              <div class="stat-label">Bundle Efficiency</div>
              <div class="stat-val">20% Improved</div>
            </div>
          </div>
        </div>
      </div>

      <hr class="divider">

      <!-- TECH STACK -->
      <div class="section-heading">⚙️ Tech Stack</div>
      <div class="tech-grid">
        <div class="tech-pill"><span class="dot" style="background:#61dafb"></span> React.js</div>
        <div class="tech-pill"><span class="dot" style="background:#f7df1e"></span> JavaScript ES6+</div>
        <div class="tech-pill"><span class="dot" style="background:#e34f26"></span> HTML5</div>
        <div class="tech-pill"><span class="dot" style="background:#264de4"></span> CSS3</div>
        <div class="tech-pill"><span class="dot" style="background:#88ce02"></span> GSAP</div>
        <div class="tech-pill"><span class="dot" style="background:#764abc"></span> Redux</div>
        <div class="tech-pill"><span class="dot" style="background:#3b82f6"></span> REST APIs</div>
        <div class="tech-pill"><span class="dot" style="background:#f05032"></span> Git / GitHub</div>
        <div class="tech-pill"><span class="dot" style="background:#8dd6f9"></span> Webpack</div>
        <div class="tech-pill"><span class="dot" style="background:#51b86a"></span> Render</div>
        <div class="tech-pill"><span class="dot" style="background:#007acc"></span> VS Code</div>
      </div>

      <hr class="divider">

      <!-- EXPERIENCE -->
      <div class="section-heading">🏢 Experience</div>

      <div class="exp-card">
        <div class="exp-header">
          <div>
            <div class="exp-role">Frontend Developer</div>
            <div class="exp-company">Tringapps Private Ltd.</div>
          </div>
          <div class="exp-date">Dec 2021 — May 2023</div>
        </div>
        <ul class="exp-list">
          <li>Developed a <strong>React.js recruitment platform</strong> with secure authentication and MCQ assessment system for candidate evaluation</li>
          <li>Built reusable responsive UI components with real-time response tracking — reduced development redundancy by <span class="exp-metric">25%</span></li>
          <li>Optimized Webpack build pipeline — improved bundle efficiency by <span class="exp-metric">20%</span></li>
          <li>Collaborated with cross-functional teams on end-to-end feature delivery, debugging, and structured code reviews</li>
        </ul>
      </div>

      <hr class="divider">

      <!-- PROJECTS -->
      <div class="section-heading">📦 Projects</div>
      <div class="projects-grid">

        <a class="project-card blue" href="https://zubair-2k.github.io/zubair-exe/" target="_blank">
          <div class="project-title">
            <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            Interactive Portfolio ✨
          </div>
          <div class="project-desc">Dynamic portfolio built with React + GSAP scroll-based animations. Asset size ~1MB for blazing fast load.</div>
          <div class="project-tags">
            <span class="project-tag">React</span>
            <span class="project-tag green">GSAP</span>
            <span class="project-tag purple">Animations</span>
          </div>
        </a>

        <a class="project-card purple" href="https://zubair-2k.github.io/GSAP_Crimson/" target="_blank">
          <div class="project-title">
            <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            Scroll Animation Landing Page
          </div>
          <div class="project-desc">Scroll-driven animations using GSAP ScrollTrigger. Synchronized with scroll behavior, zero lag.</div>
          <div class="project-tags">
            <span class="project-tag">GSAP</span>
            <span class="project-tag green">ScrollTrigger</span>
            <span class="project-tag purple">Performance</span>
          </div>
        </a>

        <a class="project-card green" href="https://zubair-2k.github.io/Cooking-App/" target="_blank">
          <div class="project-title">
            <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            Cooking Recipe App
          </div>
          <div class="project-desc">Scalable recipe app handling 4,000+ records via RESTful API. Dynamic routing + deployed on Render & GitHub Pages.</div>
          <div class="project-tags">
            <span class="project-tag">React</span>
            <span class="project-tag green">REST API</span>
            <span class="project-tag amber">Render</span>
          </div>
        </a>

        <a class="project-card coral" href="https://zubair-2k.github.io/Spiderman_Game/" target="_blank">
          <div class="project-title">
            <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            Spider-Man Parallax Website
          </div>
          <div class="project-desc">Immersive parallax scrolling experience with layered GSAP animations for depth and visual storytelling.</div>
          <div class="project-tags">
            <span class="project-tag">GSAP</span>
            <span class="project-tag green">Parallax</span>
            <span class="project-tag purple">Scroll Perf</span>
          </div>
        </a>

        <a class="project-card amber" href="https://zubair-2k.github.io/Portfolio/" target="_blank">
          <div class="project-title">
            <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            Personal Portfolio v1
          </div>
          <div class="project-desc">First personal portfolio — foundation for iterative UI/UX improvements across later versions.</div>
          <div class="project-tags">
            <span class="project-tag">HTML/CSS</span>
            <span class="project-tag green">UI/UX</span>
            <span class="project-tag purple">JavaScript</span>
          </div>
        </a>

      </div>

      <hr class="divider">

      <!-- GITHUB STATS -->
      <div class="section-heading">📊 GitHub Stats</div>
      <div class="stats-row">
        <div class="stats-img-placeholder">
          📈 GitHub Stats Card
          <code>Live after pasting Markdown into your README</code>
        </div>
        <div class="stats-img-placeholder">
          🗣️ Top Languages Card
          <code>theme=tokyonight · layout=compact</code>
        </div>
      </div>

      <hr class="divider">

      <!-- CONNECT -->
      <div class="section-heading">🤝 Connect</div>
      <div class="connect-links">
        <a class="connect-link" href="https://zubair-2k.github.io/zubair-exe/" target="_blank">🌐 Portfolio</a>
        <a class="connect-link" href="mailto:zubair2kdeveloper@gmail.com">📧 Email</a>
        <a class="connect-link" href="https://github.com/zubair-2k" target="_blank">🐙 GitHub</a>
      </div>

      <div class="readme-footer">
        ⚛️ React.js · JavaScript · GSAP · REST APIs · Webpack<br>
        <img src="https://komarev.com/ghpvc/?username=zubair-2k&color=58a6ff&style=flat-square" alt="profile views" style="vertical-align:middle; margin-top:6px; display:inline;">
      </div>

    </div>
  </div>

  <!-- MARKDOWN COPY PANEL -->
  <div class="md-panel">
    <div class="md-panel-header">
      <span class="md-panel-title">📋 Copy this into your README.md (zubair-2k/zubair-2k repo)</span>
      <button class="copy-btn" onclick="copyMarkdown()">Copy Markdown</button>
    </div>
    <div class="md-code" id="md-content"><span class="md-head"># Hi, I'm Zubair A 👋</span>

<span class="md-green">### Frontend Developer · React.js</span>

<span class="md-blue">> Frontend Developer skilled in React.js, JavaScript, GSAP, and responsive UI development.
> Building interactive web applications with REST API integration and performance optimization.
</span>

![Open to Work](https://img.shields.io/badge/Open%20to%20Work-green?style=flat-square)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

---

<span class="md-head">## ⚙️ Tech Stack</span>

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=greensock&logoColor=black)
![Redux](https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Webpack](https://img.shields.io/badge/Webpack-8DD6F9?style=for-the-badge&logo=webpack&logoColor=black)

---

<span class="md-head">## 💼 Experience</span>

**Frontend Developer — Tringapps Private Ltd.** *(Dec 2021 – May 2023)*

- Developed a **React.js recruitment platform** with secure authentication and MCQ assessment system
- Built reusable responsive UI components with real-time response tracking — reduced redundancy by **25%**
- Optimized Webpack build pipeline — improved bundle efficiency by **20%**
- Collaborated with cross-functional teams on end-to-end delivery, debugging, and code reviews

---

<span class="md-head">## 🚀 Projects</span>

| Project | Description | Live |
|---------|-------------|------|
| **Interactive Portfolio** | React + GSAP scroll animations, ~1MB asset size | [🔗 Live](https://zubair-2k.github.io/zubair-exe/) |
| **Scroll Animation Landing Page** | GSAP ScrollTrigger, zero-lag scroll sync | [🔗 Live](https://zubair-2k.github.io/GSAP_Crimson/) |
| **Cooking Recipe App** | 4,000+ records, RESTful API, Render + GitHub Pages deploy | [🔗 Live](https://zubair-2k.github.io/Cooking-App/) |
| **Spider-Man Parallax Website** | Layered GSAP parallax animations, depth & storytelling | [🔗 Live](https://zubair-2k.github.io/Spiderman_Game/) |
| **Personal Portfolio v1** | First portfolio, iterative UI/UX foundation | [🔗 Live](https://zubair-2k.github.io/Portfolio/) |

---

<span class="md-head">## 📊 GitHub Stats</span>

![Zubair's GitHub stats](https://github-readme-stats.vercel.app/api?username=zubair-2k&show_icons=true&theme=tokyonight&hide_border=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=zubair-2k&layout=compact&theme=tokyonight&hide_border=true)

---

<span class="md-head">## 🤝 Connect with me</span>

[![Portfolio](https://img.shields.io/badge/Portfolio-0d1117?style=for-the-badge&logo=About.me&logoColor=white)](https://zubair-2k.github.io/zubair-exe/)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zubair2kdeveloper@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zubair-2k)

---

<span class="md-purple">⚛️ React.js · JavaScript · GSAP · REST APIs · Webpack</span>

![Profile Views](https://komarev.com/ghpvc/?username=zubair-2k&color=58a6ff&style=flat-square)</div>
  </div>

</div>

<script>
function copyMarkdown() {
  const el = document.getElementById('md-content');
  const text = el.innerText;
  navigator.clipboard.writeText(text).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✅ Copied!';
    setTimeout(() => btn.textContent = 'Copy Markdown', 2000);
  });
}
</script>
</body>
</html>
