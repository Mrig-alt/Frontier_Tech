# Case Study: Change Healthcare (USA, 2024)

**Why this matters for MindMap:** Change Healthcare is not primarily a data sensitivity story. It is a **concentration risk and systemic dependency** story. For MindMap's insurance vertical, the lesson is about what happens when a single platform becomes load-bearing infrastructure for an entire industry.

---

## What Happened

Change Healthcare, a subsidiary of UnitedHealth Group, acts as the central clearinghouse for US medical billing — processing roughly 50% of all US medical claims. The ALPHV/BlackCat ransomware group breached the system through a Citrix remote access portal that had no MFA enabled. A known, unpatched vulnerability in a remote access gateway was the door to the largest healthcare data breach in US history.

Estimated 100 to 190 million individuals affected — approximately one third of the US population.

## The Failures

- **No MFA on a Citrix remote access portal.** A years-old, known vulnerability, unpatched and unauthenticated. The same single-credential failure present in Aurora and Medibank, at incomparably larger scale.
- **Systemic concentration.** When one clearinghouse processes 50% of US medical billing and it goes down, pharmacies cannot process prescriptions, hospitals cannot get paid, and clinics operate on paper. The attack did not just steal data — it severed infrastructure.
- **UnitedHealth downplayed severity for weeks.** Congressional testimony, regulatory scrutiny, and a prolonged credibility collapse followed. Understatement in a crisis is as operationally damaging as the breach itself.

## Relevance to MindMap

MindMap's AuroraVitality-equivalent risk: the behavioral data pipeline for the insurance pilot. If MindMap's signal ingestion layer or correlation model goes down during a live pilot, the partner insurer's claims prevention model breaks. MindMap must not become a single point of failure in its partner's underwriting infrastructure.

The architecture answer is the same as the security answer: **no single dependency without a fallback**. The insurance pilot data pipeline should be designed so MindMap's unavailability degrades the partner's model gracefully, not catastrophically.

The governance answer from Change Healthcare: when something significant happens, say so immediately and completely. Regulators and partners treat delayed or minimized disclosure as a separate and compounding failure.
