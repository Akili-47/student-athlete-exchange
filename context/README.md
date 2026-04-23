# Context: Source Document Evidence Base

This directory contains structured summaries of the source documents that form the intellectual and operational foundation of The Exchange Protocol. These summaries exist so that Claude Code can read the full evidence base when generating governance artifacts, ensuring that every document it produces is traceable back to its source.

## How to Use This Directory

When generating a new governance document, instruct Claude Code to read the relevant context files first. For example:

```text
Read context/01-WPLDS-2015.md and context/02-Followership-Doctrine.md, then create ARC-000-FRMW-v1.0.md.
```

## Source Documents

| File | Source | What It Provides |
|---|---|---|
| `01-WPLDS-2015.md` | West Point Leader Development System (2015) | System architecture, continuous assessment, documentation standards |
| `02-Followership-Doctrine.md` | British Army Followership Doctrine Note (2023) | TAC role definition, Challenge Spectrum, exemplary follower model |
| `03-Army-Leadership-Doctrine.md` | British Army Leadership Doctrine (2021) | Mission Command, governance philosophy, audit trail requirement |
| `04-Drucker-Managing-Oneself.md` | Peter Drucker, HBR (1999) | Self-knowledge diagnostic, feedback analysis, personal operating model |
| `05-Level-Launch.md` | Level Launch (2016) | Multi-stakeholder journey structure, athletic identity crisis |
| `06-Productio.md` | Productio Platform (2019-2020) | Accountability layer design, workflow architecture |
| `07-BMA-Workup.md` | SAX Workup 12.1.21 | Operational model, curriculum, TAC definition, competitive landscape |
| `08-OSU-Startup-Weekend.md` | The Future Is Now, Huffington Post (2013) | Origin story, proof of concept |

## Traceability

Every governance document in this repository should be traceable to at least one source in this directory. The **Architecture Principles (ARC-000-PRIN)** are the primary document that maps principles to sources. The **Origin Document (ARC-000-ORIG)**, when created, will provide the full lineage narrative.
