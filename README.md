# student-athlete-exchange

**Athletic departments that run The Exchange become what Ivy League schools are to consulting firms: a recognized pipeline for developing the kind of judgment that employers cannot train for after the fact.**

Every session pairs a small group of athletes with an experienced domain expert — someone who has worked inside the kind of organization being mapped. Not a credentialed instructor. Not a guest lecturer. Someone whose job it was to make decisions in that environment, and who can tell an athlete exactly why their read of the landscape is wrong.

The athletes map the organization. The expert challenges every placement. The result is a verified record of professional judgment — built inside the athlete's existing schedule, without a classroom, without a new budget line, and without a mandate.

This repository holds the public governance architecture for The Exchange: the principles it runs on, the stakeholder analysis, the risk register, the business case, the requirements, and the deployment plan. Everything is open. No meeting required to review it.

---

## The problem

Most athletes cannot do internships. The schedule does not allow it. NIL contracts reach a small percentage. Career services programs were designed for students who have time. The result is that athletes graduate with strong skills and no verifiable record of using them professionally.

The problem is not motivation. It is not capability. The problem is that every existing tool for building professional credibility was designed for people who have time.

---

## What The Exchange produces

Each session pairs a cohort of athletes with a domain expert — someone who has worked inside a real organization in the target industry and made real decisions there. Together they map the competitive landscape of a real partner organization.

| What gets produced | What it means |
|---|---|
| **Landscape** | The athlete maps a real industry for a real organization, challenged by a domain expert against what actually happens — not what research claims |
| **Team record** | The session documents how the athlete contributed, what they challenged, and how they responded to correction — a more accurate picture of professional behavior than any interview question produces |
| **Results** | The partner organization received the map and used it. What they did with it — the decision it informed, the strategy it changed — is documented in the portfolio entry |

The athlete does not say "I developed strategic thinking skills." They open a portfolio and say: here is the map I produced, here is who verified it, here is what the organization did with it. That is not a conversation about potential. That is a record of results.

---

## Four years of verifiable work

One session is a start. Four years is a body of work no other candidate in the hiring pool can match.

| Year | Focus | What the athlete builds |
|---|---|---|
| **Year 1** | Self mapping | Map your own context — skills, network, and strategic awareness made visible for the first time |
| **Year 2** | Landscape mapping | Map the domains you want to enter — learn to read where industries are moving and where the leverage is |
| **Year 3** | Organizational mapping | Map actual organizations — produce your first verifiable deliverable for a real partner |
| **Year 4** | Portfolio | A body of work any organization can open, read, and evaluate directly |

---

## For athletic departments

The House v. NCAA settlement creates compliance pressure across Division I — including MEAC institutions operating with smaller budgets than Power Five programs.

The Exchange satisfies the beyond-NIL professional development mandate while producing auditable records that satisfy accreditation requirements — at near-zero operational cost. One chapter replaces or supplements one career services function. The protocol costs nothing to operate once established. The first session is the proof of concept — no contract required to begin.

---

## How to build a chapter

The protocol is designed to be adopted quietly, starting with a single proof-of-concept session. You do not need a massive budget, a department-wide mandate, or a new software platform to begin. 

Here is the minimum viable path to running your first session:

| Step | What you need | Why it matters |
|---|---|---|
| **1. Legal Clearance** | Have your compliance officer review the [Business Case](projects/001-chapter-mvp/ARC-001-SOBC-v1.1.md) and [Data Protection Impact Assessment](projects/000-global/ARC-000-DPIA-v1.0.md). | Confirms the output is professional development, not an NIL deal, and addresses FERPA + GDPR-adjacent rights — clearing the path for athletes to participate safely. |
| **2. Find a TAC** | Identify one domain expert (TAC) who has operated at a professional level in a target industry within the last five years. | The TAC is the challenger. Without someone who knows what reality looks like in that industry, the session is just an academic exercise. |
| **3. Find a Partner** | Identify one real organization willing to have their competitive landscape mapped. | The athletes need a real target. The partner organization receives the final map as the deliverable. |
| **4. Run the Session** | Four athletes, one TAC, one partner target. The athletes build the map; the TAC challenges it. | This is the proof of concept. The session produces the first verifiable portfolio entry. |
| **5. Evaluate** | Look at the portfolio entry produced by the athletes. | That single piece of evidence closes the conversation about whether to adopt the protocol department-wide. |

The full, detailed deployment sequence — including the exact compliance gates and deliverables for each phase — is documented in the [MVP Deployment Plan](projects/001-chapter-mvp/ARC-001-PLAN-v1.0.md).

---

## The Methodology: Wardley Mapping

**The map is not the product. The method is.**

Wardley Mapping is a structured way of evaluating any industry — how value moves from raw components to the end user, what is rare or common, what is changing fast or stable, and where the real leverage is. Athletes learn it by doing it, session after session, under challenge from a domain expert.

What an athlete carries after graduation is not the portfolio. It is the method. Wardley Mapping is Creative Commons licensed and platform-independent — it works at any employer, in any industry, for as long as the athlete keeps using it. Unlike NIL (which addresses income during eligibility) or career services (which addresses resume formatting), the method compounds for decades after eligibility ends.

The full methodology document — including the five dimensions of the value proposition, the learning ecosystem, and how maps connect to the wider mapping community — is here: [ARC-000-METH-v1.1 — Mapping Methodology](projects/000-global/ARC-000-METH-v1.1.md).

### The Foundation: swardleymaps.com

