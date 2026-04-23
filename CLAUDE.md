# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A governance documentation repository for **The Exchange Protocol** — a structured program for student-athlete professional development using Wardley Mapping sessions, domain expert (TAC) challenge, and cryptographic portfolio attribution. There is no source code. All work product is Markdown governance documents.

Public repository: `github.com/Akili-47/student-athlete-exchange`

---

## Document naming convention

`ARC-{project_id}-{TYPE}-v{version}.md`

- `000` = global / cross-chapter artifacts
- `001` = Chapter MVP (MEAC Conference deployment)

| Type code | Document type |
|---|---|
| PRIN | Architecture Principles |
| WARD | Wardley Map (syntax for create.wardleymaps.ai) |
| SOBC | Strategic Outline Business Case (UK Green Book 5-Case) |
| REQ | Chapter Requirements (functional + non-functional) |
| RISK | Risk Register (HM Treasury Orange Book) |
| STKE | Stakeholder Analysis |
| FRMW | Framework / Compliance Checklist |
| DPIA | Data Protection Impact Assessment |
| ADR | Architecture Decision Record |
| METH | Methodology document |
| PLAN | Deployment or operational plan |
| BRIEF | Participant briefing |

---

## Repository structure

```
projects/
  000-global/           # Cross-chapter artifacts (principles, global wardley map)
    wardley-maps/
  001-chapter-mvp/      # MEAC Conference MVP deployment documents
```

---

## Document frontmatter (required on every document)

```markdown
# ARC-{id}-{TYPE}-v{version} — {Protocol Name}: {Document Title}

**Status:** Draft | Approved  
**Version:** {n.n}  
**Date:** {Month Year}  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Chapter:** {id} — {chapter name}      ← omit for global documents
**Framework:** {governing framework}    ← include when applicable
```

---

## Closing footer (required on every document)

```
*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
```

---

## Protocol core concepts

- **TAC** — Tactical Advisory Challenger. A practitioner who has operated in the mapped domain professionally within the last five years. Not a facilitator — a challenger.
- **ETU** — Execution Trace Unit. SCQA-format (Situation / Complication / Question / Answer) capture at session close. Co-signed by Map Lead and TAC.
- **Assumption Delta** — The gap between where research places a component and where the TAC places it based on operational reality. This is the core value of every session.
- **Work Ledger** — Dual-hash attribution system with Bitcoin-anchored timestamps. Shared payload = organizational verification hash. Private payload = athlete-owned provenance hash.
- **ECHO Substrate** — Proprietary execution intelligence dataset that compounds across sessions. Governed by separate license (not CC or MIT).
- **Map Lead** — Session facilitator responsible for ETU capture and artifact version control.

---

## Six architecture principles (non-negotiable)

1. User need anchors everything — named user at top of every value chain
2. Domain expertise governs quality — TAC must have operated in domain within last 5 years
3. The practitioner owns the work — dual-hash enforces athlete ownership, not policy
4. The assumption delta is the value — research placement vs. TAC placement must be documented
5. The protocol governs, not the founder — no founder approval needed for compliant chapters
6. Open method, proprietary substrate — Wardley Mapping (CC), session format (MIT), ECHO (proprietary)

---

## When creating new documents

- Follow the naming convention exactly — document IDs are references in other documents
- Version control is the compliance record — commit artifacts with meaningful messages
- Compliance evidence fields in REQ documents must be specific and verifiable by third parties
- Risk scores = Likelihood (1–5) × Impact (1–5); thresholds: 1–4 Low, 5–9 Medium, 10–16 High, 17–25 Critical
- Wardley Map syntax targets `create.wardleymaps.ai` — coordinates are `[visibility, evolution]` where evolution runs 0.0 (genesis) → 1.0 (commodity)
