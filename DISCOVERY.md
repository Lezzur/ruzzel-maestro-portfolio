# Discovery Brief — Ruzzel Maestro Portfolio Website

**Date:** 2026-04-19
**Participants:** Rick / Ruzzel (owner), @lisa (documentation), @jony-ive (design + screenshots), @tony-stark (copy + deployment), @light (screenshots, deferred), @l-lawliet (review)
**Status:** Draft — live session, active decisions still incoming
**Confidence:** Medium
Core structure, design system, and case study list are settled. 3 of 7 case study pages still need to be built. Screenshot pipeline and per-case-study copy are unresolved dependencies.

---

## 1. Problem Space

- **The problem:** Rick has 7 substantial AI engineering projects with no single place that presents them coherently to potential clients. Without a portfolio, his capability is invisible — prospects can't evaluate what he's built or why they'd hire him over a generalist.
- **Who experiences it:** Rick, when pursuing freelance/contract work. Prospective clients who need to evaluate him before engaging.
- **Current workarounds:** Fragmented GitHub repos with uneven READMEs, no unified brand or positioning.
- **Why now:** 7 case studies are at a point where they can be showcased. Website is partially built — active sprint to complete and launch.
- **Evidence quality:** Settled

---

## 2. Users and Context

### Primary User: Prospective Clients
- **Who they are:** Founders, operators, or technical leads who need AI automation, integration, or custom tooling built. They are evaluating whether Rick can deliver at the level they need.
- **Context of use:** Likely landed from a referral, LinkedIn, or cold outreach. They're trying to answer "can this person actually build what I need?" Case studies are the primary trust signal.
- **What success looks like:** They initiate contact (email or message).
- **What makes them leave:** No evidence of real work. Generic copy. Slow loading. No clear way to reach out.

### Secondary User: Rick (Self-Representation)
- **Who they are:** The builder — uses the site as a living credential that gets updated as new work ships.
- **Context of use:** Sharing the URL in outreach, proposals, and conversations.

### Anti-Users
- **Who this is NOT for:** Job recruiters looking for a traditional CV. Rick is positioning as an independent specialist, not a job seeker.
- **Evidence quality:** Settled

---

## 3. Proposed Solution Shape

- **Product type:** Static portfolio website (HTML5 + Tailwind CSS CDN + Vanilla JS)
- **Core interaction model:** Browse/consume — visitors scroll through hero, skills, and case studies, then initiate contact
- **Key differentiator:** Positions Rick as "The Elite Architect of Automation" — premium, focused, high-conviction aesthetic. Not a generic portfolio template.
- **Delivery model:** Static files, Git → Vercel (migrating from Netlify — no build process required)
- **Evidence quality:** Settled

---

## 4. Repository & Technical Details

- **Repo:** `Lezzur/ruzzel-maestro-portfolio`
- **Stack:** HTML5 / Tailwind CSS (CDN) / Vanilla JS / Static
- **Design system:** Defined in `docs/DESIGN_SYSTEM.md`
- **Deployment target:** Vercel (no build step — static HTML push-to-deploy)
- **Previous deployment:** Netlify (being migrated)
- **Case study pages (existing):** `gonogo.html`, `asbuilt.html`, `nodeadfish.html`, `vaital.html`
- **Case study pages (missing):** `protoculture.html`, `accounting-service.html`, `shaiya.html`

---

## 5. Design System (Locked)

Approved by Rick in this session. Defined in `docs/DESIGN_SYSTEM.md`.

| Token | Value | Usage |
|---|---|---|
| Background | `#131313` / `#0A0A0A` | Page background |
| Surface | `#201F1F` | Cards, elevated content |
| Primary accent | `#800000` (Maroon) | CTAs, highlights, grid pattern |
| Primary hover | `#FF6B6B` | Active states |
| Text primary | `#E5E2E1` | Body text, headings |
| Text secondary | `#E2BFB9` | Labels, supporting text |
| Heading font | Inter Bold 700–900 | All headings |
| Body font | Inter 400 | All body |
| Label font | Space Grotesk 400–500 | Tags, labels, uppercase UI |
| Border radius | 0px | All elements (sharp corners) |

