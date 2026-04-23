# ARC-000-FRMW-v1.0 — The Exchange Protocol: Chapter Compliance Framework

**Status:** Draft  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Framework:** Six Architecture Principles (ARC-000-PRIN); UK Government Green Book 5-Case Model; HM Treasury Orange Book; FERPA (20 U.S.C. § 1232g)

---

## Purpose

This is the authoritative compliance framework for
any Exchange chapter. It is the enforcement mechanism
Principle 5 requires.

Principle 5 — "The protocol governs, not the founder" —
needs a concrete way to verify a chapter's compliance
without contacting the founder. This document is that
way. Every chapter adopts this framework by filing a
signed local instance — for example, ARC-001-FRMW for
chapter 001. The local instance copies the structure
below, records chapter-specific evidence, and is signed
by the three roles defined in Section F.

A third party verifies compliance by reading the
chapter's signed instance alongside this global
document. No founder conversation is required.

The framework ties every chapter governance artifact
to an external framework with named authority. External
frameworks do the heavy lifting. The Exchange Protocol
defines only what is specific to Exchange chapters.
Everything else is inherited from published standards.

---

## Framework Map

Chapter governance documents implement external
frameworks. The framework authority, not the protocol,
defines what "done" looks like inside each case.

| Governance document | External framework | Authority | Where applied |
|---|---|---|---|
| ARC-{id}-SOBC | UK Government Green Book 5-Case Model | HM Treasury | Strategic, Economic, Commercial, Financial, Management cases |
| ARC-{id}-RISK | HM Treasury Orange Book | HM Treasury | Likelihood × Impact scoring; thresholds 1–4 Low, 5–9 Medium, 10–16 High, 17–25 Critical |
| ARC-{id}-REQ + ARC-000-DPIA | FERPA (20 U.S.C. § 1232g) | US Department of Education | Data subject rights, disclosure log, school official exception |
| ARC-000-PRIN | Six Architecture Principles | The Exchange Protocol | Self-enforcing — principle-by-principle compliance matrix |
| ARC-000-ADR | Nygard ADR format | Open standard | Context / Decision / Consequences |
| ARC-000-METH | Wardley Mapping (CC BY-SA) | Simon Wardley / wardleymaps.com | Map syntax, evolution axis, value chain |

Internal reference documents (non-framework):
ARC-{id}-STKE (stakeholder analysis), ARC-000-WARD
(protocol Wardley Map), ARC-000-BRIEF (participant
briefing).

---

## Section A — Principle Compliance

Six items. One per principle. A chapter that cannot
check all six is not an Exchange chapter.

- [ ] **P1 — User need anchors everything.**
  Named user at the top of every value chain.
  **Evidence:** session artifact for Session 1
  showing named user and traced dependencies.

- [ ] **P2 — Domain expertise governs quality.**
  TAC has operated in the mapped domain
  within the last five years.
  **Evidence:** TAC credential document per NFR-002,
  listing domain and dates of professional operation.

- [ ] **P3 — The practitioner owns the work.**
  Athletes hold the private payload key.
  No institutional clause claims portfolio ownership.
  **Evidence:** participation agreement per NFR-001;
  dual-hash per ADR-002.

- [ ] **P4 — The assumption delta is the value.**
  ETU at session close documents research-vs-TAC
  placement for every challenged component.
  **Evidence:** signed SCQA ETU per FR-006 and ADR-003.

- [ ] **P5 — The protocol governs, not the founder.**
  Chapter's local FRMW instance signed by the three
  roles in Section F. No founder approval sought
  or granted.
  **Evidence:** signed FRMW committed to chapter
  repository path.

- [ ] **P6 — Open method, proprietary substrate.**
  No chapter agreement grants rights to ECHO data.
  **Evidence:** chapter–partner agreement clause
  specifying ECHO substrate reservation.

---

## Section B — Requirements Compliance

Functional and non-functional requirements per the
chapter's ARC-{id}-REQ.

### Functional

- [ ] **FR-000** — All participants read Wardley Mapping 101
  and ARC-000-BRIEF before Session 1. TAC confirms at
  session open.
- [ ] **FR-001** — TAC pre-session canvas documented
  before Phase 1 (named user, domain boundary,
  known assumption traps).
- [ ] **FR-002** — Phase 1 open capture visible in
  session artifact prior to clustering.
- [ ] **FR-003** — Phase 2 cluster pre-challenge and
  post-challenge states documented with TAC notes.
- [ ] **FR-004** — Phase 3 value chain traces every
  component to the named user, removed components
  noted.
- [ ] **FR-005** — Phase 4 assumption delta recorded
  per challenged component (research placement,
  TAC placement, why the delta exists).
- [ ] **FR-006** — SCQA session record co-signed by
  Map Lead and TAC before session close, timestamped.

### Non-Functional

- [ ] **NFR-001** — Participation agreement on file
  for every athlete before Session 1.
- [ ] **NFR-002** — TAC credential document on file
  before first session.
- [ ] **NFR-003** — Session artifacts committed to
  version-controlled repository with timestamp
  before the next session begins.
