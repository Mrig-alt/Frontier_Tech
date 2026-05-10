# Aurora Insurance — Scenario and Incident Analysis

**Classification:** Research context for MindMap insurance vertical  
**Use:** Informs Layer 4 architecture decisions and individual report framing  
**Do not reference Aurora by name in external MindMap materials**

---

## Organisation Context

| Attribute | Detail |
|---|---|
| Name | Aurora Insurance |
| Sector | Life and health insurance, adjacent reinsurance |
| Size | 5,200 employees, 8 million policyholders, 11 European countries |
| AUM | €18 billion |
| HQ | Amsterdam, with offices in Munich, Madrid, Warsaw |
| Products | Term life, whole-life, private health, chronic condition specialists, B2B group life/health, AuroraVitality wellness app |
| Tech stack | Hybrid Azure/private cloud, ML-driven underwriting, behavioral signal ingestion, early quantum-classical portfolio optimization |

## What Made Aurora Valuable — and Vulnerable

Aurora had built a competitive moat out of behavioral data. While the rest of the European life and health market was still arguing about whether to use credit bureau data, Aurora had been training ML models on aggregated, opt-in digital behavior signals — search trends, app usage, fitness tracker data — for nearly a decade. By 2025, their underwriting was 18% more accurate than the market average.

That moat was the problem. The more sensitive and long-lived the data, the more valuable it is to a patient attacker. Aurora's genetic profiles, HIV status records, mental health claims, and behavioral histories were exactly the kind of data worth waiting years to decrypt. The competitive advantage and the attack surface were the same thing.

## The Incident

**When the breach actually happened:** Late 2023. A cloud engineer's privileged credentials were compromised through a targeted phishing operation. Over four months, an attacker exfiltrated approximately 1.2 TB of encrypted data — claims files, behavioral profiles, genetic test results — along with associated metadata. The exfiltration was deliberately slow and low-volume to stay below volumetric detection thresholds. Classic advanced persistent threat behavior.

**What the attacker did with it:** Nothing, immediately. The data was stored. The attacker waited.

**When it became public:** April 2026. A forum post appeared with a sample of Aurora customer data — encrypted, but with metadata intact. Claim IDs, policy types, dates. Aurora confirmed the data was real. Three weeks later, the same actor posted again — this time with partial decryption. Tens of thousands of records, including HIV status, therapy notes, genetic predisposition data, and behavioral profiles linking individuals to specific search histories, appeared on paste sites. The message: *"We harvested two years ago. We waited. Now you understand."

**The press call the next morning had one question. The CFO didn't have an answer.**

## Why AES-256 Wasn't the Problem

A common misreading of this incident is that the encryption failed. It didn't — not in the classical sense. AES-256 was not broken. What likely occurred was one of two things:

1. A quantum-assisted attack on the **key exchange mechanism** (RSA/ECC used during key establishment, not AES itself). The cipher was fine. The handshake was vulnerable.
2. A side-channel compromise of key material that the investigation didn't catch.

This distinction matters for MindMap. The lesson is not "use stronger encryption." The lesson is that **long-lived sensitive data under classical key exchange is an HNDL target by design**. The data should either not exist in identifiable form by the time quantum decryption is viable, or it should be under hybrid PQC schemes from the start.

## Why the CISO Was Right and Ignored

The CISO had been warning the board about quantum risk for two years. The board allocated €4M to a post-quantum readiness assessment — due to start in Q3 2026. It never started.

The failure wasn't technical incompetence. It was a **risk perception gap**:
- The threat felt distant and probabilistic
- The CFO framed cryptographic infrastructure as a cost center, not a liability
- The business case for ML underwriting was concrete and revenue-generating; the case for PQC readiness was abstract and defensive
- No one at board level had accountability for the gap between the CISO's warning and a budget decision

By early 2026, ENISA had been issuing PQC guidance since 2021. NIST finalized its PQC standards (FIPS 203, 204, 205) in August 2024. The EU Commission's PQC roadmap required member states to begin national strategies by December 2026. Aurora's Q3 assessment was already behind the regulatory curve, not just the threat curve.

**The €4M deferred became a €180M–€460M liability.** See `cost-of-inaction.md` for the full arithmetic.
