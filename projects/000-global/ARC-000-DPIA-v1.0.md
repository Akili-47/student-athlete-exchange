# ARC-000-DPIA-v1.0 — The Exchange Protocol: Data Protection Impact Assessment

**Status:** Draft  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Framework:** FERPA (20 U.S.C. § 1232g); GDPR-adjacent principles (ICO DPIA guidance)

---

> **In plain language.** For university legal teams and compliance officers. Documents what athlete data the Exchange collects (cryptographic hashes and session artifacts — no grades, health, or financial data), how FERPA and GDPR-adjacent rights are handled, and six identified risks with mitigations. One risk — blockchain-anchored timestamps vs. the right to erasure — is flagged for external legal review before any EU-resident athlete enrolls.

## Purpose

This DPIA assesses the data protection risks created
by the Exchange Protocol's Work Ledger and session
artifacts. It is a global governance artifact. Every
compliant chapter adopts this DPIA by reference and
confirms the evidence fields against local conditions.

The data subjects are college athletes at any accredited
institution receiving federal funding, regardless of
conference affiliation, division, or sport. Where chapters
operate internationally or enroll EU-resident athletes,
GDPR applies in addition to FERPA.

---

## Scope

### Data subjects

College athletes at accredited higher-education
institutions. The DPIA does not restrict itself to
any conference, division, or sport. Accreditation
by a recognized accrediting body plus federal funding
triggers FERPA coverage by default.

### Data processed

1. **Shared payload hash** — SHA-256 of session artifact
   plus session metadata. Stored by the chapter and
   anchored to Bitcoin per ADR-001.
2. **Private payload hash** — SHA-256 of full artifact
   plus athlete-private material. Key held by the athlete.
   Anchored to Bitcoin per ADR-001 and ADR-002.
3. **Session artifacts** — pre-work canvas (TAC),
   phase outputs (Phases 1–4), SCQA session record (ETU),
   participation agreement. Version controlled per NFR-003.
4. **Participant identifiers** — athlete name, TAC name,
   Map Lead name, session date, domain boundary.

Biometric, health, financial, academic-grade, and
disciplinary data are **out of scope by design**.
The Exchange does not collect these categories.

### Data controllers and processors

- **Chapter (data controller)** — defines purposes and
  means of processing. Holds the shared payload.
- **Athlete (data subject and joint controller for
  private payload)** — holds the private key.
  Controls scope of private payload content.
- **Institution (joint controller where a chapter is
  institutionally embedded)** — may ingest session
  records into institutional systems. Governed by the
  chapter–institution agreement, not by this DPIA.

### Lawful basis

Primary: **contract** — chapter participation agreement
signed before Session 1 (NFR-001).

Secondary: **explicit consent** — required for any
disclosure beyond the session, including institutional
ingestion, public portfolio publication, or transfer
to third parties.

Legitimate interest is not invoked. Contract and
consent cover all processing.

---

## Data inventory

| Item | Contains PII? | Storage | Retention | Controller |
|---|---|---|---|---|
| Shared payload hash | No (hash only) | Chapter repository + Bitcoin | Indefinite | Chapter |
| Private payload hash | No (hash only) | Athlete-held + Bitcoin | Indefinite | Athlete |
| Shared payload metadata | Yes (names, date, domain) | Chapter repository | Until pseudonymization request | Chapter |
| Private payload content | Athlete's choice | Athlete-held | Athlete decision | Athlete |
| Session artifacts (maps, ETU) | Yes (participant names) | Version-controlled repository | Indefinite | Chapter |
| Participation agreement | Yes (signature, contact) | Chapter records | 7 years post-session | Chapter |

---

## GDPR-adjacent principle mapping

