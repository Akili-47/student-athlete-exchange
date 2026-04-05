# ARC-001-RISK-v1.0 — The Exchange Protocol: Risk Register

**Status:** Approved  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Chapter:** 001 — MVP Deployment, MEAC Conference  
**Framework:** HM Treasury Orange Book  

---

## Purpose

This register documents every material risk to The Exchange
protocol at MVP deployment stage. Each risk is rated,
mitigated, and assigned an owner.

A risk with no documented mitigation is an assumption.
This document converts assumptions into managed decisions.

---

## Risk Rating Scale

**Likelihood:** 1 (rare) → 5 (near certain)  
**Impact:** 1 (negligible) → 5 (protocol-ending)  
**Score:** Likelihood × Impact  

| Score | Rating |
|---|---|
| 1–4 | Low |
| 5–9 | Medium |
| 10–16 | High |
| 17–25 | Critical |

---

## RISK 01 — Protocol dilution

**Description:**
A chapter adopts the Exchange name but drops TAC
governance to reduce friction. Sessions run without
domain expert challenge. Portfolio entries are produced
without assumption delta documentation. The protocol
degrades into a Wardley Mapping workshop with no
quality gate.

**Likelihood:** 4  
**Impact:** 5  
**Score:** 20 — Critical  

**Root cause:**
TAC recruitment is the hardest part of deployment.
When a chapter cannot find a qualified TAC,
the temptation is to proceed without one.

**Mitigation:**
Principle 2 (domain expertise governs quality)
is non-negotiable. No TAC, no session.
No session, no portfolio entry.
The compliance checklist (ARC-000-FRMW) requires
TAC credential documentation before first session.
Chapter recognition is withheld until satisfied.

**Owner:** Protocol governance (GitHub repository)  
**Residual risk:** Medium — self-policing protocol
requires community enforcement at scale.

---

## RISK 02 — Founder dependency

**Description:**
The Exchange cannot operate without Akili King
explaining, interpreting, or approving decisions.
Every chapter conversation requires his presence.
The protocol does not scale.

**Likelihood:** 4  
**Impact:** 4  
**Score:** 16 — High  

**Root cause:**
Fourteen years of iteration exists in Akili's head,
not in documented form. The governance architecture
being built now is the mitigation. Until it is
complete, the risk is active.

**Mitigation:**
Protocol lives in public GitHub repository.
MIT licensed. Any competent architect can read,
understand, and operate it without founder involvement.
Principle 5 (protocol governs, not founder) is
the architectural response to this risk.
ADR-004 documents the full origin lineage so
the reasoning behind every decision is accessible
without a conversation.

**Owner:** Akili King — mitigation in progress  
**Residual risk:** Low — once governance
architecture is complete and published.

---

## RISK 03 — Institutional IP capture

**Description:**
A university legal department claims ownership
of portfolio entries produced by athletes
during their enrollment. Work product created
using university resources is asserted as
institutional property. Athletes lose control
of their portfolios at graduation.

**Likelihood:** 3  
**Impact:** 5  
**Score:** 15 — High  

**Root cause:**
Most university IP policies were written for
research outputs and patentable discoveries —
not for student professional development portfolios.
The language is broad enough to create ambiguity.

**Mitigation:**
Principle 3 (practitioner owns the work)
is non-negotiable. Dual-hash Work Ledger
creates a cryptographic ownership record
that predates any institutional claim.
Bitcoin-anchored timestamps establish
athlete ownership at the moment of creation.
DPIA (ARC-001-DPIA) documents the legal basis
for this boundary before university contract
is signed. Contract language must explicitly
acknowledge athlete ownership of portfolio entries.

**Owner:** Akili King — legal review required
before first university contract execution  
**Residual risk:** Medium — requires per-institution
legal review. Cannot be fully mitigated by
protocol alone.

---

## RISK 04 — NCAA compliance conflict

**Description:**
An NCAA compliance officer determines that
The Exchange constitutes a benefit to athletes
that creates NIL or amateurism complications.
The university terminates the engagement.
The protocol is associated with compliance risk
rather than compliance solution.

**Likelihood:** 2  
**Impact:** 5  
**Score:** 10 — High  

