# Layer 1: Behavioral Data

This layer is the foundation of MindMap. It ingests publicly available human behavioral signals and prepares them for quantum ML processing in Layer 2.

## What It Captures
- **Google Trends** — 10–20 years of search intent signals. Google controls ~80% of global search (136B monthly visits). This is not a proxy for what people think — it IS what people are actively searching, in real time.
- **Social Media Emotional Signals** — Twitter/X, Reddit, Meta platforms. Population-level emotional state mapping across demographics and geographies.
- **fMRI / BCI Research Anchors** — Meta TRIBE v2 (500+ hours, 700 subjects, 23% improvement in neural encoding) and IBM + Inclusive Brains BCI study (June 2025) used as scientific validation of the behavioral signal layer.

## Privacy Architecture
Data is aggregated at **population level, not individual level**. This is a deliberate design decision — it is MindMap's privacy and consent architecture, not a limitation.

## Data Source Mix
![Data Source Mix](layer1-data-sources.png)

Google Trends dominates at ~38% of the signal mix, followed by Meta platforms (18%) and Twitter/X (22%). fMRI/BCI research anchors represent a small but scientifically critical 5% — these are the studies that validate the behavioral-to-neural bridge hypothesis.

## Why This Layer Is Defensible
- No single competitor aggregates all four source types into one behavioral signal pipeline
- The Google Trends data going back 10–20 years creates a historical behavioral baseline that cannot be recreated
- Population-level aggregation means no GDPR / consent friction at the data acquisition stage

## Platform Flow
![Platform Architecture Funnel](layer1-platform-funnel.png)

The funnel shows how raw behavioral signal volume is processed and compressed through all 4 MindMap layers — Layer 1 starts with the widest possible signal aperture and narrows to actionable industry output.
