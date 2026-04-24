# ARC-001-PLAN-v1.0 — The Exchange Protocol: MVP Deployment Plan

**Status:** Draft  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Chapter:** 001 — MVP Deployment, MEAC Conference  

---

> **In plain language.** The sequenced plan for getting the first MEAC chapter from nothing to a signed, dual-hashed portfolio entry. The MVP success condition is narrow by design: one university, one TAC, one partner organization, one compliant session, one portfolio entry. That first output is the evidence that closes every subsequent conversation.

## Purpose

This document defines the sequenced plan for deploying the first
compliant Exchange chapter at a MEAC member institution.

MVP success condition: one university, one TAC, one partner organization,
one compliant session, one dual-hashed portfolio entry.
That output is the evidence that closes every subsequent conversation.

---

## Governance Gate

No external conversation begins until the governance architecture
is complete enough that a university general counsel can read it
without a founder explanation.

---

## Phase 0 — Governance Completion

**Objective:**
Close the documentation gaps identified in the risk register.
The protocol cannot govern itself if its own documents are missing.

**Deliverables:**

| Document | Description | Dependency |
|---|---|---|
| ARC-000-FRMW-v1.0 | Compliance checklist. TAC credential template. Chapter recognition criteria. | None |
| ARC-000-DPIA-v1.0 | Data protection impact assessment. Legal basis for dual-hash athlete ownership boundary. Required before university contract execution. | ARC-000-FRMW |
| ADR-004-v1.0 | Origin lineage decision record. Foot in the Door (2012) → SAX (2013) → GP Monticello (2024) → Exchange (2026). Establishes IP provenance. | None |

**Gate:** All three documents committed to repository before Phase 1 begins.

**Owner:** Akili King  
**Risk addressed:** R02 (founder dependency), R03 (institutional IP capture), R06 (origin IP dispute)

---

## Phase 1 — Legal Clearance

**Objective:**
Ensure the SOBC and DPIA can survive review by a university
general counsel and an NCAA compliance officer before any
institutional conversation begins.

**Deliverables:**

| Action | Output | Owner |
|---|---|---|
| SOBC legal review | Confirmed: portfolio entry = professional development output, not NIL deal, not benefit with monetary value. Written opinion or sign-off. | Akili King + legal counsel |
| DPIA review | Confirmed: dual-hash boundary is legally defensible. Contract language template that explicitly preserves athlete ownership. | Akili King + legal counsel |

**Gate:** Written legal clearance on file before first university pitch meeting.

**Owner:** Akili King  
**Risk addressed:** R03 (institutional IP capture), R04 (NCAA compliance conflict)

---

## Phase 2 — TAC Recruitment

**Objective:**
Identify and credential one TAC for the first session.
No TAC, no session. This is the hardest step in the deployment.

**Qualification criteria (NFR-002):**
- Operated in sports business, NIL, athlete representation,
  brand partnerships, or sports marketing at a professional level
- Within the last five years
- Not academic knowledge — operational knowledge

**Deliverables:**

| Item | Description |
|---|---|
| TAC credential document | Domain specified. Dates of professional operation specified. Signed by TAC. Filed before first session. |
| TAC briefing | TAC reads ARC-001-REQ-v1.0. Confirms understanding of challenger role vs. facilitator role. Confirms FR-001 pre-work responsibility. |
| ARC-000-FRMW compliance checklist | Signed by TAC. Chapter recognition withheld until complete. |

**Gate:** Credential document on file and compliance checklist signed
before any session date is set.

**Owner:** Akili King  
**Risk addressed:** R01 (protocol dilution), R05 (TAC quality degradation)

---

## Phase 3 — Institutional Engagement

**Objective:**
Secure agreement from one MEAC athletic department to run
a proof of concept session. Contract is not required first.
The POC session produces the evidence that closes the contract.

**Sequence:**

1. **Pitch meeting** — present SOBC Case 1 (strategic) and Case 2 (economic)
   to athletic director and compliance officer.
   Reference this repository for due diligence.
   Do not pitch the contract. Pitch the session.

2. **Compliance review** — institutional legal reviews ARC-000-DPIA-v1.0
   and ARC-001-SOBC-v1.1 independently.
   No founder explanation required — that is the test.

3. **Agreement** — one of two paths:
   - **POC letter of intent:** Run one session, inspect the portfolio entry output,
     decide on contract after. No budget approval required at this stage.
   - **University contract:** $15,000–35,000 annually.
     Requires explicit language preserving athlete portfolio ownership
     (see ARC-000-DPIA-v1.0 contract template).

**Deliverables:**

| Item | Description |
|---|---|
| Pitch deck or one-pager | Derived from ARC-001-SOBC-v1.1 and ARC-001-STKE-v1.0. Points to repository for governance documentation. |
| Signed POC letter of intent or university contract | Date, institution name, point of contact, session scope. |
| Athlete cohort confirmed | Minimum four athletes. Yellow participants (no domain experience) welcome. |

**Gate:** Signed agreement and athlete cohort confirmed before Phase 4 begins.

