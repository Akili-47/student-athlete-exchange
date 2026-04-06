# ARC-000-METH-v1.1 — Mapping Methodology and Learning Ecosystem

**Document ID:** ARC-000-METH-v1.1  
**Status:** Active  
**Scope:** Global — applies to all Exchange chapters  
**Owner:** Akili King, Lead Researcher  

---

## Purpose

This document explains the analytical method at the center of The Exchange, why it works, and how athletes learn it. It is written for athletic directors, university administrators, and domain experts. 

The Exchange does not teach strategy in a classroom. It uses a specific tool — **Wardley Mapping** — to force athletes to make decisions under pressure from a domain expert. The learning ecosystem that supports this process is entirely open, verifiable, and exists independently of the athletic department.

---

## The Method: Wardley Mapping

Every Exchange session is built around a single analytical tool: a Wardley Map.

A Wardley Map is a visual picture of how an industry actually works — not how it is described in reports, but how value actually moves from raw components to the end user. It shows what is rare and what is common, what is changing fast and what is stable, and where the real leverage is.

When an athlete maps a real organization with a domain expert (the TAC), they are not doing a theoretical exercise. They are producing a picture of where that organization sits in its competitive landscape. The TAC challenges every placement. If the athlete's reasoning does not hold up against the TAC's operational experience, the map changes. 

The result is a map that reflects reality, not assumptions. The gap between what the athlete assumed and what the TAC proved is the learning artifact.

---

## The Learning Ecosystem (The Glidepath)

Athletes do not need to study strategy before their first session. They learn the method by doing it. 

The Exchange relies on a three-tier external ecosystem to support this learning process. This structure mirrors the West Point model: the standard is held externally, the resources are available to everyone, and the individual decides how far they want to go.

### 1. The Practical Layer: wardleymaps.com
*The starting point for volunteers.*

[wardleymaps.com](https://www.wardleymaps.com) is the community-built, plain-language resource layer. It is where athletes go to understand the mechanics of the tool without getting bogged down in academic theory.

**How The Exchange uses it:**
*   **Before the first session:** Volunteers read the [15-minute 101 Guide](https://www.wardleymaps.com/guides/wardley-mapping-101). This is the only prerequisite.
*   **Between sessions:** Athletes review [real-world case studies](https://www.wardleymaps.com/practice) (e.g., healthcare, retail, supply chain) to see how the method applies to the industries they are mapping.
*   **During sessions:** TACs and Map Leads use the [tools and templates](https://www.wardleymaps.com/resources) provided on the site to run the room.

### 2. The Foundational Layer: swardleymaps.com
*The doctrine for Map Leads.*

[swardleymaps.com](https://www.swardleymaps.com/) is the official home of Wardley Maps by Simon Wardley. It provides the core doctrine, the book, and the fundamental principles that define why the method works.

**How The Exchange uses it:**
You do not need the doctrine to participate in a session. However, athletes who progress to Year 3 and Year 4 (preparing to become Map Leads) use this layer to understand the deeper strategic cycles (Boyd's OODA loop, Sun Tzu's five factors) that govern the maps they are building.

### 3. The Capability Layer: wardleymaps.ai
*The formal reference for progression.*

[wardleymaps.ai](https://wardleymaps.ai) is an AI-powered platform that includes map creation tools and a formal training pathway.

**How The Exchange uses it:**
The Exchange does not mandate external certification. Instead, the [Wardleymaps.ai training pathway](https://www.wardleymaps.ai/training) serves as a **reference map** for an athlete's development. 
*   A Year 1 volunteer operates at the *Awareness* level.
*   A Year 2 active mapper is doing the work of the *Foundation* level.
*   A Year 4 Map Lead is operating at the *Practitioner/Expert* level.

The athlete does not study to pass these levels; they achieve these levels as a byproduct of running sessions. The platform provides the formal vocabulary for what they already know how to do.

---

## The Public Record: Wardley Map Repository

**Platform:** [github.com/swardley/WARDLEY-MAP-REPOSITORY](https://github.com/swardley/WARDLEY-MAP-REPOSITORY/tree/main)

The Wardley Map Repository is the global open research archive for the mapping community. It contains maps across dozens of domains, including education, healthcare, finance, government, and defence.

**How The Exchange connects to it:**
Maps produced in Exchange sessions are written in the exact same plain-text format used throughout the repository. This means any map produced by an athlete and verified by a TAC is natively compatible with the global archive.

This is an option, not a requirement. An athlete who maps a healthcare provider has created something that belongs in the healthcare folder of the repository. Contributing it makes their work publicly verifiable and connects their portfolio to a recognized global research standard.

---

## Map Format

All maps in the repository — and all maps produced in Exchange sessions — use a simple plain-text format. A map file looks like this:

```text
title [Organization Name] — Competitive Landscape
anchor user [0.95, 0.50]
component [capability] [0.70, 0.30]
component [dependency] [0.40, 0.80]
evolve [capability] 0.85
```

No specialist software is required. Any text editor opens it. Any browser-based tool (like onlinewardleymaps.com or MapKeep) renders it visually. This keeps the barrier to participation near zero for athletes, TACs, and partner organizations.

---

## License

The Exchange Protocol is MIT Licensed.  
Session method: Creative Commons — Wardley Mapping by Simon Wardley (CC BY-SA 4.0).  
Maps contributed to the Wardley Map Repository are licensed under CC BY-SA 4.0.
