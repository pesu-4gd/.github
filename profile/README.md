<div align="center">

<img src="https://img.shields.io/badge/Status-Active-27ae60?style=for-the-badge&labelColor=0b0f1a" />
<img src="https://img.shields.io/badge/Version-2.0-3b82f6?style=for-the-badge&labelColor=0b0f1a" />
<img src="https://img.shields.io/badge/Last_Updated-2026--03--11-f59e0b?style=for-the-badge&labelColor=0b0f1a" />

# PESU Project Plan

*"We build technology for good — purposeful products, principled engineering, people-first culture."*

🏢 **Owner: Engineering Excellence Team** &nbsp;|&nbsp; 📍 **4Good.AI Organisation** &nbsp;|&nbsp; 🔄 **Living Document**

</div>

---

## 🤝 Code of Conduct

We expect everyone in this organisation — contributors, reviewers, leads — to act with respect and professionalism.

📄 Full Code of Conduct: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

- Be kind and constructive in reviews and discussions
- Assume good intent
- Raise concerns through the right channels
- Zero tolerance for harassment or exclusion

---

## 🍳 4Good Dev Cookbook

Your practical guide to getting things done here. 📖 Full Cookbook: [Wiki → Dev Cookbook](#)

- Setting up your local development environment
- Running services locally and with Docker
- Common debugging patterns
- How to use our internal tooling and libraries
- Environment variables and secrets management
- How to write and run tests

---

## 🎯 Mission & Vision

**Mission:** Build AI-powered products that are ethical, accessible, and genuinely useful for people and organisations.

**Vision:** To be a trusted engineering organisation where great ideas become great products — with discipline, speed, and integrity.

### Core Values

| Value | Description |
|---|---|
| 🤝 Shared Ownership | Everyone is responsible for quality |
| 🛡️ Reliability First | We ship things that work |
| 🔄 Continuous Improvement | We get better every sprint |
| 🌟 Collaborative Excellence | We build together, not in silos |

---

## 🌿 PESU Products

All products under the PESU umbrella. Each has its own repo, team, and roadmap — all governed by shared standards in this handbook.

<div align="center">

```
                        ┌─────────────────────────────┐
                        │      4Good.AI — PESU         │
                        │   Engineering Organisation   │
                        └──────────────┬──────────────┘
                                       │
          ┌──────────┬──────────┬──────┴──────┬──────────┬──────────┐
          │          │          │             │          │          │
```

</div>

<div align="center">

<svg viewBox="0 0 1060 340" xmlns="http://www.w3.org/2000/svg" width="100%">
  <defs>
    <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <linearGradient id="lg1" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#16a34a"/></linearGradient>
    <linearGradient id="lg2" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#d97706"/></linearGradient>
    <linearGradient id="lg3" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#3b82f6"/></linearGradient>
    <linearGradient id="lg4" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#8b5cf6"/></linearGradient>
    <linearGradient id="lg5" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#ec4899"/></linearGradient>
    <linearGradient id="lg6" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="#06b6d4"/></linearGradient>
  </defs>

  <!-- ROOT NODE -->
  <rect x="340" y="10" width="380" height="58" rx="14" fill="#0f1e38" stroke="#3b82f6" stroke-width="2" filter="url(#glow)"/>
  <text x="530" y="34" text-anchor="middle" font-family="Arial,sans-serif" font-size="16" font-weight="800" fill="#93c5fd">4Good.AI — PESU</text>
  <text x="530" y="54" text-anchor="middle" font-family="Arial,sans-serif" font-size="10" fill="#4a6888" letter-spacing="1.5">ENGINEERING ORGANISATION</text>

  <!-- VERTICAL STEM -->
  <line x1="530" y1="68" x2="530" y2="104" stroke="#3b82f6" stroke-width="2"/>

  <!-- HORIZONTAL RAIL -->
  <line x1="88" y1="104" x2="972" y2="104" stroke="#1e3a5f" stroke-width="2"/>

  <!-- BRANCH DROPS -->
  <line x1="88"  y1="104" x2="88"  y2="132" stroke="url(#lg1)" stroke-width="2"/>
  <line x1="247" y1="104" x2="247" y2="132" stroke="url(#lg2)" stroke-width="2"/>
  <line x1="406" y1="104" x2="406" y2="132" stroke="url(#lg3)" stroke-width="2"/>
  <line x1="565" y1="104" x2="565" y2="132" stroke="url(#lg4)" stroke-width="2"/>
  <line x1="724" y1="104" x2="724" y2="132" stroke="url(#lg5)" stroke-width="2"/>
  <line x1="883" y1="104" x2="883" y2="132" stroke="url(#lg6)" stroke-width="2"/>

  <!-- RAIL DOTS -->
  <circle cx="88"  cy="104" r="4" fill="#16a34a"/>
  <circle cx="247" cy="104" r="4" fill="#d97706"/>
  <circle cx="406" cy="104" r="4" fill="#3b82f6"/>
  <circle cx="565" cy="104" r="4" fill="#8b5cf6"/>
  <circle cx="724" cy="104" r="4" fill="#ec4899"/>
  <circle cx="883" cy="104" r="4" fill="#06b6d4"/>
  <circle cx="530" cy="104" r="5" fill="#3b82f6"/>

  <!-- CARD 1 — Evals (green) -->
  <rect x="19" y="132" width="138" height="190" rx="13" fill="#0f2a1e" stroke="#16a34a" stroke-width="1.5"/>
  <text x="88" y="162" text-anchor="middle" font-size="20">🧪</text>
  <text x="88" y="182" text-anchor="middle" font-family="Arial,sans-serif" font-size="12" font-weight="700" fill="#4ade80">Evals</text>
  <text x="88" y="198" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#86efac">AI evaluation &amp;</text>
  <text x="88" y="210" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#86efac">benchmarking</text>
  <rect x="26" y="222" width="36" height="16" rx="4" fill="rgba(22,163,74,0.25)" stroke="#16a34a" stroke-width="0.8"/>
  <text x="44" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#4ade80">DEMO</text>
  <rect x="69" y="222" width="36" height="16" rx="4" fill="rgba(22,163,74,0.25)" stroke="#16a34a" stroke-width="0.8"/>
  <text x="87" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#4ade80">REPO</text>
  <rect x="112" y="222" width="36" height="16" rx="4" fill="rgba(22,163,74,0.25)" stroke="#16a34a" stroke-width="0.8"/>
  <text x="130" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#4ade80">DOCS</text>
  <line x1="30" y1="248" x2="146" y2="248" stroke="#16a34a" stroke-width="0.5" opacity="0.3"/>
  <text x="88" y="265" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" fill="#4a7a5a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
  <rect x="28" y="273" width="117" height="38" rx="7" fill="rgba(22,163,74,0.07)" stroke="#16a34a" stroke-width="0.5"/>
  <text x="88" y="288" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#86efac">Wiki: Linked</text>
  <text x="88" y="302" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#86efac">Issues: Tracked</text>

  <!-- CARD 2 — Digital Strategy (amber) -->
  <rect x="178" y="132" width="138" height="190" rx="13" fill="#1e1a0f" stroke="#d97706" stroke-width="1.5"/>
  <text x="247" y="162" text-anchor="middle" font-size="20">📈</text>
  <text x="247" y="182" text-anchor="middle" font-family="Arial,sans-serif" font-size="12" font-weight="700" fill="#fbbf24">Digital Strategy</text>
  <text x="247" y="198" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#fcd34d">Strategic insights &amp;</text>
  <text x="247" y="210" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#fcd34d">analytics tools</text>
  <rect x="185" y="222" width="36" height="16" rx="4" fill="rgba(217,119,6,0.25)" stroke="#d97706" stroke-width="0.8"/>
  <text x="203" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#fbbf24">DEMO</text>
  <rect x="228" y="222" width="36" height="16" rx="4" fill="rgba(217,119,6,0.25)" stroke="#d97706" stroke-width="0.8"/>
  <text x="246" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#fbbf24">REPO</text>
  <rect x="271" y="222" width="36" height="16" rx="4" fill="rgba(217,119,6,0.25)" stroke="#d97706" stroke-width="0.8"/>
  <text x="289" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#fbbf24">DOCS</text>
  <line x1="189" y1="248" x2="305" y2="248" stroke="#d97706" stroke-width="0.5" opacity="0.3"/>
  <text x="247" y="265" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" fill="#7a5a20" letter-spacing="0.5">PESU · 4GOOD.AI</text>
  <rect x="187" y="273" width="117" height="38" rx="7" fill="rgba(217,119,6,0.07)" stroke="#d97706" stroke-width="0.5"/>
  <text x="247" y="288" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#fcd34d">Wiki: Linked</text>
  <text x="247" y="302" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#fcd34d">Issues: Tracked</text>

  <!-- CARD 3 — Placements (blue) -->
  <rect x="337" y="132" width="138" height="190" rx="13" fill="#0f1a2e" stroke="#3b82f6" stroke-width="1.5"/>
  <text x="406" y="162" text-anchor="middle" font-size="20">🎓</text>
  <text x="406" y="182" text-anchor="middle" font-family="Arial,sans-serif" font-size="12" font-weight="700" fill="#60a5fa">Placements</text>
  <text x="406" y="198" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#93c5fd">Career placement &amp;</text>
  <text x="406" y="210" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#93c5fd">recruitment system</text>
  <rect x="344" y="222" width="36" height="16" rx="4" fill="rgba(59,130,246,0.25)" stroke="#3b82f6" stroke-width="0.8"/>
  <text x="362" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#60a5fa">DEMO</text>
  <rect x="387" y="222" width="36" height="16" rx="4" fill="rgba(59,130,246,0.25)" stroke="#3b82f6" stroke-width="0.8"/>
  <text x="405" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#60a5fa">REPO</text>
  <rect x="430" y="222" width="36" height="16" rx="4" fill="rgba(59,130,246,0.25)" stroke="#3b82f6" stroke-width="0.8"/>
  <text x="448" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#60a5fa">DOCS</text>
  <line x1="348" y1="248" x2="464" y2="248" stroke="#3b82f6" stroke-width="0.5" opacity="0.3"/>
  <text x="406" y="265" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" fill="#2a4a7a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
  <rect x="346" y="273" width="117" height="38" rx="7" fill="rgba(59,130,246,0.07)" stroke="#3b82f6" stroke-width="0.5"/>
  <text x="406" y="288" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#93c5fd">Wiki: Linked</text>
  <text x="406" y="302" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#93c5fd">Issues: Tracked</text>

  <!-- CARD 4 — Experimental (purple) -->
  <rect x="496" y="132" width="138" height="190" rx="13" fill="#1a0f2e" stroke="#8b5cf6" stroke-width="1.5"/>
  <text x="565" y="162" text-anchor="middle" font-size="20">⚗️</text>
  <text x="565" y="182" text-anchor="middle" font-family="Arial,sans-serif" font-size="12" font-weight="700" fill="#a78bfa">Experimental</text>
  <text x="565" y="198" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#c4b5fd">R&amp;D sandbox</text>
  <text x="565" y="210" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#c4b5fd">for new ideas</text>
  <rect x="503" y="222" width="36" height="16" rx="4" fill="rgba(139,92,246,0.25)" stroke="#8b5cf6" stroke-width="0.8"/>
  <text x="521" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#a78bfa">DEMO</text>
  <rect x="546" y="222" width="36" height="16" rx="4" fill="rgba(139,92,246,0.25)" stroke="#8b5cf6" stroke-width="0.8"/>
  <text x="564" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#a78bfa">REPO</text>
  <rect x="589" y="222" width="36" height="16" rx="4" fill="rgba(139,92,246,0.25)" stroke="#8b5cf6" stroke-width="0.8"/>
  <text x="607" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#a78bfa">DOCS</text>
  <line x1="507" y1="248" x2="623" y2="248" stroke="#8b5cf6" stroke-width="0.5" opacity="0.3"/>
  <text x="565" y="265" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" fill="#4a3a7a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
  <rect x="505" y="273" width="117" height="38" rx="7" fill="rgba(139,92,246,0.07)" stroke="#8b5cf6" stroke-width="0.5"/>
  <text x="565" y="288" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#c4b5fd">Wiki: Linked</text>
  <text x="565" y="302" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#c4b5fd">Issues: Tracked</text>

  <!-- CARD 5 — Alumni Portal (pink) -->
  <rect x="655" y="132" width="138" height="190" rx="13" fill="#1a0f14" stroke="#ec4899" stroke-width="1.5"/>
  <text x="724" y="162" text-anchor="middle" font-size="20">🏛️</text>
  <text x="724" y="182" text-anchor="middle" font-family="Arial,sans-serif" font-size="12" font-weight="700" fill="#f472b6">Alumni Portal</text>
  <text x="724" y="198" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#fbcfe8">Alumni network &amp;</text>
  <text x="724" y="210" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#fbcfe8">engagement hub</text>
  <rect x="662" y="222" width="36" height="16" rx="4" fill="rgba(236,72,153,0.25)" stroke="#ec4899" stroke-width="0.8"/>
  <text x="680" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#f472b6">DEMO</text>
  <rect x="705" y="222" width="36" height="16" rx="4" fill="rgba(236,72,153,0.25)" stroke="#ec4899" stroke-width="0.8"/>
  <text x="723" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#f472b6">REPO</text>
  <rect x="748" y="222" width="36" height="16" rx="4" fill="rgba(236,72,153,0.25)" stroke="#ec4899" stroke-width="0.8"/>
  <text x="766" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#f472b6">DOCS</text>
  <line x1="666" y1="248" x2="782" y2="248" stroke="#ec4899" stroke-width="0.5" opacity="0.3"/>
  <text x="724" y="265" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" fill="#7a2a4a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
  <rect x="664" y="273" width="117" height="38" rx="7" fill="rgba(236,72,153,0.07)" stroke="#ec4899" stroke-width="0.5"/>
  <text x="724" y="288" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#fbcfe8">Wiki: Linked</text>
  <text x="724" y="302" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#fbcfe8">Issues: Tracked</text>

  <!-- CARD 6 — Course Generation (cyan) -->
  <rect x="814" y="132" width="138" height="190" rx="13" fill="#0a1e22" stroke="#06b6d4" stroke-width="1.5"/>
  <text x="883" y="162" text-anchor="middle" font-size="20">📚</text>
  <text x="883" y="182" text-anchor="middle" font-family="Arial,sans-serif" font-size="12" font-weight="700" fill="#22d3ee">Course Generation</text>
  <text x="883" y="198" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#a5f3fc">AI-powered curriculum</text>
  <text x="883" y="210" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" fill="#a5f3fc">&amp; course builder</text>
  <rect x="821" y="222" width="36" height="16" rx="4" fill="rgba(6,182,212,0.25)" stroke="#06b6d4" stroke-width="0.8"/>
  <text x="839" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#22d3ee">DEMO</text>
  <rect x="864" y="222" width="36" height="16" rx="4" fill="rgba(6,182,212,0.25)" stroke="#06b6d4" stroke-width="0.8"/>
  <text x="882" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#22d3ee">REPO</text>
  <rect x="907" y="222" width="36" height="16" rx="4" fill="rgba(6,182,212,0.25)" stroke="#06b6d4" stroke-width="0.8"/>
  <text x="925" y="233" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="700" fill="#22d3ee">DOCS</text>
  <line x1="825" y1="248" x2="941" y2="248" stroke="#06b6d4" stroke-width="0.5" opacity="0.3"/>
  <text x="883" y="265" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" fill="#1a5a6a" letter-spacing="0.5">PESU · 4GOOD.AI</text>
  <rect x="823" y="273" width="117" height="38" rx="7" fill="rgba(6,182,212,0.07)" stroke="#06b6d4" stroke-width="0.5"/>
  <text x="883" y="288" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#a5f3fc">Wiki: Linked</text>
  <text x="883" y="302" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" fill="#a5f3fc">Issues: Tracked</text>
</svg>

</div>

> 📌 All product demos, live environments, and staging URLs are maintained in the [Wiki → Environments](#)

---

## ✅ Quality Management System (QMS)

Our QMS defines how we maintain and improve quality across the organisation. 📖 Full QMS: [Wiki → Quality Management System](#)

- Testing strategy (unit, integration, end-to-end)
- Release quality gates
- Incident postmortem process
- Audit and compliance requirements
- SLA/SLO definitions per product

---

## 🔗 Key Links & Resources

| Resource | Link |
|---|---|
| 📖 Organisation Wiki | [Wiki Home](#) |
| 🍳 Dev Cookbook | [Wiki → Dev Cookbook](#) |
| ✅ QMS | [Wiki → Quality Management System](#) |
| ⚙️ Shared GitHub Config | [.github repo](.github/) |
| 🤝 Contributing Guide | [CONTRIBUTING.md](CONTRIBUTING.md) |
| 📜 Code of Conduct | [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) |
| 🚀 4Good Product Demos | [Wiki → Environments](#) |

---

<div align="center">

*This handbook is a living document. Raise a Discussion or PR to propose changes.*

**Last Updated: 2026-03-11 • Version: 2.0 • Made with care by the PESU Engineering Team**

</div>