**Design principles:**
- No 1px borders — use background tonal shifts
- Sharp corners throughout
- Monochromatic — 90% neutral, maroon used sparingly
- Generous whitespace (luxury aesthetic)
- Intentional asymmetry

**3 design decisions from Jony (this session):**
1. Approved
2. Approved
3. Screenshots — deferred until blockers resolved (handled by @light post-sprint)

---

## 6. Case Studies (7 Total)

Rick confirmed 7 case studies. Protoculture is the strongest.

| # | Project | Repo | Live URL | Stack | Status | Page |
|---|---------|------|----------|-------|--------|------|
| 1 | **Protoculture** (MacrossV2) | `Lezzur/protoculture` | — | JavaScript/Node.js | Pre-build, specs complete | Missing — priority |
| 2 | **Gonogo** | `Lezzur/gonogo` | gonogo-neon.vercel.app | Python | Shipped | `gonogo.html` ✓ |
| 3 | **Nodeadfish** (Job Offer Composer) | `Lezzur/nodeadfish` | — | Next.js + Firebase + Gemini | Built | `nodeadfish.html` ✓ |
| 4 | **VaiTAL** | `Lezzur/VaiTAL` | vaital.vercel.app | Next.js + Supabase + Gemini | Built | `vaital.html` ✓ |
| 5 | **Accounting Service (Numera)** | `Lezzur/accounting-service` | — | Turborepo + Next.js + Supabase + Claude | Full spec complete | Missing |
| 6 | **Shaiya** | `Lezzur/shaiya` | — | Next.js | Built | Missing |
| 7 | **asBuilt** | `Lezzur/asBuilt` | — | Next.js + Firebase | Built | `asbuilt.html` ✓ |

### Protoculture — What It Is (Strongest Case Study)
A complete rebuild of the Macross multi-agent chat platform. Protoculture is the execution backend powering an agent orchestration system with 7+ agent phases, multi-provider support (Claude, Gemini, OpenAI), and a Docker-based deployment. All specs are implementation-ready. Positions Rick as someone who builds production-grade AI infrastructure — not just wrappers.

### Gonogo — What It Is
Autonomous AI agent that crawls a web app, runs quality audits across 7 lenses (functionality, design, UX, performance, accessibility, code, content), and delivers dual reports — one for humans, one for coding AIs. Python-based with a web UI.

### Nodeadfish — What It Is
AI-powered job offer composer. Multi-step wizard for composing, sending, and negotiating job offer letters in real time. Role-based access (Owner, Candidate), provision-level negotiation, Firebase persistence, Gemini for conflict detection, `.docx` generation. Next.js + Firebase + Gemini.

### VaiTAL — What It Is
AI-powered personal health intelligence platform. Transforms raw lab reports into actionable insights via document parsing and Google Gemini. Next.js 16 + Supabase + Google Gemini.

### Accounting Service (Numera) — What It Is
Full-stack accounting platform for a PH accounting firm. Marketing website + internal Toolbox (CRM + Workdesk). AI layer handles document ingestion (Gmail API), OCR/parsing (Claude/Gemini), transaction categorization, BIR form generation, and report drafts. Turborepo monorepo. Supabase (PostgreSQL + Auth + Storage + Edge Functions). Most complex architecture of the 7. Full discovery brief, PRD, tech spec, API spec, and barker plan exist in repo.

### Shaiya — What It Is
Content agency Next.js platform consolidating 7 agency modules into a single codebase, single database, single deployment.

### asBuilt — What It Is
AI-powered codebase scanner. Analyzes a codebase and generates two documents: a technical reference for AI coding assistants and a human-readable overview for stakeholders. Inputs: zip, folder, or GitHub repo. Multi-provider LLM support. Next.js + Firebase.

---

## 7. Copy Strategy

- **Source:** Copy for each case study page is extracted from the project's own repo (READMEs, spec docs, discovery briefs). NOT AI-generated placeholders.
- **Owner identity:**
  - Name: Ruzzel Maestro
  - Positioning: "Elite Architect of Automation"
  - Remote — no location stated
  - Contact: rocketturtles.creative@gmail.com
