# Discovery Brief — Ruzzel Maestro Portfolio Website

**Date:** 2026-04-19
**Participants:** Rick / Ruzzel (owner), @lisa (documentation), @jony-ive (design + screenshots), @tony-stark (copy + deployment), @light (screenshots, deferred), @l-lawliet (review)
**Status:** Draft — live session, active decisions still incoming
**Confidence:** Medium
Core structure, design system, and case study list are settled. Tech stack decision (framework TBD by @tony-stark) and design handoff (`rocketturtles-handoff`) pending. 3 of 7 case study pages still need to be built.

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

- **Product type:** Portfolio website — full production build (NOT static prototype)
- **Core interaction model:** Browse/consume — visitors scroll through hero, skills, and case studies, then initiate contact
- **Key differentiator:** Positions Rick as "The Elite Architect of Automation" — premium, focused, high-conviction aesthetic. Not a generic portfolio template.
- **Delivery model:** Git → Vercel. Domain: **rocketturtles.com** (Rick-owned, free Vercel plan supports custom domains with auto-SSL)
- **Tech stack:** To be determined by @tony-stark — must use whatever complete framework is appropriate for production (the existing HTML files are design prototypes only, not the shipping codebase)
- **Evidence quality:** Settled (with stack TBD)

---

## 4. Repository & Technical Details

- **Repo:** `Lezzur/ruzzel-maestro-portfolio`
- **Stack:** TBD — @tony-stark to decide appropriate production framework. **The existing `.html` files in the repo are design prototypes only — not the shipping codebase.**
- **Design source:** Rick provided updated design handoff as `rocketturtles-handoff` in the repo. @jony-ive to locate and apply.
- **Design system reference:** `docs/DESIGN_SYSTEM.md` (may be superseded by `rocketturtles-handoff`)
- **Domain:** `rocketturtles.com` (Rick owns it). Compatible with Vercel free (Hobby) plan — no extra cost, auto-SSL via Let's Encrypt, A record for apex domain.
- **Deployment target:** Vercel
- **Previous deployment:** Netlify (being migrated)
- **Screenshot order:** Protoculture → Accounting-service → Shaiya → Gonogo → Nodeadfish → VaiTAL → asBuilt (Rick's specified order, per @light's assignment)

---

## 5. Design System (Updated)

Base tokens below from original `docs/DESIGN_SYSTEM.md`. Rick has provided an updated design handoff (`rocketturtles-handoff` in repo) — @jony-ive to review and apply. The handoff supersedes the original where they conflict.

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
| 1 | **Protoculture** (Macross) | `Lezzur/protoculture` | — | JavaScript/Node.js | **Built and live** (this is the app we're on right now) | Missing — priority |
| 2 | **Gonogo** | `Lezzur/gonogo` | gonogo-neon.vercel.app | Python | Shipped | `gonogo.html` ✓ |
| 3 | **Nodeadfish** (Job Offer Composer) | `Lezzur/nodeadfish` | — | Next.js + Firebase + Gemini | Built | `nodeadfish.html` ✓ |
| 4 | **VaiTAL** | `Lezzur/VaiTAL` | vaital.vercel.app | Next.js + Supabase + Gemini | Built | `vaital.html` ✓ |
| 5 | **Accounting Service (Numera)** | `Lezzur/accounting-service` | — | Turborepo + Next.js + Supabase + Claude | Full spec complete | Missing |
| 6 | **Shaiya** | `Lezzur/shaiya` | — | Next.js | Built | Missing |
| 7 | **asBuilt** | `Lezzur/asBuilt` | — | Next.js + Firebase | Built | `asbuilt.html` ✓ |

### Protoculture — What It Is (Strongest Case Study)
This is Macross — the multi-agent platform we're running on right now. Built, functioning, and live. Protoculture is the execution backend powering multi-agent orchestration: multi-provider support (Claude, Gemini, OpenAI), Docker-based deployment, agent personalities, room-based collaboration, real-time routing. The strongest case study because it's the most complex system Rick has shipped, and it's demonstrably running in production.

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
- Must ship as a proper production build (not static prototype files)
- Domain: rocketturtles.com on Vercel free plan (confirmed feasible)
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
| Static HTML files are design prototypes only | The existing .html files are not the shipping codebase — @tony-stark to determine production framework | Rick | 2026-04-19 |
| Dark maroon design system | Premium, elite positioning — "Elite Architect of Automation" | Jony Ive | Prior sessions |
| Deployment: Netlify → Vercel | Consolidating to Vercel across all projects | Rick | 2026-04-19 |
| Domain: rocketturtles.com | Rick owns this URL; Vercel free plan supports it with auto-SSL | Rick | 2026-04-19 |
| Protoculture = strongest case study | It IS Macross — built, live, running right now | Rick | 2026-04-19 |
| Updated design handoff: rocketturtles-handoff | Rick provided updated design in repo; supersedes original DESIGN_SYSTEM.md where they conflict | Rick | 2026-04-19 |
| Screenshot order confirmed | Protoculture → Accounting-service → Shaiya → Gonogo → Nodeadfish → VaiTAL → asBuilt | Rick | 2026-04-19 |

---

## 12. Open Questions

All items are either resolved or genuinely post-launch decisions.

| # | Question | Status |
|---|----------|--------|
| OQ-1 | Which screenshots needed per case study page? | Resolved — @jony-ive browsing repos to produce the list |
| OQ-2 | Contact form / CTA mechanism on portfolio site? | Resolved — out of v1 scope (static site, no form backend) |
| OQ-3 | Domain / URL for the portfolio? | Resolved — rocketturtles.com. Vercel free plan supports it. |
| OQ-4 | What production framework for the website? | Open — @tony-stark to decide. Static HTML files are prototypes only. Must use whatever complete tech is appropriate. |
| OQ-5 | Where is the `rocketturtles-handoff` design file? | Open — Rick says it's in the repo but not visible in root or docs/. @jony-ive to locate. |

---

## 13. Recommendation

- **Proceed to build?** Yes — unblocked
- **Immediate next steps:**
  1. @jony-ive: Locate `rocketturtles-handoff` design file in repo and apply updated design direction
  2. @tony-stark: Decide production framework, build the site (HTML files are prototypes only)
  3. @tony-stark: Wire rocketturtles.com → Vercel (A record at DNS registrar, free plan)
  4. @light: Screenshots in Rick's specified order — Protoculture → Accounting-service → Shaiya → Gonogo → Nodeadfish → VaiTAL → asBuilt
- **Suggested focus:** Protoculture page first — it's live (Macross), most complex, sets the bar
- **Launch gate:** All 7 case study pages built + rocketturtles.com live on Vercel. Screenshots additive post-launch.

---

_Document maintained by @lisa. Update this file as decisions are made in session._
