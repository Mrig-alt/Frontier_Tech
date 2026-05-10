# Case Study: Vastaamo (Finland, 2020)

**Why this matters for MindMap:** Vastaamo is the case where the breach did not kill the company. The cover-up did. It is the clearest available proof that concealment is always worse than disclosure — and the closest structural parallel to what Aurora faced.

---

## What Happened

Vastaamo was a large private psychotherapy centre in Finland, holding the therapy session notes, social security numbers, and personal data of approximately 40,000 patients.

**The breach:** Began in November 2018. The attacker had access for months. The root causes were severe:
- The patient database was completely unencrypted — therapy notes in plaintext
- The root administrator account had no password
- The database was directly exposed to the open internet with no firewall or network segmentation
- No anomaly detection existed

**The CEO's knowledge:** An internal investigation in early 2019 confirmed ongoing attacker access and that data had been exfiltrated. CEO Tuomas Ville Tapio — who had personally set up the insecure database — chose not to disclose. No GDPR notification was filed. No customers were informed. The board was not told.

**The extortion (2020):** Two years later, the attacker attempted to extort Vastaamo. When the clinic refused to pay, the attacker emailed patients directly — individually — demanding €200–€500 each or their therapy notes would be published on a Tor board.

**The collapse:** The breach became public not through Vastaamo's disclosure but through the attacker's actions. The Finnish DPA investigated. Vastaamo went bankrupt and was liquidated. Tapio was prosecuted. The attacker, Aleksanteri Kivimäki, was eventually sentenced to over six years in prison.

---

## What the Finnish DPA Found

The €608,000 fine (the maximum applicable at the time) covered four violations:
1. Failure to implement adequate technical and organisational measures for highly sensitive personal data
2. Intentional failure to notify the supervisory authority and data subjects without undue delay
3. Failure to document the breach adequately
4. Failure to conduct an adequate DPIA

The fine was not what killed Vastaamo. Reputational collapse, patient litigation, insurance disputes, and the complete destruction of the operating model — no patient would return to a clinic that had exposed their most intimate disclosures — made recovery impossible.

---

## Aurora Mirror Table

| Vastaamo Failure | Aurora Equivalent |
|---|---|
| Unencrypted database | Behavioral and genetic data not field-level encrypted |
| No-password root account | Single privileged credential as sole access barrier |
| CEO concealed 2019 knowledge | Board deferred known quantum risk for 2+ years |
| 18-month GDPR notification silence | Any delay past 72h to Dutch DPA now compounds liability |
| No network segmentation | Hybrid Azure/private cloud with unclear blast-radius boundaries |
| Attacker undetected for months | 4-month exfiltration window missed entirely |

---

## The Single Lesson

The cover-up kills the company, not the breach. Transparency, disclosure, and remediation are survivable. Concealment is not. Every organisation that has survived a breach of comparable severity chose the Medibank/Anthem path — disclosed fast, cooperated, and proved the conditions no longer existed. Vastaamo chose the other path. It no longer exists.

---

## MindMap Implication

MindMap's incident response protocol must include a pre-drafted 72-hour GDPR notification, a customer communication template, and named ownership of the disclosure decision at board level before the insurance pilot goes live. The Vastaamo lesson is not about technical controls. It is about what the organisation does in the first 72 hours after awareness.
