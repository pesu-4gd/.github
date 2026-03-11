# 4Good.AI — Organisation Handbook

**Last Updated:** 2025-03  
**Owner:** Engineering Excellence Team  
**Status:** Active | Version 2.0

> *"We build technology for good — purposeful products, principled engineering, people-first culture."*

---

## Who We Are

**4Good.AI** is an AI-first product and engineering organisation building intelligent systems that create real-world impact. We operate across multiple product lines under a unified engineering culture — one that values clarity, ownership, and continuous improvement.

If you are new here, this is your starting point. Everything you need to understand how we work, what we build, and how to contribute is either here or linked from here.

---

## Table of Contents

1. [Mission & Vision](#mission--vision)
2. [What We Build — 4Good Products](#what-we-build--4good-products)
3. [Organisation Structure](#organisation-structure)
4. [How We Work — Systems & Flows](#how-we-work--systems--flows)
5. [Project Planning & Sprint Structure](#project-planning--sprint-structure)
6. [Issue & Discussion Workflow](#issue--discussion-workflow)
7. [Issue Templates](#issue-templates)
8. [Bug Triage & Resolution](#bug-triage--resolution)
9. [Team KRAs](#team-kras)
10. [Contributing Standards](#contributing-standards)
11. [Code of Conduct](#code-of-conduct)
12. [Dev Cookbook](#dev-cookbook)
13. [Quality Management System (QMS)](#quality-management-system-qms)
14. [Key Links & Resources](#key-links--resources)
15. [Contacts & Escalation](#contacts--escalation)
16. [Glossary](#glossary)

---

## Mission & Vision

**Mission:** Build AI-powered products that are ethical, accessible, and genuinely useful for people and organisations.

**Vision:** To be a trusted engineering organisation where great ideas become great products — with discipline, speed, and integrity.

**Core Values:**
- Shared ownership — everyone is responsible for quality
- Reliability first — we ship things that work
- Continuous improvement — we get better every sprint
- Collaborative excellence — we build together, not in silos

---

## What We Build — 4Good Products

We maintain multiple products under the 4Good umbrella. Each product has its own repository, team, and roadmap — but all follow the shared standards defined in this handbook.

| Product | Description | Demo URL | Repo |
|---|---|---|---|
| 4Good Product 1 | *(Description)* | [Demo](#) | [Repo](#) |
| 4Good Product 2 | *(Description)* | [Demo](#) | [Repo](#) |
| 4Good Product 3 | *(Description)* | [Demo](#) | [Repo](#) |

> All product demos, live environments, and staging URLs are maintained in the [Wiki → Environments](wiki-link).

---

## Organisation Structure

```
4Good.AI (GitHub Organisation)
│
├── .github/                    ← Org-level templates, workflows, shared configs
├── org-handbook (this repo)    ← Central handbook, standards, non-repo docs
├── product-1/
├── product-2/
├── product-3/
└── shared-libs/
```

**Teams:**
- **Platform & Infrastructure** — shared services, cloud, DevOps
- **Product Engineering** — frontend, backend per product line
- **Security & SRE** — reliability, on-call, compliance
- **QA** — quality processes, test frameworks

Each team links back to this central handbook. Team-specific docs live in their own repos but must reference standards defined here.

---

## How We Work — Systems & Flows

### The Core Flow

```
Discussion → Issue → PR → Deploy → Wiki
```

- **Discussions** are where ideas, proposals, infrastructure decisions, and process questions begin. We talk first before we create work items.
- **Issues** are created from discussions once there is clarity and agreement on what needs to be done.
- **PRs** are linked to issues and go through review before merge.
- **Deploy** follows the release pipeline.
- **Wiki** captures the outcome — decisions, architecture, learnings — for future reference.

> **Key principle:** Discussions are for thinking. Issues are for doing. Wiki is for remembering.

We prioritise discussing *what we are solving and why* over reporting *how fast we are moving*. Velocity is an outcome of clarity, not a goal in itself.

---

## Project Planning & Sprint Structure

### Org-Level Project Plans

Every product team maintains **two project plans** in the org repo:

1. **Feature Release Plan** — tracks upcoming features, milestones, timelines
2. **Bug Tracker** — primarily for production bugs; dev environment bugs tracked separately

Plans live at the org level and individual team repos link into them. This gives leadership visibility across all teams in one place.

### Sprint Structure

- **Sprint duration:** 2 weeks (agreed during Lunch Demo — Shrijul's proposal adopted)
- **Sprint planning** happens between the team and the org repo project board
- **Sprint retro** uses the sprint plan to show what was completed, what was deferred, and why

### Milestones

Each milestone contains:
- Sub-issues broken down by individual
- Tasks assigned clearly with owners
- A delivery date tied to a release or fix window

### Tracking Growth

We track the following to understand team health over time:
- Tasks completed per sprint
- Bugs raised vs bugs resolved
- Milestone completion rate

This gives us a **trend of growth** — not just point-in-time velocity.

---

## Issue & Discussion Workflow

### Step-by-Step Flow

```
1. DISCUSSION (GitHub Discussions)
   └─ Raise the topic — infra, application, process, etc.
   └─ Teams discuss, align, and decide

2. ISSUE (GitHub Issues)
   └─ Created from the discussion once scope is clear
   └─ Tagged with type: Enhancement / Bug / Blank
   └─ Assigned to milestone and person
   └─ PR linked when work begins

3. DEPLOY
   └─ PR merged → pipeline runs → deploy tracked on issue

4. WIKI
   └─ Outcomes, decisions, architecture captured for future reference
```

### Discussion Categories

| Category | Use For |
|---|---|
| Infrastructure | Cloud, DevOps, environment decisions |
| Application | Feature design, architecture, API contracts |
| Process | Sprint planning, workflow changes, team norms |
| Security | Access, compliance, vulnerability disclosures |

---

## Issue Templates

We use three issue templates to keep work items consistent:

### 1. Enhancement
Used for new features, improvements, and planned changes.

Fields: Title, Problem Statement, Proposed Solution, Acceptance Criteria, Linked Discussion, Milestone, Assignee

### 2. Bug
Used for defects found in production or development.

Fields: Title, Environment (Prod/Dev), Steps to Reproduce, Expected vs Actual Behaviour, Severity (P0/P1/P2), Linked RCA, Assignee

### 3. Blank
Use sparingly — only when neither Enhancement nor Bug fits. Prefer structured templates where possible.

> All templates are defined in [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/)

---

## Bug Triage & Resolution

Every bug goes through three stages:

### Stage 1 — Triage
Assign a priority level:
- **P0** — Critical. Production is down or severely impacted. Drop everything.
- **P1** — High. Major feature broken. Fix within current sprint.
- **P2** — Medium. Non-critical issue. Schedule in next sprint.

### Stage 2 — RCA (Root Cause Analysis)
Identify where the issue lives:
- **Ground Level** — code logic, service behaviour
- **Data Access** — database queries, data integrity
- **User Session** — auth, session management, permissions

### Stage 3 — Resolution
Fix is implemented, reviewed, deployed, and documented. Outcome logged in Wiki.

---

## Team KRAs

Each team defines Key Result Areas that align with org-level goals. KRAs are reviewed every quarter.

| Area | What We Measure |
|---|---|
| Reliability | Uptime, MTTR, incident frequency |
| Delivery | Milestone completion rate, sprint throughput |
| Quality | Bug rate, test coverage, P0/P1 incidents |
| Collaboration | PR review turnaround, documentation completeness |
| Growth | New contributors onboarded, knowledge shared |

> Team KRAs are maintained in the [Wiki → Team KRAs](wiki-link). Each team lead is responsible for updating them each quarter.

---

## Contributing Standards

Before contributing to any repo in this organisation, please read:

- [Contributing Guide](CONTRIBUTING.md) — how to raise issues, submit PRs, and get reviews
- [Branching & Git Workflow](wiki-link) — naming conventions, branch strategy, commit standards
- [Code Review Standards](wiki-link) — what reviewers look for, turnaround expectations
- [Versioning Policy](wiki-link) — how we version releases

**Quick rules:**
- Always create a Discussion before an Issue for any significant change
- Link your PR to its Issue
- No direct pushes to `main` — all changes go through PRs
- Every PR needs at least one reviewer approval

---

## Code of Conduct

We expect everyone in this organisation — contributors, reviewers, leads — to act with respect and professionalism.

Full Code of Conduct: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

Summary:
- Be kind and constructive in reviews and discussions
- Assume good intent
- Raise concerns through the right channels
- Zero tolerance for harassment or exclusion

---

## Dev Cookbook

The Dev Cookbook is your practical guide to getting things done here. It covers:

- Setting up your local development environment
- Running services locally and with Docker
- Common debugging patterns
- How to use our internal tooling and libraries
- Environment variables and secrets management
- How to write and run tests

Full Cookbook: [Wiki → Dev Cookbook](wiki-link)

---

## Quality Management System (QMS)

Our QMS defines how we maintain and improve quality across the organisation. It covers:

- Testing strategy (unit, integration, end-to-end)
- Release quality gates
- Incident postmortem process
- Audit and compliance requirements
- SLA/SLO definitions per product

Full QMS: [Wiki → Quality Management System](wiki-link)

---

## Key Links & Resources

| Resource | Link |
|---|---|
| Organisation Wiki | [Wiki Home](wiki-link) |
| Dev Cookbook | [Wiki → Dev Cookbook](wiki-link) |
| QMS | [Wiki → QMS](wiki-link) |
| Org-Level Project Plans | [GitHub Projects](projects-link) |
| Shared GitHub Config | [.github repo](.github/) |
| Issue Templates | [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) |
| Contributing Guide | [CONTRIBUTING.md](CONTRIBUTING.md) |
| Code of Conduct | [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) |
| 4Good Product Demos | [Wiki → Environments](wiki-link) |
| Team KRAs | [Wiki → Team KRAs](wiki-link) |

---

## Contacts & Escalation

| Role | Responsibilities | Contact |
|---|---|---|
| CTO / Head of Engineering | Vision, architecture, major decisions | `@cto` |
| Platform Lead | Shared services, infrastructure | `@platform-lead` |
| Security Lead | Security, audits, compliance | `@security` |
| SRE Lead | On-call, monitoring, reliability | `@sre` |
| Engineering Manager | Team leadership, delivery | `@eng-manager` |

For incidents: follow the [Incident Response Process](wiki-link)  
For access issues: contact `@platform-lead`  
For process questions: raise a Discussion under the Process category

---

## Glossary

| Term | Meaning |
|---|---|
| KRA | Key Result Area — what a team is measured on |
| P0 / P1 / P2 | Bug priority levels (P0 = critical) |
| RCA | Root Cause Analysis — understanding why a bug happened |
| RFC | Request for Comments — a formal proposal for a process or architectural change |
| SLO | Service Level Objective — internal reliability target |
| SLA | Service Level Agreement — external reliability commitment |
| MTTR | Mean Time to Recovery — how fast we recover from incidents |
| Sprint Retro | Sprint Retrospective — team review of what was completed and what to improve |
| QMS | Quality Management System |
| Triage | The process of classifying and prioritising bugs |

---

*This handbook is a living document. Raise a Discussion or PR to propose changes. All changes go through the standard RFC process.*

**Made with care by the 4Good.AI Engineering Team**
