# Case Study: Medibank (Australia, 2022)

**Why this matters for MindMap:** Medibank is the closest structural parallel to Aurora's actual data exposure — a health insurer with a rich, categorized claims database. What it got wrong is operationally preventable. What it got right explains why it survived.

---

## What Happened

Hackers affiliated with the REvil ransomware group breached Medibank, one of Australia's largest private health insurers, and accessed the data of 9.7 million current and former customers. The entry point: a third-party IT contractor's credentials were stolen and used to access Medibank's network. No MFA was enforced on VPN access. One compromised contractor account opened the building.

Medibank detected unusual activity and began an investigation. The attackers threatened to publish the data unless a $9.7M ransom was paid. Following Australian government guidance, Medibank refused.

The attackers then began releasing data on the dark web — and they did it with maximum psychological intent. They sorted the leaked files into **"naughty" and "nice" lists**, deliberately exposing records related to HIV status, drug and alcohol addiction, mental health treatment, and abortion history. The categorization was not random. They used Medibank's own data structure — searchable, relational, categorized by diagnosis code — to sort by harm.

## The Technical Failures

- **No MFA on VPN access.** One contractor credential, no second factor. Direct parallel to Aurora's single phished cloud engineer credential.
- **Excessive access rights.** One compromised account could reach sensitive claims data across the entire customer base. No least-privilege architecture, no scoped access by role or task.
- **Detection and containment lag.** Attackers had time to map, stage, and prepare the data before the alarm was raised.
- **Data architecture as harm amplifier.** The relational, diagnosis-coded structure of the claims database made it trivially easy for attackers to sort records by condition. For MindMap: behavioral profiles and ML feature stores are equally structured. If exfiltrated, they are equally sortable.

## What Medibank Did Right

- **Refused to pay the ransom.** Following government guidance, Medibank did not pay. This is credited with preventing the precedent that payment stops publication.
- **Was transparent with customers.** Medibank communicated directly and openly about what was taken. This protected them from regulatory sanction for concealment.
- **Stock fell 18% but the company survived.** The contrast with Vastaamo is the lesson: early transparency, however painful, is survivable.

## Relevance to MindMap

Medibank's core failure — one contractor credential, no MFA, excessive access rights — is exactly what MindMap's Layer 4 zero-trust architecture closes. Just-in-time access provisioning, hardware security keys on all privileged accounts, and scoped access by task mean a compromised account reaches a bounded compartment, not the full data store.

The data architecture lesson is equally important. MindMap's population-level aggregation model addresses individual re-identification risk at the platform level. But the insurance pilot's correlation study outputs must be reviewed for metadata and structural re-identification risk before delivery to the partner insurer — a relational output is still sortable by harm even if the underlying data is aggregated.
