# Case Study: Anthem (USA, 2015)

**Why this matters for MindMap:** Anthem is the cleanest structural parallel to Aurora's actual incident vector — a state-sponsored phishing attack on a database administrator's credentials. It is also the case that most clearly demonstrates what least-privilege access architecture would have changed.

---

## What Happened

State-sponsored hackers breached Anthem Inc., one of the largest US health insurers, through a phishing attack that compromised a database administrator's credentials. The attackers used those credentials to access a database containing the records of 78.8 million people — names, dates of birth, medical IDs, Social Security numbers, employment information.

Unlike Medibank or Vastaamo, the hackers did not steal medical diagnostic records. They stole PII and PHI at scale. The result: a $115 million class-action settlement and a $16 million penalty paid to the US Department of Health and Human Services.

## The Failures

- **Phishing compromised admin credentials.** Identical to Aurora's 2023 cloud engineer compromise. The entry mechanism is the most common vector in healthcare breaches — and the most preventable.
- **Admin credentials meant encryption was irrelevant.** The attacker authenticated legitimately. AES-256 at rest protects against an attacker who doesn't have valid credentials. Against one who does, it does nothing. This is the core argument Aurora's lawyers will face: *"Your AES-256 was irrelevant once credentials were stolen."*
- **One admin credential, entire database.** No least-privilege architecture. A compromised account reached 78.8 million records because that account had standing access to all of them.

## What Anthem Did Right

- Cooperated with the FBI immediately
- Offered free identity protection services to affected individuals
- Made a public commitment to improved encryption and access controls
- Early, cooperative response is credited with limiting legal exposure to a manageable (if record-breaking) settlement

## The Least-Privilege Lesson

The single most actionable lesson from Anthem: **a compromised admin account should reach a defined blast radius, not the entire database**. If the credential that was phished had only scoped, task-limited access to the specific database partition required for their role, the breach would have been a serious incident rather than 78.8 million records.

This is Decision 1 in MindMap's Layer 4: just-in-time access provisioning, no standing permissions, scoped by task. The Anthem breach is the documented proof of what the absence of that architecture costs.

## Relevance to MindMap

MindMap's insurance pilot requires privileged admin access to the data pipeline and correlation model outputs. Those roles must be scoped to their task, time-limited, and covered by FIDO2/WebAuthn hardware keys. The Anthem incident is the price of not doing that — and at 78.8 million records, it is a conservatively small version of what is possible at scale.
