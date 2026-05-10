# Case Study: Medibank (Australia, 2022)

**Why this matters for MindMap:** Medibank is the case where a company made most of the same entry-point mistakes as Aurora, suffered severe reputational damage, but survived — because they disclosed fast, refused to pay the ransom, and were transparent with customers. It is also the case that shows how data structure itself is a harm amplifier.

---

## What Happened

Medibank is one of Australia's largest private health insurers, holding the health records of approximately 9.7 million current and former customers.

**The breach:** A third-party IT contractor's credentials were stolen and used to access Medibank's network. No MFA was enforced on VPN access. One set of credentials, full access.

Excessive access rights meant the compromised account could reach sensitive claims data across the entire customer base — not just the contractor's operational scope.

Delayed containment: Medibank's detection and response timeline gave the attackers time to stage and exfiltrate data before the alarm was raised.

**The extortion:** The attackers (affiliated with the REvil ransomware group) demanded a $9.7M ransom. Following Australian government guidance, Medibank refused to pay.

**The weaponisation:** The attackers then published the data. Critically, they categorised the leaked files to maximise psychological damage — creating "naughty" and "nice" lists. The "naughty" list deliberately exposed customers treated for HIV status, drug and alcohol addiction, mental health issues, and abortions. This was not random data dumping. It was structured, targeted psychological warfare enabled by the fact that the data was searchable and relational.

---

## What Medibank Got Right

- Refused the ransom (following government guidance)
- Disclosed publicly and cooperated with regulators
- Was transparent with customers about what had been taken
- Did not understate the severity

This protected them from regulatory sanction for concealment. The company survived. Their stock fell approximately 18% but recovered over the following year.

---

## What Medibank Got Wrong

- No MFA on VPN access — same single-credential failure as Aurora and Anthem
- Third-party contractor credential hygiene was inadequate
- Excessive access rights meant blast radius was the entire customer base
- Detection and containment timeline allowed full data staging

---

## The Data Architecture Lesson

The attackers' ability to create "naughty" and "nice" lists was not a function of how much data they stole. It was a function of how the data was structured. Searchable, relational, categorised claims records made it trivially easy to sort by diagnosis code. The harm was amplified by the architecture, not just the volume.

MindMap's population-level aggregation model addresses individual re-identification at the raw data layer. But the insurance pilot's correlation study outputs — if they contain linkable metadata — could still be sorted, filtered, and weaponised in exactly the same way. Metadata stripping and differential privacy on model outputs are not theoretical requirements. Medibank is what happens when they are missing.

---

## MindMap Implication

Third-party access controls, MFA on all privileged and remote access, and data architecture that prevents post-exfiltration sorting are all non-negotiable for the insurance pilot. The entry point (contractor credentials, no MFA) is the same failure vector as Aurora's phished cloud engineer. The architectural control is the same: just-in-time access, hardware security keys, scoped permissions with no standing access to the full dataset.
