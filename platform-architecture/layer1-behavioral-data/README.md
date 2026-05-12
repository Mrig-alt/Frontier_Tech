# Layer 1: Behavioral Data

MindMap's first layer captures population-level behavioral signals from publicly available sources. It is the raw input to the entire platform — no proprietary data, no consent issues, no individual tracking.

---

## What This Layer Does

It listens to what populations are actually doing — what they search, what they post, what they react to — and converts that into structured signal data for Layer 2.

This is not demographic data. It is not survey data. It is live behavioral exhaust: the unfiltered, unscripted record of what humans are thinking about in real time.

---

## Data Sources

| Source | Signal Type | Weight in Platform | Why It Matters |
|---|---|---|---|
| Google Trends | Search intent by keyword/region | ~38% | 80% of global search, 136B monthly visits. This IS what people are thinking. |
| Twitter/X | Real-time emotional reaction, sentiment spikes | ~22% | Fastest signal for behavioural events (fear, panic, policy backlash) |
| Reddit | Deep discussion, niche community sentiment | ~15% | Higher signal-to-noise on specific topics (health anxiety, drug side effects, claims) |
| Meta Platforms | Passive engagement signals, demographic overlays | ~18% | Largest social graph; behavioural pattern consistency across age groups |
| fMRI / BCI Research | Neural circuit reference data | ~5% | Anchors population signals to neuroscience (Meta TRIBE v2, Harvard/Google brain maps) |
| Other signals | News, forums, search adjacency | ~2% | Edge signals for specific verticals |

---

## Why Google Trends Is the Core

Google controls approximately 80% of global search. Its Trends dataset spans 10–20 years of search history, is freely accessible, is structured by keyword and geography, and reflects what people are actively thinking about — not what they say they think in surveys.

For pharma: if people are searching "depression not responding to medication" in specific geographies, that is a cohort signal.
For insurance: if people are searching "flood risk home" or "chest pain at night" in high-claim zip codes, that is a risk event signal.
For public health: if people are searching "government can't be trusted" in swing regions, that is a policy response signal.

None of this requires individual identification. It is population-level by design.

---

## Privacy Architecture

- All data is aggregated at population level — no individual is ever tracked or identified
- Google Trends data is publicly available and aggregated by Google before it reaches MindMap
- Social media signals are processed at sentiment/keyword level, not user level
- This is the consent architecture: the platform never touches individual data
- EU AI Act (2026–2027 high-risk classification) compliance: MindMap's data layer does not trigger individual consent requirements because it does not process individual personal data

---

## What Layer 2 Receives

Layer 1 outputs structured time-series signal vectors:
- Keyword cluster → geographic region → time window → signal intensity
- Sentiment polarity (positive/negative/neutral) per topic cluster
- Behavioural trend velocity (rate of change, not just level)

These vectors feed directly into the quantum ML classification engine in Layer 2.

---

## Visual Reference
- See: `visuals/chart6-data-sources.png` — data source mix breakdown
- See: `visuals/chart3-platform-funnel.png` — how Layer 1 feeds into the full architecture
