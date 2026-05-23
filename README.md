<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maneesh S — Resume</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0e0e0f;
    --surface: #141416;
    --border: #242428;
    --accent: #c8f135;
    --accent2: #5b8cff;
    --text: #e8e8e8;
    --muted: #7a7a85;
    --tag-bg: #1c1c20;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-size: 13.5px;
    line-height: 1.65;
    min-height: 100vh;
  }

  .page {
    max-width: 860px;
    margin: 0 auto;
    padding: 56px 60px;
    position: relative;
  }

  /* Subtle grid lines background */
  .page::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,0.015) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.015) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .content { position: relative; z-index: 1; }

  /* ── HEADER ── */
  header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 40px;
    padding-bottom: 32px;
    border-bottom: 1px solid var(--border);
    gap: 24px;
  }

  .name-block {}

  .name {
    font-family: 'DM Serif Display', serif;
    font-size: 42px;
    line-height: 1.1;
    letter-spacing: -0.5px;
    color: #fff;
    margin-bottom: 6px;
  }

  .name span {
    color: var(--accent);
  }

  .title-tag {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .title-tag::before {
    content: '';
    display: inline-block;
    width: 6px;
    height: 6px;
    background: var(--accent);
    border-radius: 50%;
    animation: blink 2s ease-in-out infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  .contact-block {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 6px;
    padding-top: 6px;
  }

  .contact-item {
    display: flex;
    align-items: center;
    gap: 7px;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.2s;
  }

  .contact-item:hover { color: var(--accent); }

  .contact-item .icon {
    width: 14px;
    height: 14px;
    opacity: 0.5;
  }

  /* ── SECTION ── */
  section {
    margin-bottom: 36px;
  }

  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── INTRO ── */
  .intro-text {
    color: #b0b0bb;
    font-size: 13.5px;
    line-height: 1.75;
    max-width: 680px;
  }

  .intro-text strong {
    color: var(--text);
    font-weight: 500;
  }

  /* ── CERTS ROW ── */
  .cert-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-top: 14px;
  }

  .cert-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 5px 12px;
    background: var(--tag-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    font-family: 'DM Mono', monospace;
    font-size: 10.5px;
    color: var(--muted);
    letter-spacing: 0.03em;
  }

  .cert-badge .dot {
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background: var(--accent2);
    flex-shrink: 0;
  }

  /* ── PROJECT CARD ── */
  .project {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px 22px;
    margin-bottom: 14px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s;
  }

  .project::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 3px;
    height: 100%;
    background: var(--accent);
    opacity: 0;
    transition: opacity 0.2s;
  }

  .project:hover {
    border-color: #333338;
  }

  .project:hover::before {
    opacity: 1;
  }

  .project-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 10px;
    gap: 12px;
  }

  .project-name {
    font-family: 'DM Serif Display', serif;
    font-size: 17px;
    color: #fff;
    letter-spacing: -0.2px;
  }

  .project-link {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: var(--accent2);
    text-decoration: none;
    letter-spacing: 0.04em;
    white-space: nowrap;
    opacity: 0.8;
    transition: opacity 0.2s;
  }

  .project-link:hover { opacity: 1; }

  .tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 14px;
  }

  .tag {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    padding: 3px 8px;
    background: #1a1a1e;
    border: 1px solid #2a2a30;
    border-radius: 3px;
    color: #6b6b78;
    letter-spacing: 0.03em;
  }

  .bullet-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 7px;
  }

  .bullet-list li {
    display: flex;
    gap: 10px;
    color: #9a9aaa;
    font-size: 13px;
    line-height: 1.6;
  }

  .bullet-list li::before {
    content: '→';
    color: var(--accent);
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .bullet-list li strong {
    color: #c8c8d4;
    font-weight: 500;
  }

  /* ── EDUCATION + SKILLS ── */
  .two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .edu-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px 20px;
  }

  .edu-school {
    font-weight: 600;
    font-size: 13.5px;
    color: var(--text);
    margin-bottom: 3px;
  }

  .edu-degree {
    font-size: 12.5px;
    color: var(--muted);
    margin-bottom: 8px;
  }

  .edu-meta {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .meta-chip {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    padding: 3px 8px;
    border-radius: 3px;
    background: #1a1a1e;
    border: 1px solid #2a2a30;
    color: var(--muted);
  }

  .meta-chip.highlight {
    border-color: #3a3a20;
    color: var(--accent);
    background: #1a1e0a;
  }

  .skills-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px 20px;
  }

  .skill-group {
    margin-bottom: 12px;
  }

  .skill-group:last-child { margin-bottom: 0; }

  .skill-group-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  .skill-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
  }

  .pill {
    font-family: 'DM Mono', monospace;
    font-size: 10.5px;
    padding: 3px 9px;
    background: #1a1a1e;
    border: 1px solid #2a2a30;
    border-radius: 3px;
    color: #8a8a98;
  }

  /* ── FOOTER ── */
  footer {
    margin-top: 36px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-note {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: #3a3a42;
    letter-spacing: 0.06em;
  }

  .seeking-badge {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 5px 12px;
    background: #141e06;
    border: 1px solid #2a3a10;
    border-radius: 4px;
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: var(--accent);
    letter-spacing: 0.05em;
  }

  .seeking-badge::before {
    content: '';
    width: 6px;
    height: 6px;
    background: var(--accent);
    border-radius: 50%;
    animation: blink 1.5s ease-in-out infinite;
  }

  @media print {
    body { background: white; color: black; }
    .page::before { display: none; }
  }
</style>
</head>
<body>
<div class="page">
<div class="content">

<!-- HEADER -->
<header>
  <div class="name-block">
    <div class="name">Maneesh <span>S</span></div>
    <div class="title-tag">CS&E Student · Software Developer</div>
  </div>
  <div class="contact-block">
    <a href="mailto:jmaneesh702@gmail.com" class="contact-item">
      <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 7 10-7"/></svg>
      jmaneesh702@gmail.com
    </a>
    <a href="tel:+916366652712" class="contact-item">
      <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6.1 6.1l.95-.94a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
      +91 63666 52712
    </a>
    <a href="https://github.com/Maneesh081" class="contact-item">
      <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
      github.com/Maneesh081
    </a>
    <a href="https://linkedin.com/in/Maneesh081" class="contact-item">
      <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
      linkedin.com/in/Maneesh081
    </a>
  </div>
</header>

<!-- INTRODUCTION -->
<section>
  <div class="section-label">Introduction</div>
  <p class="intro-text">
    Final-year <strong>Computer Science & Engineering</strong> student at Government SKSJTI, Bangalore (VTU), with a CGPA of <strong>7.5/10.0</strong>. I build things that solve real problems — from productivity-focused Android launchers and AI-powered browser tools to P2P file-sharing clients and malware detection extensions. My interests span <strong>systems programming, applied ML, mobile development, and cybersecurity</strong>. Actively seeking internship or entry-level software development roles.
  </p>
  <div class="cert-row">
    <div class="cert-badge"><span class="dot"></span> AWS Cloud Practitioner</div>
    <div class="cert-badge"><span class="dot"></span> Cisco CCNA</div>
    <div class="cert-badge"><span class="dot"></span> VTU 2022 Scheme · 6th Semester</div>
  </div>
</section>

<!-- PROJECTS -->
<section>
  <div class="section-label">Projects</div>

  <!-- Zlaunch -->
  <div class="project">
    <div class="project-header">
      <div class="project-name">Zlaunch — Minimal Android Launcher</div>
      <a href="https://github.com/Maneesh081" class="project-link">↗ github.com/Maneesh081</a>
    </div>
    <div class="tech-tags">
      <span class="tag">Kotlin</span>
      <span class="tag">Android SDK</span>
      <span class="tag">SharedPreferences</span>
      <span class="tag">AppWidgetHost</span>
    </div>
    <ul class="bullet-list">
      <li>Reduced digital distraction for users by building a full Android home-screen replacement that <strong>hides non-whitelisted apps by default</strong>, targeting Android 8.0–14 (API 26–34).</li>
      <li>Improved focus time, as measured by a <strong>live focus-duration timer</strong> always visible on screen, by implementing a Focus Mode that clears all UI to a minimal clock-only view.</li>
      <li>Shipped a production-ready <strong>v1.0.0 release</strong> on GitHub, as validated by public availability, by architecting a clean whitelist system using SharedPreferences and AppWidgetHost APIs.</li>
    </ul>
  </div>

  <!-- Flow -->
  <div class="project">
    <div class="project-header">
      <div class="project-name">Flow — AI Flowchart Builder</div>
      <a href="https://github.com/Maneesh081" class="project-link">↗ github.com/Maneesh081</a>
    </div>
    <div class="tech-tags">
      <span class="tag">React 18</span>
      <span class="tag">TypeScript</span>
      <span class="tag">Vite</span>
      <span class="tag">React Flow</span>
      <span class="tag">Gemini 2.5 Flash API</span>
      <span class="tag">Tailwind CSS</span>
    </div>
    <ul class="bullet-list">
      <li>Reduced diagram creation from hours to <strong>seconds</strong>, as measured by real-time generation from plain-English input, by integrating Gemini 2.5 Flash API into a React 18 + TypeScript browser app.</li>
      <li>Increased diagram accuracy, as measured by support for <strong>7 node types</strong> and iterative AI refinement via follow-up prompts, by building a custom auto-layout algorithm and prompt pipeline.</li>
      <li>Delivered a <strong>zero-setup browser tool</strong> with dark/light mode, as measured by no-backend architecture, by engineering the full stack in TypeScript with clean component separation.</li>
    </ul>
  </div>

  <!-- Winters -->
  <div class="project">
    <div class="project-header">
      <div class="project-name">Winters — Browser Virus Scanner</div>
      <a href="https://github.com/Maneesh081" class="project-link">↗ github.com/Maneesh081</a>
    </div>
    <div class="tech-tags">
      <span class="tag">Python</span>
      <span class="tag">scikit-learn</span>
      <span class="tag">JavaScript</span>
      <span class="tag">Chrome Extension API</span>
    </div>
    <ul class="bullet-list">
      <li>Improved download safety, as measured by a <strong>real-time 0–100% risk score</strong> per file, by engineering heuristic analysis combining extension classification, filename pattern matching, and an allowlist.</li>
      <li>Increased malware detection coverage across <strong>trojans, ransomware, spyware, and adware</strong>, as measured by a trainable ML pipeline, by building train_model.py that exports a .pkl model into the extension.</li>
      <li>Delivered instant browser verdicts with <strong>risk explanations via Chrome notifications</strong>, as measured by cross-format coverage including PDFs, executables, and archives.</li>
    </ul>
  </div>

  <!-- Torrent Clone -->
  <div class="project">
    <div class="project-header">
      <div class="project-name">Torrent Clone — P2P File Sharing</div>
      <a href="https://github.com/Maneesh081" class="project-link">↗ github.com/Maneesh081</a>
    </div>
    <div class="tech-tags">
      <span class="tag">Python</span>
      <span class="tag">P2P Networking</span>
      <span class="tag">Multithreading</span>
    </div>
    <ul class="bullet-list">
      <li>Implemented a functional <strong>BitTorrent-style client</strong>, as measured by successful parallel peer downloads, by building file segmentation, peer discovery, and concurrent connections using Python threading primitives.</li>
      <li>Demonstrated distributed systems depth, as measured by working <strong>tracker communication and piece verification</strong>, by replicating core BitTorrent protocol logic from scratch.</li>
    </ul>
  </div>

  <!-- Simple Kernel -->
  <div class="project">
    <div class="project-header">
      <div class="project-name">Simple Kernel — Browser Linux Terminal</div>
      <a href="https://github.com/Maneesh081" class="project-link">↗ github.com/Maneesh081</a>
    </div>
    <div class="tech-tags">
      <span class="tag">HTML</span>
      <span class="tag">CSS</span>
      <span class="tag">JavaScript</span>
    </div>
    <ul class="bullet-list">
      <li>Built a <strong>fully browser-based Linux terminal emulator</strong> with no backend, supporting commands like cat, nano, ls, mkdir, and touch with authentic monospace aesthetics and blinking cursor.</li>
    </ul>
  </div>
</section>

<!-- EDUCATION + SKILLS -->
<section>
  <div class="section-label">Education & Skills</div>
  <div class="two-col">
    <div class="edu-card">
      <div class="edu-school">Govt. SKSJTI, Bangalore</div>
      <div class="edu-degree">B.E. — Computer Science & Engineering</div>
      <div class="edu-meta">
        <span class="meta-chip highlight">CGPA 7.5 / 10.0</span>
        <span class="meta-chip">VTU · 2022 Scheme</span>
        <span class="meta-chip">2022 – 2026</span>
      </div>
    </div>
    <div class="skills-card">
      <div class="skill-group">
        <div class="skill-group-label">Languages</div>
        <div class="skill-pills">
          <span class="pill">Kotlin</span>
          <span class="pill">Python</span>
          <span class="pill">TypeScript</span>
          <span class="pill">JavaScript</span>
          <span class="pill">C</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Frameworks & Tools</div>
        <div class="skill-pills">
          <span class="pill">React</span>
          <span class="pill">Android SDK</span>
          <span class="pill">scikit-learn</span>
          <span class="pill">Tailwind</span>
          <span class="pill">Git</span>
          <span class="pill">Docker</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-label">Cloud & Networking</div>
        <div class="skill-pills">
          <span class="pill">AWS</span>
          <span class="pill">CCNA</span>
          <span class="pill">Linux</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-note">MANEESH S · RESUME · 2025</div>
  <div class="seeking-badge">Open to Internships & Entry-Level Roles</div>
</footer>

</div>
</div>
</body>
</html>
