<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>GitHub Profile \u2014 Shy4n7</title>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=Syne:wght@600;800&display=swap" rel="stylesheet"/>
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg: #080b10;
  --surface: #0e1219;
  --surface2: #131822;
  --border: #1c2333;
  --accent: #e8c96d;
  --dim: #4a5568;
  --text: #b0bcd4;
  --white: #e8edf8;
  --mono: 'IBM Plex Mono', monospace;
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--mono);
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem 1rem 4rem;
  gap: 1.2rem;
}

.page-label {
  font-size: 0.62rem;
  letter-spacing: 0.22em;
  color: var(--dim);
  text-transform: uppercase;
  border: 1px solid var(--border);
  padding: 0.35rem 1rem;
  border-radius: 999px;
}

.card {
  width: 100%;
  max-width: 720px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  overflow: hidden;
}

/* HEADER */
.header {
  padding: 2.2rem 2.4rem 1.8rem;
  border-bottom: 1px solid var(--border);
  background: linear-gradient(160deg, #0e1522 0%, #0a0f18 100%);
  position: relative;
  overflow: hidden;
}

.header::after {
  content: '';
  position: absolute;
  top: -80px; right: -80px;
  width: 260px; height: 260px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(232,201,109,0.05) 0%, transparent 65%);
  pointer-events: none;
}

.h-name {
  font-family: 'Syne', sans-serif;
  font-size: 1.9rem;
  font-weight: 800;
  color: var(--white);
  letter-spacing: -0.01em;
  line-height: 1;
  margin-bottom: 0.5rem;
}

.h-handle {
  font-size: 0.72rem;
  color: var(--accent);
  letter-spacing: 0.06em;
  margin-bottom: 1rem;
}

.h-bio {
  font-size: 0.76rem;
  color: var(--text);
  line-height: 1.7;
  max-width: 480px;
  margin-bottom: 1.2rem;
  border-left: 2px solid var(--border);
  padding-left: 0.9rem;
}

.h-tags {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.h-tag {
  font-size: 0.62rem;
  padding: 0.22rem 0.65rem;
  border: 1px solid var(--border);
  border-radius: 4px;
  color: var(--dim);
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

/* BODY */
.body {
  padding: 2rem 2.4rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.section-label {
  font-size: 0.58rem;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--dim);
  margin-bottom: 0.9rem;
  display: flex;
  align-items: center;
  gap: 0.8rem;
}
.section-label::after { content: ''; flex: 1; height: 1px; background: var(--border); }

/* STATS */
.stats-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.8rem;
}

.stat-box {
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1rem 1.2rem;
}

.stat-box img {
  width: 100%;
  border-radius: 6px;
  display: block;
  filter: brightness(0.95);
}

/* PROJECTS */
.project-list { display: flex; flex-direction: column; gap: 0.7rem; }

.project-row {
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: start;
  gap: 1rem;
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1rem 1.2rem;
  transition: border-color 0.18s;
  cursor: default;
}
.project-row:hover { border-color: rgba(232,201,109,0.25); }

.proj-name {
  font-size: 0.78rem;
  font-weight: 600;
  color: var(--white);
  margin-bottom: 0.3rem;
  letter-spacing: 0.02em;
}

.proj-desc {
  font-size: 0.65rem;
  color: var(--dim);
  line-height: 1.6;
  margin-bottom: 0.55rem;
}

.proj-tags { display: flex; gap: 0.4rem; flex-wrap: wrap; }

.proj-tag {
  font-size: 0.58rem;
  padding: 0.15rem 0.5rem;
  border-radius: 3px;
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border);
  color: var(--dim);
  letter-spacing: 0.04em;
}

.proj-lang {
  display: flex;
  align-items: center;
  gap: 0.4rem;
  font-size: 0.62rem;
  color: var(--dim);
  white-space: nowrap;
  padding-top: 2px;
}

.lang-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

/* TECH */
.tech-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
  gap: 0.5rem;
}

.tech-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.65rem;
  color: var(--text);
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 5px;
  padding: 0.45rem 0.7rem;
}
.tech-item:hover { border-color: rgba(232,201,109,0.2); }
.t-dot { width: 6px; height: 6px; border-radius: 50%; flex-shrink: 0; }

/* FOOTER */
.footer {
  padding: 1rem 2.4rem;
  border-top: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.6rem;
  color: var(--dim);
}

.footer a { color: var(--accent); text-decoration: none; }

/* MD PANEL */
.md-panel {
  width: 100%;
  max-width: 720px;
  background: #0a0d12;
  border: 1px solid var(--border);
  border-radius: 12px;
  overflow: hidden;
}

.md-header {
  display: flex; align-items: center; justify-content: space-between;
  padding: 0.75rem 1.2rem;
  border-bottom: 1px solid var(--border);
  background: var(--surface);
}

.md-title { font-size: 0.64rem; color: var(--dim); letter-spacing: 0.08em; }

.copy-btn {
  font-size: 0.62rem;
  padding: 0.28rem 0.75rem;
  border-radius: 5px;
  border: 1px solid rgba(232,201,109,0.35);
  background: rgba(232,201,109,0.05);
  color: var(--accent);
  cursor: pointer;
  font-family: var(--mono);
  transition: background 0.18s;
}
.copy-btn:hover { background: rgba(232,201,109,0.1); }

.md-body {
  padding: 1.2rem 1.5rem;
  font-size: 0.66rem;
  line-height: 1.85;
  color: #6a7a96;
  white-space: pre-wrap;
  max-height: 440px;
  overflow-y: auto;
}
</style>
</head>
<body>

<div class="page-label">Profile Preview \u2014 Shy4n7</div>

<div class="card">

  <div class="header">
    <div class="h-name">Shyan Paul</div>
    <div class="h-handle">@Shy4n7 \u2014 github.com/Shy4n7</div>
    <div class="h-bio">AI/ML \u00b7 Computer Systems \u00b7 Astrophysics<br>Curious about both code and the cosmos.</div>
    <div class="h-tags">
      <span class="h-tag">Python</span>
      <span class="h-tag">TypeScript</span>
      <span class="h-tag">Machine Learning</span>
      <span class="h-tag">Deep Learning</span>
      <span class="h-tag">Tamil Nadu, India</span>
    </div>
  </div>

  <div class="body">

    <!-- STATS -->
    <div>
      <div class="section-label">stats</div>
      <div class="stats-grid">
        <div class="stat-box">
          <img src="https://github-readme-stats.vercel.app/api?username=Shy4n7&show_icons=true&theme=github_dark&hide_border=true&bg_color=0e1219&title_color=e8c96d&icon_color=6a7a96&text_color=b0bcd4" alt="GitHub Stats"/>
        </div>
        <div class="stat-box">
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Shy4n7&layout=compact&theme=github_dark&hide_border=true&bg_color=0e1219&title_color=e8c96d&text_color=b0bcd4" alt="Top Languages"/>
        </div>
      </div>
    </div>

    <!-- PROJECTS -->
    <div>
      <div class="section-