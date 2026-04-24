# ARC-001-REQ-v1.0 — The Exchange Protocol: Chapter Requirements

**Status:** Approved  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Chapter:** 001 — MVP Deployment, MEAC Conference  

---

> **In plain language.** What a compliant Exchange chapter must actually do. Seven functional requirements describe what happens in every session, phase by phase. Four non-functional requirements cover athlete ownership, TAC domain currency, version-controlled artifacts, and third-party verifiability. A chapter meets them or it does not — no waiver, no exception.

## Purpose

This document defines what a compliant Exchange chapter
must do. These are not guidelines. They are requirements.

Compliance is binary — a chapter meets them or it does not.
A chapter that does not meet these requirements is not
an Exchange chapter regardless of what it calls itself.

---

## FUNCTIONAL REQUIREMENTS

### FR-000 — Baseline preparation standard

Before participating in any Exchange session —
athlete, TAC, or observer — every participant
reads the following document:

**Wardley Mapping 101: A Beginner's Guide**
https://www.wardleymaps.com/guides/wardley-mapping-101

15 minutes. Beginner level.
Built by Krzysztof Daniel. Approved by Simon Wardley.
Licensed CC BY-SA 4.0.

This is the only preparation required before Session 1.
It is not optional for athletes.
It is not optional for TACs.

The guide establishes shared vocabulary across all
participants regardless of prior experience:
genesis / custom / product / commodity,
value chain, user need, evolution positioning.

**The two lines every participant must internalize:**

"Do not speculate."
The TAC corrects honest placements.
The TAC cannot unwind a defended guess.

"You might have many custom components.
It does not mean that everyone else has them."
This is Custom Bias. The TAC will challenge it
in every session. The guide names it in advance.

**What this guide does not cover:**

The guide explains how to build a map.
It does not explain what changes in an Exchange session.

Athletes also read ARC-000-BRIEF-v1.0.md before
Session 1. That document covers the three distinctions
the 101 guide cannot make:
- The map is a deliverable, not a practice exercise
- The TAC is a challenger, not a teacher
- The gap between where research placed a component
  and where the TAC placed it is the portfolio entry

**Compliance evidence:** TAC confirms at session open
that all athletes have read both documents.
No test. No quiz. The session surfaces compliance.

---

### FR-001 — TAC pre-session setup

Before athletes arrive, the TAC defines the segmented
canvas for the session. This includes:

- Named user at the top of the value chain
- Domain boundary conditions (what is in scope)
- Known assumption traps in the domain
  (where research commonly misrepresents reality)

The TAC does not facilitate the session.
The TAC challenges it. The distinction is architectural.
A facilitator guides process. A challenger tests assumptions.

**Compliance evidence:** TAC pre-work documented
in session artifact before Phase 1 begins.

---

### FR-002 — Phase 1: Open capture

Phase 1 produces unfiltered component capture.
No structure. No filtering. No judgment on relevance.

Every participant adds what they believe matters.
Yellow participants (no domain experience) contribute
alongside Orange participants (domain experience).
The naive question belongs here — it often surfaces
the assumption the TAC is waiting to challenge.

**Compliance evidence:** Session artifact shows
all participant contributions before clustering begins.

---

### FR-003 — Phase 2: Theme clustering with TAC challenge

Components are clustered into coherent themes.
The TAC challenges every cluster boundary.

If a component is in a cluster, the TAC asks why.
If a component is excluded, the TAC asks why.
No cluster is accepted without TAC interrogation.

**Compliance evidence:** Session artifact shows
pre-challenge clusters and post-challenge clusters
as distinct states with TAC challenge notes.

---

### FR-004 — Phase 3: Value chain traced to user need

The value chain anchors to the named user need
established in TAC pre-work (FR-001).

Every component must trace to that user need.
If a component cannot be traced, it is removed.
The TAC enforces this requirement — not the Map Lead.

**Compliance evidence:** Session artifact shows
value chain with named user at top and dependency
lines traced downward. Removed components noted.

