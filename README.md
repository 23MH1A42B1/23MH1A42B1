<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Murali Nadipena — GitHub README</title>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html, body {
    background: #0d1117;
    color: #c9d1d9;
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
  }
  .readme-wrap {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 24px 60px;
  }

  /* ── HERO ── */
  .hero-banner {
    width: 100%;
    height: 120px;
    background: linear-gradient(135deg, #0d1117 0%, #1f6feb 60%, #58a6ff 100%);
    clip-path: ellipse(100% 100% at 50% 0%);
    margin-bottom: -20px;
  }
  .hero {
    text-align: center;
    padding: 36px 0 28px;
    position: relative;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -40px; left: 50%;
    transform: translateX(-50%);
    width: 600px; height: 320px;
    background: radial-gradient(ellipse at center, rgba(88,166,255,0.10) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-greeting {
    font-size: 13px;
    color: #58a6ff;
    letter-spacing: 3.5px;
    text-transform: uppercase;
    font-weight: 600;
    margin-bottom: 14px;
  }
  .hero-name {
    font-size: 44px;
    font-weight: 700;
    color: #e6edf3;
    line-height: 1.1;
    margin-bottom: 6px;
  }
  .hero-name span {
    background: linear-gradient(135deg, #58a6ff 0%, #bc8cff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .typing-container {
    font-family: 'Fira Code', monospace;
    font-size: 17px;
    color: #7ee787;
    margin: 18px 0 22px;
    min-height: 30px;
  }
  .cursor {
    display: inline-block;
    width: 2px; height: 19px;
    background: #7ee787;
    animation: blink 1s step-end infinite;
    vertical-align: middle;
    margin-left: 2px;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
  .hero-desc {
    font-size: 15px;
    color: #8b949e;
    max-width: 560px;
    margin: 0 auto 28px;
    line-height: 1.75;
  }
  .socials {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-bottom: 20px;
  }
  .social-badge {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 8px 16px;
    border-radius: 22px;
    font-size: 13px;
    font-weight: 600;
    text-decoration: none;
    transition: transform 0.15s, opacity 0.15s;
  }
  .social-badge:hover { transform: translateY(-2px); opacity: 0.85; }
  .badge-linkedin  { background: #0a66c2; color: #fff; }
  .badge-github    { background: #21262d; color: #e6edf3; border: 1px solid #30363d; }
  .badge-twitter   { background: #1d9bf0; color: #fff; }
  .badge-instagram { background: linear-gradient(45deg,#f58529,#dd2a7b,#515bd4); color:#fff; }
  .badge-reddit    { background: #ff4500; color: #fff; }
  .badge-email     { background: #ea4335; color: #fff; }
  .meta-badges {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .meta-badge {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 6px;
    padding: 4px 12px;
    font-size: 12px;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
  }
  .meta-badge span { color: #58a6ff; font-weight: 600; }

  /* ── DIVIDER ── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, #21262d 20%, #30363d 50%, #21262d 80%, transparent);
    margin: 36px 0;
  }

  /* ── SECTION HEADER ── */
  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 22px;
  }
  .section-header .icon { font-size: 20px; }
  .section-header h2 {
    font-size: 18px;
    font-weight: 700;
    color: #e6edf3;
    white-space: nowrap;
  }
  .section-header .line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, #21262d, transparent);
  }

  /* ── ABOUT ── */
  .about-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    align-items: start;
  }
  @media(max-width:640px){ .about-layout{ grid-template-columns:1fr; } }
  .code-block {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 12px;
    padding: 20px 22px;
    font-family: 'Fira Code', monospace;
    font-size: 13px;
    line-height: 1.8;
    color: #c9d1d9;
  }
  .code-key   { color: #58a6ff; }
  .code-colon { color: #8b949e; }
  .code-val   { color: #7ee787; }
  .code-str   { color: #f0883e; }
  .code-arr   { color: #bc8cff; }
  .code-comment{ color: #484f58; }
  .about-cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }
  .about-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 14px 16px;
    transition: border-color 0.2s, transform 0.2s;
    cursor: default;
  }
  .about-card:hover { border-color: #58a6ff; transform: translateY(-2px); }
  .about-card .label {
    font-size: 10px;
    color: #58a6ff;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-weight: 700;
    margin-bottom: 5px;
  }
  .about-card .value {
    font-size: 12.5px;
    color: #c9d1d9;
    line-height: 1.5;
  }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
  }
  @media(max-width:600px){ .stats-grid{ grid-template-columns:1fr; } }
  .stat-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 12px;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.15s;
  }
  .stat-card:hover { border-color: #30363d; transform: translateY(-2px); }
  .stat-card img { width: 100%; display: block; }
  .stat-card.full { grid-column: 1/-1; }
  .stat-card.half { max-width: 420px; }
  .stat-placeholder {
    padding: 24px;
    text-align: center;
    color: #8b949e;
    font-size: 13px;
  }
  .stat-placeholder small { display: block; color: #484f58; font-size: 11px; margin-top: 4px; }

  /* ── SKILLS ── */
  .skill-category { margin-bottom: 22px; }
  .skill-cat-title {
    font-size: 11px;
    color: #58a6ff;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 700;
    font-family: 'Fira Code', monospace;
    margin-bottom: 14px;
    padding-left: 2px;
  }
  .skill-bars { display: flex; flex-direction: column; gap: 11px; }
  .skill-bar-row {
    display: grid;
    grid-template-columns: 140px 1fr 40px;
    align-items: center;
    gap: 14px;
  }
  .skill-bar-label {
    font-size: 13px;
    color: #c9d1d9;
    font-family: 'Fira Code', monospace;
  }
  .skill-bar-track {
    height: 7px;
    background: #21262d;
    border-radius: 5px;
    overflow: hidden;
  }
  .skill-bar-fill {
    height: 100%;
    border-radius: 5px;
    width: 0;
    transition: width 1.4s cubic-bezier(0.22,1,0.36,1);
  }
  .skill-pct { font-size: 11px; color: #8b949e; font-family: 'Fira Code', monospace; text-align: right; }
  .cl-python  { background: linear-gradient(90deg,#3776ab,#ffd343); }
  .cl-js      { background: linear-gradient(90deg,#f7df1e,#e8a000); }
  .cl-react   { background: linear-gradient(90deg,#61dafb,#0080a6); }
  .cl-sql     { background: linear-gradient(90deg,#4479a1,#23e3ff); }
  .cl-ml      { background: linear-gradient(90deg,#ff6f61,#bc8cff); }
  .cl-node    { background: linear-gradient(90deg,#6da55f,#3b7a3e); }
  .cl-docker  { background: linear-gradient(90deg,#0db7ed,#0060a0); }
  .cl-aws     { background: linear-gradient(90deg,#ff9900,#c46b00); }
  .badge-row  { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px; }
  .tech-pill {
    padding: 5px 13px;
    border-radius: 20px;
    font-size: 12px;
    font-family: 'Fira Code', monospace;
    font-weight: 500;
    border: 1px solid;
    transition: transform 0.15s, box-shadow 0.15s;
    cursor: default;
  }
  .tech-pill:hover { transform: scale(1.06); box-shadow: 0 0 8px rgba(88,166,255,0.2); }
  .pill-blue   { background:#0c2d48; color:#58a6ff; border-color:#1f6feb; }
  .pill-green  { background:#0d2b1d; color:#3fb950; border-color:#1a7f37; }
  .pill-purple { background:#1b1244; color:#bc8cff; border-color:#6e40c9; }
  .pill-orange { background:#2d1b00; color:#f0883e; border-color:#9e6a03; }
  .pill-teal   { background:#0c2d30; color:#39c5cf; border-color:#0e7a82; }
  .pill-red    { background:#2d0e0e; color:#f85149; border-color:#b62324; }
  .pill-yellow { background:#2d2200; color:#e3b341; border-color:#9e6a03; }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px;
  }
  .project-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 12px;
    padding: 20px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
    cursor: default;
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
  }
  .pc-blue::before   { background: linear-gradient(90deg,#58a6ff,#1f6feb); }
  .pc-green::before  { background: linear-gradient(90deg,#3fb950,#1a7f37); }
  .pc-purple::before { background: linear-gradient(90deg,#bc8cff,#6e40c9); }
  .pc-orange::before { background: linear-gradient(90deg,#f0883e,#9e6a03); }
  .project-card:hover { border-color: #30363d; transform: translateY(-3px); }
  .proj-icon { font-size: 26px; margin-bottom: 10px; }
  .proj-name { font-size: 15px; font-weight: 700; color: #e6edf3; margin-bottom: 7px; }
  .proj-desc { font-size: 13px; color: #8b949e; line-height: 1.65; margin-bottom: 14px; }
  .proj-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 14px; }
  .proj-tag {
    padding: 2px 9px;
    background: #21262d;
    border-radius: 10px;
    font-size: 11px;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
  }
  .proj-meta { display: flex; gap: 14px; font-size: 12px; color: #8b949e; }

  /* ── TROPHIES ── */
  .trophy-wrap {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 12px;
    padding: 20px;
    text-align: center;
  }
  .trophy-wrap img { max-width: 100%; border-radius: 8px; }

  /* ── QUOTE ── */
  .quote-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-left: 3px solid #58a6ff;
    border-radius: 0 12px 12px 0;
    padding: 22px 26px;
  }
  .quote-text { font-size: 15px; font-style: italic; color: #c9d1d9; line-height: 1.75; margin-bottom: 10px; }
  .quote-author { font-size: 12px; color: #58a6ff; font-family: 'Fira Code', monospace; }

  /* ── CONNECT ── */
  .connect-section {
    text-align: center;
    padding: 10px 0;
  }
  .connect-section p { font-size: 15px; color: #8b949e; margin-bottom: 20px; line-height: 1.7; }
  .connect-btns { display: flex; flex-wrap: wrap; gap: 12px; justify-content: center; }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 11px 22px;
    border-radius: 8px;
    font-size: 14px;
    font-weight: 600;
    text-decoration: none;
    transition: transform 0.15s, opacity 0.15s;
  }
  .connect-btn:hover { transform: translateY(-2px); opacity: 0.88; }
  .btn-linkedin { background: #0a66c2; color: #fff; }
  .btn-email    { background: #ea4335; color: #fff; }
  .btn-github   { background: #21262d; color: #e6edf3; border: 1px solid #30363d; }

  /* ── FOOTER BANNER ── */
  .footer-banner {
    width: 100%;
    height: 100px;
    background: linear-gradient(135deg, #58a6ff 0%, #1f6feb 50%, #0d1117 100%);
    clip-path: ellipse(100% 100% at 50% 100%);
    margin-top: 40px;
  }
  .footer-text {
    text-align: center;
    margin-top: -60px;
    padding-top: 10px;
    font-size: 12px;
    color: #484f58;
    font-family: 'Fira Code', monospace;
  }
  .footer-text span { color: #f85149; }
  .footer-text a { color: #58a6ff; text-decoration: none; }
</style>
</head>
<body>

<div class="hero-banner"></div>

<div class="readme-wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-greeting">Welcome to my GitHub</div>
    <div class="hero-name">Hi, I'm <span>Murali Nadipena</span> 👋</div>
    <div class="typing-container">
      <span id="typed"></span><span class="cursor"></span>
    </div>
    <div class="hero-desc">
      Full Stack Developer &amp; ML Enthusiast — turning raw data into intelligent applications.
      Building scalable systems from Kakinada ☁️ to the cloud.
    </div>
    <div class="socials">
      <a class="social-badge badge-linkedin" href="https://www.linkedin.com/in/murali-nadipena-5960782b2/" target="_blank">in LinkedIn</a>
      <a class="social-badge badge-github" href="https://github.com/23mh1a42b1" target="_blank">⌥ GitHub</a>
      <a class="social-badge badge-twitter" href="https://x.com/_murali_13" target="_blank">𝕏 Twitter</a>
      <a class="social-badge badge-instagram" href="https://instagram.com/_murali__13" target="_blank">◈ Instagram</a>
      <a class="social-badge badge-reddit" href="https://reddit.com/user/murali__13" target="_blank">◉ Reddit</a>
      <a class="social-badge badge-email" href="mailto:nadipenamurali13@gmail.com">✉ Email</a>
    </div>
    <div class="meta-badges">
      <div class="meta-badge">👁 Profile Views: <span>Loading…</span></div>
      <div class="meta-badge">📍 Kakinada, India 🇮🇳</div>
      <div class="meta-badge">⚡ Open to Collaborate</div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ABOUT -->
  <div class="section-header">
    <span class="icon">👤</span>
    <h2>About Me</h2>
    <div class="line"></div>
  </div>
  <div class="about-layout">
    <div class="code-block">
      <div><span class="code-key">name</span><span class="code-colon">: </span><span class="code-str">"Murali Nadipena"</span></div>
      <div><span class="code-key">location</span><span class="code-colon">: </span><span class="code-str">"Kakinada, AP 🇮🇳"</span></div>
      <div><span class="code-key">role</span><span class="code-colon">: </span><span class="code-str">"Full Stack Dev &amp; ML Enthusiast"</span></div>
      <div style="margin-top:6px"><span class="code-key">currently_working_on</span><span class="code-colon">:</span></div>
      <div style="padding-left:16px"><span class="code-arr">- </span><span class="code-val">Full Stack Development</span></div>
      <div style="padding-left:16px"><span class="code-arr">- </span><span class="code-val">AI-based Projects</span></div>
      <div style="margin-top:6px"><span class="code-key">learning</span><span class="code-colon">:</span></div>
      <div style="padding-left:16px"><span class="code-arr">- </span><span class="code-val">Machine Learning</span></div>
      <div style="padding-left:16px"><span class="code-arr">- </span><span class="code-val">Data Analytics</span></div>
      <div style="padding-left:16px"><span class="code-arr">- </span><span class="code-val">Scalable Data Pipelines</span></div>
      <div style="margin-top:6px"><span class="code-key">ask_me_about</span><span class="code-colon">: </span><span class="code-str">"Python, SQL, Web Dev"</span></div>
      <div><span class="code-key">fun_fact</span><span class="code-colon">: </span><span class="code-str">"Data → Insights ✨"</span></div>
    </div>
    <div class="about-cards">
      <div class="about-card">
        <div class="label">🔭 Working On</div>
        <div class="value">Full Stack & AI projects</div>
      </div>
      <div class="about-card">
        <div class="label">🌱 Learning</div>
        <div class="value">ML & Data Pipelines</div>
      </div>
      <div class="about-card">
        <div class="label">👯 Collaborate</div>
        <div class="value">ML models & Web Apps</div>
      </div>
      <div class="about-card">
        <div class="label">💬 Ask Me</div>
        <div class="value">Python · SQL · React</div>
      </div>
      <div class="about-card">
        <div class="label">⚡ Fun Fact</div>
        <div class="value">Data into insights daily</div>
      </div>
      <div class="about-card">
        <div class="label">📍 Location</div>
        <div class="value">Kakinada, India 🇮🇳</div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- STATS -->
  <div class="section-header">
    <span class="icon">📊</span>
    <h2>GitHub Stats</h2>
    <div class="line"></div>
  </div>
  <div class="stats-grid">
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api?username=23mh1a42b1&show_icons=true&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9&rank_icon=github" alt="GitHub Stats"
        onerror="this.parentNode.innerHTML='<div class=stat-placeholder>📊 GitHub Stats<br><small>Public repos needed to display</small></div>'"/>
    </div>
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=23mh1a42b1&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&text_color=c9d1d9&layout=compact&langs_count=8" alt="Top Languages"
        onerror="this.parentNode.innerHTML='<div class=stat-placeholder>🗣 Top Languages<br><small>Push some code to see this</small></div>'"/>
    </div>
    <div class="stat-card full">
      <img src="https://github-readme-streak-stats.herokuapp.com?user=23mh1a42b1&theme=github-dark-blue&hide_border=true&background=161b22&stroke=30363d&ring=58a6ff&fire=f0883e&currStreakLabel=58a6ff&sideLabels=8b949e&dates=484f58" alt="Streak Stats"
        onerror="this.parentNode.innerHTML='<div class=stat-placeholder>🔥 Streak Stats<br><small>Start contributing to see your streak!</small></div>'"/>
    </div>
  </div>

  <div class="divider"></div>

  <!-- SKILLS -->
  <div class="section-header">
    <span class="icon">🛠</span>
    <h2>Skills &amp; Tech Stack</h2>
    <div class="line"></div>
  </div>

  <div class="skill-category">
    <div class="skill-cat-title">// proficiency levels</div>
    <div class="skill-bars" id="bars">
      <div class="skill-bar-row"><span class="skill-bar-label">Python</span><div class="skill-bar-track"><div class="skill-bar-fill cl-python" data-w="88"></div></div><span class="skill-pct">88%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">SQL</span><div class="skill-bar-track"><div class="skill-bar-fill cl-sql" data-w="85"></div></div><span class="skill-pct">85%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">JavaScript</span><div class="skill-bar-track"><div class="skill-bar-fill cl-js" data-w="82"></div></div><span class="skill-pct">82%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">React</span><div class="skill-bar-track"><div class="skill-bar-fill cl-react" data-w="78"></div></div><span class="skill-pct">78%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">Node.js</span><div class="skill-bar-track"><div class="skill-bar-fill cl-node" data-w="74"></div></div><span class="skill-pct">74%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">ML / AI</span><div class="skill-bar-track"><div class="skill-bar-fill cl-ml" data-w="72"></div></div><span class="skill-pct">72%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">Docker</span><div class="skill-bar-track"><div class="skill-bar-fill cl-docker" data-w="65"></div></div><span class="skill-pct">65%</span></div>
      <div class="skill-bar-row"><span class="skill-bar-label">AWS / Azure</span><div class="skill-bar-track"><div class="skill-bar-fill cl-aws" data-w="60"></div></div><span class="skill-pct">60%</span></div>
    </div>
  </div>

  <div class="skill-category">
    <div class="skill-cat-title">// languages &amp; frameworks</div>
    <div class="badge-row">
      <span class="tech-pill pill-blue">Python</span>
      <span class="tech-pill pill-yellow">JavaScript</span>
      <span class="tech-pill pill-orange">Java</span>
      <span class="tech-pill pill-blue">C++</span>
      <span class="tech-pill pill-teal">React</span>
      <span class="tech-pill pill-green">Node.js</span>
      <span class="tech-pill pill-teal">FastAPI</span>
      <span class="tech-pill pill-teal">TailwindCSS</span>
      <span class="tech-pill pill-green">NumPy</span>
      <span class="tech-pill pill-purple">Pandas</span>
    </div>
  </div>

  <div class="skill-category">
    <div class="skill-cat-title">// cloud &amp; databases</div>
    <div class="badge-row">
      <span class="tech-pill pill-orange">AWS</span>
      <span class="tech-pill pill-blue">Azure</span>
      <span class="tech-pill pill-orange">Firebase</span>
      <span class="tech-pill pill-teal">Snowflake</span>
      <span class="tech-pill pill-green">MongoDB</span>
      <span class="tech-pill pill-blue">MySQL</span>
      <span class="tech-pill pill-green">Supabase</span>
      <span class="tech-pill pill-blue">SQLite</span>
    </div>
  </div>

  <div class="skill-category">
    <div class="skill-cat-title">// tools &amp; devops</div>
    <div class="badge-row">
      <span class="tech-pill pill-red">Docker</span>
      <span class="tech-pill pill-orange">Git</span>
      <span class="tech-pill pill-purple">GitHub</span>
      <span class="tech-pill pill-orange">Postman</span>
      <span class="tech-pill pill-yellow">Power BI</span>
      <span class="tech-pill pill-blue">Jira</span>
      <span class="tech-pill pill-red">Figma</span>
      <span class="tech-pill pill-teal">Canva</span>
      <span class="tech-pill pill-orange">Adobe PS</span>
      <span class="tech-pill pill-blue">Lightroom</span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- PROJECTS -->
  <div class="section-header">
    <span class="icon">🚀</span>
    <h2>Featured Projects</h2>
    <div class="line"></div>
  </div>
  <div class="projects-grid">
    <div class="project-card pc-blue">
      <div class="proj-icon">🤖</div>
      <div class="proj-name">AI Data Insights Engine</div>
      <div class="proj-desc">End-to-end ML pipeline that transforms raw datasets into actionable dashboards with natural language querying.</div>
      <div class="proj-tags">
        <span class="proj-tag">Python</span><span class="proj-tag">FastAPI</span><span class="proj-tag">Pandas</span><span class="proj-tag">React</span>
      </div>
      <div class="proj-meta"><span>⭐ Stars</span><span>🍴 Forks</span><span>🟡 Python</span></div>
    </div>
    <div class="project-card pc-green">
      <div class="proj-icon">📊</div>
      <div class="proj-name">Snowflake Analytics Dashboard</div>
      <div class="proj-desc">Real-time BI dashboard connecting Snowflake data warehouse with interactive visualizations and live queries.</div>
      <div class="proj-tags">
        <span class="proj-tag">Snowflake</span><span class="proj-tag">SQL</span><span class="proj-tag">Node.js</span><span class="proj-tag">Recharts</span>
      </div>
      <div class="proj-meta"><span>⭐ Stars</span><span>🍴 Forks</span><span>🟢 JS</span></div>
    </div>
    <div class="project-card pc-purple">
      <div class="proj-icon">🧠</div>
      <div class="proj-name">ML Model Deployment Kit</div>
      <div class="proj-desc">Containerized boilerplate for training, versioning, and deploying ML models to AWS with full CI/CD pipelines.</div>
      <div class="proj-tags">
        <span class="proj-tag">Docker</span><span class="proj-tag">AWS</span><span class="proj-tag">FastAPI</span><span class="proj-tag">GH Actions</span>
      </div>
      <div class="proj-meta"><span>⭐ Stars</span><span>🍴 Forks</span><span>🔵 Python</span></div>
    </div>
    <div class="project-card pc-orange">
      <div class="proj-icon">🌐</div>
      <div class="proj-name">Full Stack Web App Starter</div>
      <div class="proj-desc">Production-ready React + Node.js template with Supabase auth, Tailwind UI, and Firebase integrations baked in.</div>
      <div class="proj-tags">
        <span class="proj-tag">React</span><span class="proj-tag">Node.js</span><span class="proj-tag">Supabase</span><span class="proj-tag">Tailwind</span>
      </div>
      <div class="proj-meta"><span>⭐ Stars</span><span>🍴 Forks</span><span>🟡 JS</span></div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- TROPHIES -->
  <div class="section-header">
    <span class="icon">🏆</span>
    <h2>GitHub Trophies</h2>
    <div class="line"></div>
  </div>
  <div class="trophy-wrap">
    <img src="https://github-profile-trophy.vercel.app/?username=23mh1a42b1&theme=algolia&no-frame=true&no-bg=true&margin-w=8&column=7"
      alt="Trophies"
      onerror="this.parentNode.innerHTML='<div style=\'color:#8b949e;font-size:13px;padding:10px\'>🏆 Trophies will appear here as you contribute more to GitHub!</div>'"/>
  </div>

  <div class="divider"></div>

  <!-- QUOTE -->
  <div class="section-header">
    <span class="icon">✍️</span>
    <h2>Dev Quote</h2>
    <div class="line"></div>
  </div>
  <div class="quote-card">
    <div class="quote-text" id="quote-text"></div>
    <div class="quote-author" id="quote-author"></div>
  </div>

  <div class="divider"></div>

  <!-- CONNECT -->
  <div class="section-header">
    <span class="icon">📬</span>
    <h2>Connect With Me</h2>
    <div class="line"></div>
  </div>
  <div class="connect-section">
    <p>I'm always open to interesting conversations, collaborations, and new opportunities!<br/>Feel free to reach out — let's build something great together. 🚀</p>
    <div class="connect-btns">
      <a class="connect-btn btn-linkedin" href="https://www.linkedin.com/in/murali-nadipena-5960782b2/" target="_blank">in  Connect on LinkedIn</a>
      <a class="connect-btn btn-email" href="mailto:nadipenamurali13@gmail.com">✉  Send an Email</a>
      <a class="connect-btn btn-github" href="https://github.com/23mh1a42b1" target="_blank">⌥  Visit GitHub</a>
    </div>
  </div>

</div>

<!-- FOOTER -->
<div class="footer-banner"></div>
<div class="footer-text">
  <a href="mailto:nadipenamurali13@gmail.com">nadipenamurali13@gmail.com</a>
  &nbsp;·&nbsp; Built with <span>♥</span> &nbsp;·&nbsp; Kakinada, India 🇮🇳
  <br/><br/>
</div>

<script>
  // Typing animation
  const phrases = [
    'Full Stack Developer 💻',
    'ML Enthusiast 🤖',
    'Data Analyst 📊',
    'Python Lover 🐍',
    'Building Intelligent Apps ✨',
    'Turning Data into Insights 🔍'
  ];
  let pi = 0, ci = 0, deleting = false;
  const el = document.getElementById('typed');
  function type() {
    const word = phrases[pi];
    if (!deleting) {
      el.textContent = word.slice(0, ++ci);
      if (ci === word.length) { deleting = true; setTimeout(type, 2000); return; }
    } else {
      el.textContent = word.slice(0, --ci);
      if (ci === 0) { deleting = false; pi = (pi + 1) % phrases.length; }
    }
    setTimeout(type, deleting ? 40 : 75);
  }
  type();

  // Animate skill bars
  setTimeout(() => {
    document.querySelectorAll('.skill-bar-fill').forEach(b => {
      b.style.width = b.dataset.w + '%';
    });
  }, 400);

  // Rotating quotes
  const quotes = [
    { q: '"Any fool can write code that a computer can understand. Good programmers write code that humans can understand."', a: '— Martin Fowler' },
    { q: '"First, solve the problem. Then, write the code."', a: '— John Johnson' },
    { q: '"In God we trust. All others must bring data."', a: '— W. Edwards Deming' },
    { q: '"The best way to predict the future is to invent it."', a: '— Alan Kay' },
    { q: '"Data is the new oil. But like oil, it must be refined to be useful."', a: '— Clive Humby' },
    { q: '"It always seems impossible until it\'s done."', a: '— Nelson Mandela' },
  ];
  const q = quotes[Math.floor(Math.random() * quotes.length)];
  document.getElementById('quote-text').textContent = q.q;
  document.getElementById('quote-author').textContent = q.a;
</script>
</body>
</html>
