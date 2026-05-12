# Layer 3: Cybersecurity & Compliance

This is not a bolt-on. It is core to why any government or regulated industry would trust MindMap with behavioral population data.

## Why This Layer Exists
The behavioral data MindMap processes is classified as **high-risk** under the EU AI Act (2026–2027). Without a robust security and compliance layer, MindMap cannot be sold to:
- Pharma (FDA validation requirements)
- Insurance (FCA / EIOPA regulatory approval)
- Government (national data sovereignty laws)

The cybersecurity layer is what converts MindMap from an interesting research platform into a commercially deployable product.

## Architecture Components
- **PQC-ready encryption** — aligned to NIST Post-Quantum Cryptography roadmap (2030 deadline for critical systems)
- **Zero-trust architecture** — no single credential reaches everything (Aurora Decision 1)
- **Differential privacy** — population-level data outputs with mathematical privacy guarantees
- **Full audit logging** — EU AI Act 2026–2027 high-risk classification compliant
- **US MIND Act (2025) compliance pathway** — neural data protection framework

## The HNDL Threat — Why Quantum Readiness Is Urgent Now
![HNDL Threat Timeline](layer3-hndl-timeline.png)

Harvest-Now-Decrypt-Later (HNDL) attacks mean adversaries are collecting encrypted behavioral data today with the intent to decrypt it once quantum computers reach sufficient capability (~2030). The window to fix this is now — not when quantum computers arrive.

**MindMap's answer to HNDL is not better encryption on a full warehouse. It is a warehouse that is mostly empty.** Data minimisation is Decision 2 of the Aurora board memo — the payload must not be worth stealing by not keeping it.

## NIST Timeline
| Milestone | Year |
|---|---|
| NIST PQC standards finalised | 2024 |
| Cybersecurity Preparedness Act enacted | 2022 |
| Critical systems migration deadline | 2030 |
| MindMap PQC architecture locked | 2026 (now) |

## Aurora Case Study Connection
The Aurora insurance breach (8M policyholders, €18B AUM at risk) is the documented real-world failure that MindMap's Layer 3 is architecturally designed to prevent. See `research/insurance/` for full case study.
