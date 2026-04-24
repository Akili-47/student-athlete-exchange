# ARC-001-WARD-v1.0 — The Exchange Protocol: MEAC Competitive Landscape

**Status:** Approved  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Akili King  
**Repository:** student-athlete-exchange  
**Chapter:** 001 — MVP Deployment, MEAC Conference  

---

> **In plain language.** A Wardley Map of the athlete development market. It shows why traditional programs (career services, NIL compliance tools like INFLCR, and networking platforms like Athlete Network) are stuck in the commodity space, and why The Exchange occupies uncontested strategic ground by focusing on verifiable judgment.

## Purpose

This map defines the strategic positioning of The Exchange against existing market alternatives. It is used to justify the deployment to Athletic Directors and Partners by demonstrating that The Exchange does not compete with their existing software subscriptions — it solves a problem those tools are structurally incapable of addressing.

---

## The Map

**Interactive version:** [View and edit on OnlineWardleyMaps](https://onlinewardleymaps.com/#19cab2f2-9eae-4f41-a9a0-2aa9c1344824)

```text
title Athlete Development Landscape — MEAC MVP Context
anchor Employer [0.95, 0.50]
anchor Student Athlete [0.90, 0.40]

component Signal of Judgment [0.80, 0.25]
component Professional Network [0.75, 0.65]
component Compliance Tracking [0.70, 0.85]
component Resume Formatting [0.65, 0.90]

component The Exchange Protocol [0.60, 0.20]
component Athlete Network [0.55, 0.70]
component INFLCR / Opendorse [0.50, 0.85]
component University Career Services [0.45, 0.90]

component Wardley Mapping Method [0.40, 0.60]
component TAC Domain Expertise [0.35, 0.15]
component ETU Session Record [0.30, 0.25]
component NCAA Bylaw 16.3 [0.25, 0.80]

Employer -> Signal of Judgment
Student Athlete -> Signal of Judgment
Student Athlete -> Professional Network
Student Athlete -> Compliance Tracking
Student Athlete -> Resume Formatting

The Exchange Protocol -> Signal of Judgment
Professional Network -> Athlete Network
Compliance Tracking -> INFLCR / Opendorse
Resume Formatting -> University Career Services

The Exchange Protocol -> Wardley Mapping Method
The Exchange Protocol -> TAC Domain Expertise
The Exchange Protocol -> ETU Session Record
The Exchange Protocol -> NCAA Bylaw 16.3

INFLCR / Opendorse -> NCAA Bylaw 16.3
University Career Services -> NCAA Bylaw 16.3

evolve Signal of Judgment 0.45
evolve The Exchange Protocol 0.40
```

---

## Strategic Analysis

### 1. The Commodity Trap (Top Right)
University Career Services and compliance tools (INFLCR, Opendorse) sit in the top right of the map. They are highly visible to the user and highly evolved (commoditized). They solve the basic operational needs of formatting a document and tracking a disclosure. Because they are commodities, they provide zero competitive differentiation for the athlete in the job market.

### 2. The Networking Illusion (Middle)
Platforms like Athlete Network sit in the product phase. They provide access to alumni and job boards. However, access is not a signal of competence. The employer still has no way to evaluate the athlete's strategic judgment until the interview, at which point the athlete is relying on stories, not evidence.

### 3. The Uncontested Space (Bottom Left)
The Exchange sits in the custom-built space, driving the evolution of "Signal of Judgment." It relies on two components that cannot be commoditized by software: **TAC Domain Expertise** (the operational reality of the industry) and the **ETU Session Record** (the athlete's captured reasoning). 

Because the Exchange relies on live human friction (the TAC challenge) rather than passive software access, it produces an artifact that employers can trust. It does not compete with INFLCR or Career Services; it operates in a space they cannot reach.

---

## Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | April 2026 | Initial release — MEAC competitive landscape map |

---

*This document is part of The Exchange Protocol governance architecture.
Built with ArcKit. Stored in version control. Publicly verifiable.*
