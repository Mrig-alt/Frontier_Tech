# Aurora Insurance — Scenario and Incident Analysis

**Purpose:** Market context for MindMap's insurance vertical. Aurora is a behavioral signal insurance platform that failed due to the absence of adequate security architecture. This document establishes what happened, why it matters, and what it confirms about the insurance vertical opportunity.

---

## Organisation Context

| Attribute | Detail |
|---|---|
| Name | Aurora Insurance |
| Sector | Life and health insurance, adjacent reinsurance |
| Size | 5,200 employees, 8 million policyholders across 11 European countries |
| Assets | €18B under management |
| HQ | Amsterdam, with major offices in Munich, Madrid, Warsaw |
| Data held | Health claims, genetic test results, HIV status, mental health records, behavioral profiles (search trends, app usage, wearable data) |
| Technology | ML-driven underwriting on behavioral signals; hybrid Azure/private cloud; AuroraVitality opt-in wellness app |

Aurora was, until the breach, considered a market leader. Their ML underwriting was 18% more accurate than the market average. Their reserves were more capital-efficient. They won a Best Innovation prize from the European Insurance Federation. The CFO and board loved the model.

The CISO had been warning the board about quantum risk for two years.

---

## The Incident

**2023:** A cloud engineer's privileged credentials were compromised through a sophisticated phishing attack. Over four months, an attacker exfiltrated approximately 1.2 TB of encrypted data — claims files, behavioral profiles, genetic test results — along with associated metadata (claim IDs, policy types, dates). The exfiltration was deliberately slow to stay below volume-based detection thresholds. No alert was triggered.

**2023–2026:** The attacker stored the encrypted data and waited. AES-256 encryption was not broken classically. What was attacked was the key exchange mechanism (RSA/ECC used during key establishment) — consistent with emerging quantum-assisted cryptanalysis. The attacker did not need to decrypt in 2023. They needed to wait until the hardware existed.

**Early 2026:** Partial decryption capability was demonstrated. A forum post appeared with a sample of Aurora customer data — encrypted, but with readable metadata. Aurora confirmed the data was real.

**Three weeks later:** The full decryption was posted publicly. Genetic profiles, HIV status, mental health claims, behavioral histories linking individuals to specific search histories — all on a paste site. The post was signed: *"We harvested two years ago. We waited. Now you understand."*

**The press call:** The CFO had no answers. The CISO had been right for two years. The board had deferred a €4M assessment into Q3 2026. That decision had already generated the liability before the assessment was even scheduled to start.

---

## Why the CISO Was Right and Ignored

The failure was not technical ignorance. It was a governance misjudgment:

- The threat felt distant and probabilistic. A €4M budget deferral felt like a reasonable commercial decision.
- The CFO framed cryptographic infrastructure as a cost center, not a liability exposure.
- The business case for ML-driven underwriting was concrete and revenue-generating. The case for post-quantum readiness was abstract and defensive.
- ENISA had been issuing formal guidance on PQC integration since 2021. NIST finalised its PQC standards (FIPS 203, 204, 205) in August 2024. Aurora's Q3 2026 assessment was already behind the regulatory curve, not just the threat curve.

The €4M deferred became a €180M–€460M liability. See `cost-of-inaction.md` for the full arithmetic.

---

## What This Confirms for MindMap

Aurora is MindMap's insurance vertical without Layer 4. The data types are identical: behavioral signals, health outcomes, long-retention personal records. The attack surface is identical: a behavioral data platform where the value of the data increases the longer it exists.

The difference is that MindMap's architecture was designed with this failure mode in mind from the start. PQC is not a future upgrade. Data minimisation is not a compliance exercise. Zero-trust access is not a post-breach patch.

Aurora makes the insurance vertical argument concrete. Any insurer considering a behavioral signal partnership will ask about data security. The answer is: we built the platform that Aurora should have been.

---

*Do not reference Aurora Insurance by name in external MindMap materials or investor decks.*
