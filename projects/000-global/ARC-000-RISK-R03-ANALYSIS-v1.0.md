# ARC-000-RISK-R03-ANALYSIS-v1.0 — The Exchange Protocol: Risk R-03 Analysis (Bitcoin Immutability vs. GDPR Article 17)

**Status:** Draft  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Framework:** GDPR Article 17 (right to erasure); EDPB Guidelines 02/2025 (draft, finalization pending); CNIL 2018 blockchain guidance

---

> **In plain language.** A focused analysis of the one DPIA risk that needs external legal review before the Exchange enrolls any EU-resident athlete: whether the Bitcoin-anchored timestamps in the Work Ledger can be reconciled with the GDPR right to erasure. **This document is not legal advice.** It is structured input *to* legal review, so the lawyer engaged on R-03 can engage with substance rather than starting from scratch.

## Purpose

This document drills down on Risk R-03 from ARC-000-DPIA-v1.0:
the conflict between Bitcoin-anchored timestamp permanence
and GDPR Article 17's right to erasure. The DPIA marks R-03's
residual risk as *Medium pending external legal review*. This
document does not change that rating. It prepares the brief
that a lawyer needs to perform the review.

The DPIA's single-paragraph mitigation summary is necessarily
compressed. R-03 is the highest-residual risk in the DPIA and
the one most exposed to changes in the EU regulatory landscape.
A serious answer requires more than a paragraph.

---

## Scope and limits

**This document is not legal advice.** It is a technical and
regulatory brief. It does not bind the Exchange Protocol, any
chapter, any institution, or any data subject. It does not
substitute for the external legal review the DPIA requires.

What this document *does*:

- States the legal question precisely.
- Documents the technical architecture in legally-relevant terms.
- Surveys the current EU regulator landscape with citations.
- Articulates the DPIA's existing mitigation argument and assesses
  its strength against the latest guidance.
- Identifies specific weak points the legal reviewer should test.
- Enumerates the discrete questions a lawyer needs to answer to
  clear R-03 to Low residual.
- Lists the evidence each chapter must maintain to demonstrate
  Article 17 compliance to a supervisory authority.

What this document *does not*:

- Provide an opinion on whether the Exchange Protocol satisfies
  Article 17.
- Reduce R-03's residual rating below Medium.
- Substitute for jurisdiction-specific legal counsel.

---

## The legal question

Stated precisely:

> When an EU-resident data subject (athlete) participates in an
> Exchange session, two artifacts are produced that bear on
> Article 17: a *shared payload hash* (held by the chapter,
> anchored to Bitcoin via OpenTimestamps) and a *private payload
> hash* (held by the athlete, also anchored to Bitcoin). If the
> athlete subsequently invokes the right to erasure under Article
> 17 GDPR, can the Exchange Protocol — through deletion of
> off-chain metadata, destruction of the athlete's private key,
> or other technical and organizational measures — comply with
> that right notwithstanding the impossibility of removing the
> anchored hashes from the Bitcoin blockchain?

The DPIA currently answers: *yes, through metadata pseudonymization
and key destruction*. The EDPB's April 2025 draft guidelines push
that answer harder than the DPIA's compressed summary acknowledges.

---

## Technical architecture (legally relevant facts)

### What is recorded on-chain

For each Exchange session artifact (a Wardley map plus session
record), the Work Ledger produces two hashes per ADR-002:

1. **Shared payload hash.** SHA-256 over the public artifact
   plus session metadata (session date, participant names by
   role, domain boundary, ETU SCQA text).
2. **Private payload hash.** SHA-256 over the full artifact
   plus athlete-private material; key held by the athlete.

Each hash is then submitted to OpenTimestamps. Per OpenTimestamps'
documented behavior, the client concatenates a 128-bit nonce to the
input hash, computes a second SHA-256 over that combined value,
and submits *that* value to a calendar server, which batches it
into a Merkle tree whose root is recorded in a Bitcoin transaction.

The on-chain Bitcoin record is therefore a hash of a hash of (the
artifact + metadata + nonce). The artifact text itself is never
on-chain. The metadata text itself is never on-chain. Reconstructing
either from the on-chain value alone is computationally infeasible
under SHA-256 preimage assumptions.

### What is recorded off-chain

In the chapter's GitHub repository:

