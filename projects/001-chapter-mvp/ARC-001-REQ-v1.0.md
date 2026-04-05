# ARC-001-REQ-v1.0 — The Exchange Protocol: Chapter Requirements

**Status:** Approved  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Chapter:** 001 — MVP Deployment, MEAC Conference  

---

## Purpose

This document defines what a compliant Exchange chapter
must do. These are not guidelines. They are requirements.

Compliance is binary — a chapter meets them or it does not.
A chapter that does not meet these requirements is not
an Exchange chapter regardless of what it calls itself.

---

## FUNCTIONAL REQUIREMENTS

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

### FR-006 — ETU captured at session close

The Map Lead captures an Execution Trace Unit (ETU)
in SCQA format at the close of every session.
This is the last ten minutes of every session.
It is not optional.

ETU structure:
- **Situation:** What the research-derived map showed
- **Complication:** What the TAC corrected and why
- **Question:** What the corrected landscape reveals
- **Answer:** What gameplay the accurate map suggests

The ETU is co-signed by the Map Lead and TAC
before the session closes.

**Compliance evidence:** Signed ETU document
timestamped before session close.

---

### FR-007 — Portfolio entry dual-hashed and timestamped

Every portfolio entry is processed through the
Work Ledger before the session closes.

Dual-hash process:
- Shared payload: organizational verification hash
- Private payload: athlete-owned provenance hash
  (includes MY READ field — athlete's own interpretation)

Bitcoin-anchored timestamp establishes ownership
at moment of creation. This record cannot be
overridden by institutional policy.

**Compliance evidence:** Work Ledger hash record
with timestamp per portfolio entry.

---

## NON-FUNCTIONAL REQUIREMENTS

### NFR-001 — Athlete owns portfolio entry

No institution — university, partner organization,
or Exchange chapter — can access the athlete's
private payload without explicit athlete consent.

The dual-hash boundary is technical, not policy.
It cannot be overridden by an institutional decision.

**Compliance evidence:** Work Ledger private payload
key held by athlete, not institution.

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
ETU, portfolio entry — are stored in a version-controlled
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
and veri
