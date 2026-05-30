# HNDL Risk & PQC Requirements — Security Lessons for MindMap Layer 4

**Context:** Harvest-Now-Decrypt-Later (HNDL) is a documented threat pattern in which adversaries exfiltrate encrypted data today and hold it for decryption once quantum hardware matures. For platforms handling long-retention behavioral and health data — like MindMap's insurance vertical — this is not a theoretical risk. NIST's 2030 PQC migration deadline makes the window concrete.

**Relevance to MindMap:** MindMap's insurance vertical processes behavioral signals correlated with claims and health outcomes. This data has long retention requirements. Any platform without PQC-ready encryption from day one exposes partner insurers to retrospective decryption of actuarial data. This is why PQC is a procurement precondition for AXA and Swiss Re, not a future upgrade.

---

## Failure Pattern 1: Single Privileged Credential as Sole Access Barrier

**Pattern:** A single compromised credential unlocks large volumes of sensitive data — claims, behavioral profiles, health records — because no just-in-time access provisioning exists.

**MindMap Layer 4 requirement:**
- Just-in-time access provisioning for all data pipeline admin roles — no standing permissions
- Hardware security keys (FIDO2/WebAuthn) mandatory for all privileged accounts
- Session recording for any admin access to insurance pilot data stores
- Blast-radius documentation: every privileged role mapped to what it can reach, minimised

**Status:** Specified in Layer 4 Zero Trust Architecture. Must be verified before insurance pilot go-live.

---

## Failure Pattern 2: Behavioral and Health Data Stored with Metadata Intact

**Pattern:** Encrypted data exfiltrated with readable metadata (claim IDs, policy types, dates). Attacker demonstrates harm from metadata alone before full decryption.

**MindMap Layer 4 requirement:**
- Population-level aggregation already reduces individual re-identification risk
- All insurance pilot correlation outputs must be reviewed for metadata stripping before delivery
- Differential privacy enforced on all model outputs, not just raw data

**Status:** Differential privacy specified in Layer 4. Metadata stripping must be explicitly added to the insurance pilot data handling protocol.

---

## Failure Pattern 3: Low-and-Slow Exfiltration Undetected

**Pattern:** Data exfiltrated over months at low volume to avoid triggering volume-based detection. No behavioural baselining of privileged accounts.

**MindMap Layer 4 requirement:**
- Audit logging must include behavioural baselining (UEBA), not just access logs
- Alert thresholds set on access pattern deviation, not just data volume
- Privileged account activity on insurance data pipelines reviewed weekly during pilot phase

**Status:** Audit logging specified for EU AI Act compliance. UEBA baselining must be explicitly added.

---

## Failure Pattern 4: Classical Encryption Insufficient for Long-Retention Behavioral Data

**Pattern:** AES-256 encryption bypassed via HNDL. Encrypted data stored for 2+ years, with partial decryption demonstrated as quantum hardware matured. Board warned and deferred action.

**MindMap Layer 4 requirement:**
- PQC-ready encryption aligned to NIST migration roadmap — hard requirement, not a future upgrade
- Insurance pilot data must be under hybrid PQC schemes (classical + CRYSTALS-Kyber/MLKEM) from day one
- Any long-retention data must never rely solely on classical encryption
- PQC migration must not be deferred — deferral is the precise failure mode that turns a manageable cost into a catastrophic liability

**Status:** PQC specified in Layer 4. Treated as hard launch requirement for insurance pilot.

---

## Failure Pattern 5: Third-Party Data Relationships as Uncontrolled Risk Surface

**Pattern:** Reliance on third-party data brokers for behavioral signals expanded the data ingress/egress surface without equivalent security controls.

**MindMap Layer 4 requirement:**
- MindMap's primary inputs (Google Trends, social media) are public and aggregated — lower risk than broker models
- Any downstream enrichment, re-identification risk, or data sharing in the insurance pilot must be explicitly assessed before go-live
- Partner insurer's data handling obligations contractually defined: minimum encryption standards, breach notification timelines, audit rights
- MindMap retains GDPR data controller responsibility for any personal data processed in the insurance vertical

**Status:** Not explicitly addressed in current Layer 4 spec. Third-party data handling protocol must be added before insurance pilot launch.

---

## Failure Pattern 6: No Governance Forcing Function for Known Risks

**Pattern:** CISO warned board about quantum risk for two years. Board deferred into future budget cycle. A manageable remediation cost became a multi-hundred-million liability.

**MindMap Layer 4 requirement:**
- Formal risk register with named owners and review dates for each identified threat
- Quantum threat timeline as a standing governance agenda item — not a one-time warning
- Any decision to defer a Layer 4 security requirement logged as an explicit risk acceptance decision, not a passive omission

**Status:** Governance structure implied in Layer 4 README. Formal risk register with named owners must be created.

---

## Summary: Failure Patterns vs. MindMap Layer 4 Status

| Failure Pattern | Layer 4 Status |
|---|---|
| Single credential access | Specified — verify in implementation |
| Metadata exposure | Differential privacy specified — metadata stripping protocol needed |
| Detection blindness | Audit logging specified — UEBA baselining must be added |
| Classical encryption only | PQC specified as hard requirement |
| Third-party risk | Public data sources used — partner contracts need explicit protocol |
| Governance vacuum | Layer 4 exists — formal risk register with owners needed |

---

*Last updated: May 2026*
*Do not reference any specific insurance company breach by name in external MindMap materials.*
