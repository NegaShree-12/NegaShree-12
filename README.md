<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nega Shree S — AI/ML Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #050810;
    --surface: #0c1120;
    --surface2: #111827;
    --border: #1e2d4a;
    --accent: #6a0dad;
    --accent2: #00e5ff;
    --accent3: #ff6b6b;
    --accent4: #a855f7;
    --text: #e2e8f0;
    --text-muted: #64748b;
    --text-dim: #94a3b8;
    --green: #22c55e;
    --gold: #f59e0b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* HERO */
  .hero {
    position: relative;
    min-height: 320px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 60px 24px 80px;
    overflow: hidden;
  }

  .hero-bg {
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, #0d1f40 0%, #1a0533 40%, #001a30 100%);
    z-index: 0;
  }

  .hero-bg::after {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 60% 50% at 50% 0%, rgba(106,13,173,0.35) 0%, transparent 70%),
      radial-gradient(ellipse 40% 40% at 80% 80%, rgba(0,229,255,0.12) 0%, transparent 60%);
  }

  .grid-overlay {
    position: absolute;
    inset: 0;
    background-image: linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
                      linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    z-index: 1;
  }

  .hero-content { position: relative; z-index: 2; }

  .hero-badge {
    display: inline-block;
    background: rgba(106,13,173,0.25);
    border: 1px solid rgba(106,13,173,0.5);
    color: var(--accent4);
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 6px 16px;
    border-radius: 100px;
    margin-bottom: 20px;
    animation: fadeDown 0.6s ease both;
  }

  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(42px, 8vw, 80px);
    font-weight: 800;
    letter-spacing: -2px;
    line-height: 1;
    background: linear-gradient(135deg, #fff 30%, var(--accent4) 70%, var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 16px;
    animation: fadeDown 0.6s 0.1s ease both;
  }

  .hero-tagline {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--text-dim);
    letter-spacing: 1px;
    animation: fadeDown 0.6s 0.2s ease both;
  }

  .hero-tagline span {
    color: var(--accent2);
    margin: 0 8px;
  }

  .hero-stats {
    display: flex;
    gap: 32px;
    justify-content: center;
    margin-top: 40px;
    animation: fadeUp 0.6s 0.4s ease both;
    flex-wrap: wrap;
  }

  .stat-item {
    text-align: center;
  }

  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 800;
    color: var(--accent2);
    display: block;
  }

  .stat-label {
    font-size: 11px;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 1px;
    font-family: 'Space Mono', monospace;
  }

  .stat-divider {
    width: 1px;
    height: 40px;
    background: var(--border);
    align-self: center;
  }

  /* WAVE */
  .wave-divider {
    width: 100%;
    margin-top: -2px;
    line-height: 0;
  }

  /* MAIN LAYOUT */
  .container {
    max-width: 960px;
    margin: 0 auto;
    padding: 0 24px;
  }

  /* SECTION */
  section {
    padding: 60px 0;
    border-bottom: 1px solid var(--border);
  }

  section:last-child { border-bottom: none; }

  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--accent2);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, var(--border), transparent);
  }

  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 32px;
    font-weight: 700;
    margin-bottom: 32px;
    color: #fff;
  }

  /* ABOUT */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }

  .about-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    transition: border-color 0.3s, transform 0.3s;
  }

  .about-card:hover {
    border-color: var(--accent4);
    transform: translateY(-3px);
  }

  .about-card.full { grid-column: 1 / -1; }

  .code-block {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    line-height: 1.8;
    color: var(--text-dim);
  }

  .code-keyword { color: #c678dd; }
  .code-class { color: #e5c07b; }
  .code-func { color: #61afef; }
  .code-str { color: #98c379; }
  .code-num { color: #d19a66; }
  .code-comment { color: #5c6370; }
  .code-attr { color: #e06c75; }

  .about-bullets { list-style: none; }

  .about-bullets li {
    padding: 10px 0;
    border-bottom: 1px solid var(--border);
    font-size: 14px;
    color: var(--text-dim);
    display: flex;
    align-items: flex-start;
    gap: 12px;
  }

  .about-bullets li:last-child { border-bottom: none; }
  .about-bullets li .icon { font-size: 16px; flex-shrink: 0; margin-top: 1px; }

  /* SKILLS */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
  }

  .skill-category {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 20px;
    transition: border-color 0.3s;
  }

  .skill-category:hover { border-color: rgba(106,13,173,0.4); }

  .skill-cat-title {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 13px;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 1.5px;
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tag {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    padding: 5px 12px;
    border-radius: 6px;
    border: 1px solid;
    transition: all 0.2s;
    cursor: default;
  }

  .tag:hover { transform: scale(1.05); }

  .tag-purple { color: #c084fc; border-color: rgba(192,132,252,0.3); background: rgba(192,132,252,0.05); }
  .tag-blue { color: #60a5fa; border-color: rgba(96,165,250,0.3); background: rgba(96,165,250,0.05); }
  .tag-cyan { color: #22d3ee; border-color: rgba(34,211,238,0.3); background: rgba(34,211,238,0.05); }
  .tag-green { color: #4ade80; border-color: rgba(74,222,128,0.3); background: rgba(74,222,128,0.05); }
  .tag-orange { color: #fb923c; border-color: rgba(251,146,60,0.3); background: rgba(251,146,60,0.05); }
  .tag-pink { color: #f472b6; border-color: rgba(244,114,182,0.3); background: rgba(244,114,182,0.05); }
  .tag-yellow { color: #fbbf24; border-color: rgba(251,191,36,0.3); background: rgba(251,191,36,0.05); }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 28px;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    right: 0; height: 3px;
    background: var(--card-accent, linear-gradient(90deg, var(--accent), var(--accent2)));
  }

  .project-card:hover {
    border-color: rgba(106,13,173,0.4);
    transform: translateY(-4px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
  }

  .project-card.featured { grid-column: 1 / -1; }

  .project-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    margin-bottom: 12px;
    gap: 12px;
  }

  .project-icon {
    width: 42px;
    height: 42px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    flex-shrink: 0;
  }

  .project-name {
    font-family: 'Syne', sans-serif;
    font-size: 18px;
    font-weight: 700;
    color: #fff;
  }

  .project-desc {
    font-size: 13px;
    color: var(--text-dim);
    margin-bottom: 16px;
    line-height: 1.7;
  }

  .project-features {
    list-style: none;
    margin-bottom: 16px;
  }

  .project-features li {
    font-size: 12px;
    color: var(--text-dim);
    padding: 3px 0;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .project-features li::before {
    content: '→';
    color: var(--accent2);
    font-family: 'Space Mono', monospace;
    font-size: 11px;
  }

  .project-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .stack-pill {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    padding: 3px 10px;
    border-radius: 4px;
    background: rgba(106,13,173,0.15);
    color: var(--accent4);
    border: 1px solid rgba(106,13,173,0.25);
  }

  .project-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--accent2);
    text-decoration: none;
    margin-top: 14px;
    transition: gap 0.2s;
  }

  .project-link:hover { gap: 10px; }

  /* LEETCODE */
  .lc-container {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 32px;
  }

  .lc-header {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 32px;
  }

  .lc-logo {
    width: 48px;
    height: 48px;
    background: rgba(255,161,22,0.1);
    border: 1px solid rgba(255,161,22,0.3);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 22px;
  }

  .lc-username {
    font-family: 'Syne', sans-serif;
    font-size: 22px;
    font-weight: 700;
    color: #fff;
  }

  .lc-rank {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--text-muted);
  }

  .lc-stats {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 32px;
    align-items: center;
  }

  .lc-total {
    text-align: center;
    position: relative;
  }

  .lc-circle {
    width: 110px;
    height: 110px;
    border-radius: 50%;
    background: conic-gradient(
      #22c55e 0deg 163deg,
      #f59e0b 163deg 330deg,
      #ef4444 330deg 360deg
    );
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  .lc-circle::after {
    content: '';
    position: absolute;
    width: 80px;
    height: 80px;
    border-radius: 50%;
    background: var(--surface);
  }

  .lc-circle-num {
    position: absolute;
    z-index: 1;
    font-family: 'Syne', sans-serif;
    font-size: 26px;
    font-weight: 800;
    color: #fff;
  }

  .lc-bars { display: flex; flex-direction: column; gap: 14px; }

  .lc-bar-row {
    display: grid;
    grid-template-columns: 60px 1fr 80px;
    gap: 12px;
    align-items: center;
    font-size: 13px;
  }

  .lc-diff { font-family: 'Space Mono', monospace; font-size: 12px; }
  .lc-diff.easy { color: #22c55e; }
  .lc-diff.medium { color: #f59e0b; }
  .lc-diff.hard { color: #ef4444; }

  .bar-track {
    height: 8px;
    background: var(--surface2);
    border-radius: 4px;
    overflow: hidden;
  }

  .bar-fill {
    height: 100%;
    border-radius: 4px;
    transition: width 1s ease;
  }

  .bar-easy { background: #22c55e; }
  .bar-medium { background: #f59e0b; }
  .bar-hard { background: #ef4444; }

  .lc-count {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--text-muted);
    text-align: right;
  }

  /* EXPERIENCE */
  .timeline { position: relative; padding-left: 28px; }

  .timeline::before {
    content: '';
    position: absolute;
    left: 0; top: 8px; bottom: 8px;
    width: 2px;
    background: linear-gradient(to bottom, var(--accent), transparent);
  }

  .timeline-item {
    position: relative;
    padding-bottom: 40px;
  }

  .timeline-item:last-child { padding-bottom: 0; }

  .timeline-dot {
    position: absolute;
    left: -33px;
    top: 4px;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--accent2);
    border: 2px solid var(--bg);
  }

  .timeline-date {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--accent2);
    letter-spacing: 1px;
    margin-bottom: 6px;
  }

  .timeline-company {
    font-family: 'Syne', sans-serif;
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    margin-bottom: 4px;
  }

  .timeline-role {
    font-size: 13px;
    color: var(--text-muted);
    margin-bottom: 16px;
    font-family: 'Space Mono', monospace;
  }

  .timeline-points { list-style: none; }

  .timeline-points li {
    font-size: 14px;
    color: var(--text-dim);
    padding: 6px 0;
    padding-left: 20px;
    position: relative;
  }

  .timeline-points li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--accent4);
    font-size: 11px;
  }

  /* ACHIEVEMENTS */
  .achievements-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
  }

  .ach-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: all 0.3s;
  }

  .ach-card:hover {
    border-color: rgba(245,158,11,0.4);
    transform: translateY(-3px);
  }

  .ach-icon { font-size: 28px; margin-bottom: 10px; }

  .ach-title {
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: #fff;
    margin-bottom: 6px;
  }

  .ach-org {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--text-muted);
  }

  /* CONNECT */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 24px;
    border-radius: 10px;
    text-decoration: none;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 1px;
    transition: all 0.25s;
    border: 1px solid;
  }

  .connect-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.3);
  }

  .btn-github { color: #fff; border-color: #333; background: #1c1c1c; }
  .btn-linkedin { color: #fff; border-color: #0a66c2; background: rgba(10,102,194,0.15); }
  .btn-leetcode { color: #ffa116; border-color: rgba(255,161,22,0.4); background: rgba(255,161,22,0.08); }
  .btn-email { color: #ea4335; border-color: rgba(234,67,53,0.4); background: rgba(234,67,53,0.08); }

  /* CURRENT FOCUS */
  .focus-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }

  .focus-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .focus-card::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--card-bg, transparent);
    opacity: 0.05;
  }

  .focus-icon { font-size: 24px; margin-bottom: 10px; }
  .focus-title {
    font-family: 'Syne', sans-serif;
    font-size: 15px;
    font-weight: 700;
    color: #fff;
    margin-bottom: 6px;
  }
  .focus-desc { font-size: 12px; color: var(--text-muted); }

  /* FOOTER */
  .footer {
    text-align: center;
    padding: 48px 24px;
    position: relative;
    overflow: hidden;
  }

  .footer-wave {
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent3), var(--accent));
    background-size: 200%;
    animation: shimmer 3s linear infinite;
  }

  .footer-text {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--text-muted);
  }

  .footer-text span {
    color: var(--accent4);
  }

  /* ANIMATIONS */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes shimmer {
    from { background-position: 0% 0; }
    to { background-position: 200% 0; }
  }

  /* RESPONSIVE */
  @media (max-width: 640px) {
    .about-grid, .projects-grid, .focus-grid { grid-template-columns: 1fr; }
    .project-card.featured { grid-column: 1; }
    .lc-stats { grid-template-columns: 1fr; }
    .hero-stats { gap: 16px; }
    .stat-divider { display: none; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-bg"></div>
  <div class="grid-overlay"></div>
  <div class="hero-content">
    <div class="hero-badge">B.Tech AI & ML · BIT · CGPA 8.72</div>
    <h1>Nega Shree S</h1>
    <p class="hero-tagline">
      AI/ML Engineer <span>·</span> Full Stack Developer <span>·</span> Blockchain Enthusiast
    </p>
    <div class="hero-stats">
      <div class="stat-item">
        <span class="stat-num">389+</span>
        <span class="stat-label">DSA Solved</span>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-item">
        <span class="stat-num">4</span>
        <span class="stat-label">Hackathons</span>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-item">
        <span class="stat-num">2</span>
        <span class="stat-label">Internships</span>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-item">
        <span class="stat-num">239</span>
        <span class="stat-label">Contributions</span>
      </div>
    </div>
  </div>
</div>

<!-- MAIN -->
<div style="background: var(--bg);">
<div class="container">

  <!-- ABOUT -->
  <section>
    <div class="section-label">00 · About</div>
    <div class="section-title">Who I Am</div>
    <div class="about-grid">
      <div class="about-card">
        <div class="code-block">
          <div><span class="code-keyword">class</span> <span class="code-class">NegaShree</span>:</div>
          <div>&nbsp;&nbsp;<span class="code-keyword">def</span> <span class="code-func">__init__</span>(self):</div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;self.<span class="code-attr">name</span> = <span class="code-str">"Nega Shree S"</span></div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;self.<span class="code-attr">role</span> = <span class="code-str">"AI/ML Engineer"</span></div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;self.<span class="code-attr">cgpa</span> = <span class="code-num">8.72</span></div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;self.<span class="code-attr">interests</span> = [</div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-str">"AI/ML"</span>, <span class="code-str">"Blockchain"</span>,</div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-str">"Full Stack"</span>, <span class="code-str">"System Design"</span></div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;]</div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;self.<span class="code-attr">dsa_solved</span> = <span class="code-num">389</span></div>
          <br>
          <div>&nbsp;&nbsp;<span class="code-keyword">def</span> <span class="code-func">say_hi</span>(self):</div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-func">print</span>(<span class="code-str">"Building the future,</span></div>
          <div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-str">one commit at a time 🚀"</span>)</div>
        </div>
      </div>
      <div class="about-card">
        <ul class="about-bullets">
          <li><span class="icon">🎓</span> B.Tech in Artificial Intelligence &amp; Machine Learning at <strong style="color:#fff">Bannari Amman Institute of Technology</strong></li>
          <li><span class="icon">💡</span> 389+ DSA Problems Solved on LeetCode — passionate about algorithms and system design</li>
          <li><span class="icon">🏆</span> Winner — Ethical Hackathon @ Amypo Technologies</li>
          <li><span class="icon">🚀</span> Finalist at <strong style="color:#fff">Codher'25</strong> (Anna University) &amp; <strong style="color:#fff">Hackxelerate'25</strong> (KPR College)</li>
          <li><span class="icon">🔗</span> Blockchain enthusiast — building transparent, secure solutions with smart contracts</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section>
    <div class="section-label">01 · Skills</div>
    <div class="section-title">Technical Arsenal</div>
    <div class="skills-grid">
      <div class="skill-category">
        <div class="skill-cat-title">💻 Languages</div>
        <div class="skill-tags">
          <span class="tag tag-orange">Java</span>
          <span class="tag tag-blue">Python</span>
          <span class="tag tag-purple">Solidity</span>
          <span class="tag tag-yellow">JavaScript</span>
          <span class="tag tag-cyan">TypeScript</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title">🌐 Frontend</div>
        <div class="skill-tags">
          <span class="tag tag-cyan">React</span>
          <span class="tag tag-orange">HTML5</span>
          <span class="tag tag-blue">CSS3</span>
          <span class="tag tag-cyan">Tailwind CSS</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title">⚙️ Backend & APIs</div>
        <div class="skill-tags">
          <span class="tag tag-green">Flask</span>
          <span class="tag tag-green">Node.js</span>
          <span class="tag tag-orange">REST API</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title">🗄️ Databases</div>
        <div class="skill-tags">
          <span class="tag tag-green">MongoDB</span>
          <span class="tag tag-blue">MySQL</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title">🤖 AI & Computer Vision</div>
        <div class="skill-tags">
          <span class="tag tag-purple">OpenCV</span>
          <span class="tag tag-cyan">YOLOv8</span>
          <span class="tag tag-pink">MediaPipe</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title">⛓️ Blockchain</div>
        <div class="skill-tags">
          <span class="tag tag-orange">Web3.js</span>
          <span class="tag tag-blue">Ethers.js</span>
          <span class="tag tag-orange">MetaMask</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-cat-title">🛠️ Tools & DevOps</div>
        <div class="skill-tags">
          <span class="tag tag-orange">Git</span>
          <span class="tag tag-purple">GitHub</span>
          <span class="tag tag-orange">Postman</span>
          <span class="tag tag-blue">VS Code</span>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section>
    <div class="section-label">02 · Projects</div>
    <div class="section-title">Featured Work</div>
    <div class="projects-grid">
      <div class="project-card featured" style="--card-accent: linear-gradient(90deg, #6a0dad, #00e5ff);">
        <div class="project-header">
          <div>
            <div class="project-icon" style="background: rgba(106,13,173,0.2); border: 1px solid rgba(106,13,173,0.4);">🤖</div>
          </div>
        </div>
        <div class="project-name" style="margin-top: 8px;">AI-Exam-Proctor</div>
        <p class="project-desc">AI-powered real-time exam proctoring system with multi-object detection and privacy-first architecture.</p>
        <ul class="project-features">
          <li>Detects multiple faces, phones, books, and laptops in real-time</li>
          <li>Privacy-focused edge architecture with local processing only</li>
          <li>Anonymized violation alerts ensuring data security and integrity</li>
        </ul>
        <div class="project-stack">
          <span class="stack-pill">React</span>
          <span class="stack-pill">Flask</span>
          <span class="stack-pill">OpenCV</span>
          <span class="stack-pill">YOLOv8</span>
          <span class="stack-pill">MediaPipe</span>
        </div>
        <a href="#" class="project-link">Coming Soon →</a>
      </div>

      <div class="project-card" style="--card-accent: linear-gradient(90deg, #22c55e, #00e5ff);">
        <div class="project-icon" style="background: rgba(34,197,94,0.15); border: 1px solid rgba(34,197,94,0.3); margin-bottom: 10px;">⛓️</div>
        <div class="project-name">AcademiChain</div>
        <p class="project-desc">Blockchain-based platform for secure, tamper-proof academic credential verification.</p>
        <ul class="project-features">
          <li>Immutable certificate storage on blockchain</li>
          <li>Transparent, tamper-proof verification system</li>
        </ul>
        <div class="project-stack">
          <span class="stack-pill">TypeScript</span>
          <span class="stack-pill">Solidity</span>
          <span class="stack-pill">Web3.js</span>
          <span class="stack-pill">React</span>
        </div>
        <a href="https://academichain-frontend.vercel.app" class="project-link" target="_blank">Live Demo →</a>
      </div>

      <div class="project-card" style="--card-accent: linear-gradient(90deg, #f59e0b, #fb923c);">
        <div class="project-icon" style="background: rgba(245,158,11,0.15); border: 1px solid rgba(245,158,11,0.3); margin-bottom: 10px;">📚</div>
        <div class="project-name">AcademicianBackend</div>
        <p class="project-desc">Robust backend system for academic management with scalable REST API architecture.</p>
        <ul class="project-features">
          <li>Scalable REST API for seamless data flow</li>
          <li>Comprehensive user auth &amp; authorization</li>
        </ul>
        <div class="project-stack">
          <span class="stack-pill">JavaScript</span>
          <span class="stack-pill">Node.js</span>
          <span class="stack-pill">REST APIs</span>
        </div>
        <a href="https://github.com/NegaShree-12/AcademicianBackend" class="project-link" target="_blank">View on GitHub →</a>
      </div>
    </div>
  </section>

  <!-- LEETCODE -->
  <section>
    <div class="section-label">03 · LeetCode</div>
    <div class="section-title">Problem Solving Progress</div>
    <div class="lc-container">
      <div class="lc-header">
        <div class="lc-logo">⚡</div>
        <div>
          <div class="lc-username">negashree</div>
          <div class="lc-rank">Global Rank #294,766</div>
        </div>
      </div>
      <div class="lc-stats">
        <div class="lc-total">
          <div class="lc-circle">
            <div class="lc-circle-num">389</div>
          </div>
          <div style="margin-top: 10px; font-family: 'Space Mono', monospace; font-size: 11px; color: var(--text-muted);">TOTAL SOLVED</div>
        </div>
        <div class="lc-bars">
          <div class="lc-bar-row">
            <span class="lc-diff easy">Easy</span>
            <div class="bar-track"><div class="bar-fill bar-easy" style="width: 18.9%"></div></div>
            <span class="lc-count">176 / 933</span>
          </div>
          <div class="lc-bar-row">
            <span class="lc-diff medium">Medium</span>
            <div class="bar-track"><div class="bar-fill bar-medium" style="width: 9.2%"></div></div>
            <span class="lc-count">186 / 2030</span>
          </div>
          <div class="lc-bar-row">
            <span class="lc-diff hard">Hard</span>
            <div class="bar-track"><div class="bar-fill bar-hard" style="width: 2.9%"></div></div>
            <span class="lc-count">27 / 916</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ACHIEVEMENTS -->
  <section>
    <div class="section-label">04 · Achievements</div>
    <div class="section-title">Recognitions & Awards</div>
    <div class="achievements-grid">
      <div class="ach-card">
        <div class="ach-icon">🥇</div>
        <div class="ach-title">Winner — Ethical Hackathon</div>
        <div class="ach-org">Amypo Technologies</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">💡</div>
        <div class="ach-title">Innovator</div>
        <div class="ach-org">Yukti Innovation Challenge</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">🎯</div>
        <div class="ach-title">Finalist — Codher'25</div>
        <div class="ach-org">Anna University, Chennai</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">🚀</div>
        <div class="ach-title">Finalist — Hackxelerate'25</div>
        <div class="ach-org">KPR College</div>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE -->
  <section>
    <div class="section-label">05 · Experience</div>
    <div class="section-title">Work History</div>
    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-date">SEP 2023 — JUN 2024</div>
        <div class="timeline-company">CRAYON'D</div>
        <div class="timeline-role">Software Development Intern</div>
        <ul class="timeline-points">
          <li>Developed reusable React components for internal tools, improving code reusability by 40%</li>
          <li>Collaborated with backend teams integrating REST APIs seamlessly</li>
          <li>Enhanced performance through modular component architecture</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot"></div>
        <div class="timeline-date">FEB 2023 — SEP 2023</div>
        <div class="timeline-company">MYECONICS</div>
        <div class="timeline-role">Full Stack Developer Intern</div>
        <ul class="timeline-points">
          <li>Built full-stack fitness booking application with user authentication</li>
          <li>Implemented backend workflows for registration and booking systems</li>
          <li>Conducted market analysis optimizing feature alignment with user needs</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- CURRENT FOCUS -->
  <section>
    <div class="section-label">06 · Focus</div>
    <div class="section-title">Currently Building</div>
    <div class="focus-grid">
      <div class="focus-card">
        <div class="focus-icon">🏗️</div>
        <div class="focus-title">System Design</div>
        <div class="focus-desc">Scalable backend systems &amp; distributed architecture</div>
      </div>
      <div class="focus-card">
        <div class="focus-icon">⛓️</div>
        <div class="focus-title">Advanced Blockchain</div>
        <div class="focus-desc">Smart contracts, DeFi protocols, Web3 integrations</div>
      </div>
      <div class="focus-card">
        <div class="focus-icon">☁️</div>
        <div class="focus-title">Cloud Architecture</div>
        <div class="focus-desc">Cloud-native apps with AI integration at scale</div>
      </div>
    </div>
  </section>

  <!-- CONNECT -->
  <section style="border-bottom: none;">
    <div class="section-label">07 · Connect</div>
    <div class="section-title" style="text-align:center;">Get In Touch</div>
    <div class="connect-row">
      <a href="https://github.com/NegaShree-12" class="connect-btn btn-github" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
      <a href="https://www.linkedin.com/in/negashree/" class="connect-btn btn-linkedin" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="https://leetcode.com/u/negashree/" class="connect-btn btn-leetcode" target="_blank">
        ⚡ LeetCode
      </a>
      <a href="mailto:negashree.al23@bitsathy.ac.in" class="connect-btn btn-email">
        ✉️ Email
      </a>
    </div>
  </section>

</div>
</div>

<!-- FOOTER -->
<div class="footer">
  <div class="footer-wave"></div>
  <p class="footer-text">
    ⭐ Fun fact: I solve DSA problems before breakfast!<br>
    <span>(Okay, maybe not breakfast — but definitely before coffee ☕)</span>
  </p>
</div>

</body>
</html>
