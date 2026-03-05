# PIPELINE PANIC: A Data Platform Consultant Game

## Game Design Document
**Designer:** Vex | **Version:** 1.0 | **Date:** 2026-03-05

---

## High Concept

You are **Morgan Flux**, an independent data platform consultant dropped into increasingly chaotic organizations. Each client is a ticking time bomb of broken pipelines, political infighting, legacy systems, and impossible deadlines. Your job: untangle their data nightmares, build something that actually works, and get out before the whole thing collapses — or your reputation does.

**Genre:** Strategy / Puzzle / Narrative Sim
**Platform:** PC (Steam), with potential mobile port for the lite mode
**Tone:** Dark comedy meets tech thriller. Think *Papers, Please* meets *Ace Attorney* meets the worst Jira board you've ever seen.

---

## What Makes It Fun

The core fantasy is **being the smartest person in the room in a room full of chaos**. Every engagement starts with a mystery: something is broken, nobody agrees on what, and everyone has an agenda. You diagnose, design, persuade, and build — under pressure, with incomplete information, against competing interests.

The game is fun because:
1. **Discovery is intrinsically rewarding** — peeling back layers of a broken system to find the root cause
2. **Every decision has tradeoffs** — there's no "correct" architecture, only the best one given constraints
3. **Human dynamics matter as much as technical skill** — the VP who wants a dashboard yesterday, the engineer who refuses to touch the legacy system, the CEO who just read an article about AI
4. **Emergent storytelling** — your choices cascade into consequences across engagements

---

## Core Mechanics

### 1. The Engagement Loop

Each level is a **client engagement** with three phases:

#### Phase 1: Discovery (Exploration/Puzzle)
- You arrive at a new client. Their data platform is visualized as an interconnected **system map** — nodes (databases, warehouses, pipelines, dashboards, APIs) connected by data flows.
- Flows are color-coded by health: green (healthy), yellow (degraded), red (broken), gray (unknown).
- Most of the map starts gray. You uncover it by **interviewing stakeholders**, **reading documentation** (often outdated or wrong), **running queries**, and **tracing data lineage**.
- Discovery is time-boxed. You can't learn everything. Choose where to dig.

#### Phase 2: Design (Strategy)
- Based on what you've learned, you propose an **architecture plan** on a blueprint board.
- Drag and drop components: data lakes, warehouses, streaming layers, orchestrators, transformation engines, governance layers, ML feature stores.
- Each component has **cost**, **complexity**, **reliability**, and **time-to-implement** stats.
- Components interact — some synergize, some conflict. A streaming layer + batch warehouse = hybrid architecture (flexible but complex). Going all-in on one paradigm is simpler but brittle.
- You must satisfy **client requirements** (displayed as constraint cards) while staying within **budget** and **timeline**.
- The client reviews your design. Different stakeholders react differently. The CFO cares about cost. The CTO cares about elegance. The data team cares about maintainability. You can't please everyone.

#### Phase 3: Implementation (Real-Time Strategy)
- Time accelerates. You manage **a team of engineers** (assigned or hired) building out your design.
- Engineers have specialties, personalities, and morale. A Spark expert assigned to dbt work gets frustrated. A junior dev on a critical path is risky but learns fast.
- **Incidents** fire randomly — pipeline failures, data quality alerts, vendor outages, security breaches. You triage in real-time: fix now, defer, escalate, or ignore (at your peril).
- A **technical debt meter** tracks shortcuts. Rush too much and it compounds. Leave too much debt and the system collapses post-delivery.
- Implementation ends when you hit the deadline or deliver early (bonus reputation).

### 2. Reputation System

Your **reputation** is your meta-progression currency, tracked across three axes:

| Axis | Earned By | Lost By |
|------|-----------|---------|
| **Technical Credibility** | Elegant designs, correct diagnoses, clean implementations | Over-engineering, misdiagnoses, production incidents |
| **Business Acumen** | On-budget, clear ROI, stakeholder satisfaction | Cost overruns, missed deadlines, ignoring business needs |
| **Team Leadership** | High morale, mentoring, clear communication | Burnout, blame-shifting, micromanagement |

Reputation unlocks:
- **Better clients** (more interesting problems, higher stakes)
- **Talent pool** (access to senior engineers, specialists)
- **Negotiating power** (bigger budgets, longer timelines, scope control)
- **Story branches** (high-reputation paths unlock secret engagements)

### 3. The Consultant's Toolkit

You carry a **toolkit** that grows over the campaign:

| Tool | Use |
|------|-----|
| **Profiler** | Run diagnostic queries on data systems to reveal hidden issues |
| **Lineage Tracer** | Visualize where data flows from source to consumption |
| **Schema Inspector** | Examine table structures, spot normalization issues, find orphaned columns |
| **Query Explainer** | Break down slow queries to find optimization opportunities |
| **Stakeholder Dossier** | Notes on each person's motivations, politics, and reliability |
| **Architecture Templates** | Pre-built patterns (Lambda, Kappa, Medallion, Mesh) you can customize |
| **Incident Playbooks** | Automated responses to common failures (unlocked through experience) |

### 4. The Politics Layer

Every client has an **org chart** with hidden dynamics:

