# ARC-000-ADR-v1.0 — The Exchange Protocol: Architecture Decision Record

**Status:** Approved  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Framework:** Michael Nygard ADR format

---

## Purpose

This document records the architecture decisions
that shape The Exchange Protocol. Each decision is
durable. Each decision is open to challenge through
the ADR process — propose a new ADR that supersedes
the prior one. Decisions are never revised in place.

The ADR log is the institutional memory of the protocol.
It exists so that a chapter onboarding three years from now
can read why a choice was made, not just what it was.

---

## Format

Each decision follows the Michael Nygard ADR structure:

- **Context** — the forces at play
- **Decision** — what was chosen
- **Consequences** — what follows, good and bad

New decisions append to this log. Superseded decisions
remain in the document with a forward pointer to the ADR
that replaced them.

Status values: Proposed, Accepted, Superseded.

---

## ADR-001 — Bitcoin anchoring for Work Ledger timestamp

**Status:** Accepted  
**Date:** April 2026

### Context

The Work Ledger records a timestamp for every portfolio
entry an athlete produces. The timestamp must outlast
any single institution — a university, a conference,
or the Exchange itself. An athlete who produces work
in 2026 must be able to prove authorship in 2046.

Candidate timestamp anchors:

1. RFC 3161 Trusted Timestamp Authority
2. Institutional database timestamps
3. Alternative blockchain (Ethereum, Solana, and others)
4. Bitcoin proof-of-work via OpenTimestamps

Timestamp authorities depend on the issuing CA remaining
operational. Institutional databases depend on the
institution's continued cooperation. Alternative
blockchains have shorter operational histories and
smaller proof-of-work security budgets.

### Decision

The Work Ledger anchors timestamps to the Bitcoin
blockchain using OpenTimestamps calendar proofs.

### Consequences

**Positive.** Verification is permissionless. Any party
can validate a timestamp against the public Bitcoin
ledger without contacting the Exchange, the chapter,
or the institution. Durability matches the operational
lifetime of Bitcoin itself — currently the longest
of any public blockchain.

**Negative.** Confirmation latency is measured in hours,
not seconds. Timestamp proofs require periodic calendar
upgrades as the Bitcoin network advances. Verification
tooling depends on Bitcoin network availability at the
time of audit, not at the time of issuance.

**Neutral.** OpenTimestamps batches many artifact hashes
into a single Bitcoin transaction. Cost scales with
calendar submissions, not with chapter volume.

---

## ADR-002 — Dual-hash attribution over single-hash

**Status:** Accepted  
**Date:** April 2026

### Context

Portfolio entries must satisfy two requirements that
conflict under a single-hash design:

1. The organization must be able to verify that a session
   produced a specific artifact (institutional verification).
2. The athlete must be able to prove authorship independent
   of the institution (athlete ownership).

A single shared hash held by the institution gives the
institution revocation power over the athlete's ownership
record. A private-only hash held by the athlete gives
the institution no verification anchor. Either design
violates Principle 3 (The practitioner owns the work).

### Decision

Every portfolio entry produces two hashes:

- **Shared payload hash** — organizational verification.
  Stored by the chapter. References the session,
  the TAC, the Map Lead, and the ETU.
- **Private payload hash** — athlete provenance.
  Key held by the athlete. References the full artifact
  plus any material the athlete chooses to keep private.

Both hashes are anchored to Bitcoin per ADR-001.

### Consequences

**Positive.** The athlete can prove authorship without
institutional cooperation. The institution can verify
the session without access to private artifact content.
Principle 3 is enforced mathematically, not by policy.

**Negative.** Athletes must safeguard their private key.
Key loss means loss of the private payload attestation.
The shared payload hash is unaffected by private key loss.

**Operational.** Chapters must run key-generation and
key-custody guidance as part of athlete onboarding.
See ARC-001-REQ NFR entries for key management requirements.

---

## ADR-003 — SCQA format for the Execution Trace Unit

**Status:** Accepted  
**Date:** April 2026

### Context

Every session closes with an Execution Trace Unit (ETU):
a durable record of what the session produced, what
assumption deltas surfaced, and what the athlete decided.
The ETU feeds the ECHO substrate, so its structure must
support cross-session aggregation.

Candidate formats:

1. Free-form prose summary
2. After-Action Review (AAR) — U.S. Army doctrine
3. Bullet-point session log
4. SCQA — Situation, Complication, Question, Answer
   (Barbara Minto, *The Pyramid Principle*)

Free-form prose does not aggregate. AAR is built for
exercises with a defined plan and outcome — it does not
fit a mapping session where the complication *is* the
outcome. Bullet-point logs record what happened without
capturing why it mattered.

### Decision

The ETU uses SCQA format. Every ETU contains four
named sections:

- **Situation** — what the map showed at session open
- **Complication** — what the TAC challenged and where
  the assumption delta surfaced
- **Question** — the strategic question the delta forced
- **Answer** — what the athlete decided, with reasoning

The ETU is co-signed by the Map Lead and the TAC
before the session closes.

### Consequences

**Positive.** The Complication field is where the
assumption delta lives. Making it a required field
enforces Principle 4 (The assumption delta is the value)
at the document level. Consistent structure enables
ECHO substrate aggregation across sessions and chapters.

**Negative.** SCQA requires practice. Early sessions
will produce weak Complication sections. Map Leads
need training on the format before running sessions.

**Reinforcing.** SCQA is a widely-taught consulting
format. Athletes exposed to the ETU discipline carry
the format into professional contexts. This is
intentional — the Exchange teaches strategic
communication through the artifact, not through
a separate curriculum.

---

## Decision Log

| ADR | Title | Status | Supersedes | Superseded by |
|---|---|---|---|---|
| 001 | Bitcoin anchoring for Work Ledger timestamp | Accepted | — | — |
| 002 | Dual-hash attribution over single-hash | Accepted | — | — |
| 003 | SCQA format for the Execution Trace Unit | Accepted | — | — |

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial release. ADR-001 through ADR-003 recorded. |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