- The artifact files (Wardley map source, ETU SCQA text)
- The session metadata (participant names, dates, domains)
- The hash values themselves
- The OpenTimestamps proof file (`.ots`) linking the hash to the
  Bitcoin transaction

In the athlete's possession:

- The athlete's private key (used for the private payload)
- Any private artifact material the athlete chose not to publish

In the institution's records (where applicable):

- Copies of artifacts ingested under a chapter–institution agreement
- Whatever metadata that agreement specifies

### What "linkability" means in this architecture

A given on-chain hash is *cryptographically* unlinkable to any
person without the off-chain metadata. It is *practically*
linkable to the athlete *only* through the chapter's repository
record (or any third-party copy of that record).

This is a critical distinction the EDPB takes seriously: a hash
on-chain is not anonymous merely because it cannot be inverted;
it remains personal data so long as *anyone* — including the
controller — holds the linking metadata.

---

## Regulator landscape

### GDPR Article 17 — the operative text

Article 17(1) gives data subjects the right to obtain erasure
"without undue delay" where one of six grounds applies (consent
withdrawn, data no longer necessary, unlawful processing, etc.).

Article 17(3) lists exceptions, including: (a) freedom of
expression, (b) legal obligation, (c) public interest in public
health, (d) archiving in the public interest / scientific or
historical research, (e) legal claims.

Recital 26 defines anonymous data as data that cannot be linked
to a person "by all means reasonably likely to be used." Data
that fails this test is pseudonymous, and pseudonymous data
remains personal data within GDPR scope.

### CNIL 2018 — Blockchain and the GDPR

The French data protection authority (CNIL) published the first
substantive DPA guidance on blockchain in November 2018. Its
key positions relevant to R-03:

- Personal data should be processed off-chain wherever possible.
- Where on-chain recording is necessary, "commitments" — keyed
  hashes computed with a secret salt — are the recommended form.
- Erasure can be achieved by *deleting the secret key* used in
  the keyed hash function plus any related off-chain metadata.
  Once the key is destroyed, the on-chain commitment is
  computationally inaccessible and effectively erased.

This is the foundational regulatory position the Exchange's
current mitigation argument tracks.

### EDPB Guidelines 02/2025 — the current authoritative draft

The European Data Protection Board adopted *Guidelines 02/2025
on processing of personal data through blockchain technologies*
on 8 April 2025. The initial public consultation ran through
9 June 2025; an extended consultation ran October 9 to December
4, 2025; over 100 responses were published in March 2026. As of
April 2026, the final version is being prepared jointly by
the EDPB and the European Commission. The April 2025 draft
remains the operative interpretation pending finalization.

The Guidelines tighten the regulatory posture meaningfully
beyond CNIL 2018. Key positions from secondary analyses
(William Fry, ActiveMind, Privacy World, Dudkowiak & Putyra)
that quote or paraphrase the draft:

- **Hashed data remains personal data.** Per the Guidelines,
  "encrypted or hashed data remains personal and the GDPR
  continues to apply." A hash on-chain does not become
  anonymous merely because it cannot be inverted — so long as
  the controller (or any party) holds the linking metadata, the
  hash is pseudonymous.
- **Off-chain storage is the architectural default.** "The
  blockchain should refer to data stored outside the blockchain
  in the company's information systems." On-chain storage of
  personal data is permitted only where there is a documented
  necessity that off-chain alternatives cannot satisfy.
- **Technical impossibility is not a defense.** The Guidelines
  state that "technical impossibility is not a justification
  for disregarding the rights of data subjects. It is the
  responsibility of the controllers to design the technical
  means and processes in such a way that the law can and
  will be complied with."
- **Privacy by design is mandatory.** The Guidelines emphasize
  that compliance must be designed in at the architectural
  stage, not retrofitted.

The Guidelines do *not* explicitly endorse cryptographic
destruction (key deletion) as fully satisfying Article 17.
They acknowledge such techniques but stop short of CNIL's
2018 position that key destruction equals erasure. This is
the most material shift since CNIL.

### Comparative DPA landscape

Beyond CNIL and the EDPB, the Spanish AEPD and Italy's GPDP have
issued blockchain-related opinions broadly compatible with the
EDPB direction. The UK ICO's position post-Brexit is less
prescriptive but generally aligns with EDPB on hashed data
remaining personal. No DPA, as of this draft's research date,
has issued a public enforcement decision specifically on a
Bitcoin-anchored timestamp service exercising Article 17.

