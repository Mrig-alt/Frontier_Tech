# MindMap – IMBA Frontier Technologies

This repository contains the group and individual work for the **MindMap** project in the IMBA Frontier Technologies course.

MindMap is a behavioral signal platform that uses Google Trends and social media data, combined with ML and quantum computing, to map and predict human behavior. It is a single platform that three industries can plug into: **Pharma**, **Insurance**, and **Public Health**.

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

## Why Layer 4 Is Non-Negotiable

In 2026, Aurora Insurance — a behavioral signal platform structurally identical to MindMap's insurance vertical — suffered a catastrophic data breach. Genetic profiles, HIV status, mental health records, and behavioral histories of tens of thousands of customers became publicly available. The company had deferred a €4M security investment. That decision created a €180M–€460M liability.

Aurora is not a cautionary tale about cybersecurity in the abstract. It is a precise description of what MindMap's insurance vertical looks like without Layer 4. Every architecture decision in Layer 4 traces directly to a documented failure at Aurora. The full analysis is in `research/insurance/`.

## Repo Structure

- `docs/` – assignment briefs, clarifications, and project timeline.
- `group-presentation/` – group deck structure, speaking scripts, and decision logic.
- `research/` – structured research notes, stress tests, sources, and analysis by vertical.
- `research/insurance/` – Aurora case analysis, breach case studies, regulatory exposure, and cost-of-inaction arithmetic that inform the insurance vertical and Layer 4 design.
- `individual/` – personal folders for each team member: pharma, insurance, public-health.
- `platform-architecture/` – MindMap platform design: data layer, quantum ML layer, cybersecurity layer.
- `data/` – non-sensitive external datasets and processed tables (if used).
- `tools/` – AI prompts and helper scripts used for research and automation.

## Decisions Locked (as of 2026-05-04)

- Platform name: **MindMap**
- Industries: Pharma (lead), Insurance (teammate 2), Public Health (teammate 3)
- Entry product for Insurance: behavioral correlation study → claims prevention pilot (not neural pricing on day 1)
- Pharma is H1 (validation); Insurance secret pilot runs in parallel; Public Health is H2/H3
- Cybersecurity (PQC, zero-trust, differential privacy) is core to the platform, not a bolt-on
