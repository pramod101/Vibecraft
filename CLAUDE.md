# CLAUDE.md — AI Assistant Guide for VibeCraft

This file provides context for AI assistants (Claude, ChatGPT, Gemini, etc.) working within the VibeCraft repository. It explains the codebase structure, conventions, and how to assist effectively.

---

## What Is This Repository?

**VibeCraft** is a **meta-framework** — not an application, but a structured system for building applications with AI assistance ("vibe coding"). It provides:

- A repeatable 8-stage SDLC process
- Reusable document templates for each stage
- Reference examples of completed projects
- Guidance for producing enterprise-grade deliverables using AI tools

This repository is **documentation-only**. There is no application source code, build system, test runner, or CI/CD pipeline at the root level.

---

## Repository Structure

```
Vibecraft/
├── README.md                          # Framework overview and getting started guide
├── CLAUDE.md                          # This file — AI assistant context
├── docs/                              # 8-stage SDLC documentation + reusable templates
│   ├── 01_Strategy_and_Vision.md      # Stage 1: Define "why" before building
│   ├── 02_Requirements.md             # Stage 2: PRD, functional/non-functional specs
│   ├── 03_Design.md                   # Stage 3: Architecture, HLD, wireframes
│   ├── 04_Build.md                    # Stage 4: Implementation guidance
│   ├── 05_Testing.md                  # Stage 5: Test strategy and test cases
│   ├── 06_Deployment.md               # Stage 6: CI/CD and release plans
│   ├── 07_Documentation_Practices.md  # Stage 7: Living documentation standards
│   ├── 08_Maintenance.md              # Stage 8: Sustain and evolve
│   ├── PRD_TEMPLATE.md                # Reusable Product Requirements Document
│   ├── HLD_TEMPLATE.md                # Reusable High-Level Design template
│   ├── TEST_PLAN_TEMPLATE.md          # Reusable test plan template
│   ├── DEPLOYMENT_CHECKLIST.md        # Pre/post-deployment checklist
│   ├── lenny-learning-hub.html        # External reference: Lenny's learning resources
│   ├── lenny-tools.html               # External reference: Lenny's tools
│   ├── lenny_guest_intelligence_v2.html
│   └── lenny_saas_benchmark_explorer.html
├── BoltApps/                          # Example: apps built with Bolt.new
│   ├── ZenFocus                       # Meditation/focus app (React + TypeScript + Vite)
│   └── Zen Focus                      # Alternate name reference (same project)
└── GoogleAIStudio/                    # Example: apps built with Google AI Studio
    ├── AccMgrAgent                    # Account Manager AI agent documentation
    └── strategic-account-planning-agent.zip
```

---

## The 8-Stage SDLC Process

Every project following VibeCraft should progress through these stages in order:

| Stage | File | Purpose | Key Artifact |
|-------|------|---------|-------------|
| 1 | `01_Strategy_and_Vision.md` | Define the problem and value | Vision statement (1 page) |
| 2 | `02_Requirements.md` | Define what must be built | PRD with acceptance criteria |
| 3 | `03_Design.md` | Architecture and UX blueprint | HLD, LLD, wireframes |
| 4 | `04_Build.md` | Implement the solution | Working code with API contracts |
| 5 | `05_Testing.md` | Validate correctness | Test plan and results |
| 6 | `06_Deployment.md` | Release to users | Deployment plan and checklist |
| 7 | `07_Documentation_Practices.md` | Capture knowledge | Dev docs, runbooks |
| 8 | `08_Maintenance.md` | Sustain and evolve | Maintenance notes, metrics |

**Do not skip stages.** Each stage produces a deliverable that informs the next.

---

## Document Templates

Templates live in `docs/` and should be **copied, not modified in place**, when starting a new project.

| Template | File | When to Use |
|----------|------|------------|
| PRD | `docs/PRD_TEMPLATE.md` | Start of every project (Stage 2) |
| HLD | `docs/HLD_TEMPLATE.md` | After PRD is approved (Stage 3) |
| Test Plan | `docs/TEST_PLAN_TEMPLATE.md` | Before implementation begins (Stage 5) |
| Deployment Checklist | `docs/DEPLOYMENT_CHECKLIST.md` | Before any release (Stage 6) |

---

## Application Complexity Levels

VibeCraft supports 5 levels of increasing complexity. Always clarify which level applies before making architecture decisions:

