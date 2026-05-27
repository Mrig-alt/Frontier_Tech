# MindMap Presentation — Full Build Brief
## For: Consultant / React Developer
## Project: IMBA 25J Frontier Technologies — Group Presentation
## Session 15 | IE Business School | May 2026

---

# TECHNICAL SETUP

- Framework: React (Vite) or Reveal.js
- Each slide: full viewport 100vw x 100vh
- Navigation: arrow keys + click, slide counter bottom right
- Theme: Dark navy #0F172A background, #7CD4FD electric blue accent, white text, Inter font
- Export: Single index.html via Vite build OR PDF export via Puppeteer
- Charts: Use recharts or react-chartjs-2 for all data visuals
- Images marked [ASSET: Ix] = drop in image file provided separately
- Screenshots marked [SCREENSHOT: Sx] = drop in screenshot file provided separately

---

# SLIDE 1 — TITLE

Layout: Full-bleed background image, centered overlay text

[ASSET: I1 — AI-generated brain/neural network, deep navy + electric blue nodes]

HEADLINE (H1, 52px, bold, white):
"MindMap"

SUBHEADLINE (H2, 28px, white):
"A Behavioral Signal Platform for Industry Disruption"

TAGLINE (H3, 18px, #7CD4FD):
"Mapping human behavior at scale — for Pharma, Insurance, and Public Health"

FOOTER (small, #94A3B8):
"IMBA 25J Frontier Technologies | IE Business School | Prof. Casimiro Juanes | May 2026"

---

# SLIDE 2 — THE PROBLEM

Layout: Header top + 3 equal cards side by side + 3 institutional proof logos at bottom

HEADER (H1, 36px, white):
"Three Industries. One Shared Blind Spot."

CARD 1 — Pharma (icon: 🔬):
Title: "Pharma Is Flying Blind"
Stat: "92% of drugs fail clinical trials"
Body: "Despite proven preclinical efficacy. The missing link: no real-time view of patient behavior before trials begin."
Source badge: "NIH / PMC, 2022"
[SCREENSHOT: S1 — NIH/PMC paper abstract screenshot]

CARD 2 — Insurance (icon: 🏦):
Title: "Insurance Looks Backwards"
Stat: "AI leaders get 6.1x total shareholder return vs laggards"
Body: "Most insurers still price risk using historical claims data — always reactive, never predictive."
Source badge: "McKinsey, Oct 2025"
[SCREENSHOT: S2 — McKinsey report cover screenshot]

CARD 3 — Public Health (icon: 🌍):
Title: "Public Health Is Always Late"
Stat: "1–2 weeks behind CDC outbreak detection"
Body: "Google Trends detected flu epidemics faster than official surveillance. Governments still use polls."
Source badge: "Ginsberg et al., Nature, 2009"
[SCREENSHOT: S3 — Nature paper abstract screenshot]

PREDATOR LINE (centered, italic, 20px, #7CD4FD, below cards):
"Google is already sitting on the most detailed map of human anxiety ever assembled.
The question is: who builds the bridge to the clinic before they do."

---

# SLIDE 3 — THE PLATFORM

Layout: Header + left column (architecture stack) + right column (data source pie chart)

HEADER (H1, 36px, white):
"MindMap — One Platform, Three Industries"

LEFT HALF — [CHART: chart7_architecture.png]
3-layer stack diagram:
- Layer 1 (bottom, dark navy): "BEHAVIORAL DATA INGESTION — Google Trends · ICD-10 · PubMed · WHO · Claims"
- Layer 2 (middle, blue): "QUANTUM ML ENGINE — IBM Willow 105 qubits · Hybrid models · Real-time inference"
- Layer 3 (top, electric blue): "PREDICTIVE OUTPUT — Trial success % · Risk scores · Outbreak alerts"
Arrows pointing upward between layers

RIGHT HALF — [CHART: chart6_datasources.png]
Pie chart: Google Trends 38%, ICD-10 22%, PubMed 18%, WHO Sentinel 12%, Claims Data 10%

CAPTION below right chart (14px, #94A3B8):
"Same behavioral data layer powers all three verticals"

---

# SLIDE 4 — WHY THESE THREE INDUSTRIES

Layout: Header + left half radar chart + right half 3 vertical mini-cards

HEADER (H1, 36px, white):
"The Logic Behind Each Vertical"

LEFT HALF — [CHART: chart4_radar.png]
Radar/spider chart, 6 axes, 3 series (Pharma, Insurance, Public Health)
Axes: Problem Severity, Data Availability, Willingness to Pay, Regulatory Fit, Time to Revenue, Strategic Proof Value

RIGHT HALF — 3 stacked mini-cards:

CARD 1 — Pharma:
"🔬 Pharma — The Validation Engine"
"If MindMap signals predict trial outcomes, pharma publishes the proof — every other industry follows."
Entry: "Behavioral cohort targeting for Phase II CNS trials"
Badge: ✅ LEAD VERTICAL

CARD 2 — Insurance:
"🏦 Insurance — The Secret Pilot"
"Runs internal pilot NOW — before pharma proof goes public — to build 3 years of proprietary data."
Entry: "Behavioral claims prevention model — AXA / Swiss Re"
Badge: ✅ COMMERCIAL ANCHOR

CARD 3 — Public Health:
"🌍 Public Health — The Scale Play"
"Governments already use polls and social listening. MindMap gives them real-time population sentiment."
Entry: "Government emotional intelligence platform"
Badge: ✅ SCALE VERTICAL

BOTTOM SEQUENCING DIAGRAM (3 boxes + arrows, full width):
[ Pharma validates ] → [ Insurance pilots in secret ] → [ Public Health scales ]
Caption: "Sequenced market entry — each stage de-risks the next"

---

# SLIDE 5 — THE TECHNOLOGY

Layout: Header + 3 icon cards top row + 2 institutional screenshots bottom row

HEADER (H1, 36px, white):
"Three Frontier Technologies — All Ready Now"

CARD 1 — Google Trends (icon: 🔍):
Title: "Behavioral Signal Layer"
Body: "136B monthly queries. 80% global search share. Already used by Federal Reserve and CDC as a leading indicator."
Proof: "Validated: Ginsberg et al., Nature, 2009"
[SCREENSHOT: S3 — Nature paper]

CARD 2 — Quantum ML (icon: ⚛️):
Title: "Quantum ML Engine"
Body: "IBM Willow chip (Dec 2024): 105 qubits. Solved a computation in under 5 minutes that would take a classical supercomputer 10 septillion years."
Proof: "Published: Nature, December 2024"
[ASSET: I3 — IBM Willow chip press photo]
[SCREENSHOT: S4 — Google Willow blog headline]

CARD 3 — Post-Quantum Crypto (icon: 🔐):
Title: "Post-Quantum Cybersecurity"
Body: "NIST released 3 finalized PQC standards August 2024 (FIPS 203/204/205). Quote: 'Can and should be put into use now.'"
Proof: "Mandated: NIST.gov, August 2024"
[SCREENSHOT: S5 — NIST press release headline]

BOTTOM ROW — 2 large institutional proof visuals side by side:
Left: [SCREENSHOT: S4 — Google Willow chip image from Google Blog]
Right: [SCREENSHOT: S5 — NIST PQC announcement page]

---

# SLIDE 6 — CYBERSECURITY

Layout: Header + before/after bar chart left + callout box right

HEADER (H1, 36px, white):
"Security Is the Foundation — Not a Feature"

LEFT — [CHART: chart5_hndl.png]
Before/after horizontal bar chart, 5 risk categories:
- Harvest Now Decrypt Later (HNDL): 9 → 2
- Data Breach (Patient/Client Records): 8 → 3
- Model Poisoning / Adversarial AI: 7 → 5
- Regulatory Non-compliance: 6 → 2
- API/Third-party Exposure: 7 → 3
Red bars = current threat. Blue bars = after PQC mitigation.

RIGHT — Callout box (#1E3A5F background, #7CD4FD border):
Title: "Real-World Cost of Inaction"
"Aurora Insurance breach: €180M–€460M exposure from unencrypted behavioral data."
"HNDL: Adversaries harvest encrypted data TODAY to decrypt when quantum matures ~2030."
"EU AI Act + GDPR: Fines up to 4% of global annual turnover."
"MindMap is built PQC-first — zero-trust, differential privacy, audit-ready from day one."

[ASSET: I4 — cybersecurity lock/shield AI image, top right corner]

---

# SLIDE 7 — MARKET OPPORTUNITY

Layout: Header + 3 KPI numbers top + grouped bar chart bottom

HEADER (H1, 36px, white):
"$82 Billion Market by 2030"

3 KPI CALLOUTS (large numbers, centered, side by side):
- "$9.3B" — label: "Total Addressable Market Today"
- "$82.3B" — label: "Projected by 2030"
- "44%" — label: "Average CAGR Across Verticals"

BOTTOM — [CHART: chart2_market.png]
Grouped bar chart, 2 bars per segment (2024 vs 2030):
- AI in Insurance: $4.5B → $45.7B
- Behavioral Risk Analytics: $2.1B → $18.3B
- AI Drug Discovery: $1.8B → $11.9B
- Public Health AI: $0.9B → $6.4B

---

# SLIDE 8 — GO-TO-MARKET

Layout: Header + funnel chart left + client targets right

HEADER (H1, 36px, white):
"From 5,000 Prospects to 12 Anchor Clients"

LEFT — [CHART: chart3_funnel.png]
Funnel top to bottom:
- Awareness: 5,000
- Interest: 1,200
- Evaluation: 300
- Pilot: 60
- Signed Contract (Year 1): 12

RIGHT — 3 target client rows:
Row 1: [ASSET: AXA logo] — "Behavioral underwriting pilot — claims prevention"
Row 2: [ASSET: Swiss Re logo] — "Actuarial model enrichment — behavioral risk layer"
Row 3: [ASSET: ECDC logo] — "Population health early-warning dashboard"

---

# SLIDE 9 — ROADMAP

Layout: Header + full-width 3-phase Gantt timeline

HEADER (H1, 36px, white):
"18-Month Path to Market"

[CHART: chart1_roadmap.png]
3 horizontal phases, color-coded:

H1 — Foundation (Jan–Jun 2026) [#1E3A5F]:
- Platform architecture build
- Google Trends + ICD-10 data partnerships
- Quantum ML proof of concept
- NIST PQC + zero-trust cybersecurity baseline

H2 — Pilot (Jul–Dec 2026) [#1D4ED8]:
- Pharma: clinical trial behavioral predictor (3 pilot clients)
- Insurance: behavioral underwriting module (AXA / Swiss Re)

H3 — Scale (Jan–Jun 2027) [#0EA5E9]:
- Public health early-warning dashboard (EU/govt contracts)
- Full post-quantum encryption rollout
- SOC 2 Type II certification

---

# SLIDE 10 — CALL TO ACTION

Layout: Header + 3 cards + closing line

HEADER (H1, 36px, white):
"We Are Looking For"

CARD 1 (icon: 🤝):
Title: "Pilot Partners"
Body: "1 pharma company · 1 insurer · 1 public health agency to co-develop and validate MindMap's behavioral signal layer"

CARD 2 (icon: 💰):
Title: "Seed Investment"
Body: "€2M to fund the 18-month roadmap to first paying revenue — platform build, data partnerships, quantum ML PoC"

CARD 3 (icon: 🧠):
Title: "Advisory Board"
Body: "Domain experts in quantum computing, insurance regulation, and EU AI Act compliance"

CLOSING LINE (H2, 28px, #7CD4FD, centered, bold):
"The data to predict the future already exists."
"MindMap connects the dots."

[ASSET: I1 — brain/neural image, subtle background]

---

# ASSET CHECKLIST

## Charts (PNG — all built, hand these over directly):
- chart1_roadmap.png       → Slide 9
- chart2_market.png        → Slide 7
- chart3_funnel.png        → Slide 8
- chart4_radar.png         → Slide 4
- chart5_hndl.png          → Slide 6
- chart6_datasources.png   → Slide 3
- chart7_architecture.png  → Slide 3
- chart8_industries.png    → Slide 4 (optional/backup)

## Images (team to source):
- I1: Brain/neural AI image — Midjourney prompt: "Abstract neural network brain map, deep navy background, glowing electric blue nodes, cinematic, no text, 16:9"
- I3: IBM Willow chip photo — https://newsroom.ibm.com (press kit)
- I4: Cybersecurity shield — Midjourney prompt: "Futuristic glowing digital padlock, dark navy background, electric blue light, post-quantum aesthetic, no text, 16:9"
- AXA logo — https://axa.com/en/press
- Swiss Re logo — https://swissre.com media center
- ECDC logo — https://ecdc.europa.eu

## Screenshots (15 min, grab these URLs):
- S1: https://pmc.ncbi.nlm.nih.gov/articles/PMC9293739/
- S2: https://insuranceasia.com/insurance/news/mckinsey-finds-insurers-lagging-peers-miss-out-ai-led-gains
- S3: https://www.nature.com/articles/nature07634
- S4: https://blog.google/innovation-and-ai/technology/research/google-willow-quantum-chip/
- S5: https://www.nist.gov/news-events/news/2024/08/nist-releases-first-3-finalized-post-quantum-encryption-standards

---

# SPEAKER NOTES

S1: "We're MindMap. We map human behavior at scale using Google search signals, quantum ML, and post-quantum security — to give pharma, insurers, and governments a real-time view of what people are actually thinking and feeling."

S2: "Three industries share one problem — they make billion-dollar decisions without knowing what humans are thinking right now. Pharma loses $3B per failed trial. Insurers miss 6x returns. Governments detect outbreaks weeks late. The data to fix this already exists."

S3: "MindMap sits between the raw behavioral signal and the industry decision. Three layers: ingest Google's behavioral map, run it through quantum ML, deliver a prediction. One platform, three industries, same data layer."

S4: "We chose these three verticals deliberately. Pharma validates the science first. Insurance runs a secret pilot now to get 3 years ahead of competitors. Public health is the scale play that follows."

S5: "All three technologies are ready now. Nature published Google Trends validation in 2009. IBM published the Willow quantum breakthrough in December 2024. NIST finalized post-quantum encryption standards in August 2024. The window is open."

S6: "Cybersecurity isn't a compliance checkbox — it's our core value proposition. Without PQC encryption, every insight we generate is a liability. The Aurora breach shows the real cost of inaction."

S7: "This is a $9.3B market today growing to $82B by 2030. We don't need to capture all of it — 12 anchor clients in Year 1 gets us to first revenue."

S8: "We're targeting AXA, Swiss Re, and the ECDC as our three anchor pilots. The funnel starts with 5,000 aware companies and filters to 12 signed contracts in Year 1."

S9: "The roadmap is sequenced to de-risk every stage. H1 builds the platform. H2 proves it with paying pilots. H3 scales globally."

S10: "We're looking for three things: pilot partners, seed investment, and advisors. The data exists. The technology is ready. We just need to build the bridge."
