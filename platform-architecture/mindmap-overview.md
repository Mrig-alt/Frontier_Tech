# MindMap Platform Architecture Overview

## What MindMap Is

MindMap is a behavioral signal platform. It takes publicly available human behavioral data (Google Trends, social media), processes it through hybrid quantum-ML models, and delivers cognitive intelligence to three industries: Pharma, Insurance, and Public Health.

It is a single platform with three industry entry points — not three separate products.

---

## The Three Layers

### Layer 1: Behavioral Data Layer
- Sources: Google Trends (10–20 years of search signal data), social media emotional signals (Twitter/X, Reddit, Meta platforms)
- What it captures: population-level emotional states, behavioral patterns, search intent signals
- Why Google Trends specifically: Google controls ~80% of global search (136B monthly visits). This is the largest, most consistent behavioral dataset available publicly. It is not a proxy — it IS what people are actually thinking about, in real time.
- Data is aggregated at population level, not individual — this is the privacy and consent architecture

### Layer 2: Quantum ML Layer
- Engine: Hybrid quantum-classical ML (IBM Quantum AI, Willow chip, 1000+ qubits)
- What it does: classifies which behavioral signals from Layer 1 predict specific outcomes in each industry vertical
  - Pharma: which signals predict trial completion / treatment response
  - Insurance: which signals predict claims events / behavioral risk
  - Public Health: which signals predict voter sentiment / policy response
- Why quantum: certain pattern-recognition problems in high-dimensional behavioral data (QUBO-type problems) are better suited to quantum approaches than classical ML at scale
- Key research anchor: IBM + Inclusive Brains BCI joint study (June 2025)

### Layer 3: Cybersecurity Layer
- This is NOT a bolt-on. It is core to why any government or regulated industry would trust MindMap.
- PQC-ready encryption (NIST Post-Quantum Cryptography roadmap)
- Zero-trust architecture
- Differential privacy on population-level data
- Full audit logging (EU AI Act 2026–2027 high-risk classification compliant)
- US MIND Act (2025 proposal) compliance pathway
- The cybersecurity layer is what makes MindMap sellable to pharma (FDA), insurance (FCA / EIOPA), and government (national data laws)

---

## How the Three Verticals Use the Same Platform

| Vertical | Input from MindMap | Output | Customer |
|---|---|---|---|
| Pharma | Behavioral signals predicting trial cohort fit | Cohort targeting score for Phase II CNS trials | Small-to-mid CNS biotech |
| Insurance | Behavioral signals predicting claims events | Behavioral correlation study → claims prevention model | AXA / Swiss Re equivalent |
| Public Health | Behavioral signals predicting voter/citizen sentiment | Population emotional intelligence dashboard | Named government |

---

## Three Horizons Roadmap

**H1 (Now):**
- Pharma: behavioral cohort targeting score for Phase II CNS trials at small CNS biotech
- Insurance: secret internal behavioral correlation pilot at one insurer
- Public Health: population sentiment dashboard pilot for one government

**H2 (12–24 months):**
- Pharma publishes proof of concept; other pharma firms adopt
- Insurance pilot internal results validate; expand to underwriting model
- Public health contracts grow; WHO / EU Commission entry
- Quantum ML biomarker scoring goes live across all verticals

**H3 (24+ months):**
- MindMap becomes the behavioral data standard across pharma, insurance, and public health globally
- Neural circuit layer added (Meta TRIBE v2 neural encoding, Harvard/Google brain activity maps)
- New standard of care for clinical trials, actuarial modeling, and population health policy

---

## Key Research Anchors

- Meta TRIBE v2: 500+ hours fMRI, 700 subjects, 23% improvement in neural encoding over prior methods
- IBM + Inclusive Brains BCI joint study (June 2025): quantum ML classifying neural circuit activation
- Harvard/Google brain activity maps: population-level neural reference data
- EU AI Act (2026–2027): classifies neural data products as high-risk — MindMap's cybersecurity layer is built to this standard