---

### FR-005 — Phase 4: Evolution positioning challenged
### against operational reality

Component evolution positioning (genesis / custom /
product / commodity) must be challenged by the TAC
against what actually happens in the domain —
not against published descriptions, analyst reports,
or AI-generated research.

This is the assumption delta. It is the core value
of every Exchange session. The gap between where
research places a component and where a domain expert
places it — based on operational reality — is what
the athlete captures and what the employer cannot
find anywhere else.

**Compliance evidence:** Session artifact documents
for each challenged component:
- Where research placed it
- Where TAC placed it
- Why the delta exists

---

### FR-006 — Session record captured at close

The Map Lead captures a structured session record
in SCQA format at the close of every session.
This is the last ten minutes of every session.
It is not optional.

SCQA structure:
- **Situation:** What the landscape looked like
  when the session began
- **Complication:** What the TAC challenged
  and what shifted as a result
- **Question:** What the corrected landscape reveals
  that was not visible before
- **Answer:** What the session concluded

The session record is co-signed by the Map Lead
and TAC before the session closes.

**Compliance evidence:** Signed session record
timestamped before session close.

---

## NON-FUNCTIONAL REQUIREMENTS

### NFR-001 — Athlete owns portfolio entry

No institution — university, partner organization,
or Exchange chapter — can claim ownership of
work product produced by an athlete in a session.

Portfolio entries belong to the athlete who produced them.
This is established in writing before the first session
through the chapter participation agreement.

**Compliance evidence:** Signed participation agreement
on file for every athlete before Session 1.

---

### NFR-002 — TAC domain currency

The TAC must have operated in the mapped domain
at a professional level within the last five years.

Academic knowledge of a domain does not qualify.
The TAC must know what actually happens —
not what published sources say happens.

**Compliance evidence:** TAC credential document
on file before first session. Domain and dates
of professional operation specified.

---

### NFR-003 — Session artifacts version controlled

All session artifacts — pre-work canvas, phase outputs,
session record — are stored in a version-controlled
system before the session is considered complete.

GitHub is the recommended system.
Any version-controlled system with timestamping qualifies.

**Compliance evidence:** Session artifacts committed
to repository with timestamp before next session begins.

---

### NFR-004 — Protocol compliance verifiable by third party

Any third party — accreditation body, legal department,
compliance officer — must be able to verify chapter
compliance without contacting the founder or chapter lead.

The public GitHub repository at:
github.com/Akili-47/student-athlete-exchange

contains all compliance criteria, requirements,
and verification evidence. No meeting required.

**Compliance evidence:** Governance repository publicly
accessible. All ARC documents versioned and linked
from the public-facing site at:
akili-47.github.io/student-athlete-exchange

---

## COMPLIANCE MATRIX

| Requirement | Enforcement Mechanism | Compliance Evidence |
|---|---|---|
| FR-000 — Baseline preparation | TAC confirmation at session open | Verbal confirmation logged in session record |
| FR-001 — TAC pre-session setup | TAC pre-work artifact | Documented canvas before Phase 1 |
| FR-002 — Phase 1 open capture | Session artifact review | All contributions visible pre-cluster |
| FR-003 — Phase 2 TAC challenge | Challenge notes in artifact | Pre/post cluster states documented |
| FR-004 — Phase 3 value chain | TAC enforcement | Named user + traced dependencies |
| FR-005 — Phase 4 evolution challenge | TAC operational knowledge | Assumption delta per component |
| FR-006 — Session record at close | Co-signed SCQA document | Timestamped record |
| NFR-001 — Athlete ownership | Participation agreement | Signed before Session 1 |
| NFR-002 — TAC domain currency | Credential document | Domain + dates on file |
| NFR-003 — Version control | Repository commit | Timestamped artifacts |
| NFR-004 — Third-party verifiability | Public repository | No meeting required |

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial release |

---

*This document is part of The Exchange Protocol governance
architecture. Built with ArcKit. Stored in version control.
Publicly verifiable.*