| Principle | Applied to Exchange Protocol |
|---|---|
| Lawfulness, fairness, transparency | Participation agreement discloses all processing in plain language before Session 1 |
| Purpose limitation | Data used only for session execution, portfolio creation, and protocol compliance verification. No secondary use without consent |
| Data minimization | No biometric, health, financial, academic-grade, or disciplinary data collected. Hash-based Work Ledger stores no raw PII |
| Accuracy | TAC challenge mechanism (FR-003, FR-005) enforces factual accuracy of session content. Athletes may request correction of metadata at any time |
| Storage limitation | Participation agreements retained 7 years. Session metadata pseudonymized on athlete request. Hash records are immutable by design — see Risk R-03 |
| Integrity and confidentiality | Dual-hash design (ADR-002) keeps the private payload under athlete control. Shared payload stores no reconstructable PII |
| Accountability | Public governance repository (NFR-004). All processing rules documented and version controlled |

---

## FERPA mapping

| FERPA element | Applied to Exchange Protocol |
|---|---|
| Education record definition | Work Ledger is **not** an education record by design — Principle 3 establishes athlete ownership. The shared payload hash is a cryptographic attestation, not an institutional record |
| School official exception | Applies only where a chapter is institutionally embedded under a written school–chapter agreement that defines "legitimate educational interest" |
| Directory information | Not used. No athlete information published without explicit consent |
| Disclosure log | Chapter maintains a disclosure log for any transmission of session artifacts to institutional systems or third parties |
| Right to inspect | Athletes may inspect any shared-payload metadata referring to them at any time via chapter repository access |
| Right to amend | Athletes may request amendment of metadata. Hash records themselves cannot be amended; correction is by superseding entry |
| Parental rights | Not applicable — participants are college-enrolled, so FERPA rights are held by the athlete |

---

## Data subject rights

- **Access.** Athletes may request a full inventory of
  their data held by the chapter, including shared
  payload metadata and session artifact references.
  Response within 30 days.
- **Rectification.** Metadata errors corrected on request.
  Hash records cannot be altered; a superseding entry is
  added with reference to the original.
- **Erasure.** Private payload: self-service via key
  destruction. Shared payload metadata: pseudonymized
  on request. Bitcoin-anchored hashes: not erasable
  (see Risk R-03).
- **Portability.** Athletes receive their complete
  data set in machine-readable format on request
  (markdown artifacts, hashes, timestamp proofs).
- **Objection.** Athletes may withdraw from the chapter
  at any time. No future sessions will reference them.
  Historic records remain unless erasure is requested.

---

## Risks and mitigations

Risk scores use the Orange Book scale per CLAUDE.md:
Likelihood (1–5) × Impact (1–5). Thresholds: 1–4 Low,
5–9 Medium, 10–16 High, 17–25 Critical.

### R-01 — Institutional coercion of athlete portfolio

**Likelihood:** 3 | **Impact:** 4 | **Score:** 12 (High)

An institution pressures an athlete to surrender private
payload access as a condition of NIL support, scholarship
renewal, or transfer clearance.

**Mitigation.** Principle 3 enforced mathematically via
the dual-hash design (ADR-002). Athlete keys never
transit institutional systems. The chapter participation
agreement explicitly prohibits key surrender clauses.

**Residual:** Low.

---

### R-02 — Athlete private key loss

**Likelihood:** 3 | **Impact:** 3 | **Score:** 9 (Medium)

An athlete loses their private key. The private payload
attestation becomes unrecoverable.

**Mitigation.** Chapter onboarding includes key custody
guidance. Key loss does not affect the shared payload —
athletes retain institutional verification. Private
payload is recoverable via athlete-configured backup;
otherwise it is not.

**Residual:** Low.

---

### R-03 — Bitcoin-anchored immutability vs. erasure rights

**Likelihood:** 5 | **Impact:** 2 | **Score:** 10 (High)

A Bitcoin-anchored hash cannot be removed from the
blockchain. An athlete exercising GDPR Article 17
(right to erasure) cannot erase the anchored hash itself.

