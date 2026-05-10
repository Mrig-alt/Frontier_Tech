# MindMap – IMBA Frontier Technologies

This repository contains the group and individual work for the **MindMap** project in the IMBA Frontier Technologies course.

MindMap is a behavioral signal platform that uses Google Trends and social media data, combined with ML and quantum computing, to map and predict human behavior. It is a single platform that three industries can plug into: **Pharma**, **Insurance**, and **Public Health**.

## Why MindMap's Insurance Vertical Exists

In 2026, Aurora Insurance — a behavioral signal platform using ML-driven underwriting on long-retention health and genetic data — suffered a "harvest now, decrypt later" breach that exposed the records of tens of thousands of customers. The regulatory and litigation exposure ran to €180M–€460M. The CISO had warned the board for two years. Nothing happened because no governance structure existed to act on the warning.

Aurora is not a cautionary tale from a different industry. It is a direct analogue of what MindMap's insurance vertical is. The difference is that MindMap was built with Layer 4 from the start. Every security and governance requirement in Layer 4 has a named failure at Aurora behind it. The full analysis is in `research/insurance/`.

## Team Structure

| Teammate | Industry Vertical | Customer Target | MindMap Role |
|---|---|---|---|
| Lead (group + individual) | Pharma | Roche / CNS biotech | Behavioral signals improve clinical trial targeting; pharma validates the science |
| Teammate 2 | Insurance | AXA / Swiss Re | Secret internal pilot: behavioral signals for claims prevention and risk modeling |
| Teammate 3 | Public Health | Government (named country) | Population sentiment mapping for electoral and policy strategy |

## Why This Structure

- The **group presentation** argues the macro disruption thesis: one platform (MindMap) disrupting three industries simultaneously.
- Each **individual report** zooms into one vertical and one named customer — meaningfully different from the group deck as required by the brief.
- **Pharma is the anchor**: insurance and public health need pharma to validate the behavioral science first. Without pharma proving the signals work, no insurer will price them and no government will rely on them.

## Repo Structure

- `docs/` – assignment briefs, clarifications, and project timeline.
- `group-presentation/` – group deck structure, speaking scripts, and decision logic.
- `research/` – structured research notes, stress tests, sources, and analysis by vertical.
  - `research/insurance/` – full Aurora case analysis: scenario, four breach case studies, regulatory exposure, cost-of-inaction arithmetic.
- `individual/` – personal folders for each team member: pharma, insurance, public-health.
  - `individual/insurance/` – insurance vertical decision log, NIST CSF post-mortem, and board memo.
- `platform-architecture/` – MindMap platform design: data layer, quantum ML layer, cybersecurity layer.
- `data/` – non-sensitive external datasets and processed tables (if used).
- `tools/` – AI prompts and helper scripts used for research and automation.

## Decisions Locked (as of 2026-05-04)

- Platform name: **MindMap**
- Industries: Pharma (lead), Insurance (teammate 2), Public Health (teammate 3)
- Entry product for Insurance: behavioral correlation study → claims prevention pilot (not neural pricing on day 1)
- Pharma is H1 (validation); Insurance secret pilot runs in parallel; Public Health is H2/H3
- Cybersecurity (PQC, zero-trust, differential privacy) is core to the platform, not a bolt-on