- [ ] **NFR-004** — Chapter governance documents
  in public repository; no meeting required
  for third-party verification.

---

## Section C — Risk Compliance (Orange Book)

Per the chapter's ARC-{id}-RISK and HM Treasury
Orange Book.

- [ ] Chapter Lead has reviewed the chapter risk
  register in full.
- [ ] Residual risk ratings for all registered risks
  accepted and recorded.
- [ ] Any chapter-specific risks added to the local
  risk register using Orange Book scoring
  (Likelihood 1–5 × Impact 1–5; thresholds
  1–4 Low, 5–9 Medium, 10–16 High, 17–25 Critical).
- [ ] **Protocol dilution mitigation** — no TAC,
  no session. No session, no portfolio entry.
  Confirmed in writing.
- [ ] **Institutional IP capture mitigation** —
  per-institution legal review complete before
  first university contract execution.
- [ ] **NCAA compliance conflict mitigation** —
  SOBC framing (compliance solution, not benefit)
  reviewed with institutional compliance officer.
- [ ] **TAC quality degradation mitigation** —
  five-year TAC domain currency window enforced
  at annual chapter review.

---

## Section D — Business Case Compliance (Green Book 5-Case)

Per the chapter's ARC-{id}-SOBC and UK Government
Green Book. Each of the five cases must be present.
Missing cases block deployment.

- [ ] **Strategic Case.** Named problem, named user,
  strategic position, origin and validation record.
- [ ] **Economic Case.** Current-state cost,
  Exchange benefit inventory, measurable outcomes
  with targets.
- [ ] **Commercial Case.** Revenue streams,
  contract model, partner organization terms.
- [ ] **Financial Case.** Cost structure,
  cashflow impact on the institution,
  funding source identified.
- [ ] **Management Case.** Delivery plan,
  Chapter Lead identified, timeline to
  Session 1, dependencies named.

---

## Section E — FERPA and Data Protection

Per ARC-000-DPIA-v1.0 and FERPA (20 U.S.C. § 1232g).
Chapter Lead confirms:

- [ ] Institutional status determined — school official
  exception under written agreement, or independent
  program outside FERPA scope.
- [ ] Participation agreement records lawful basis
  (contract plus explicit consent for any disclosure
  beyond the session).
- [ ] Disclosure log active before Session 1; any
  transmission of artifacts to institutional systems
  or third parties recorded.
- [ ] Data inventory confirms no biometric, health,
  financial, academic-grade, or disciplinary data
  collected.
- [ ] Athlete private-key custody guidance delivered
  during onboarding; key loss consequences understood.
- [ ] **Bitcoin immutability vs. GDPR erasure review** —
  external legal review complete before any
  EU-resident athlete onboards.

---

## Section F — Governance Sign-off

Sign-off is performed on the chapter's local instance
of this framework, not on this global template. Each
chapter instance carries its own signature table and
evidence records.

A chapter is recognized when its local instance is
signed by three roles. Signatures attest to review,
not to approval by the founder. Principle 5 forbids
founder approval gates.

| Role | Attestation |
|---|---|
| Chapter Lead (or Sponsor) | Sections A through E reviewed. Residual risks accepted. Chapter ready for Session 1. |
| Map Lead | Session protocol compliance (FR-001 through FR-006) in place. Artifacts will be committed per NFR-003. |
| TAC (at least one) | Domain currency confirmed per NFR-002. Challenge posture per Principle 4 and Followership Doctrine (AC 72029, 2023) understood and accepted. |

Sign-off is recorded by committing the completed
chapter instance to the chapter's repository path.
The commit hash is the compliance record. No external
approval authority exists.

---

## How a Third Party Verifies Compliance

No founder call. No meeting. Three steps.

1. Read the chapter's signed FRMW instance at the
   chapter's repository path.
2. Confirm each referenced artifact exists at the
   cited location and version.
3. Confirm commit timestamps precede any claimed
   session date.

This is Principle 5 operating as designed.

---

## Source Documents

- ARC-000-PRIN-v1.0 — six non-negotiable principles
- ARC-000-ADR-v1.0 — ADR-001 (Bitcoin anchoring),
  ADR-002 (dual-hash), ADR-003 (SCQA ETU)
- ARC-000-DPIA-v1.0 — data protection risks and
  FERPA/GDPR mapping
- ARC-000-BRIEF-v1.0 — athlete participant briefing
- Chapter's ARC-{id}-REQ — functional and
  non-functional requirements
- Chapter's ARC-{id}-RISK — Orange Book risk register
- Chapter's ARC-{id}-SOBC — Green Book 5-case business
  case
- BMA Workup (SAX 12.1.21) — TAC role as domain
  challenger; curriculum evidence base
- British Army Followership Doctrine Note AC 72029
  (2023) — responsibility to challenge as the
  doctrinal basis of the TAC posture

---

## Chapter Instances

| Chapter | Local FRMW instance | Status |
|---|---|---|
| 001 — MEAC MVP | ARC-001-FRMW-v1.0 | Draft |

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial release — global compliance framework. Chapter 001 instance exists at ARC-001-FRMW-v1.0. |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
