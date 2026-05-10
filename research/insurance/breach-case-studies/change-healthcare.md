# Case Study: Change Healthcare (USA, 2024)

**Why this matters for MindMap:** Change Healthcare is the concentration risk case. It shows what happens when a single platform becomes so central to an industry's operations that its failure does not just harm that platform — it paralyses the entire ecosystem downstream.

---

## What Happened

Change Healthcare is a subsidiary of UnitedHealth Group that processes approximately 50% of US medical billing — the clearinghouse through which pharmacies and hospitals submit claims and get paid.

**The breach:** The ALPHVBlackCat ransomware group gained access through a Citrix remote access portal. No MFA had been implemented on this portal — a known vulnerability, publicly documented, left unpatched and unauthenticated.

**The scale:** This is the largest healthcare data breach in US history, affecting an estimated 100–192 million individuals — roughly one in three Americans.

**The systemic impact:** Beyond the data theft, the attack severed the digital infrastructure that pharmacies and hospitals use to process prescriptions and get paid. Clinics operated on paper. Patients paid out-of-pocket for life-saving medications. Some healthcare providers nearly went bankrupt due to halted cash flow.

**The response failure:** UnitedHealth downplayed the severity of the incident for weeks after the attack. This triggered Congressional testimony, intense regulatory scrutiny, and a credibility loss that made the eventual full disclosure more damaging, not less.

---

## What Went Wrong

- No MFA on a remote access gateway — a basic, known control, absent
- A known, unpatched Citrix vulnerability was the entry point
- Concentration of 50% of US medical billing in a single platform created systemic risk beyond the platform itself
- Understatement of severity in early public communications compounded regulatory and reputational damage

---

## The Concentration Risk Lesson

Change Healthcare was not primarily a data sensitivity story. It was a single-point-of-failure story. When one platform holds a disproportionate share of critical infrastructure, its security posture is not just its own business risk — it is a systemic risk to every downstream dependency.

MindMap's behavioral data pipeline feeding ML underwriting represents a similar concentration risk within the insurance vertical. If that pipeline is compromised or taken offline, the insurer's underwriting model does not function. The pilot design needs resilience architecture, not just security architecture.

---

## MindMap Implication

The insurance pilot needs a defined blast-radius ceiling. If MindMap's behavioral signal pipeline is disrupted, what is the fallback for the partner insurer? What is the maximum operational dependency MindMap will accept from a single partner? Concentration risk is a design decision, not just a security one. Change Healthcare is what happens when that decision is not made explicitly.