- **Tone:** Premium, direct, technical confidence. Not humble. Not hustle-bro. Architect energy.
- **@tony-stark** is handling copy extraction and placement from project repos.

---

## 8. Screenshot Pipeline

- **Owner:** @light
- **Status:** Deferred — will be produced after other blockers are resolved
- **What's needed:** @jony-ive is browsing the repos and listing which screenshots need to be taken (live app UI shots, architecture diagrams, etc.)
- **Blockers:** Screenshots not needed to unblock remaining 3 case study page builds — copy and layout can proceed without them (image slots can be placeholder-framed)

---

## 9. Scope and Boundaries

### In Scope (v1)
- Main portfolio page (`index.html`) — hero, positioning, case study grid, contact
- 7 individual case study pages (4 done, 3 in progress)
- Design system fully implemented
- Deployed on Vercel (static, no build)

### Explicitly Out of Scope
- Backend / contact form processing — no server, no form submissions v1
- Analytics — not discussed
- Blog / writing section — not discussed
- Mobile-specific UX testing — not discussed, assumed responsive via Tailwind

### Deferred (v2+)
- Screenshots from live apps — deferred pending @light's pipeline
- CTA / contact form depth — not yet decided for portfolio site (exists for rocketanimate separately)

---

## 10. Constraints and Risks

### Hard Constraints
- Static only — no server, no build step (this is a constraint and a feature)
- Netlify → Vercel migration: no-touch, just change deployment target
- No location on site

### Key Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| 3 missing case study pages block launch | High | Medium | Build pages before screenshots; ship with placeholder image frames if needed |
| Copy quality varies by repo README quality | Medium | Medium | @tony-stark extracts from spec docs (discovery briefs, PRDs), not just READMEs |
| Screenshots delayed indefinitely | Low | Low | Pages can ship without screenshots; add when ready |

---

## 11. Key Decisions Log

| Decision | Rationale | Made By | Date |
|----------|-----------|---------|------|
| No location on site | Rick works from anywhere — location is irrelevant and potentially limiting | Rick | 2026-04-19 |
| Copy extracted from project repos | Placeholder copy is worse than no copy — source from actual spec docs | Rick | 2026-04-19 |
| Screenshots deferred | Unblocks page builds; @light handles separately | Rick | 2026-04-19 |
| Static HTML + Tailwind (no framework) | No build pipeline needed; instant deploy; already built | Design/Dev | Prior sessions |
| Dark maroon design system | Premium, elite positioning — "Elite Architect of Automation" | Jony Ive | Prior sessions |
| Deployment: Netlify → Vercel | Consolidating to Vercel across all projects | Rick | 2026-04-19 |
| Protoculture = strongest case study | Most technically complex; demonstrates AI infrastructure depth | Rick | 2026-04-19 |

---

## 12. Open Questions

All items are either resolved or genuinely post-launch decisions.

| # | Question | Status |
|---|----------|--------|
| OQ-1 | Which screenshots needed per case study page? | Resolved — @jony-ive browsing repos to produce the list |
| OQ-2 | Contact form / CTA mechanism on portfolio site? | Resolved — out of v1 scope (static site, no form backend) |
| OQ-3 | Domain / URL for the portfolio? | Open — not stated in session. Assumed Vercel subdomain or custom domain. **Rick to confirm.** |

---

## 13. Recommendation

- **Proceed to build?** Yes — unblocked
- **Immediate next steps:**
  1. @jony-ive: Browse each repo, produce screenshot list
  2. @tony-stark: Build 3 missing case study pages (protoculture, accounting-service, shaiya) using copy from project repos
  3. @tony-stark: Set up git → Vercel deployment (no build, push-to-deploy)
  4. @light: Screenshots pipeline (post-blocker, async)
- **Suggested focus:** Protoculture page first — it's the strongest case study and sets the quality bar for the other two missing pages
- **Launch gate:** All 7 case study pages built + Vercel deployment live. Screenshots are post-launch additive.

---

_Document maintained by @lisa. Update this file as decisions are made in session._
