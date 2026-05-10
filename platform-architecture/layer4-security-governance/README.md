# Layer 4: Security and Governance

MindMap's Layer 4 is the reason regulated industries — insurance, pharma, government — can trust the platform. It is not a compliance checkbox. It is the architectural layer that separates MindMap from every behavioral signal platform that failed before it.

## Why This Layer Exists

In 2026, Aurora Insurance operated a behavioral signal platform that was, in every material respect, what MindMap's insurance vertical is designed to be. Behavioral data, ML-driven underwriting, long-retention health and genetic records. Aurora had no equivalent of this layer. The result was a "harvest now, decrypt later" breach that exposed the genetic profiles, HIV status, and therapy records of tens of thousands of customers. The regulatory and litigation exposure ran to €180M–€460M.

Every requirement in this layer has a named failure at Aurora behind it. This is not theoretical risk management. It is documented, priced, and publicly visible.

The full Aurora case analysis — including the four breach case studies (Vastaamo, Medibank, Change Healthcare, Anthem), regulatory exposure, and cost-of-inaction arithmetic — is in `research/insurance/`.

## What This Layer Covers

- **Zero-trust access architecture** — no standing permissions, just-in-time provisioning, hardware security keys (FIDO2/WebAuthn) on all privileged accounts
- **Post-quantum cryptography (PQC)** — NIST-aligned, hybrid classical + CRYSTALS-Kyber for all long-retention insurance pilot data from day one, not a future upgrade
- **Data minimisation by design** — behavioral signals retained in aggregated, non-identifiable form; raw personal data has a hard deletion date built into the architecture
- **Differential privacy** — enforced on all model outputs, not just raw data
- **Behavioral audit logging (UEBA)** — access pattern deviation alerts, not just volume thresholds; privileged account activity reviewed weekly during pilot
- **Data segmentation** — health, behavioral, and genetic data stores separated with no automatic cross-pathways; a breach in one layer cannot reach the others
- **Third-party data handling protocol** — partner insurer obligations contractually defined; audit rights, breach notification timelines, minimum encryption standards
- **Formal risk register** — named owners, review dates, and explicit risk acceptance decisions for any deferred requirement

## Files

- `aurora-breach-lessons.md` — the six failure patterns from Aurora mapped to MindMap's Layer 4 protections, with implementation status for each