**Mitigation.** The anchor is a hash of a hash. It
contains no PII and cannot be reversed to PII without
the original metadata. The chapter pseudonymizes or
deletes the metadata on request, which renders the
anchored hash unlinkable to the athlete. This is the
standard approach for blockchain-anchored systems under
current regulator guidance. **Flagged for external legal
review before the first EU-resident athlete onboards.**

**Residual:** Medium (pending legal review).

---

### R-04 — Session artifacts contain unintended PII

**Likelihood:** 2 | **Impact:** 3 | **Score:** 6 (Medium)

Map content or ETU narrative contains personal
information about the athlete, a third party, or
proprietary domain information.

**Mitigation.** Map Lead reviews the artifact before
commit. Redaction is applied before version control.
Athletes may request review and redaction at any time.

**Residual:** Low.

---

### R-05 — Institutional ingestion converts artifacts to education records

**Likelihood:** 4 | **Impact:** 2 | **Score:** 8 (Medium)

An institution ingests session artifacts into its
record system. Those copies become FERPA-governed
education records under the institution's control.

**Mitigation.** A chapter–institution agreement is
required before any ingestion. The agreement specifies
scope, purpose, retention, and athlete consent
requirements. Artifacts in the chapter repository
remain athlete-owned regardless of institutional copies.

**Residual:** Low.

---

### R-06 — Cross-border transfer without adequacy mechanism

**Likelihood:** 2 | **Impact:** 3 | **Score:** 6 (Medium)

An EU-resident athlete's data is processed on US
infrastructure without an adequate transfer mechanism.

**Mitigation.** Chapters enrolling EU-resident athletes
implement Standard Contractual Clauses or an equivalent
mechanism in the participation agreement. The hash-based
Work Ledger minimizes exposure — most cross-border data
is non-reversible cryptographic material.

**Residual:** Low.

---

## Residual risk and outcome

After mitigation:

- R-03 at **Medium** — pending external legal review
  on blockchain anchoring vs. GDPR Article 17 before
  any EU-resident athlete onboards.
- R-05 at **Low** — controlled by per-chapter
  institutional agreement.
- All other risks at **Low** after mitigation.

**DPIA outcome.** Processing may proceed subject to:

1. Legal review of R-03 before first EU-resident athlete.
2. Signed chapter–institution agreement before any
   artifact ingestion (R-05).

---

## Compliance evidence

| Requirement | Evidence source | Owner |
|---|---|---|
| Participation agreement on file | Chapter records per NFR-001 | Chapter |
| Private key custody guidance delivered | Onboarding checklist countersigned by athlete | Chapter |
| Disclosure log maintained | Chapter ledger, commit-timestamped | Chapter |
| Redaction review before commit | Session artifact metadata with Map Lead sign-off | Map Lead |
| Institutional agreement (if ingestion occurs) | Signed chapter–institution agreement in chapter records | Chapter |
| EU data subject SCCs (if applicable) | Participation agreement addendum | Chapter |

---

## Consultation

This DPIA references:

- ARC-000-PRIN-v1.0 — Architecture Principles (esp. P3)
- ARC-000-ADR-v1.0 — ADR-001, ADR-002, ADR-003
- ARC-001-REQ-v1.0 — FR-003, FR-005, FR-006, NFR-001,
  NFR-003, NFR-004
- ARC-001-RISK-v1.0 — Chapter risk register
  (cross-reference)
- BMA Workup (SAX 12.1.21) — curriculum scope and
  TAC role as domain challenger
- WPLDS 2015 Handbook — Work Ledger as the
  Cadet Development Report analogue

External consultation required before Approved status:

- Institutional Registrar or FERPA compliance officer
  (chapter-specific).
- Data Protection Officer — for chapters enrolling
  EU-resident athletes.
- Legal counsel on R-03 — blockchain anchoring vs.
  GDPR Article 17.

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial draft. Global governance artifact covering any compliant chapter. Pending legal review on R-03 before first EU-resident athlete |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
