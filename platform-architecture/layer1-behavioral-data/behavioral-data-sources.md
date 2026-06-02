# Layer 1 — Behavioral Data Sources

## What This Layer Does

Layer 1 is the ingestion foundation of the MindMap platform. It captures population-level behavioral signals from a curated set of public, licensed, and partner data sources and normalises them into a unified signal pipeline that feeds Layer 2 (neural mapping) and Layer 3 (quantum ML engine).

MindMap does **not** ingest raw individual query data. It uses **indexed, population-level behavioral signals** — aggregate trends, not personal records.

---

## Primary Data Sources

### 1. Google Trends
- **Role:** Backbone of the behavioral signal pipeline (~38% of total signal weight)
- **Scale:** 136 billion searches/month; 20-year historical archive; 230 countries; 90 languages
- **Access model:** Population-level indexed signals via the Google Trends API (currently in active alpha, signalling commercial intent); supplemented by licensed data partners
- **Key precedent:** Ginsberg et al. (2009), *Nature* — Google Trends signals achieved a **0.97 correlation** with CDC influenza surveillance data, with a **1–2 week lead time** ahead of official reporting
- **What it captures:** Search volume trends by topic, geography, and time — a real-time proxy for what populations are thinking, fearing, and wanting
- **Important framing:** MindMap uses population-level behavioral signals indexed from Google Trends — not raw query data, not individual tracking

### 2. ICD-10 Claims & Diagnostic Codes
- **Role:** Clinical anchor layer — maps behavioral signals to verified health outcomes
- **Scale:** Covers all major insurance and health system claims globally
- **Use:** Validates that behavioral signals (Layer 1) correlate with downstream clinical events (Layer 3 output)
- **Partners:** Insurance co-development partners (AXA, Swiss Re) contribute claims data during pilot

### 3. PubMed / Academic Literature Signals
- **Role:** Scientific validation layer — ensures behavioral indicators map to peer-reviewed biomarkers
- **Scale:** 35M+ citations; updated continuously
- **Use:** Cross-references MindMap signal definitions with published clinical literature

### 4. WHO Global Sentinel Surveillance
- **Role:** Public health ground truth layer
- **Scale:** 194 member states; standardised disease surveillance
- **Use:** Validates population health signal accuracy for the public health vertical (H3)

### 5. Social Signal APIs
- **Role:** Supplementary behavioral signal layer
- **Sources:** Licensed social media signal APIs (aggregated, anonymised, population-level)
- **Use:** Adds behavioral texture beyond search intent — conversation volume, sentiment polarity, topic velocity
- **Important:** No individual-level data; consent architecture applied at source

### 6. Insurance Claims Data (Co-Development Partner Contribution)
- **Role:** Outcome validation for the insurance vertical
- **Partners:** AXA, Swiss Re (H1 pilot)
- **Use:** Trains the behavioral claims prevention model by linking behavioral signals to historical claims outcomes
- **Governance:** Strict data sharing agreement; aggregated; no individual policyholder tracking

---

## Signal Pipeline Architecture

```
Raw Behavioral Signal Sources
        |
        v
  Signal Normalisation Layer
  (indexed, aggregated, anonymised)
        |
        v
  Topic Taxonomy Mapping
  (health, financial, environmental, social domains)
        |
        v
  Temporal Alignment
  (standardised time series: daily, weekly, rolling 30-day)
        |
        v
  Geographic Segmentation
  (country, region, city — matched to insurer/pharma/gov jurisdiction)
        |
        v
  Output: Normalised Behavioral Signal Feed → Layer 2
```

---

## Data Volume & Scale

| Source | Monthly Signal Volume | Historical Depth | Geographic Coverage |
|---|---|---|---|
| Google Trends (indexed) | 136B searches/month basis | 20 years | 230 countries, 90 languages |
| ICD-10 Claims | Partner-contributed | Rolling 5-year | 11+ European countries (pilot) |
| PubMed | 35M citations | Full archive | Global |
| WHO Sentinel | 194 member states | 15+ years | Global |
| Social Signal APIs | Licensed volume | Rolling 2-year | Global (filtered by pilot jurisdiction) |

---

## Why This Layer Is the Moat Foundation

The behavioral data layer is where MindMap's competitive advantage begins to compound:

- **Volume:** 136B monthly searches is the largest behavioral dataset ever assembled
- **History:** 20 years of longitudinal signal allows the model to identify cycles, not just snapshots
- **Breadth:** 230 countries, 90 languages means the model generalises globally — not just English-speaking markets
- **Neutrality:** MindMap is a neutral broker between data and industry — it does not own the data, it owns the **intelligence layer on top of it**
- **Compounding:** Every dataset added improves model accuracy; every industry pilot adds validated outcome data that no competitor can replicate

No pharma company, insurer, or government has built this integration. Google has the data but faces antitrust restrictions on exclusive vertical productisation. MindMap occupies the gap.

---

## Key Citation

> Ginsberg, J. et al. (2009). *Detecting influenza epidemics using search engine query data.* Nature, 457, 1012–1014.
> — Demonstrated 0.97 correlation between Google search trends and CDC flu surveillance, with 1–2 week predictive lead time. This is the empirical foundation for MindMap's behavioral signal thesis.

---

## H1 Implementation Plan

- **Month 1–2:** Google Trends API integration (alpha access); ICD-10 data pipeline from insurance co-development partner
- **Month 3:** WHO Sentinel feed live; social signal API licensed and normalised
- **Month 4–6:** Full signal taxonomy mapped across health, financial, and environmental domains
- **Month 6:** Normalised behavioral signal feed handed off to Layer 2 (neural mapping)

---

*Part of the MindMap 3-Layer Behavioral Intelligence Infrastructure. See `platform-architecture/mindmap-overview.md` for full platform context.*
