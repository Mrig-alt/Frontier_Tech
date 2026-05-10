# Case Study: Anthem (USA, 2015)

**Why this matters for MindMap:** Anthem is the cleanest structural parallel to Aurora's actual entry vector — a phishing attack compromising a database administrator's credentials — and the case that most clearly demonstrates why least-privilege access architecture is the correct response, not better encryption.

---

## What Happened

Anthem Inc. was one of the largest health insurers in the United States, holding records for approximately 78.8 million current and former customers.

**The breach:** State-sponsored hackers compromised a database administrator's credentials through a sophisticated phishing attack. The attacker authenticated legitimately using the stolen credentials and exfiltrated records containing names, dates of birth, medical IDs, Social Security numbers, and employment information.

**The outcome:** A $115M class-action settlement — the largest healthcare data breach settlement in US history at the time — and a $16M penalty paid to the US Department of Health and Human Services.

---

## The Encryption Argument

Anthem had encryption in place. It did not help. The attacker used legitimate credentials to authenticate to the database and query it directly. Encryption at rest is irrelevant when the attacker is authenticated as an authorised user.

This is the core argument Aurora's lawyers will face: "Your AES-256 was irrelevant once credentials were stolen." The defence is not better encryption. The defence is that least-privilege access architecture and just-in-time provisioning mean a compromised admin account can only ever reach a defined, bounded subset of the data — not the entire database.

---

## What Anthem Did Right in Response

- Cooperated fully with the FBI
- Provided free credit monitoring and identity protection services to affected individuals
- Made a public commitment to improved security practices
- Did not understate the breach or delay disclosure

This response is largely credited with limiting legal exposure to a manageable settlement. The company survived.

---

## The Least-Privilege Lesson

A compromised admin credential should reach a defined blast radius, not the entire database. Least-privilege access architecture means the attacker, even with valid credentials, can only go so far. The scope of what any single account can reach is the architectural control that encryption cannot provide.

At Aurora, one phished cloud engineer credential opened 1.2 TB of records across claims, behavioral profiles, and genetic data. There was no blast-radius ceiling. The Anthem lesson is that this is an architecture decision, not a security policy. It has to be built in.

---

## MindMap Implication

Just-in-time access provisioning and scoped permissions for all data pipeline admin roles in the insurance pilot are non-negotiable. The Anthem entry vector — a phished privileged credential — is the most common enterprise attack vector available. MindMap cannot prevent phishing. It can ensure that when a credential is phished, the attacker lands in a bounded compartment, not the full data store.
