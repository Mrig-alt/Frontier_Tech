# Layer 4 — Post-Quantum Security & Governance

## What This Layer Does

Layer 4 is the security and governance envelope that wraps the entire MindMap stack. It is not a feature bolted on after the fact — it is the **commercial prerequisite**. Without it, no insurer signs a data-sharing agreement, no government deploys the platform, and no pharma partner shares trial outcome data.

This layer addresses two simultaneous threats:
1. **The HNDL threat** — adversaries are harvesting encrypted data today to decrypt it post-quantum
2. **The regulatory deadline** — 2030 is the US federal critical systems quantum-safe mandate

---

## The HNDL Threat — Why This Is Urgent Now

**HNDL = Harvest Now, Decrypt Later**

Adversaries (state-level and criminal) are already storing encrypted policyholder records, clinical trial data, and government communications today — with the intent to decrypt them once sufficiently powerful quantum computers are available. The encryption protecting that data today (RSA-2048, ECC) will be breakable by quantum computers within this decade.

This means the breach has **already happened** for organisations that have not migrated to post-quantum cryptography. The data is already in adversary hands. The only question is when the decryption key arrives.

### Why Insurance Is the Most Exposed Vertical

- Insurers hold genetic profiles, HIV status, mental health records, and behavioral histories
- These records are stored for decades (long beyond the useful life of current encryption)
- A single encrypted database stolen today contains 10–30 years of irreversible personal data
- GDPR fines for mishandling health and genetic data: up to 4% of annual global turnover

---

## NIST Post-Quantum Cryptography Standards

The US National Institute of Standards and Technology (NIST) finalised three post-quantum cryptography standards:

| Standard | Algorithm | Purpose |
|---|---|---|
| **FIPS 203** | ML-KEM (Kyber) | Key encapsulation / key exchange |
| **FIPS 204** | ML-DSA (Dilithium) | Digital signatures |
| **FIPS 205** | SLH-DSA (SPHINCS+) | Stateless hash-based signatures |

These replace RSA and ECC as the encryption foundation for sensitive data at rest and in transit. MindMap's architecture is built on FIPS 203/204/205 from day one.

---

## Regulatory Landscape

| Regulation | Jurisdiction | Key Requirement | Relevant to MindMap |
|---|---|---|---|
| **Quantum Computing Cybersecurity Preparedness Act 2022** | United States | Federal agencies must migrate to PQC; critical infrastructure encouraged | Yes — 2030 deadline |
| **NIST PQC Standards (FIPS 203/204/205)** | United States (global influence) | PQC migration standard | Yes — MindMap built on these |
| **EU AI Act** | European Union | Cognitive/neural data requires explicit consent architecture; high-risk AI classification rules | Yes — Layer 4 enforces consent |
| **EU Digital Services Act (DSA) 2025** | European Union | Platforms must assess and mitigate mental harm from algorithmic outputs | Yes — applies to public health vertical |
| **US MIND Act** | United States | Neural data sovereignty and consent | Yes — applies to brain-state signal use |
| **GDPR Article 83** | European Union | Health and genetic data mishandling: fines up to 4% annual global turnover | Yes — insurance vertical exposure |

---

## MindMap Security Architecture

### Zero-Trust Architecture
No user, system, or process is trusted by default — inside or outside the network perimeter. Every access request is verified, every session is scoped, every data movement is logged.

### Post-Quantum Encryption
- All data at rest: encrypted with FIPS 203-compliant key encapsulation
- All data in transit: FIPS 204-compliant digital signatures
- Key rotation: automated, crypto-agile (designed to swap algorithms without re-architecting the system)

### Differential Privacy
Noise injection at the data layer ensures that even if outputs are analysed in aggregate, no individual signal can be reverse-engineered.

### Neural Data Sovereignty
Explicit consent architecture for any signal that touches cognitive or health-adjacent data. Consent is logged, auditable, and revocable. This is the EU AI Act compliance requirement for the public health vertical.

### Audit Trail
Immutable audit log for every data access, every model inference, and every output delivered to a partner. Required for GDPR accountability and EU AI Act compliance documentation.

---

## The Two-Track Insurance Entry — Layer 4 as the Door Opener

Layer 4 is what makes the Two-Track Insurance pitch work:

**Track 1 — Defensive (Immediate):** Deploy PQC migration on the insurer's most sensitive data assets. This is the CISO's fire extinguisher — a compliance problem they already have, with a 2030 hard deadline. MindMap enters the relationship on the CISO's terms, requiring no behavioral data sharing to start. Outcome: trust established, compliance closed.

**Track 2 — Offensive (H1 Pilot):** Once trust is established via Track 1, the behavioral claims prevention study begins. Consent-based, aggregated signals only, Life & Health vertical first. By the time competitors recognise what is being built, the 3-year proprietary data advantage is already in place.

> "Without this layer, no insurer or government signs the contract. It is not a feature — it is the commercial prerequisite."

---

## The 2030 Deadline — Why Timing Is Decisive

```
2022  Quantum Computing Cybersecurity Preparedness Act signed into law
2024  NIST PQC standards finalised (FIPS 203/204/205)
2025  HNDL attacks confirmed as active threat vector
2026  MindMap PQC architecture live — insurers begin Track 1 migration
2028  RSA-2048 obsolescence approaching; competitors begin retrofitting
2030  Critical systems quantum-safe deadline — MindMap already there
2031  Competitors still completing migration; MindMap 5 years ahead
```

The 2030 deadline is not a distant risk. It is 4 years away. Every organisation that defers PQC migration is adding to the window in which their already-harvested data can be decrypted.

---

## Chart Reference

**Chart 5 — HNDL Threat vs. MindMap PQC Readiness Timeline** shows the threat escalation curve against MindMap's readiness position. See `group-presentation/exhibits/` for chart data.
