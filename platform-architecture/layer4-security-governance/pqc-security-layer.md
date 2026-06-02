# Layer 4 — Post-Quantum Security & Governance

## What This Layer Does

Layer 4 is the commercial prerequisite of the MindMap platform. It is not a feature — it is the reason regulated industries can sign the contract.

Health insurers handle genetic profiles, mental health records, and behavioral histories. Pharma companies handle trial data, patient cohorts, and proprietary biomarker models. Governments handle population-level sentiment and public health intelligence. **None of these entities will share data with a platform that cannot guarantee quantum-safe security and regulatory compliance.**

Layer 4 solves that problem. It is MindMap's deepest competitive moat — the layer that Big Tech cannot credibly own because they are the threat.

---

## The Threat: Harvest Now, Decrypt Later (HNDL)

### What HNDL Is
Adversaries are **already stealing** encrypted data today — at scale, systematically, and patiently — with the intent to decrypt it once quantum hardware is powerful enough to break current encryption standards.

This is not a future threat. It is happening now.

### The Timeline
- **Today:** RSA-2048 and AES-256 (current industry standards) are secure against classical computers
- **2027–2030:** Quantum hardware reaches the threshold where these standards become vulnerable
- **2030:** NIST and US federal mandate deadline for critical systems to be quantum-safe
- **The gap:** Any sensitive data encrypted today that is also stolen today will be decryptable within the HNDL window

### Why Insurers and Pharma Are at Highest Risk
- **Insurance:** Policyholder genetic profiles, mental health records, behavioral histories — the most sensitive personal data class; targeted by HNDL attackers specifically because the data is long-lived and high-value
- **Pharma:** Proprietary trial data, biomarker IP, patient cohorts — competitive intelligence worth billions
- **Both:** Operate under GDPR, HIPAA, and emerging neural data regulations — a post-quantum breach triggers regulatory liability on top of competitive harm

---

## The Regulatory Framework

### NIST Post-Quantum Cryptography Standards
- **FIPS 203** (ML-KEM / CRYSTALS-Kyber): Key encapsulation mechanism — replaces RSA for secure key exchange
- **FIPS 204** (ML-DSA / CRYSTALS-Dilithium): Digital signature algorithm — replaces RSA/ECDSA for authentication
- **FIPS 205** (SLH-DSA / SPHINCS+): Stateless hash-based digital signature — secondary signature standard
- **Status:** Finalised by NIST; these are the global standard for post-quantum cryptographic migration

### Quantum Computing Cybersecurity Preparedness Act (2022)
- **Jurisdiction:** United States federal law
- **Status:** Signed into law; 4 years in force as of 2026
- **Mandate:** Federal agencies must inventory cryptographic systems and develop migration plans to NIST PQC standards
- **Industry implication:** Any company operating with US federal contracts, US-regulated financial data, or US healthcare data must be on a PQC migration path

### 2030 Critical Systems Deadline
- All critical infrastructure and high-sensitivity data systems must be quantum-safe by 2030
- Insurance and pharma data systems are explicitly in scope
- **MindMap is ahead of this deadline by design — not retrofitting, already there**

### EU AI Act (2024)
- Cognitive and behavioral data is classified as sensitive; systems processing it require:
  - Explicit consent architecture
  - High-risk AI system documentation
  - Human oversight mechanisms
  - Transparency and explainability requirements
- MindMap's consent architecture and population-level aggregation are designed to comply from day one

### US MIND Act
- Neural data sovereignty legislation
- Restricts commercial use of individual neural and cognitive data
- MindMap uses population-level indexed signals — compliant by design

### EU Digital Services Act (DSA, 2025)
- Large platforms must assess and mitigate mental harm from algorithmic outputs
- MindMap outputs are B2B intelligence, not consumer-facing — outside direct DSA scope; monitored for downstream use by clients

---

## MindMap's Security Architecture

### 1. Post-Quantum Encryption (NIST FIPS 203/204/205)
- All data in transit encrypted with CRYSTALS-Kyber (FIPS 203) key encapsulation
- All authentication via CRYSTALS-Dilithium (FIPS 204) digital signatures
- No legacy RSA or ECDSA in production systems
- Crypto-agile architecture: algorithm swap possible without full system rebuild as standards evolve

### 2. Zero-Trust Architecture
- No implicit trust for any user, device, or network segment
- Every access request verified: identity + device + context + task scope
- Least-privilege access: every role scoped to minimum required permissions
- Access expires when the task is complete — no standing, open-ended permissions
- Directly addresses the single-credential blast-radius failure pattern seen in major insurance breaches

### 3. Differential Privacy
- All population-level outputs are differentially private: mathematical guarantee that no individual can be re-identified from aggregate signals
- Privacy budget managed per query: prevents adversarial reconstruction through repeated queries
- Standard: ε-differential privacy (epsilon budget set conservatively for regulated industry clients)

### 4. Consent Architecture
- All behavioral signal data processing requires explicit, documented consent at source
- Consent audit trail maintained immutably for regulatory inspection
- Data minimisation by design: only signals required for the specific analytical task are processed
- Deletion timelines built into architecture: signals expire when purpose is fulfilled

### 5. Regulatory Audit Trail
- Every inference run, data access event, and model output is logged immutably
- GDPR Article 30 Records of Processing Activities maintained automatically
- Incident response playbook embedded in platform operations (not a side document)

---

## The Two-Track Insurance Pitch

The security layer is the key to MindMap's insurance market entry strategy. It enables a two-track pitch to AXA and Swiss Re:

### Track 1 — Defend (Immediate Revenue)
> "You have sensitive policyholder data that is being targeted by HNDL attackers right now. You have a 2030 deadline. We can migrate your most sensitive data assets to quantum-safe encryption. This is the CISO's problem today — we solve it."

- No behavioral data sharing required
- Immediate compliance value
- Entry point: CISO signs off, MindMap is in the door
- Revenue: Professional services + PQC migration licensing
- Timeline: H1 2026

### Track 2 — Offend (H1 Pilot, Builds the Moat)
> "Once the house is secure, let's build the advantage. A behavioral claims prevention study — consent-based, aggregated signals, Life & Health first. By the time competitors realise what you've built, the model is three years ahead of them."

- Requires Track 1 trust established first
- Behavioral pilot: claims prevention, not premium discrimination
- 3-year proprietary data advantage built in secret
- Timeline: H1 pilot → H2 underwriting model → Scale 2027

---

## Why Big Tech Cannot Own This Layer

| Player | Why They Cannot Credibly Own This |
|---|---|
| Google | They are the source of the behavioral data — regulated industries will not let Google hold both the data and the security key |
| Microsoft / Azure | Too closely tied to US government surveillance infrastructure for EU regulated clients |
| AWS | Same sovereign concern; no neutral broker positioning |
| Traditional Cybersecurity Firms | Have the security expertise but not the behavioral data layer or the industry domain knowledge |

**MindMap is the neutral broker.** It does not own the underlying data. It owns the intelligence layer and the security architecture that makes regulated industries trust it.

---

## Certification Roadmap

| Certification | Target | Status |
|---|---|---|
| SOC 2 Type II | H2 2027 | Planned |
| ISO 27001 | H2 2027 | Planned |
| GDPR Article 25 (Privacy by Design) | H1 2026 | Built into architecture |
| NIST PQC FIPS 203/204/205 | H1 2026 | Implemented |
| EU AI Act High-Risk System Documentation | H1 2026 | In preparation |

---

*Part of the MindMap 3-Layer Behavioral Intelligence Infrastructure. See `platform-architecture/mindmap-overview.md` for full platform context.*