---

## The current mitigation argument (restated from DPIA)

R-03 in ARC-000-DPIA-v1.0 reads (paraphrased):

> The anchor is a hash of a hash. It contains no PII and cannot
> be reversed to PII without the original metadata. The chapter
> pseudonymizes or deletes the metadata on request, which renders
> the anchored hash unlinkable to the athlete. This is the
> standard approach for blockchain-anchored systems under current
> regulator guidance. Flagged for external legal review before
> the first EU-resident athlete onboards.

The argument has three propositions:

- **P1.** The on-chain value is not PII (because it is a hash
  of a hash with a nonce).
- **P2.** Deletion of off-chain metadata renders the on-chain
  value unlinkable to the data subject.
- **P3.** Functional unlinkability satisfies Article 17.

---

## Strength assessment

### Where the argument is supported by current guidance

- **The hybrid off-chain/on-chain architecture** is exactly
  what EDPB 2025 recommends. The Exchange does not store
  personal data on-chain; it stores cryptographic references
  that point to off-chain artifacts. This is the architectural
  default the Guidelines endorse.
- **OpenTimestamps' nonce-and-rehash** further reduces
  linkability beyond a bare SHA-256 of the artifact.
- **CNIL 2018** explicitly accepts key destruction as a path
  to functional erasure. P3 is at least one DPA's position.
- **No public enforcement decision** has yet treated this
  architecture as Article 17-noncompliant.

### Where the argument is potentially weak

- **P1 is contested by EDPB 2025.** The Guidelines explicitly
  state that hashed data remains personal data. The "hash of
  a hash isn't PII" framing in the DPIA is not consistent with
  the EDPB draft. A lawyer reviewing R-03 will start here.
- **P2 depends on every metadata copy being deleted.** If the
  institution has ingested artifacts under a chapter–institution
  agreement, or if a partner organization retains its copy of
  the map deliverable, deleting only the chapter's repository
  metadata does not achieve unlinkability. The mitigation must
  cover *all* off-chain metadata holders, not just the chapter.
- **P3 is the EDPB's harder question.** The Guidelines do not
  explicitly endorse cryptographic destruction as full Article
  17 compliance. CNIL 2018 does. The EDPB direction-of-travel
  is toward stricter readings.
- **Athlete-held private key** introduces a third party (the
  athlete) whose cooperation is required for full erasure of
  the private payload. If an athlete previously shared their
  key with an employer (a normal use case), erasure of the
  private payload becomes coordinated, not unilateral.
- **The Bitcoin transaction itself reveals a timestamp.** Even
  with all metadata deleted, the on-chain record evidences that
  *some* hash was anchored at a specific moment. Forensic
  re-identification — by an adversary with contextual knowledge
  of who participated in which session — is not foreclosed by
  metadata deletion alone.

---

## Specific questions for legal review

A lawyer engaged to clear R-03 needs to answer these:

1. **Hashed data classification.** Under EDPB Guidelines
   02/2025 as it stands (draft, finalization pending), does
   the OpenTimestamps double-hashing render the on-chain value
   anonymous, pseudonymous, or personal data?
2. **Cryptographic destruction equivalence.** Does deletion of
   off-chain metadata plus destruction of the athlete's private
   key satisfy Article 17 erasure obligations under EDPB 2025?
   How does the answer change if the EDPB final version
   tightens further?
3. **Multi-party metadata.** Where the institution has ingested
   artifacts under a chapter–institution agreement, what
   technical and organizational measures must the chapter take
   to ensure institutional copies are also subject to erasure
   on a single Article 17 request?
4. **Article 17(3) exceptions.** Do any of the Article 17(3)
   exceptions plausibly apply to Exchange portfolio artifacts
   — particularly (d) archiving in the public interest /
   scientific or historical research, given the open licensing
   of session method (CC BY-SA) and contributions to the
   Wardley Map Repository?
5. **Public publication conflict.** Where an athlete has
   contributed a map to the public Wardley Map Repository under
   CC BY-SA 4.0, and subsequently invokes Article 17, what is
   the chapter's obligation regarding the published copy and
   downstream redistributions?
6. **Jurisdiction.** Does the Exchange's use of Bitcoin
   anchoring (a globally distributed ledger) constitute
   processing in the EU when the only EU connection is one
   enrolled EU-resident athlete? What triggers EU jurisdictional
   reach in this architecture?
