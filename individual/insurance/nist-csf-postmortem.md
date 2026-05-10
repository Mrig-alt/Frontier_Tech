# Aurora Insurance — NIST CSF 2.0 Post-Mortem

**Framework:** NIST Cybersecurity Framework 2.0 (6 functions)  
**Purpose:** Gap analysis against Aurora's actual failure modes; informs MindMap Layer 4 design  
**Note:** This document is the technical appendix referenced in the board memo. It is not the memo itself.

---

## Function 1: GOVERN

**What NIST CSF 2.0 requires:** Establish, communicate, and monitor cybersecurity risk management strategy, expectations, and policy across the organisation.

**What Aurora had:** An annual security slide deck presented to the board. A CISO with no formal escalation path to a budget decision. A €4M post-quantum readiness assessment deferred into Q3 2026 without a named owner or accountability mechanism.

**The gap:**
- No board-level cyber risk committee
- No risk tolerance statement that would have required action on a known threat
- No formal mechanism to convert a CISO warning into a budget decision
- Cybersecurity governed as IT cost management, not enterprise risk management

**NIST CSF 2.0 Outcome GV.RM:** Risk management policies, processes, and procedures are established, communicated, and enforced. Aurora had the first but not the second or third.

**MindMap implication:** Layer 4 formal risk register with named owners and review dates. Any deferral of a security requirement logged as an explicit risk acceptance decision.

---

## Function 2: IDENTIFY

**What NIST CSF 2.0 requires:** Develop an organisational understanding of cybersecurity risk to systems, people, assets, data, and capabilities.

**What Aurora had:** No cryptographic asset inventory. No formal classification of data by sensitivity tier and retention profile. No documented blast radius assessment — what each privileged role could reach, and what the consequence of compromise would be.

**The gap:**
- 1.2 TB of data was exfiltrated without the organisation knowing what was in it until a researcher posted it publicly
- No asset register would have identified AuroraVitality behavioral data and genetic records as the highest-risk long-lived assets requiring PQC-priority treatment
- Third-party data broker relationships not mapped as risk surface

**NIST CSF 2.0 Outcome ID.AM:** Assets are identified and managed. Aurora could not account for what was taken because it had not catalogued what it held.

**MindMap implication:** Explicit data asset inventory for the insurance pilot. Blast radius documented per privileged role before pilot goes live.

---

## Function 3: PROTECT

**What NIST CSF 2.0 requires:** Develop and implement appropriate safeguards to ensure delivery of critical services.

**What Aurora had:** AES-256 encryption at rest. Standard perimeter controls. No MFA on privileged cloud access. No PAM (Privileged Access Management) tooling. No field-level encryption or tokenization of the most sensitive data categories. No data minimisation policy enforced by architecture.

**The gap:**
- Single credential as sole access barrier to the full data estate
- Encryption present but key exchange mechanism not protected against quantum-assisted attack
- No scoped, time-limited access — standing permissions meant a compromised account never expired
- Long-retention identifiable data created an HNDL target by design

**NIST CSF 2.0 Outcome PR.AC:** Identities and credentials are issued, managed, verified, revoked, and audited for authorised users. Aurora had none of the lifecycle management that makes this real.

**MindMap implication:** JIT access provisioning, FIDO2/WebAuthn on all privileged accounts, hybrid PQC encryption (CRYSTALS-Kyber) on all long-retention insurance pilot data, hard deletion dates by architecture.

---

## Function 4: DETECT

**What NIST CSF 2.0 requires:** Develop and implement appropriate activities to identify the occurrence of a cybersecurity event.

**What Aurora had:** Volume-based anomaly detection. Standard cloud access logging. No behavioral baselining of privileged accounts. No UEBA (User and Entity Behavior Analytics).

**The gap:**
- The attacker specifically chose low-and-slow exfiltration to stay below volumetric thresholds — the detection system was optimised for the wrong adversary
- Four months of active exfiltration went undetected
- No alert mechanism existed for access pattern deviation, only data volume deviation

**NIST CSF 2.0 Outcome DE.AE:** Anomalous activity is detected and the potential impact of events is understood. Aurora's detection capability was blind to the actual attack pattern.

**MindMap implication:** Audit logging with behavioral baselining (UEBA-equivalent) not just access logs. Alert thresholds on access pattern deviation. Weekly privileged account activity review during pilot phase.

---

## Function 5: RESPOND

**What NIST CSF 2.0 requires:** Develop and implement appropriate activities to take action regarding a detected cybersecurity incident.

**What Aurora had:** No incident response playbook for a breach of this category. No pre-drafted GDPR Article 33 notification. No pre-assigned roles for crisis response. No pre-drafted customer communications.

**The gap:**
- The CFO walked into a press call without answers because no one had prepared the answers
- 72-hour GDPR notification window to the Dutch DPA was not met
- NIS2 parallel notifications to national CERTs across 11 countries had no documented process
- No paste-site takedown protocol existed

**NIST CSF 2.0 Outcome RS.CO:** Response activities are coordinated with internal and external stakeholders. Aurora had no coordination framework — response was improvised under maximum pressure.

**MindMap implication:** Pre-drafted breach notification templates. Named incident response roles assigned before pilot goes live. 72-hour GDPR notification workflow documented and tested.

---

## Function 6: RECOVER

**What NIST CSF 2.0 requires:** Develop and implement appropriate activities to maintain plans for resilience and to restore any capabilities or services that were impaired due to a cybersecurity incident.

**What Aurora had:** No crypto-agility in the architecture — migrating to PQC required a full stack rewrite rather than an algorithm swap. No customer trust restoration plan. No post-incident roadmap prepared in advance.

**The gap:**
- Recovery was impossible to plan in advance because the underlying architecture did not support it
- Crypto-agility (the ability to swap cryptographic algorithms without rewriting the stack) was not designed in, meaning the PQC migration will now happen under crisis conditions and at crisis cost
- No framework for rebuilding customer trust existed — Medibank's survival was partly attributable to having a credible remediation narrative ready

**NIST CSF 2.0 Outcome RC.RP:** Recovery plans incorporate lessons learned. Aurora had no recovery plan to incorporate lessons into.

**MindMap implication:** Crypto-agile architecture from day one — algorithms are modular and swappable. Incident recovery runbook prepared before insurance pilot launches.

---

## Summary Gap Table

| NIST CSF Function | Aurora Status | Critical Gap | MindMap Layer 4 Response |
|---|---|---|---|
| Govern | No board cyber committee, no risk tolerance statement | CISO warnings had nowhere to land | Formal risk register, named owners, explicit deferral logging |
| Identify | No cryptographic asset inventory, no blast radius map | Did not know what was taken or how sensitive it was | Data asset inventory, blast radius per privileged role |
| Protect | AES-256 present, no MFA, no PAM, no data minimisation | Single credential opened everything; HNDL target by design | JIT access, FIDO2, hybrid PQC, hard deletion dates |
| Detect | Volume-based only, no UEBA | 4-month exfiltration invisible to detection | Behavioral baselining, pattern deviation alerts |
| Respond | No IR playbook, no pre-drafted notifications | CFO had no answers; GDPR window missed | Pre-drafted notifications, named IR roles, 72h workflow |
| Recover | No crypto-agility, no recovery plan | PQC migration now happens under crisis conditions | Modular crypto architecture, incident recovery runbook |

---

*This post-mortem is the technical foundation for the board memo in `individual/insurance/board-memo.md` and the architecture requirements in `platform-architecture/layer4-security-governance/aurora-breach-lessons.md`.*
