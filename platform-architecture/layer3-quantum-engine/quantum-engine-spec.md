# Layer 3 — Quantum ML Engine

## What This Layer Does

Layer 3 is the inference engine of the MindMap platform. It takes structured behavioral indicators from Layer 2 and runs combinatorial inference at a scale and depth that classical machine learning cannot match — producing probability-weighted predictive outputs for each industry vertical.

This is where behavioral signals become **actionable predictions**: trial success probabilities for pharma, behavioural risk scores for insurers, outbreak early warnings for public health.

---

## Why Quantum ML — Not Classical ML

Classical ML (XGBoost, neural networks, regression) finds patterns in historical samples. It is excellent at recognising what has happened before.

Quantum ML evaluates **combinatorial interactions** — it asks a fundamentally different question: *what is the probability distribution across all possible combinations of signals firing simultaneously?*

### The Insurance Example
A classical model prices hurricane direct property damage based on historical claims.

A quantum model simultaneously evaluates:
- Storm track probability
- Infrastructure failure cascades
- Supply chain disruption knock-ons
- Population displacement patterns
- Business interruption timelines
- Secondary health claim spikes
- Regional economic stress amplification

All of these interact. Classical ML linearises them. Quantum ML holds the full combinatorial space open.

### The Pharma Example
A classical model identifies patients who match historical trial profiles.

A quantum model simultaneously evaluates:
- Which behavioral signal clusters predict treatment response
- How those clusters interact with genetic and lifestyle indicators
- Which combinations are predictive vs. confounded
- How the signal combination shifts across geographies and time periods

This is not a marginal improvement in accuracy. It is a different class of question.

---

## Hardware: Google Willow

- **Owner:** Google Quantum AI
- **Announced:** December 2024
- **Qubits:** 105
- **Mode:** Hybrid quantum-classical
- **Key capability:** Error correction at scale — Google Willow demonstrated that adding more qubits *reduces* error rates, solving a fundamental challenge that had blocked practical quantum ML
- **Relevance to MindMap:** Willow's hybrid architecture is designed for exactly the class of combinatorial optimisation problems MindMap requires

> **Correction note:** All references to "IBM Willow" in earlier deck versions are incorrect. Willow is **Google's** chip. IBM's quantum platform is used separately for enterprise access in H2. There is no chip called "IBM Willow."

---

## Implementation Roadmap: Three Phases

### H1 — Quantum-Inspired on Classical Hardware (Now → mid-2026)
- **What:** Quantum-inspired algorithms running on classical hardware
- **Why:** Full quantum hardware is not yet production-ready for enterprise workloads at scale
- **How:** Tensor network methods, variational quantum eigensolver (VQE) simulations, and quantum annealing approximations run on GPU clusters
- **Output:** Functionally equivalent to quantum ML for the signal volumes in the H1 insurance pilot
- **Cost:** Standard cloud compute (AWS/GCP) — no quantum hardware licensing in H1

### H2 — IBM Quantum Enterprise Access (2026–2027)
- **What:** Run production inference workloads on IBM Quantum's enterprise access program
- **Why:** As signal volume scales with pharma and public health verticals, quantum hardware provides meaningful accuracy and speed improvements over classical simulation
- **How:** IBM Quantum Network enterprise access; MindMap workloads scheduled on available quantum hardware
- **Output:** Pharma trial cohort targeting at full scale; insurance behavioral risk scoring at portfolio level

### H3 — Full Quantum Infrastructure (2028–2030)
- **What:** Dedicated quantum compute access as hardware matures
- **Why:** Google Willow roadmap targets fault-tolerant quantum computing by 2029–2030; MindMap's architecture is designed to scale into this
- **How:** Google Quantum AI partnership or direct enterprise hardware access
- **Output:** Full combinatorial behavioral inference across all three verticals at global scale

---

## Output by Vertical

### Pharma Output: Trial Success Probability Scores
- **Input:** Behavioral signal clusters from Layer 2 matched to trial indication
- **Output:** Probability-weighted cohort scoring — which patient populations show behavioral signals predictive of treatment response
- **Format:** Quantum ML Biomarker API — a licensable classification engine for pharma trial sponsors
- **Validation:** Pharma pilot results published publicly in H2 to establish scientific credibility

### Insurance Output: Behavioral Risk Scores
- **Input:** Behavioral signal clusters from Layer 2 matched to claims history (co-development partner data)
- **Output:** Forward-looking behavioral risk scores by geography, demographic segment, and signal cluster
- **Format:** API integration into insurer's underwriting model (layered on top of existing RPA/XGBoost, not replacing it)
- **Use:** Claims prevention, not premium discrimination — consent-based, aggregated, regulatory safe by design

### Public Health Output: Outbreak Early Warning & Population Sentiment
- **Input:** Behavioral signal clusters from Layer 2 matched to disease surveillance data (WHO Sentinel)
- **Output:** Outbreak probability scores by region; population sentiment dashboards in real time
- **Format:** Dashboard API for public health agencies (ECDC, EU Commission, NHS, WHO)
- **Lead time:** Targets 1–2 week early warning ahead of official surveillance reporting (validated by Ginsberg 2009 precedent)

---

## Competitive Position

| Capability | MindMap | IBM Watson Health | Palantir | IQVIA.ai |
|---|---|---|---|---|
| Behavioral signal layer | ✅ | ❌ | ❌ | ❌ |
| Quantum ML inference | ✅ | ⚠️ (hardware only, no behavioral data) | ❌ | ❌ |
| Multi-vertical platform | ✅ | ❌ | ❌ | ❌ |
| Post-quantum security | ✅ | ❌ | ❌ | ❌ |
| EU AI Act compliance | ✅ | ⚠️ | ❌ | ❌ |

**IBM has the quantum hardware but no behavioral dataset. MindMap has the behavioral dataset and the quantum ML layer. Remove either and the product does not exist.**

---

## Key Technical Specs Summary

| Parameter | Spec |
|---|---|  
| Primary quantum hardware | Google Willow (105 qubits, hybrid quantum-classical) |
| H1 interim approach | Quantum-inspired algorithms on classical GPU infrastructure |
| H2 scale approach | IBM Quantum enterprise access |
| Inference type | Combinatorial optimisation; forward probability distribution |
| Primary ML paradigm | Hybrid quantum-classical variational circuits |
| Output format | Probability-weighted industry indicator scores via API |
| Latency target (H2) | Sub-hour batch inference; real-time streaming for public health |

---

*Part of the MindMap 3-Layer Behavioral Intelligence Infrastructure. See `platform-architecture/mindmap-overview.md` for full platform context.*