7. **Final guidelines impact.** Once EDPB Guidelines 02/2025
   are finalized jointly with the Commission, what specific
   provisions should be re-tested against this architecture?

---

## Evidence checklist for chapters

To demonstrate Article 17 readiness to a supervisory authority,
each chapter enrolling EU-resident athletes should maintain:

- **Documented privacy-by-design rationale.** Why on-chain
  hashing was chosen, what off-chain alternatives were
  considered, why off-chain alone was insufficient.
- **A complete inventory of off-chain metadata locations.**
  Chapter repository, institutional record system (where
  applicable), partner organization copies, athlete-held
  copies. Each location named, each retention policy
  documented.
- **A documented erasure procedure.** Step-by-step process
  for deleting metadata across every inventoried location
  on a single Article 17 request, including the procedure
  for athlete-held private key destruction.
- **A documented timeframe.** Article 17 requires "without
  undue delay" — typically interpreted as 30 days. The
  procedure must complete within that window.
- **A disclosure log.** Every transmission of session
  artifacts to institutions, partners, or third parties
  recorded with date, recipient, and purpose. This log is
  consulted on every Article 17 request.
- **Athlete key custody guidance.** Documentation that the
  athlete was informed at onboarding that their private key
  is theirs to manage, that key loss has consequences, and
  that key destruction is the path to erasing the private
  payload.
- **A re-identification risk assessment.** Documented analysis
  of forensic re-identification scenarios (timestamp + context
  → person), with the chapter's view on whether such scenarios
  are "reasonably likely" under Recital 26.
- **A standing chapter–institution agreement clause.** Where
  artifacts are ingested institutionally, the agreement names
  Article 17 cooperation as a chapter–institution obligation,
  not a unilateral chapter promise.

---

## What this document changes

Nothing operationally. The DPIA's residual risk on R-03 remains
**Medium pending external legal review** until a qualified
lawyer answers the seven questions above.

What this document *does* change is the readiness for that legal
review. A lawyer reading this document plus the DPIA plus the ADR
should be able to engage substantively with the R-03 question
within hours rather than days.

The Exchange should not enrol any EU-resident athlete until:

1. The seven questions are answered in writing by qualified
   counsel familiar with EDPB Guidelines 02/2025 (final or draft).
2. The chapter implements the evidence checklist above.
3. The DPIA is updated to reflect counsel's answers (and R-03
   residual rating is re-evaluated).

Until those steps are complete, R-03 remains the gating risk on
EU enrollment. Chapters in the United States are unaffected by
this constraint; FERPA and the CCPA do not raise the same
immutability tension.

---

## Cross-references

- ARC-000-DPIA-v1.0 — Risk R-03 (the source flag this analysis expands)
- ARC-000-ADR-v1.0 — ADR-001 (Bitcoin anchoring), ADR-002 (dual-hash)
- ARC-000-FRMW-v1.0 — Section E (FERPA + data protection compliance)
- ARC-001-FRMW-v1.0 — Chapter 001 explicitly defers EU-resident
  enrollment until R-03 legal review completes

External primary sources:

- Regulation (EU) 2016/679 ("GDPR"), Article 17 and Recital 26
- EDPB Guidelines 02/2025 on processing of personal data through
  blockchain technologies (April 2025 draft, finalization
  pending as of April 2026)
- CNIL, *Blockchain: Solutions for a responsible use of the
  blockchain in the context of personal data* (November 2018)
- OpenTimestamps protocol specification

External secondary sources consulted:

- William Fry, "EDPB Guidelines raise questions on how GDPR
  interacts with blockchain"
- ActiveMind Legal, "EDPB on data protection in blockchain"
- Privacy World, "From Blocks to Rights: Privacy and Blockchain
  in the Eyes of the EU Data Protection Authorities" (May 2025)
- Dudkowiak & Putyra, "EDPB Blockchain Guidelines 2025"
- Oxford Academic, *Journal of Cybersecurity*, "Reconciling
  blockchain technology and data protection laws" (2025)

---

## Version history

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial draft. Structured input to external legal review of DPIA Risk R-03. Synthesizes EDPB Guidelines 02/2025 (draft), CNIL 2018, and the Exchange's specific architecture. Not legal advice. |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
