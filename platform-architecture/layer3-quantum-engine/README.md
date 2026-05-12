# Layer 3: Cybersecurity & Compliance

Layer 3 is not a bolt-on. It is the reason any regulated industry would trust MindMap with their data infrastructure, and the reason MindMap is defensible as a long-term platform rather than a point solution.

Without Layer 3, MindMap cannot be sold to pharma (FDA oversight), insurance (FCA/EIOPA regulation), or government (national data laws). Layer 3 is what makes the platform sellable.

---

## The HNDL Problem — Why This Layer Exists Now

Harvest Now, Decrypt Later (HNDL) attacks are already active. Adversaries are capturing encrypted data today — insurance policy data, pharma trial data, government health records — with the intention of decrypting it once quantum computers reach sufficient power (estimated: 2028–2030 based on NIST timelines).

AES-256, which most enterprises currently use, is not the problem. The problem is that data being encrypted today will still be sensitive in 2030. The Aurora case study (see `research/insurance/aurora-scenario.md`) shows exactly how this plays out: a CISO raises the HNDL risk in 2024, gets overruled as theoretical, and the organisation is exposed by 2026.

MindMap's Layer 3 is built against this reality — not against a future threat.

---

## What Layer 3 Contains

### Post-Quantum Cryptography (PQC)
- NIST Post-Quantum Cryptography roadmap compliant (2024 standards: ML-KEM, ML-DSA, SLH-DSA)
- All data in transit and at rest encrypted with PQC-ready algorithms
- Migration path from classical to quantum-resistant encryption documented and staged
- The HNDL fix is not "better locks" — it is data minimisation (see Decision 2 in the Aurora board memo): not keeping data that doesn't need to be kept so the payload is not worth harve