[swardleymaps.com](https://www.swardleymaps.com/) is the official home of Wardley Maps. It is the foundational source for the method, providing the core doctrine, the book, and the fundamental principles. The Exchange relies on this source to ensure athletes learn the method directly from its origin.

### Wardleymaps.ai

[Wardleymaps.ai](https://wardleymaps.ai) is the AI-powered resource platform for Wardley Mapping. It contains 182+ books, 137 podcast episodes, 400+ curated resources, a browser-based map creation tool, and ArcKit — the same architecture governance toolkit used to produce The Exchange's governance documents. Domain experts preparing for sessions and athletes in Year 2 (Landscape Mapping) draw directly from this library.

### Wardley Map Repository

[Simon Wardley's Map Repository](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main) is the open research archive of maps produced by the global mapping community. Maps are organized by industry domain — including [education](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main/education), [healthcare](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main/healthcare), [finance](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main/finance), [government](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main/government), and [defence](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main/defence). Maps produced in Exchange sessions use the same plain-text format as every map in the repository, making them directly compatible for contribution under the Creative Commons license (CC BY-SA 4.0) that governs the collection.

---

## What is in this repository

```
student-athlete-exchange/
├── projects/
│   ├── 000-global/
│   │   ├── ARC-000-PRIN-v1.0.md      # Six non-negotiable protocol rules
│   │   ├── ARC-000-METH-v1.1.md      # Mapping methodology and value proposition
│   │   ├── ARC-000-ADR-v1.0.md       # Architecture decisions (Bitcoin, dual-hash, SCQA)
│   │   ├── ARC-000-BRIEF-v1.0.md     # Athlete briefing (plain-language pre-session)
│   │   ├── ARC-000-DPIA-v1.0.md      # Data protection (FERPA + GDPR-adjacent)
│   │   ├── ARC-000-FRMW-v1.0.md      # Compliance framework (chapter template)
│   │   └── wardley-maps/
│   │       └── ARC-000-WARD-v1.0.md  # Protocol Wardley map
│   └── 001-chapter-mvp/
│       ├── ARC-001-STKE-v1.0.md      # Stakeholder analysis — athletes, TACs, universities, partners
│       ├── ARC-001-RISK-v1.0.md      # Risk register — seven risks, rated and mitigated (Orange Book)
│       ├── ARC-001-SOBC-v1.1.md      # Business case — Green Book 5-Case model
│       ├── ARC-001-REQ-v1.0.md       # Chapter requirements — what a compliant chapter must do
│       ├── ARC-001-FRMW-v1.0.md      # MEAC chapter's signed compliance instance
│       └── ARC-001-PLAN-v1.0.md      # MVP deployment plan — MEAC conference
├── context/                           # Source documents that informed the protocol
├── CLAUDE.md                          # Instructions for Claude Code (AI assistant)
├── index.html                         # Public-facing website (GitHub Pages)
├── LICENSE                            # MIT license
└── README.md                          # This file
```

---

## Protocol documentation

The full governance architecture is publicly verifiable. Each document is linked below.

| Document | What it covers |
|---|---|
| [Architecture Principles](projects/000-global/ARC-000-PRIN-v1.0.md) | Six non-negotiable rules the protocol runs on |
| [Mapping Methodology](projects/000-global/ARC-000-METH-v1.1.md) | Why Wardley Mapping is the value proposition |
| [Architecture Decision Record](projects/000-global/ARC-000-ADR-v1.0.md) | Bitcoin anchoring, dual-hash attribution, SCQA ETU format |
| [Athlete Briefing](projects/000-global/ARC-000-BRIEF-v1.0.md) | Plain-language guide athletes read before Session 1 |
| [Data Protection Impact Assessment](projects/000-global/ARC-000-DPIA-v1.0.md) | FERPA and GDPR-adjacent protections |
| [Compliance Framework](projects/000-global/ARC-000-FRMW-v1.0.md) | Protocol-wide compliance checklist (chapter template) |
| [Stakeholder Analysis](projects/001-chapter-mvp/ARC-001-STKE-v1.0.md) | Athletes, domain experts (TACs), universities, and partner organizations |
| [Risk Register](projects/001-chapter-mvp/ARC-001-RISK-v1.0.md) | Seven risks, each rated and mitigated (Orange Book) |
| [Business Case](projects/001-chapter-mvp/ARC-001-SOBC-v1.1.md) | Green Book 5-Case model for MEAC chapter engagement |
| [Chapter Requirements](projects/001-chapter-mvp/ARC-001-REQ-v1.0.md) | What a compliant chapter must do |
| [MEAC Compliance Instance](projects/001-chapter-mvp/ARC-001-FRMW-v1.0.md) | Chapter 001's signed compliance record |
| [MVP Deployment Plan](projects/001-chapter-mvp/ARC-001-PLAN-v1.0.md) | Sequenced plan for the first MEAC session |

---

## The origin

I played football at West Point and Oregon State. I tried out for the San Francisco 49ers and got cut. After 18 years of football, the identity that defined everything was suddenly irrelevant.

I became a Ranger — The SeaBass, 1-Bravo, B. CO. 2/75, 2nd Battalion, 75th Ranger Regiment. I served in Afghanistan and was part of Operation Red Wings, the recovery mission for Navy SEAL Marcus Luttrell.

When I came back to athletics — as Managing Director of the OSU Athletics Leadership Institute — I gave athletes a problem to solve: how do you build real work credibility on a 34-hour athletic schedule? One team built the Student Athlete Exchange. It won first place at the 2013 OSU Startup Weekend.

That was the first answer. The Exchange is what thirteen years of field work revealed the answer actually needed to be.

— Akili King, Lead Researcher

---

## Start the conversation

One university. One domain expert. One partner organization. One session. The portfolio entry closes the conversation.

[akili.king@hardy47.com](mailto:akili.king@hardy47.com)

---

## License

The Exchange Protocol is MIT Licensed.
Session method: Creative Commons — Wardley Mapping by Simon Wardley.

