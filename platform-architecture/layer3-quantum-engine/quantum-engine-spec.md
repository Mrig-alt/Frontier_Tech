# Layer 3 — Quantum-ML Engine

## What This Layer Does

Layer 3 is the prediction engine. It takes the structured behavioral feature vectors from Layer 2 and evaluates them using a hybrid quantum-classical machine learning architecture to produce forward-looking probability scores for each industry vertical.

This is where MindMap's core computational advantage sits.

---

## Why Quantum ML — Not Just Classical ML

Classical ML finds patterns in samples. It is exceptionally good at identifying correlations in historical data and extrapolating them forward.

Quantum ML evaluates **combinatorial interactions** — it can simultaneously assess how multiple variables interact with each other across the full solution space, not just along the dimensions a classical model was trained to recognise.

### Concrete Example

A classical actuarial model prices hurricane risk by looking at:
- Historical storm frequency in a region
- Property values
- Proximity to coastline

A quantum model simultaneously evaluates:
- Storm trajectory + infrastructure vulnerability + supply chain disruption + business interruption exposure + population health response + secondary flood risk + reinsurance cascade effects

These are not independent variables — they interact. Quantum computing evaluates those interactions across the full combinatorial space. That is a fundamentally different question from what classical ML answers.

---

## Core Hardware: Google Willow

| Specification | Detail |
|---|---|
| **Name** | Google Willow |
| **Owner** | Google Quantum AI |
| **Announced** | December 2024 |
| **Qubits** | 105 |
| **Architecture** | Hybrid quantum-classical |
| **Key capability** | Error correction at scale; combinatorial inference |

> ⚠️ **Correction note:** Google Willow is a **Google** chip, announced December 2024 by Google Quantum AI. It is not an IBM product. Any reference to "IBM Willow" anywhere in project materials is incorrect and must be updated.

---

## Three-Horizon Hardware Roadmap

| Horizon | Timeframe | Approach | Status |
|---|---|---|---|
| H1 | Now – mid 2026 | Quantum-inspired algorithms on classical hardware | Available today |
| H2 | 2026 – 2027 | IBM Quantum enterprise access programs for scaling | Available via partnership |
| H3 | 2028+ | Full quantum as hardware matures (Google Willow + successors) | Hardware maturing |

The H1 approach uses quantum-inspired algorithms — classical algorithms that mimic quantum computational approaches — to deliver meaningful performance improvements over standard ML while full quantum hardware access is being secured. This is not a compromise; it is the standard commercial deployment path for enterprise quantum ML in 2026.

---

## Output by Vertical

| Vertical | Layer 3 Output |
|---|---|
| **Insurance** | Behavioral risk scores; forward-looking claims probability; anomaly flags for prevention intervention |
| **Pharma** | Trial success probability by behavioral cohort; patient response classification; recruitment targeting scores |
| **Public Health** | Outbreak probability by region; population sentiment index; policy response modelling |

---

## Why No Competitor Has This Layer

- **IBM** has quantum hardware but no behavioral signal dataset to feed it
- **Palantir** has prediction engines but no quantum ML and no behavioral data
- **Google** has both the Willow hardware and the Trends data — but faces antitrust restrictions on exclusive vertical productisation
- **IQVIA** serves large pharma with classical ML; no quantum engine exists in their stack

MindMap is the only platform that combines the behavioral data (Layer 1), the mapping science (Layer 2), and the quantum-ML processing (Layer 3) in a single integrated architecture.

---

## Chart Reference

**Chart 1 — Three Horizons Roadmap** shows the H1/H2/H3 quantum hardware progression alongside all other platform milestones. **Chart 5 — HNDL Threat vs. MindMap PQC Readiness Timeline** shows where the quantum computing threat intersects with MindMap's security readiness. See `group-presentation/exhibits/` for chart data.
