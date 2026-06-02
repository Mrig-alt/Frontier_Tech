# Layer 1 — Behavioral Data Sources

## What This Layer Does

Layer 1 is the ingestion and indexing layer. It captures population-level behavioral signals from public and licensed data sources and feeds them into MindMap's processing pipeline. This is not raw query data — it is indexed, aggregated behavioral signal output that reflects what populations are searching, fearing, and seeking at scale.

---

## Primary Data Source: Google Trends

**Scale:** 136 billion searches per month across Google's global index  
**History:** 20-year archive (2004–present)  
**Coverage:** 230 countries, 90 languages  
**Access model:** Population-level indexed signals via Google Trends API (currently in active alpha, signaling commercial intent); supplemented by licensed data partners and social signal APIs

### Why Google Trends Is the Backbone

Google Trends does not expose raw queries. It exposes relative search interest indices — normalised signals showing how frequently a given topic is searched relative to total search volume in a given region and time period. This makes it:

- **Privacy-safe by design:** No individual is tracked; only population-level patterns are visible
- **Real-time:** Updated within hours, not weeks
- **Historically deep:** 20 years of comparable signal history
- **Geographically granular:** Country, region, and city-level breakdowns

### Validated Precedent: Ginsberg et al., *Nature* (2009)

Ginsberg et al. demonstrated that Google search index data could predict CDC influenza-like illness (ILI) surveillance data with a **0.97 correlation coefficient** and a **1–2 week lead time** ahead of official CDC reporting. This is the foundational proof that population behavioral signals carry genuine predictive power for health outcomes.

> **Important scope note:** The Ginsberg 2009 finding applies specifically to flu/ILI detection. MindMap extends this logic across broader health, financial, and behavioral signal categories — but the Ginsberg paper is cited only for flu/ILI validation.

---

## Secondary Data Sources

| Source | Signal Type | Use Case |
|---|---|---|
| ICD-10 (WHO) | Clinical diagnosis codes | Mapping behavioral signals to clinical outcomes |
| PubMed / MEDLINE | Peer-reviewed literature | Signal validation and biomarker cross-referencing |
| WHO Sentinel Surveillance | Official epidemiological data | Outbreak early warning baseline |
| Social media APIs (licensed) | Public sentiment signals | Supplementary behavioral trend data |
| Insurance claims data (partner-provided) | Historical claims patterns | Model training and validation for insurance vertical |
| EBRAINS Atlas | Brain activity mapping | Neural-behavioral output correlation (Layer 2 input) |

---

## Data Pipeline Architecture

```
[Google Trends API] ──┐
[ICD-10 / WHO]        ├──► [Signal Normalisation] ──► [Behavioral Index] ──► Layer 2
[PubMed]              |
[Social APIs]         ┘
[Claims Data] ──────────► [Outcome Mapping] ──► [Model Training] ──► Layer 2
```

### Key Pipeline Properties

- **Aggregation-first:** All signals are processed at population level before any industry output is generated. No individual-level tracking.
- **Consent architecture:** For any data beyond public indices, explicit consent and EU AI Act-compliant data governance apply.
- **Differential Privacy:** Applied at ingestion to ensure statistical noise prevents reverse-engineering of individual signals.
- **Latency:** Near-real-time ingestion for Trends signals; daily refresh for clinical and claims data.

---

## Why No Competitor Has This Layer

- **Google** holds the raw data but faces antitrust restrictions on exclusive vertical productisation
- **IBM / Palantir** have no behavioral signal pipeline at this scale
- **IQVIA** has pharma data but no cross-vertical behavioral intelligence layer
- **Traditional insurers** have claims data but zero real-time behavioral signal ingestion

Remove Layer 1 and the entire platform has nothing to process. It is the foundation.

---

## Chart Reference

**Chart 6 — Layer 1 Data Source Mix** shows Google Trends as the backbone at 38% of the behavioral signal pipeline. See `group-presentation/exhibits/` for chart data.
