# Layer 2: Quantum ML Engine

Layer 2 takes the structured behavioral signal vectors from Layer 1 and classifies which patterns predict specific real-world outcomes in each industry vertical. This is where behavioral data becomes behavioral intelligence.

---

## What This Layer Does

It answers the question: *out of all the behavioral signals we are capturing, which ones actually predict something useful for a paying customer?*

For pharma: which signals predict trial completion or treatment response in CNS patients?
For insurance: which signals predict claims events, fraud, or behavioral risk shifts?
For public health: which signals predict voter sentiment change or policy backlash?

---

## Why Quantum ML

Behavioral signal classification at population scale is a high-dimensional pattern recognition problem. The number of possible signal combinations across thousands of keywords, hundreds of geographies, and multi-year time windows creates a combinatorial complexity that classical ML handles poorly at scale.

Quantum approaches — specifically QUBO (Quadratic Unconstrained Binary Optimization) formulations — are better suited to this class of problem. IBM's Willow chip (1000+ qubits) and hybrid quantum-classical architectures allow MindMap to run classification models that would be computationally prohibitive on classical hardware alone.

Key research anchor: IBM + Inclusive Brains BCI joint study (June 2025) — demonstrated quantum ML classifying neural circuit activation patterns from behavioral signal data. This is the scientific precedent MindMap's classification engine is built on.

---

## How It Works

1. Receives signal vectors from Layer 1
2. Runs hybrid quantum-classical classification to identify which signal clusters correlate with target outcomes per vertical
3. Outputs a scored, ranked behavioral signal set — the "behavioral correlation map" — for each vertical
4. Passes output to Layer 3 (security wrapping) before delivery to industry customers

---

## Per-Vertical Classification Outputs

| Vertical | Input Signal | Classification Output | Customer Product |
|---|---|---|---|
| Pharma | Search + social signals in CNS treatment categories | Cohort targeting score — probability of trial fit | Sold to small-to-mid CNS biotech as H1 product |
| Insurance | Search + social signals in health, property, financial anxiety categories | Behavioural risk correlation score — claims event predictor | Sold as internal pilot to one L&H insurer |
| Public Health | Search + social signals in policy, government trust, health anxiety | Population emotional intelligence dashboard — sentiment by region | Sold to named government as pilot dashboard |

---

## The Causal Bridge — The One Unresolved Assumption

MindMap's Layer 2 produces *correlation* between behavioral signals and outcomes. It does not yet prove *causation*.

This is the single most important scientific assumption in the entire platform:
- Does a behavioral signal cluster *predict* a trial dropout because it reflects the same underlying psychological state that causes dropout?
- Or does it merely *correlate* historically without causal mechanism?

The causal bridge is the next major research milestone. It is not needed for H1 commercial pilots — correlation-based products have clear commercial value and precedent (actuarial models are correlation-based). But it is required for H2 regulatory-grade products (FDA-grade trial design, clinical decision support).

This is not a weakness to hide — it is the research roadmap. MindMap's H1 products work without causation. H2 requires it.

---

## Visual Reference
- See: `visuals/chart4-radar.png` — industry readiness scores including Science Maturity dimension
- See: `visuals/chart1-roadmap.png` — three horizons showing when quantum ML goes live across verticals
