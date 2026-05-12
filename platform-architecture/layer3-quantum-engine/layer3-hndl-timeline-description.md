# Layer 3 — HNDL Threat vs MindMap PQC Readiness

## What This Chart Shows
A dual-line time series (2020–2030) showing the escalating Harvest-Now-Decrypt-Later (HNDL) threat index against MindMap's post-quantum cryptography readiness index.

## Key Data Points

| Year | HNDL Threat Level (0–10) | MindMap PQC Readiness (0–10) |
|---|---|---|
| 2020 | 2 | 0 |
| 2022 | 4 | 0 |
| 2024 | 6 | 0 |
| 2026 (Now) | 8 | 6 |
| 2028 | 9 | 8 |
| 2030 | 10 | 9 |

## Why 2026 Is the Critical Year
- HNDL threat is already at 8/10 — adversaries have been harvesting encrypted data for years
- MindMap PQC readiness moves from 0 to 6 in 2026 because this is when the architecture decisions are being locked
- The 2030 NIST deadline is the hard wall — any system not quantum-ready by then is compromised by default

## Aurora Connection
The Aurora breach scenario is used as the case study illustrating what happens when an insurance company ignores this curve. AES-256 was not the failure — the architecture assumptions underneath it were. MindMap's Layer 3 is built from the Aurora post-mortem, not from theoretical security frameworks.
