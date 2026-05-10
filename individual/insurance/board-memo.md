# Aurora Insurance: Post-Breach Strategic Response

**PRIVATE AND CONFIDENTIAL**  
**To:** Aurora Insurance Board of Directors  
**From:** Group 4 — IE Business School  
**Re:** Post-Breach Strategic Response  
**Date:** May 2026  

---

## The Situation

The genetic profiles, HIV status, mental health records, and behavioral histories of tens of thousands of Aurora customers are now publicly available online. They were stolen in 2023. They became decryptable in early 2026. They are on paste sites today.

This happened because the board deferred a €4M security investment two years ago. That decision will now cost Aurora somewhere between €180M and €460M in regulatory fines, litigation, and lost business. That is the conservative end of the range. This memo is asking the board to make a different choice today.

---

## What Actually Failed

Four things went wrong, and each one has a decision attached to it:

- **A single stolen password opened the entire building.** One compromised login gave an attacker access to 1.2 TB of our most sensitive records. No second barrier, no time limit, nothing scoped by task. One key, every room.

- **Once inside, there were no walls.** Health records, genetic profiles, and behavioral data all sat in the same connected environment. A breach in one layer meant everything was reachable. Nothing limited how bad it could get.

- **We were holding far more than we needed.** Years of fully identifiable behavioral profiles and health records, kept well beyond any underwriting purpose. The attacker did not need to rush. They waited for the data to become decryptable. We gave them something worth waiting for.

- **When the data went public, there was no plan.** No regulatory notification was ready. No customer communications were drafted. No one had a defined role. The CFO walked into a press call without answers.

The same problem runs through all four: cybersecurity was treated as a technology cost to manage, not a business risk to govern.

---

## What Is at Stake

Aurora holds the records of 8 million policyholders across 11 European countries: health conditions, genetic test results, years of behavioral data. Under European law, the maximum fine for mishandling this category of data is 4% of annual global turnover, roughly €60M at Aurora's scale. Class action litigation across 11 jurisdictions, based on what comparable cases have actually cost, adds another €100M to €300M in exposure. Customer attrition of 5 to 10% across the affected base is a further €32M to €96M in lost annual premium revenue.

**Total cost of doing nothing: €180M to €460M.**

The programme to fix this costs €15M to €25M over three years. That is roughly 5 to 10 cents for every euro of risk it removes.

---

## What the Board Should Approve

### Decision 1 — No single account should ever open everything

No employee, at any level, should hold open-ended access to the full range of sensitive customer data. Access gets scoped to the task, expires when the task is done, and requires more than one form of verification. Not as a one-time fix but as the standing rule for how Aurora operates going forward.

The next phishing attack will happen. When it does, the attacker should land in a small, bounded compartment, not walk into 1.2 TB of health and genetic records. Every major insurer working with data this sensitive already operates this way. Aurora was the exception.

**Owner:** CISO  |  **Cost:** ~€2M to €4M  |  **Deadline:** September 2026

---

### Decision 2 — A breach should have a ceiling

Controlling who gets in and controlling what they can reach are two different problems. Decision 1 handles the first. This one handles the second.

Aurora's most sensitive data categories, health records, behavioral profiles, and genetic data, should not sit in one connected environment where one credential opens all of it. Each category needs its own store, with no automatic pathways between them. A breach in the behavioral data layer should not touch the genetic records. Future incidents will happen. This decision determines how much of the company they can take with them.

**Owner:** CISO  |  **Cost:** ~€3M to €5M  |  **First Milestone:** December 2026

---

### Decision 3 — Stop keeping data that is worth stealing

The attack worked because what was stolen was valuable enough to wait years for. Health records, genetic profiles, and behavioral histories that stay fully identifiable for a decade are exactly what a patient attacker goes after. Better encryption is not the answer. The answer is to make sure that by the time anyone tries to use what they took, most of it is gone.

Aurora's underwriting models do not need a ten-year archive of linked, identifiable personal records. They need signals. Those signals can be retained in aggregated, non-identifiable form once the underwriting decision is made. The raw personal data should have a hard deletion date built into the system from day one, not reviewed in a future policy cycle.

Not better locks on a full warehouse. A warehouse that is mostly empty.

**Owner:** CDO and CISO jointly  |  **Cost:** ~€4M to €7M  |  **First Milestone:** March 2027

---

### Decision 4 — Someone at board level needs to own this

The CISO raised this for two years. Nothing happened because no one at board level had it as their responsibility to act. A Board Cyber Risk Committee, with a named chair and a quarterly agenda, gives security risk a formal home at the top of the organisation. It reviews risk tolerance, holds the CISO and CDO to milestones, and brings in an independent external assessment every year.

This also fixes the fourth failure directly. When the next incident happens, the response plan exists in advance. Notifications are pre-drafted. Roles are assigned. The CFO goes into the press call with answers.

**Owner:** Board Chair  |  **Cost:** ~€1M to €2M annually  |  **First Meeting:** Within 30 days

---

## The Roadmap

| Phase | Timeframe | Key Actions | Cost |
|---|---|---|---|
| Stabilise | 0 to 90 days | MFA on all privileged access; regulatory notification filed; customer communications sent; paste-site takedown initiated; incident response roles assigned | ~€500K |
| Harden | 3 to 12 months | Scoped access enforced; data stores segmented by category; board committee established; crisis response playbook finalised | ~€6M to €9M |
| Transform | 12 to 36 months | Data deletion timelines enforced by architecture; AuroraVitality pipeline rebuilt with minimisation from the ground up; third-party data contracts renegotiated | ~€8M to €15M |

---

## The Decision the Board Cannot Defer

Every organisation that has come through a breach of this type did the same thing. Moved fast, told the truth, and showed that what went wrong had been fixed at the root. Every organisation that did not come through made the same mistake: managed the headlines instead of fixing the problem.

The four decisions in this memo are not a response to this breach. They are what Aurora should have had in place already. The breach is what forced the conversation.

**The board can make a different decision today.**

---

*Appendix available on request: NIST CSF 2.0 post-mortem, asset prioritisation matrix, historical breach comparisons (Vastaamo, Medibank, Anthem, Change Healthcare), full control gap analysis.*
