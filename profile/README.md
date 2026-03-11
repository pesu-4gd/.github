<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PESU Project Plan — 4Good.AI</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500&display=swap');

  :root {
    --bg: #0b0f1a;
    --surface: #111827;
    --surface2: #1a2236;
    --border: #1e2d45;
    --text: #e8edf5;
    --muted: #7a8fa8;
    --accent1: #3b82f6;
    --accent2: #10b981;
    --accent3: #f59e0b;
    --accent4: #8b5cf6;
    --accent5: #ef4444;
    --accent6: #06b6d4;
    --p0: #ef4444;
    --p1: #f59e0b;
    --p2: #10b981;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.7;
  }

  /* ── HEADER ── */
  header {
    background: linear-gradient(135deg, #0b0f1a 0%, #0f1c35 50%, #0b1525 100%);
    border-bottom: 1px solid var(--border);
    padding: 60px 40px 50px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  header::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 60% at 50% -10%, rgba(59,130,246,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .badge-row {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
    margin-bottom: 24px;
  }
  .badge {
    font-family: 'DM Sans', sans-serif;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 4px 12px;
    border-radius: 20px;
    border: 1px solid;
  }
  .badge-blue  { color: #93c5fd; border-color: #1e40af; background: rgba(59,130,246,0.1); }
  .badge-green { color: #6ee7b7; border-color: #065f46; background: rgba(16,185,129,0.1); }
  .badge-amber { color: #fcd34d; border-color: #92400e; background: rgba(245,158,11,0.1); }

  header h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    background: linear-gradient(135deg, #e8edf5 30%, #93c5fd 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 12px;
  }
  header p.tagline {
    color: var(--muted);
    font-size: 15px;
    font-style: italic;
    max-width: 540px;
    margin: 0 auto 20px;
  }
  .meta-row {
    display: flex;
    justify-content: center;
    gap: 24px;
    flex-wrap: wrap;
    font-size: 12px;
    color: var(--muted);
  }
  .meta-row span { display: flex; align-items: center; gap: 6px; }

  /* ── LAYOUT ── */
  .container { max-width: 1100px; margin: 0 auto; padding: 0 32px 80px; }

  /* ── TOC ── */
  .toc {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 28px 32px;
    margin: 40px 0;
  }
  .toc h2 { font-family: 'Syne', sans-serif; font-size: 14px; text-transform: uppercase; letter-spacing: 0.1em; color: var(--muted); margin-bottom: 16px; }
  .toc-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
    gap: 6px 20px;
  }
  .toc-grid a {
    color: #93c5fd;
    text-decoration: none;
    font-size: 13.5px;
    padding: 4px 0;
    border-bottom: 1px solid transparent;
    transition: border-color 0.2s, color 0.2s;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .toc-grid a:hover { color: #bfdbfe; border-bottom-color: #1e40af; }

  /* ── SECTIONS ── */
  section { margin-top: 56px; }
  section h2 {
    font-family: 'Syne', sans-serif;
    font-size: 1.5rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 10px;
  }
  section h3 {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 600;
    color: #93c5fd;
    margin: 24px 0 10px;
  }
  p { color: #c9d4e3; margin-bottom: 10px; }
  ul { padding-left: 20px; color: #c9d4e3; }
  ul li { margin-bottom: 5px; }

  /* ── PRODUCT TREE ── */
  .tree-section { margin-top: 56px; }
  .tree-section h2 { font-family: 'Syne', sans-serif; font-size: 1.5rem; font-weight: 700; letter-spacing: -0.01em; margin-bottom: 28px; padding-bottom: 12px; border-bottom: 1px solid var(--border); display: flex; align-items: center; gap: 10px; }

  /* SVG tree wrapper */
  .tree-svg-wrap {
    width: 100%;
    overflow-x: auto;
    padding-bottom: 8px;
  }
  .tree-svg-wrap svg {
    display: block;
    margin: 0 auto;
    min-width: 760px;
  }

  /* Product cards (foreignObject) */
  .product-card {
    border-radius: 14px;
    padding: 16px 12px 14px;
    text-align: center;
    border: 1px solid;
    transition: transform 0.2s, box-shadow 0.2s;
    height: 100%;
    box-sizing: border-box;
  }
  .product-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 32px rgba(0,0,0,0.5);
  }
  .product-card .icon { font-size: 24px; margin-bottom: 7px; }
  .product-card .name {
    font-family: 'Syne', sans-serif;
    font-size: 11.5px;
    font-weight: 700;
    letter-spacing: 0.01em;
    line-height: 1.3;
    margin-bottom: 5px;
  }
  .product-card .desc {
    font-size: 10px;
    line-height: 1.4;
    opacity: 0.72;
  }
  .product-card .links {
    margin-top: 9px;
    display: flex;
    gap: 5px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .product-card .links a {
    font-size: 9.5px;
    font-weight: 600;
    padding: 3px 7px;
    border-radius: 5px;
    text-decoration: none;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    transition: opacity 0.2s;
  }
  .product-card .links a:hover { opacity: 0.8; }

  /* Per-product colour themes — used in SVG tree */
  .c1 { background: linear-gradient(135deg,#0f2a1e,#132616); border-color: #16a34a; }
  .c1 .name { color: #4ade80; } .c1 .desc { color: #86efac; }
  .c1 .links a { background: rgba(22,163,74,0.18); color: #4ade80; }
  .s1 { background: #16a34a; }

  .c2 { background: linear-gradient(135deg,#1e1a0f,#261f12); border-color: #d97706; }
  .c2 .name { color: #fbbf24; } .c2 .desc { color: #fcd34d; }
  .c2 .links a { background: rgba(217,119,6,0.18); color: #fbbf24; }
  .s2 { background: #d97706; }

  .c3 { background: linear-gradient(135deg,#0f1a2e,#111e36); border-color: #3b82f6; }
  .c3 .name { color: #60a5fa; } .c3 .desc { color: #93c5fd; }
  .c3 .links a { background: rgba(59,130,246,0.18); color: #60a5fa; }
  .s3 { background: #3b82f6; }

  .c4 { background: linear-gradient(135deg,#1a0f2e,#1e1236); border-color: #8b5cf6; }
  .c4 .name { color: #a78bfa; } .c4 .desc { color: #c4b5fd; }
  .c4 .links a { background: rgba(139,92,246,0.18); color: #a78bfa; }
  .s4 { background: #8b5cf6; }

  .c5 { background: linear-gradient(135deg,#1a0f14,#241318); border-color: #ec4899; }
  .c5 .name { color: #f472b6; } .c5 .desc { color: #fbcfe8; }
  .c5 .links a { background: rgba(236,72,153,0.18); color: #f472b6; }
  .s5 { background: #ec4899; }

  .c6 { background: linear-gradient(135deg,#0a1e22,#0c2428); border-color: #06b6d4; }
  .c6 .name { color: #22d3ee; } .c6 .desc { color: #a5f3fc; }
  .c6 .links a { background: rgba(6,182,212,0.18); color: #22d3ee; }
  .s6 { background: #06b6d4; }

  /* ── FLOW DIAGRAM ── */
  .flow-row {
    display: flex;
    align-items: center;
    gap: 0;
    margin: 16px 0;
    flex-wrap: wrap;
  }
  .flow-node {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 12px 20px;
    font-size: 13px;
    font-weight: 500;
    white-space: nowrap;
  }
  .flow-node.highlight { border-color: var(--accent1); color: #93c5fd; background: rgba(59,130,246,0.08); }
  .flow-arrow {
    padding: 0 10px;
    color: var(--muted);
    font-size: 18px;
  }

  /* ── TABLES ── */
  table { width: 100%; border-collapse: collapse; margin: 16px 0; font-size: 13.5px; }
  th {
    background: var(--surface2);
    color: var(--muted);
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 0.07em;
    padding: 10px 14px;
    text-align: left;
    border-bottom: 1px solid var(--border);
  }
  td {
    padding: 11px 14px;
    border-bottom: 1px solid rgba(30,45,69,0.6);
    color: #c9d4e3;
    vertical-align: top;
  }
  tr:hover td { background: rgba(255,255,255,0.02); }

  /* ── PRIORITY BADGES ── */
  .p-badge {
    display: inline-block;
    font-size: 11px;
    font-weight: 700;
    padding: 2px 8px;
    border-radius: 5px;
    letter-spacing: 0.05em;
  }
  .p0 { background: rgba(239,68,68,0.15); color: #f87171; border: 1px solid rgba(239,68,68,0.3); }
  .p1 { background: rgba(245,158,11,0.15); color: #fbbf24; border: 1px solid rgba(245,158,11,0.3); }
  .p2 { background: rgba(16,185,129,0.15); color: #34d399; border: 1px solid rgba(16,185,129,0.3); }

  /* ── CALLOUT ── */
  .callout {
    background: rgba(59,130,246,0.07);
    border-left: 3px solid #3b82f6;
    border-radius: 0 10px 10px 0;
    padding: 14px 18px;
    margin: 16px 0;
    font-size: 13.5px;
    color: #93c5fd;
  }
  .callout.green { background: rgba(16,185,129,0.07); border-color: #10b981; color: #6ee7b7; }
  .callout.amber { background: rgba(245,158,11,0.07); border-color: #f59e0b; color: #fcd34d; }

  /* ── SPRINT STAGES ── */
  .stages {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin: 20px 0;
  }
  .stage-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
  }
  .stage-card h4 {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    margin-bottom: 10px;
  }
  .stage-card ul { padding-left: 16px; font-size: 13px; }
  .stage-card li { margin-bottom: 4px; color: #c9d4e3; }
  .stage-triage h4 { color: #f87171; }
  .stage-rca h4 { color: #fbbf24; }
  .stage-res h4 { color: #34d399; }

  /* ── LINKS ── */
  a { color: #60a5fa; text-decoration: none; }
  a:hover { color: #93c5fd; text-decoration: underline; }

  /* ── KEY LINKS GRID ── */
  .links-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 10px;
    margin: 16px 0;
  }
  .link-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 16px;
    display: flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
    color: var(--text);
    font-size: 13px;
    font-weight: 500;
    transition: border-color 0.2s, background 0.2s;
  }
  .link-card:hover { border-color: #3b82f6; background: rgba(59,130,246,0.06); text-decoration: none; }
  .link-card .licon { font-size: 18px; }

  /* ── FOOTER ── */
  footer {
    border-top: 1px solid var(--border);
    text-align: center;
    padding: 32px;
    color: var(--muted);
    font-size: 12.5px;
  }
  footer em { color: #60a5fa; font-style: normal; }

  /* ── RESPONSIVE ── */
  @media (max-width: 860px) {
    .products-row { grid-template-columns: repeat(3, 1fr); }
    .h-bar { width: 60%; }
    .stages { grid-template-columns: 1fr; }
  }
  @media (max-width: 540px) {
    .products-row { grid-template-columns: repeat(2, 1fr); }
    header { padding: 40px 20px 36px; }
    .container { padding: 0 16px 60px; }
  }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="badge-row">
    <span class="badge badge-blue">Status: Active</span>
    <span class="badge badge-green">Version 2.0</span>
    <span class="badge badge-amber">Last Updated: 2026-03-11</span>
  </div>
  <h1>PESU Project Plan</h1>
  <p class="tagline">"We build technology for good — purposeful products, principled engineering, people-first culture."</p>
  <div class="meta-row">
    <span>🏢 Owner: Engineering Excellence Team</span>
    <span>📍 4Good.AI Organisation</span>
    <span>🔄 Living Document</span>
  </div>
</header>

<div class="container">



  <!-- CODE OF CONDUCT -->
  <section id="conduct">
    <h2>🤝 Code of Conduct</h2>
    <p>We expect everyone in this organisation — contributors, reviewers, leads — to act with respect and professionalism.</p>
    <p>Full Code of Conduct: <a href="CODE_OF_CONDUCT.md">CODE_OF_CONDUCT.md</a></p>
    <ul>
      <li>Be kind and constructive in reviews and discussions</li>
      <li>Assume good intent</li>
      <li>Raise concerns through the right channels</li>
      <li>Zero tolerance for harassment or exclusion</li>
    </ul>
  </section>

  <!-- DEV COOKBOOK -->
  <section id="cookbook">
    <h2>🍳 4Good Dev Cookbook</h2>
    <p>Your practical guide to getting things done here. Full Cookbook: <a href="#">Wiki → Dev Cookbook</a></p>
    <ul>
      <li>Setting up your local development environment</li>
      <li>Running services locally and with Docker</li>
      <li>Common debugging patterns</li>
      <li>How to use our internal tooling and libraries</li>
      <li>Environment variables and secrets management</li>
      <li>How to write and run tests</li>
    </ul>
  </section>

  <!-- MISSION -->
  <section id="mission">
    <h2>🎯 Mission & Vision</h2>
    <p><strong>Mission:</strong> Build AI-powered products that are ethical, accessible, and genuinely useful for people and organisations.</p>
    <p><strong>Vision:</strong> To be a trusted engineering organisation where great ideas become great products — with discipline, speed, and integrity.</p>
    <h3>Core Values</h3>
    <ul>
      <li><strong>Shared ownership</strong> — everyone is responsible for quality</li>
      <li><strong>Reliability first</strong> — we ship things that work</li>
      <li><strong>Continuous improvement</strong> — we get better every sprint</li>
      <li><strong>Collaborative excellence</strong> — we build together, not in silos</li>
    </ul>
  </section>

  <!-- PRODUCT TREE -->
  <section class="tree-section" id="products">
    <h2>🌿 PESU Products</h2>
    <p style="color:var(--muted);margin-bottom:4px;">All products under the PESU umbrella. Each has its own repo, team, and roadmap — all governed by shared standards in this handbook.</p>

    <!-- SVG TREE: viewBox 1000 x 380, root centred at x=500 y=60, 6 cards below -->
    <div class="tree-svg-wrap">
    <svg viewBox="0 0 1060 400" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="width:100%;max-width:1060px;">
      <defs>
        <!-- glow filter for root -->
        <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
          <feGaussianBlur stdDeviation="4" result="blur"/>
          <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
        </filter>
        <!-- gradients for each branch line -->
        <linearGradient id="lg1" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#16a34a"/></linearGradient>
        <linearGradient id="lg2" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#d97706"/></linearGradient>
        <linearGradient id="lg3" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#3b82f6"/></linearGradient>
        <linearGradient id="lg4" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#8b5cf6"/></linearGradient>
        <linearGradient id="lg5" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#ec4899"/></linearGradient>
        <linearGradient id="lg6" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#06b6d4"/></linearGradient>
      </defs>

      <!-- ── ROOT NODE ── x=380..680 y=8..68 -->
      <rect x="340" y="10" width="380" height="62" rx="14" ry="14"
            fill="#0f1e38" stroke="#3b82f6" stroke-width="2" filter="url(#glow)"/>
      <text x="530" y="37" text-anchor="middle" font-family="Syne,sans-serif"
            font-size="17" font-weight="800" fill="#93c5fd">4Good.AI — PESU</text>
      <text x="530" y="57" text-anchor="middle" font-family="DM Sans,sans-serif"
            font-size="10.5" fill="#4a6888" letter-spacing="1">ENGINEERING ORGANISATION</text>

      <!-- ── VERTICAL STEM from root to horizontal rail ── -->
      <!-- root bottom-centre: x=530 y=72 → rail y=110 -->
      <line x1="530" y1="72" x2="530" y2="110" stroke="#3b82f6" stroke-width="2"/>

      <!-- ── HORIZONTAL RAIL y=110, from x=88 to x=972 ── -->
      <!-- (centres of 6 cards at x=88,247,406,565,724,883; card width≈138, gap≈21) -->
      <line x1="88" y1="110" x2="972" y2="110" stroke="#1e3a5f" stroke-width="2"/>

      <!-- ── 6 BRANCH DROPS (rail → card top) y=110 → y=142 ── -->
      <!-- card centres: 88, 247, 406, 565, 724, 883 -->
      <line x1="88"  y1="110" x2="88"  y2="142" stroke="url(#lg1)" stroke-width="2"/>
      <line x1="247" y1="110" x2="247" y2="142" stroke="url(#lg2)" stroke-width="2"/>
      <line x1="406" y1="110" x2="406" y2="142" stroke="url(#lg3)" stroke-width="2"/>
      <line x1="565" y1="110" x2="565" y2="142" stroke="url(#lg4)" stroke-width="2"/>
      <line x1="724" y1="110" x2="724" y2="142" stroke="url(#lg5)" stroke-width="2"/>
      <line x1="883" y1="110" x2="883" y2="142" stroke="url(#lg6)" stroke-width="2"/>

      <!-- ── DOT connectors on rail ── -->
      <circle cx="88"  cy="110" r="4" fill="#16a34a"/>
      <circle cx="247" cy="110" r="4" fill="#d97706"/>
      <circle cx="406" cy="110" r="4" fill="#3b82f6"/>
      <circle cx="565" cy="110" r="4" fill="#8b5cf6"/>
      <circle cx="724" cy="110" r="4" fill="#ec4899"/>
      <circle cx="883" cy="110" r="4" fill="#06b6d4"/>
      <circle cx="530" cy="110" r="5" fill="#3b82f6"/>

      <!-- ══════════════════════════════════════════
           PRODUCT CARDS  (x = centre-69, y=142, w=138, h=230)
           centres: 88, 247, 406, 565, 724, 883
           ══════════════════════════════════════════ -->

      <!-- CARD 1 — Evals (#16a34a green) -->
      <rect x="19" y="142" width="138" height="230" rx="13" fill="#0f2a1e" stroke="#16a34a" stroke-width="1.5"/>
      <text x="88" y="174" text-anchor="middle" font-size="22">🧪</text>
      <text x="88" y="196" text-anchor="middle" font-family="Syne,sans-serif" font-size="12" font-weight="700" fill="#4ade80">Evals</text>
      <text x="88" y="213" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#86efac">AI evaluation &amp;</text>
      <text x="88" y="225" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#86efac">benchmarking platform</text>
      <!-- Demo pill -->
      <rect x="28" y="238" width="36" height="17" rx="5" fill="rgba(22,163,74,0.2)" stroke="#16a34a" stroke-width="0.8"/>
      <text x="46" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#4ade80" letter-spacing="0.5">DEMO</text>
      <!-- Repo pill -->
      <rect x="70" y="238" width="36" height="17" rx="5" fill="rgba(22,163,74,0.2)" stroke="#16a34a" stroke-width="0.8"/>
      <text x="88" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#4ade80" letter-spacing="0.5">REPO</text>
      <!-- Docs pill -->
      <rect x="112" y="238" width="36" height="17" rx="5" fill="rgba(22,163,74,0.2)" stroke="#16a34a" stroke-width="0.8"/>
      <text x="130" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#4ade80" letter-spacing="0.5">DOCS</text>
      <!-- Divider -->
      <line x1="30" y1="264" x2="146" y2="264" stroke="#16a34a" stroke-width="0.5" opacity="0.3"/>
      <text x="88" y="280" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9" fill="#4a7a5a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
      <rect x="30" y="290" width="117" height="70" rx="8" fill="rgba(22,163,74,0.07)" stroke="#16a34a" stroke-width="0.5"/>
      <text x="88" y="307" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#86efac">Sprint: 2 weeks</text>
      <text x="88" y="322" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#86efac">Plans: Feature + Bug</text>
      <text x="88" y="337" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#86efac">Wiki: Linked</text>
      <text x="88" y="352" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#86efac">Issues: Tracked</text>

      <!-- CARD 2 — Digital Strategy (#d97706 amber) -->
      <rect x="178" y="142" width="138" height="230" rx="13" fill="#1e1a0f" stroke="#d97706" stroke-width="1.5"/>
      <text x="247" y="174" text-anchor="middle" font-size="22">📈</text>
      <text x="247" y="196" text-anchor="middle" font-family="Syne,sans-serif" font-size="12" font-weight="700" fill="#fbbf24">Digital Strategy</text>
      <text x="247" y="213" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#fcd34d">Strategic insights &amp;</text>
      <text x="247" y="225" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#fcd34d">analytics tools</text>
      <rect x="187" y="238" width="36" height="17" rx="5" fill="rgba(217,119,6,0.2)" stroke="#d97706" stroke-width="0.8"/>
      <text x="205" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#fbbf24" letter-spacing="0.5">DEMO</text>
      <rect x="229" y="238" width="36" height="17" rx="5" fill="rgba(217,119,6,0.2)" stroke="#d97706" stroke-width="0.8"/>
      <text x="247" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#fbbf24" letter-spacing="0.5">REPO</text>
      <rect x="271" y="238" width="36" height="17" rx="5" fill="rgba(217,119,6,0.2)" stroke="#d97706" stroke-width="0.8"/>
      <text x="289" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#fbbf24" letter-spacing="0.5">DOCS</text>
      <line x1="189" y1="264" x2="305" y2="264" stroke="#d97706" stroke-width="0.5" opacity="0.3"/>
      <text x="247" y="280" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9" fill="#7a5a20" letter-spacing="0.5">PESU · 4GOOD.AI</text>
      <rect x="189" y="290" width="117" height="70" rx="8" fill="rgba(217,119,6,0.07)" stroke="#d97706" stroke-width="0.5"/>
      <text x="247" y="307" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fcd34d">Sprint: 2 weeks</text>
      <text x="247" y="322" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fcd34d">Plans: Feature + Bug</text>
      <text x="247" y="337" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fcd34d">Wiki: Linked</text>
      <text x="247" y="352" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fcd34d">Issues: Tracked</text>

      <!-- CARD 3 — Placements (#3b82f6 blue) -->
      <rect x="337" y="142" width="138" height="230" rx="13" fill="#0f1a2e" stroke="#3b82f6" stroke-width="1.5"/>
      <text x="406" y="174" text-anchor="middle" font-size="22">🎓</text>
      <text x="406" y="196" text-anchor="middle" font-family="Syne,sans-serif" font-size="12" font-weight="700" fill="#60a5fa">Placements</text>
      <text x="406" y="213" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#93c5fd">Career placement &amp;</text>
      <text x="406" y="225" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#93c5fd">recruitment system</text>
      <rect x="346" y="238" width="36" height="17" rx="5" fill="rgba(59,130,246,0.2)" stroke="#3b82f6" stroke-width="0.8"/>
      <text x="364" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#60a5fa" letter-spacing="0.5">DEMO</text>
      <rect x="388" y="238" width="36" height="17" rx="5" fill="rgba(59,130,246,0.2)" stroke="#3b82f6" stroke-width="0.8"/>
      <text x="406" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#60a5fa" letter-spacing="0.5">REPO</text>
      <rect x="430" y="238" width="36" height="17" rx="5" fill="rgba(59,130,246,0.2)" stroke="#3b82f6" stroke-width="0.8"/>
      <text x="448" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#60a5fa" letter-spacing="0.5">DOCS</text>
      <line x1="348" y1="264" x2="464" y2="264" stroke="#3b82f6" stroke-width="0.5" opacity="0.3"/>
      <text x="406" y="280" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9" fill="#2a4a7a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
      <rect x="348" y="290" width="117" height="70" rx="8" fill="rgba(59,130,246,0.07)" stroke="#3b82f6" stroke-width="0.5"/>
      <text x="406" y="307" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#93c5fd">Sprint: 2 weeks</text>
      <text x="406" y="322" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#93c5fd">Plans: Feature + Bug</text>
      <text x="406" y="337" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#93c5fd">Wiki: Linked</text>
      <text x="406" y="352" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#93c5fd">Issues: Tracked</text>

      <!-- CARD 4 — Experimental (#8b5cf6 purple) -->
      <rect x="496" y="142" width="138" height="230" rx="13" fill="#1a0f2e" stroke="#8b5cf6" stroke-width="1.5"/>
      <text x="565" y="174" text-anchor="middle" font-size="22">⚗️</text>
      <text x="565" y="196" text-anchor="middle" font-family="Syne,sans-serif" font-size="12" font-weight="700" fill="#a78bfa">Experimental</text>
      <text x="565" y="213" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#c4b5fd">R&amp;D sandbox</text>
      <text x="565" y="225" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#c4b5fd">for new ideas</text>
      <rect x="505" y="238" width="36" height="17" rx="5" fill="rgba(139,92,246,0.2)" stroke="#8b5cf6" stroke-width="0.8"/>
      <text x="523" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#a78bfa" letter-spacing="0.5">DEMO</text>
      <rect x="547" y="238" width="36" height="17" rx="5" fill="rgba(139,92,246,0.2)" stroke="#8b5cf6" stroke-width="0.8"/>
      <text x="565" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#a78bfa" letter-spacing="0.5">REPO</text>
      <rect x="589" y="238" width="36" height="17" rx="5" fill="rgba(139,92,246,0.2)" stroke="#8b5cf6" stroke-width="0.8"/>
      <text x="607" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#a78bfa" letter-spacing="0.5">DOCS</text>
      <line x1="507" y1="264" x2="623" y2="264" stroke="#8b5cf6" stroke-width="0.5" opacity="0.3"/>
      <text x="565" y="280" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9" fill="#4a3a7a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
      <rect x="507" y="290" width="117" height="70" rx="8" fill="rgba(139,92,246,0.07)" stroke="#8b5cf6" stroke-width="0.5"/>
      <text x="565" y="307" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#c4b5fd">Sprint: 2 weeks</text>
      <text x="565" y="322" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#c4b5fd">Plans: Feature + Bug</text>
      <text x="565" y="337" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#c4b5fd">Wiki: Linked</text>
      <text x="565" y="352" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#c4b5fd">Issues: Tracked</text>

      <!-- CARD 5 — Alumni Portal (#ec4899 pink) -->
      <rect x="655" y="142" width="138" height="230" rx="13" fill="#1a0f14" stroke="#ec4899" stroke-width="1.5"/>
      <text x="724" y="174" text-anchor="middle" font-size="22">🏛️</text>
      <text x="724" y="196" text-anchor="middle" font-family="Syne,sans-serif" font-size="12" font-weight="700" fill="#f472b6">Alumni Portal</text>
      <text x="724" y="213" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#fbcfe8">Alumni network &amp;</text>
      <text x="724" y="225" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#fbcfe8">engagement hub</text>
      <rect x="664" y="238" width="36" height="17" rx="5" fill="rgba(236,72,153,0.2)" stroke="#ec4899" stroke-width="0.8"/>
      <text x="682" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#f472b6" letter-spacing="0.5">DEMO</text>
      <rect x="706" y="238" width="36" height="17" rx="5" fill="rgba(236,72,153,0.2)" stroke="#ec4899" stroke-width="0.8"/>
      <text x="724" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#f472b6" letter-spacing="0.5">REPO</text>
      <rect x="748" y="238" width="36" height="17" rx="5" fill="rgba(236,72,153,0.2)" stroke="#ec4899" stroke-width="0.8"/>
      <text x="766" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#f472b6" letter-spacing="0.5">DOCS</text>
      <line x1="666" y1="264" x2="782" y2="264" stroke="#ec4899" stroke-width="0.5" opacity="0.3"/>
      <text x="724" y="280" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9" fill="#7a2a4a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
      <rect x="666" y="290" width="117" height="70" rx="8" fill="rgba(236,72,153,0.07)" stroke="#ec4899" stroke-width="0.5"/>
      <text x="724" y="307" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fbcfe8">Sprint: 2 weeks</text>
      <text x="724" y="322" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fbcfe8">Plans: Feature + Bug</text>
      <text x="724" y="337" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fbcfe8">Wiki: Linked</text>
      <text x="724" y="352" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#fbcfe8">Issues: Tracked</text>

      <!-- CARD 6 — Course Generation (#06b6d4 cyan) -->
      <rect x="814" y="142" width="138" height="230" rx="13" fill="#0a1e22" stroke="#06b6d4" stroke-width="1.5"/>
      <text x="883" y="174" text-anchor="middle" font-size="22">📚</text>
      <text x="883" y="196" text-anchor="middle" font-family="Syne,sans-serif" font-size="12" font-weight="700" fill="#22d3ee">Course Generation</text>
      <text x="883" y="213" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#a5f3fc">AI-powered curriculum</text>
      <text x="883" y="225" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9.5" fill="#a5f3fc">&amp; course builder</text>
      <rect x="823" y="238" width="36" height="17" rx="5" fill="rgba(6,182,212,0.2)" stroke="#06b6d4" stroke-width="0.8"/>
      <text x="841" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#22d3ee" letter-spacing="0.5">DEMO</text>
      <rect x="865" y="238" width="36" height="17" rx="5" fill="rgba(6,182,212,0.2)" stroke="#06b6d4" stroke-width="0.8"/>
      <text x="883" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#22d3ee" letter-spacing="0.5">REPO</text>
      <rect x="907" y="238" width="36" height="17" rx="5" fill="rgba(6,182,212,0.2)" stroke="#06b6d4" stroke-width="0.8"/>
      <text x="925" y="250" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" font-weight="700" fill="#22d3ee" letter-spacing="0.5">DOCS</text>
      <line x1="825" y1="264" x2="941" y2="264" stroke="#06b6d4" stroke-width="0.5" opacity="0.3"/>
      <text x="883" y="280" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="9" fill="#1a5a6a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
      <rect x="825" y="290" width="117" height="70" rx="8" fill="rgba(6,182,212,0.07)" stroke="#06b6d4" stroke-width="0.5"/>
      <text x="883" y="307" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#a5f3fc">Sprint: 2 weeks</text>
      <text x="883" y="322" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#a5f3fc">Plans: Feature + Bug</text>
      <text x="883" y="337" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#a5f3fc">Wiki: Linked</text>
      <text x="883" y="352" text-anchor="middle" font-family="DM Sans,sans-serif" font-size="8.5" fill="#a5f3fc">Issues: Tracked</text>

    </svg>
    </div>

    <div class="callout green" style="margin-top:8px;">
      All product demos, live environments, and staging URLs are maintained in the <a href="#">Wiki → Environments</a>.
    </div>
  </section>

  <!-- QMS -->
  <section id="qms">
    <h2>✅ Quality Management System (QMS)</h2>
    <p>Our QMS defines how we maintain and improve quality across the organisation. Full QMS: <a href="#">Wiki → Quality Management System</a></p>
    <ul>
      <li>Testing strategy (unit, integration, end-to-end)</li>
      <li>Release quality gates</li>
      <li>Incident postmortem process</li>
      <li>Audit and compliance requirements</li>
      <li>SLA/SLO definitions per product</li>
    </ul>
  </section>

  <!-- KEY LINKS -->
  <section id="links">
    <h2>🔗 Key Links & Resources</h2>
    <p style="margin-bottom:16px;">Click any card below to open the resource. Replace the <code>#</code> placeholders with your actual document links.</p>

    <div class="links-grid">
      <a class="link-card" href="#">
        <span class="licon">📖</span>
        <div><div style="font-size:12px;color:var(--muted);">Navigation</div>Organisation Wiki</div>
      </a>
      <a class="link-card" href="#">
        <span class="licon">🍳</span>
        <div><div style="font-size:12px;color:var(--muted);">Developer Guide</div>Dev Cookbook</div>
      </a>
      <a class="link-card" href="#">
        <span class="licon">✅</span>
        <div><div style="font-size:12px;color:var(--muted);">Quality</div>QMS</div>
      </a>
      <a class="link-card" href=".github/">
        <span class="licon">⚙️</span>
        <div><div style="font-size:12px;color:var(--muted);">Config</div>Shared GitHub Config (.github)</div>
      </a>
      <a class="link-card" href="CONTRIBUTING.md">
        <span class="licon">🤝</span>
        <div><div style="font-size:12px;color:var(--muted);">Guidelines</div>Contributing Guide</div>
      </a>
      <a class="link-card" href="CODE_OF_CONDUCT.md">
        <span class="licon">📜</span>
        <div><div style="font-size:12px;color:var(--muted);">Policy</div>Code of Conduct</div>
      </a>
      <a class="link-card" href="#">
        <span class="licon">🚀</span>
        <div><div style="font-size:12px;color:var(--muted);">Products</div>4Good Product Demos</div>
      </a>
    </div>
  </section>

</div>

<!-- FOOTER -->
<footer>
  <p>This handbook is a living document. Raise a Discussion or PR to propose changes. All changes go through the standard RFC process.</p>
  <p style="margin-top:8px;">Last Updated: <em>2026-03-11</em> &nbsp;•&nbsp; Version: <em>2.0</em> &nbsp;•&nbsp; Made with care by the <em>PESU Engineering Team</em></p>
</footer>

</body>
</html>