**Owner:** Akili King  
**Risk addressed:** R07 (MEAC adoption failure)

---

## Phase 4 — Partner Organization Engagement

**Objective:**
Identify and brief one partner organization to provide the
mapping target for the first session.

**Criteria:**
- Operating in or adjacent to the MEAC athlete ecosystem
- Willing to receive a Wardley Map of their competitive landscape
  produced by athletes under TAC supervision
- Engagement fee: $2,500–7,500 (waived for first POC at founder discretion)

**Deliverables:**

| Item | Description |
|---|---|
| Partner organization briefing | Partner understands: the deliverable is a Wardley Map, produced by athletes, challenged by TAC, not a consulting engagement. |
| Mapping target defined | Named user need for the session established in coordination with partner org and TAC. Feeds into TAC pre-work (FR-001). |
| Signed engagement agreement | Scope, deliverable, timeline, fee (or waiver). No rights granted to ECHO substrate (Principle 6). |

**Gate:** Mapping target confirmed and TAC pre-work canvas drafted
before session date is set.

**Owner:** Akili King  
**Risk addressed:** R01 (protocol dilution — partner org sets a real target, not a practice target)

---

## Phase 5 — First Session Execution

**Objective:**
Run one fully compliant session per ARC-001-REQ-v1.0.
Every functional requirement must be satisfied.
Every compliance evidence item must be produced.

**Session checklist (FR-001 through FR-007):**

| Requirement | Compliance evidence |
|---|---|
| FR-001 — TAC pre-session setup | Pre-work canvas committed to repository before athletes arrive |
| FR-002 — Phase 1 open capture | Session artifact shows all contributions before clustering |
| FR-003 — Phase 2 clustering with TAC challenge | Pre- and post-challenge cluster states documented with TAC notes |
| FR-004 — Phase 3 value chain | Value chain shows named user at top, dependency lines traced down, removed components noted |
| FR-005 — Phase 4 evolution positioning | Each challenged component documented: research placement / TAC placement / delta reason |
| FR-006 — ETU captured at close | Signed ETU in SCQA format, co-signed by Map Lead and TAC, timestamped before session closes |
| FR-007 — Portfolio entry dual-hashed | Work Ledger hash record with Bitcoin-anchored timestamp per portfolio entry |

**Gate:** All seven compliance evidence items produced and committed
to repository before session is considered complete (NFR-003).

**Owner:** Map Lead (session) + Akili King (compliance verification)

---

## Phase 6 — POC Close and Evaluation

**Objective:**
Verify protocol compliance, deliver the partner organization
Wardley Map, and evaluate whether the POC output closes
the university contract conversation.

**Deliverables:**

| Item | Description |
|---|---|
| Compliance verification report | Checklist against ARC-001-REQ-v1.0. All seven FRs satisfied. All four NFRs satisfied. Signed by Map Lead. |
| Partner org deliverable | Published Wardley Map of partner organization's competitive landscape. Produced by athletes. Challenged by TAC. Delivered to partner org. |
| Athlete portfolio entries | Dual-hashed, timestamped, athlete-accessible. Count: one per participating athlete. |
| ETU dataset — session one | First SCQA record committed to repository. Seed of the ECHO substrate. |
| POC evaluation memo | What worked. What broke. What the next session requires. Feeds ARC-001-PLAN-v2.0. |

**Gate:** Compliance verification report signed and all artifacts
committed before the contract conversation is opened (if on POC path).

**Owner:** Akili King

---

## Milestone Summary

| Phase | Milestone | Gate condition |
|---|---|---|
| 0 — Governance | FRMW, DPIA, ADR-004 committed | All three documents in repository |
| 1 — Legal | Legal clearance on file | Written opinion before first pitch |
| 2 — TAC | TAC credentialed and signed | Credential doc + compliance checklist filed |
| 3 — Institution | Agreement signed | POC letter or contract executed |
| 4 — Partner | Mapping target confirmed | TAC pre-work canvas drafted |
| 5 — Session | Compliant session run | All FR-001–FR-007 evidence items committed |
| 6 — POC close | Compliance report signed | All artifacts in repository |

---

## Documents Referenced

| Document | Status | Purpose |
|---|---|---|
| ARC-000-PRIN-v1.0 | Approved | Six governing principles |
| ARC-000-FRMW-v1.0 | Draft | Compliance checklist and TAC credential template |
| ARC-001-SOBC-v1.1 | Draft | Strategic, Economic, Commercial, Financial, Management cases for MEAC pitch |
| ARC-001-REQ-v1.0 | Approved | Session compliance requirements |
| ARC-001-RISK-v1.0 | Approved | Risk register with mitigations |
| ARC-001-STKE-v1.0 | Approved | Stakeholder analysis for MEAC context |
| ARC-000-DPIA-v1.0 | Draft | Athlete data ownership legal basis (FERPA + GDPR-adjacent) |
| ADR-004-v1.0 | **Not yet written** | Origin lineage decision record |

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial release — MEAC MVP deployment |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
