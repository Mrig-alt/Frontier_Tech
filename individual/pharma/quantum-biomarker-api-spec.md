# Quantum ML Biomarker API — Technical Specification

## Overview

The Quantum ML Biomarker API is a licensable REST API that delivers probability-weighted patient cohort targeting scores for pharma trial sponsors. It is the primary commercial product of MindMap's pharma vertical.

---

## API Architecture

```
Pharma Sponsor Trial Management System
            |
            v
    MindMap Quantum ML Biomarker API
            |
     +------+------+
     |             |
     v             v
Layer 1          Layer 2
Behavioral       Neural Mapping
Data Pipeline    & Biomarker
                 Cross-Reference
     |             |
     +------+------+
            |
            v
     Layer 3: Quantum ML
     Combinatorial Inference
     (Google Willow / quantum-inspired)
            |
            v
     API Response:
     - Cohort probability scores
     - Geographic heat maps
     - Temporal signal windows
     - Trial site recommendations
```

---

## Endpoint Specification (H2)

### POST /v1/cohort-score
Returns probability-weighted cohort targeting scores for a given trial indication.

**Request body:**
```json
{
  "indication": "MDD",
  "trial_phase": "Phase_II",
  "geographies": ["DE", "FR", "ES", "NL"],
  "signal_window_days": 90,
  "inclusion_criteria": {
    "age_range": ["18-65"],
    "prior_treatment": ["SSRI_failure"]
  }
}
```

**Response:**
```json
{
  "request_id": "uuid",
  "generated_at": "ISO8601",
  "cohort_scores": [
    {
      "geography": "DE",
      "region": "Bavaria",
      "probability_score": 0.84,
      "signal_confidence": "high",
      "estimated_eligible_population": 12400,
      "signal_window_peak": "2026-07-15"
    }
  ],
  "recommended_trial_sites": [
    {
      "site_id": "DE_MUN_01",
      "catchment_score": 0.91,
      "rationale": "Highest behavioral signal concentration for MDD indication in signal window"
    }
  ]
}
```

### GET /v1/signal-map
Returns a real-time behavioral signal heat map for a given indication and geography.

### GET /v1/temporal-window
Returns the optimal enrollment timing window based on behavioral signal peak prediction.

---

## Privacy & Security Compliance

- All outputs are population-level aggregates: no individual patient data in any API response
- Differential privacy applied: ε-budget managed per client per query period
- All data in transit: NIST FIPS 203 (CRYSTALS-Kyber) post-quantum encryption
- Authentication: FIPS 204 (CRYSTALS-Dilithium) digital signatures
- Audit log: every API call logged immutably for GDPR Article 30 compliance
- Data processing agreement: required before API access granted

---

## Integration Targets

| Platform | Integration Type | Status |
|---|---|---|
| Medidata Rave | REST API plugin | H2 target |
| Veeva Vault Clinical | REST API plugin | H2 target |
| Oracle Clinical One | REST API plugin | H2 target |
| Custom trial sponsor systems | Direct REST API | Available H1 pilot |

---

## Pricing Model (H2)

| Tier | Description | Price |
|---|---|---|
| Pilot | Single indication, 1 geography, 90-day signal window | $50K flat |
| Standard | Up to 3 indications, 5 geographies, 12-month access | $200K/year |
| Enterprise | Unlimited indications, global, full temporal window access | $500K+/year |

---

*Technical specification for the Quantum ML Biomarker API. See `individual/pharma/pharma-report.md` for the full strategic report.*
