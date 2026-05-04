# Repo Map — MindMap Project

This document tells you **where to find what** in the Frontier_Tech repo for the MindMap project.

---

## 1. High-Level Overview

- `README.md`
  - What MindMap is
  - Three industries (Pharma, Insurance, Public Health)
  - Team structure and decisions locked as of 2026-05-04

- `docs/`
  - `project-evolution.md` — how the idea evolved from first insight → Vision 1 vs 2 → three verticals → pharma anchor → insurance/public health reframes → rename to MindMap

- `group-presentation/`
  - `script.md` — 6-slide script for the group deck, fully aligned to MindMap and confirmed industry choices
  - `decision-log.md` — group-level decisions (what was decided, when, and why)

- `individual/`
  - `pharma/decisions.md` — decisions specific to the pharma vertical
  - `insurance/decisions.md` — decisions specific to the insurance vertical
  - `public-health/decisions.md` — decisions specific to the public-health vertical

- `research/`
  - Core research and stress tests supporting the project

- `platform-architecture/`
  - `mindmap-overview.md` — technical view of MindMap (three layers + how each vertical uses them)

---

## 2. Group Presentation Content

**Goal:** understand everything needed to build and defend the 6–10 slide group deck.

- Start here:
  - `README.md` — one-paragraph explanation of MindMap and the three industries
  - `group-presentation/script.md` — slide-by-slide story

- For "why this structure?" questions:
  - `group-presentation/decision-log.md` — when and why we chose three verticals, pharma as anchor, secret pilot logic, etc.
  - `docs/project-evolution.md` — chronological story of how the idea evolved

- For detailed backing for each industry:
  - `research/stress-tests/pharma-stress-test.md`
  - `research/stress-tests/insurance-stress-test.md`
  - `research/stress-tests/public-health-stress-test.md`

---

## 3. Individual Reports

Each teammate's individual report is anchored in one vertical. Use these files:

- **Pharma (Lead)**
  - `individual/pharma/decisions.md` — all key choices for the report (entry customer, product, business model)
  - `research/stress-tests/pharma-stress-test.md` — deeper reasoning and objections addressed
  - `platform-architecture/mindmap-overview.md` — tech explanation for the platform section

- **Insurance (Teammate 2)**
  - `individual/insurance/decisions.md` — all key choices (secret pilot, entry product correction, misalignment fixed)
  - `research/stress-tests/insurance-stress-test.md` — full stress test logic
  - `platform-architecture/mindmap-overview.md` — explanation of how MindMap feeds insurance models

- **Public Health (Teammate 3)**
  - `individual/public-health/decisions.md` — key choices (electoral intelligence framing, regulation advantage)
  - `research/stress-tests/public-health-stress-test.md` — full stress test logic
  - `platform-architecture/mindmap-overview.md` — explanation of how MindMap feeds public health use case

---

## 4. Research and Evidence

To support claims in slides and reports:

- `research/core-project-sources.md`
  - Core deep research (AI ROI, brain mapping, quantum ML, cybersecurity/regulation)

- `research/industry-pain-points.md`
  - Real industry pain points in banking, pharma, logistics, industrial/energy

- `research/cybersecurity-opportunities.md`
  - How cybersecurity becomes a core product opportunity (AI, XR, blockchain, quantum)

- `research/frontier-research-sources.md`
  - Where to find frontier research across AI, AR/VR, blockchain, quantum, cybersecurity

- `research/underexplored-intersections.md`
  - Intersections between frontier tech and industries not yet fully exploited

- `research/stress-tests/`
  - Detailed reasoning for pharma, insurance, public health vertical choices

---

## 5. Platform and Technology

- `platform-architecture/mindmap-overview.md`
  - Three layers of MindMap: behavioral data, quantum ML, cybersecurity
  - How each industry vertical uses the same platform
  - Three Horizons roadmap (H1, H2, H3)
  - Key research anchors

Use this file (`docs/repo-map.md`) as the starting point for anyone new to the project or any teammate trying to understand where to find a specific piece of reasoning.