| Level | Type | Typical Build Time | Example Projects |
|-------|------|--------------------|-----------------|
| 1 | Static Sites | 10–20 min | Landing pages, portfolios |
| 2 | Interactive UI | 20–40 min | Calculators, lead capture forms |
| 3 | BaaS Integration | 45–90 min | Dashboards, data trackers |
| 4 | Full-Stack CRUD | 2–4 hours | CRM, workflow tools |
| 5 | Enterprise SaaS | Days | Multi-tenant platforms |

---

## Supported Tools and Tech Stack

### AI Tools
- **ChatGPT Plus / Google AI Pro / Claude** — Primary co-pilots for all stages
- **ChatPRD** — Specialized for generating PRDs and strategy documents

### Development Platforms
- **Bolt.new** — Rapid front-end and full-stack apps (React, TypeScript, Vite)
- **Replit** — Browser-based IDE for full-stack development
- **Lovable** — AI-native app builder

### Backend / BaaS
- **Firebase** — Auth, Firestore, Functions
- **Supabase** — Postgres-based BaaS alternative

### Hosting
- **Railway** — Simple deployment for containerized apps and APIs

### Design & UX
- **Framer** — Interaction design and prototyping
- **Figma** — UI design and wireframing
- **Mobbin / Magic Patterns** — UI inspiration and pattern references

### Integration & Testing
- **Postman** — API testing and documentation
- **n8n** — Workflow automation
- **PostHog** — Analytics and feature flags

---

## Example Projects

### Zen Focus (`BoltApps/ZenFocus`)
- **Type:** Meditation and focus timer app
- **Stack:** React, TypeScript, Vite, Tailwind CSS, Web Audio API, Lucide React
- **Built with:** Bolt.new
- **Features:** 4-second breathing cycles, session durations (5/10/15/30 min), 432Hz bell audio, animated gradients

### Account Manager Agent (`GoogleAIStudio/AccMgrAgent`)
- **Type:** AI-powered strategic account planning agent
- **Built with:** Google AI Studio
- **Purpose:** Helps account managers identify high-value opportunities

---

## Core Conventions for AI Assistants

### When Helping with Documentation
- Follow the template structure exactly — sections, headings, and order matter
- Keep Vision Statements to 1–2 sentences maximum
- Success metrics must be **measurable and quantitative**
- Each stage document should end with a "Deliverables Checklist"
- Documents should be written for an **executive and engineering audience simultaneously**

### When Helping with Code (BoltApps / examples)
- Preferred stack for new projects: **React + TypeScript + Vite + Tailwind CSS**
- Use **Lucide React** for icons
- Use **Web Audio API** for any audio functionality (no third-party audio libs unless necessary)
- Code should be self-contained and deployable from Bolt.new or Replit without external setup

### When Adding New Examples
- Create a subdirectory under `BoltApps/` (Bolt-generated apps) or `GoogleAIStudio/` (AI Studio agents)
- Include a README.md documenting: what the app does, tech stack, how to run it, and key features
- Reference the VibeCraft SDLC stage artifacts that were used to build it

### When Updating Framework Documentation
- Stage documents (`01_` through `08_`) define the **framework itself** — edit conservatively
- Templates in `docs/` are the canonical starting points for new projects — keep them generic and reusable
- The `README.md` is the main entry point — keep it concise and accurate

---

## What This Repository Is NOT

- Not a deployable application
- Not a monorepo with shared packages or build tooling
- Not a place to store production code (examples only)
- No automated tests, linters, or CI/CD pipelines at root level

---

## Git Workflow

- **Default branch:** `master`
- **Remote:** `https://github.com/pramod101/Vibecraft`
- **Author:** Pramod Kumar
- Commit messages use plain `"Add files via upload"` style historically; prefer descriptive messages for new commits
- No branch protection rules configured; push directly to `master` for framework updates

---

## Philosophy

1. **Deliver something valuable early** — Start lean, at Complexity Level 1 or 2
2. **Iterate with structure** — Add discipline and documentation incrementally
3. **Produce professional artifacts** — Every stage should generate something stakeholders can read
4. **Version and evolve** — This framework improves with every project that uses it

---

## Quick Reference: Required Artifacts per Project

Before any project is considered complete, it should have produced:

- [ ] Vision & Strategy statement (1 page)
- [ ] PRD with user stories and acceptance criteria
- [ ] HLD with architecture diagram
- [ ] Wireframes or UI flow
- [ ] Test plan and test results log
- [ ] Deployment plan and post-deployment verification
- [ ] Technical documentation and user guide
- [ ] Maintenance notes and monitoring setup

---

*Last updated: 2026-03-21*
*Framework version: 0.1.0*
*Maintained by: [Pramod Kumar](https://github.com/pramod101)*