**Root cause:**
NCAA compliance frameworks were not designed
with structured professional development protocols
in mind. Novel programs create interpretation risk.

**Mitigation:**
Portfolio entry is professional development output —
not compensation, not NIL deal, not benefit
with monetary value attached.
SOBC (ARC-001-SOBC) documents this distinction
in the Strategic Case section.
The Exchange positions itself as the compliance
solution to House v. NCAA pressure —
not as an additional compliance burden.
TAC participation is volunteer — no compensation
flows to athletes through The Exchange protocol.

**Owner:** Akili King — SOBC legal review
recommended before first university pitch  
**Residual risk:** Low — correct framing
eliminates most interpretation risk.

---

## RISK 05 — TAC quality degradation

**Description:**
TACs who were current in their domain at
recruitment become stale over time. A TAC
who operated in NIL in 2020 is evaluating
a 2027 NIL landscape map using outdated
operational knowledge. The assumption delta
— the core value of the session — is wrong.

**Likelihood:** 3  
**Impact:** 4  
**Score:** 12 — High  

**Root cause:**
Sports business and NIL move fast.
A five-year-old operational perspective
may no longer reflect what actually happens
in the domain. The TAC's value is current
operational knowledge, not historical expertise.

**Mitigation:**
TAC renewal requirement documented in
Principle 2: must have operated in domain
within last five years.
TAC renewal check at chapter annual review.
Athletes are encouraged to flag when TAC
corrections do not match their own research —
this is itself a weak signal worth capturing.

**Owner:** Chapter Map Lead  
**Residual risk:** Low — five-year renewal
window is conservative for most domains.

---

## RISK 06 — Origin IP dispute

**Description:**
A third party claims prior rights to The Exchange
concept, the SAX framework, or the Foot in the Door
portfolio-as-credential model. Akili's fourteen-year
development history is challenged.

**Likelihood:** 1  
**Impact:** 4  
**Score:** 4 — Low  

**Root cause:**
SAX framework was given to Charlie Gilmur
for execution at OSU Startup Weekend 2013.
Foot in the Door (2012) introduced the portfolio
concept as a future aspiration. Both predate
any third-party claim.

**Mitigation:**
ADR-004 documents the full origin lineage:
Foot in the Door (2012) → SAX (2013, Akili's
framework, first place OSU Startup Weekend,
published in Athletic Management) →
GP Monticello field deployment (2024) →
The Exchange protocol (2026).
Athletic Management article is dated public record.
OSU Startup Weekend results are documented.
ECHO provisional patents establish substrate
priority dates from April 2025.

**Owner:** Akili King  
**Residual risk:** Low — documented public
record predates any plausible competing claim.

---

## RISK 07 — MEAC-specific adoption failure

**Description:**
MEAC athletic departments face budget constraints
that prevent contract execution even when
the protocol is compelling. The first university
conversation produces interest but no commitment.
MVP deployment stalls.

**Likelihood:** 3  
**Impact:** 3  
**Score:** 9 — Medium  

**Root cause:**
MEAC institutions operate with significantly
smaller athletic budgets than Power Five programs.
A career services contract, even at near-zero cost,
requires budget approval cycles that can take
an academic year.

**Mitigation:**
The Exchange MVP requires one university,
one TAC, one partner organization,
one engagement. Not a contract first.
A proof of concept session can run before
any contract is signed — the portfolio entry
is the evidence that closes the contract
conversation. Start with the session.
Let the output sell the contract.

**Owner:** Akili King  
**Residual risk:** Low — proof of concept
model bypasses budget approval for first engagement.

---

## Risk Summary

| Risk | Score | Rating | Status |
|---|---|---|---|
| R01 — Protocol dilution | 20 | Critical | Mitigated by Principle 2 |
| R02 — Founder dependency | 16 | High | Mitigation in progress |
| R03 — Institutional IP capture | 15 | High | Legal review required |
| R04 — NCAA compliance conflict | 10 | High | SOBC framing mitigates |
| R05 — TAC quality degradation | 12 | High | Renewal requirement mitigates |
| R06 — Origin IP dispute | 4 | Low | ADR-004 documents lineage |
| R07 — MEAC adoption failure | 9 | Medium | POC model bypasses |

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial release — MEAC MVP deployment |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
