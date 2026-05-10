# Aurora Insurance — Regulatory and Legal Exposure

**Purpose:** Documents the regulatory and legal framework that applied to Aurora, and that will apply to any behavioral signal insurance platform operating in the EU. This directly informs MindMap's compliance architecture.

---

## GDPR (General Data Protection Regulation)

**Articles in play:** 5 (data minimisation principle), 25 (data protection by design and default), 32 (appropriate technical measures), 33 (72-hour breach notification to supervisory authority), 34 (direct notification to affected individuals when high risk).

**Key exposure:** The breach involved special-category data — health, genetic, sexual orientation (via HIV status) — across 11 EU countries. GDPR Article 32 requires "appropriate technical and organisational measures." Regulators can argue that AES-256 without post-quantum key protection was not appropriate given ENISA guidance available since 2021 and NIST PQC standards finalised in August 2024.

**Maximum fine:** 4% of annual global turnover. At Aurora's scale (~€1.5B annual premium revenue), that is approximately €60M — before litigation.

**Lead supervisory authority:** Dutch DPA (Autoriteit Persoonsgegevens), given Aurora's Amsterdam HQ.

**Genetic data:** Carries the highest protection tier under GDPR. Its exposure — combined with behavioral profiles linking individuals to specific search histories — creates individual harm that is permanent and irreversible. Regulators treat this with maximum severity.

---

## DORA (Digital Operational Resilience Act)

**Article 9:** ICT risk management for financial entities must account for quantum threats to cryptography. Aurora's hybrid Azure/private cloud setup and reliance on third-party data brokers compounds the third-party risk exposure under DORA. The insurer is not shielded by a vendor's failure to be PQC-ready.

---

## NIS2 Directive

Aurora operates critical infrastructure — insurance is explicitly in scope. Incident reporting to national CERTs across all 11 countries must occur within 24 hours of becoming aware of a significant incident. Parallel to GDPR notification, not a replacement for it.

---

## 2026 Legal Precedent

A 2026 Delhi High Court case (a HealthTech class action) established that companies can be sued today for failing to adopt NIST PQC standards, because the standards exist and the threat is known. EU courts are expected to follow similar logic, given ENISA's published warnings. This removes the "standards didn't exist" defence that earlier breaches could rely on.

---

## Cyber Insurance

As of 2026, insurers are actively adding quantum exclusion clauses to cyber insurance policies. Aurora may find that its own cyber coverage is inadequate for the exact liability it now faces — a compounding problem where the breach triggers costs that the policy no longer covers.

---

## MindMap Implication

Every regulatory requirement above applies to any behavioral signal insurance platform operating in the EU. MindMap's Layer 4 is designed to satisfy GDPR Articles 5, 25, and 32 by default. PQC compliance addresses DORA Article 9. Audit logging and incident response protocols address NIS2. These are not additions for regulatory comfort — they are the baseline for operating in this market.
