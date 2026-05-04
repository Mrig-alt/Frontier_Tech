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

## Repo Structure

- `docs/` – assignment briefs, clarifications, and project timeline.
- `group-presentation/` – group deck structure, speaking scripts, and decision logic.
- `research/` – structured research notes, stress tests, sources, and analysis by vertical.
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