- **Allies** who support your work and provide resources
- **Blockers** who resist change (the DBA who's been running the same Oracle instance since 2008)
- **Wild Cards** who might help or hinder depending on how you play them
- **Shadow IT** — rogue departments running their own data stacks that nobody told you about

You manage politics through **dialogue encounters** (branching conversations with skill checks). Say the right thing to the resistant VP and they become an ally. Push too hard and they escalate to the CEO to kill your project.

---

## Storyline

### Act 1: The Grind (Engagements 1-4)
Morgan is a newly independent consultant after getting burned out at a big consulting firm. Early clients are small — a startup with a spaghetti Postgres setup, a mid-size company migrating off spreadsheets. Stakes are low. You're learning the ropes, building reputation.

**Tone:** Light, tutorial-flavored. Mistakes are forgivable.

### Act 2: The Big Leagues (Engagements 5-8)
Reputation growing, you land bigger fish. A Fortune 500 retail company with 200 data sources. A healthcare org with strict compliance requirements. A fintech startup burning cash on a over-architected platform that does nothing.

**Tone:** Pressure builds. Office politics get nasty. You start making enemies.

### Act 3: The Impossible Client (Engagements 9-10)
You're recruited for a legendary engagement: **Ouroboros Corp**, a massive conglomerate whose data platform has been "in migration" for seven years across three consulting firms. Everyone who's tried has failed or been fired. The system is a labyrinth. The politics are venomous. The timeline is insane.

**Tone:** Thriller. Something is deeply wrong at Ouroboros — and it's not just technical.

### The Twist
Deep in the Ouroboros engagement, you discover the platform isn't broken by accident. Someone has been deliberately sabotaging migrations to keep the consulting contracts flowing. The trail leads back to your old firm. The final act becomes a race to expose the corruption while delivering a working platform — with your former colleagues actively working against you.

### Multiple Endings
- **The Clean Build:** Expose the conspiracy, deliver the platform, become legendary
- **The Pragmatist:** Deliver the platform, bury the conspiracy, cash out
- **The Burnout:** Fail the engagement, reputation destroyed, return to employment
- **The Insider:** Join the conspiracy, become the fixer, morally compromised but wealthy
- **The Architect:** Build something so elegant it becomes an industry standard (secret ending, requires max technical reputation)

---

## Art Direction

### Visual Style
**Isometric pixel art with a neon-noir palette.** Think *Hyper Light Drifter* meets corporate office aesthetics.

- **System maps** rendered as glowing circuit-board-style diagrams with data flowing as particles along paths
- **Office environments** are detailed pixel art — cluttered desks, server rooms with blinking lights, conference rooms with whiteboards covered in diagrams
- **Characters** are expressive pixel portraits with dialogue boxes
- **The blueprint board** uses a clean, technical aesthetic — graph paper background, precise component sprites, connection lines that animate when data flows

### Audio
- **Soundtrack:** Lo-fi electronic with jazz influences. Calm during discovery, tense during incidents, triumphant on successful delivery. Different client industries get distinct musical flavors (fintech = glitchy and fast, healthcare = measured and precise, retail = chaotic and upbeat).
- **SFX:** Satisfying clicks for connecting components, alarm sounds for incidents, keyboard clatter ambiance, the dreaded Slack notification sound when stakeholders message you.

---

## Progression & Meta-Game

### Campaign Mode
10 story engagements with branching paths. ~15-20 hours for a single playthrough. High replayability due to different approaches, political choices, and endings.

### Endless Consulting Mode
Procedurally generated clients with randomized:
- Industry and company size
- Existing tech stack (from "pristine greenfield" to "archaeological horror")
- Stakeholder personalities and politics
- Budget and timeline constraints
- Incident types and frequency

Compete on leaderboards for highest reputation score, fastest delivery, or most creative architectures.

### Challenge Engagements
Hand-crafted puzzles based on real-world data platform nightmares:
- "The client has 47 microservices each with their own database. Consolidate without downtime."
- "The CEO saw a demo of a graph database and now wants everything migrated by Friday."
- "Someone deployed to production on a Friday at 4:59 PM. You have the weekend to fix it."
- "The data warehouse has 12,000 tables. 11,500 are unused. Figure out which 500 matter."

---

## Monetization

**Premium game, no microtransactions.** Potential DLC for additional story arcs:
- **"The Government Contract"** — bureaucracy, security clearances, and waterfall methodology
- **"The Acquisition"** — two companies merging their incompatible data platforms
- **"The AI Hype Cycle"** — every stakeholder wants AI, nobody has clean data

---

## Why This Game Works

1. **Untapped setting:** Nobody has made a game about this world, but millions of people live in it
2. **Real expertise becomes gameplay:** Actual data platform knowledge translates to better play, but the game teaches non-technical players through discovery
3. **The human element:** It's not just about technology — it's about navigating people, politics, and pressure
4. **Dark comedy resonance:** Anyone who's worked in tech will recognize these situations and laugh (or cry)
5. **Genuine strategic depth:** Architecture decisions have real tradeoffs, not obvious "right answers"
6. **Narrative hooks:** The conspiracy thriller gives purpose to what could be dry subject matter

---

## Summary

**Pipeline Panic** takes the real tension of data platform consulting — the impossible timelines, the political minefields, the archeological horror of legacy systems — and turns it into a strategy game with genuine depth and a story worth caring about. It's *Papers, Please* for the data age: mundane work elevated to art through smart design and dark humor.
