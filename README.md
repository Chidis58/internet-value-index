# 🌍 Internet Value Index (IVI)

> **Measure what your internet can actually do — not just how many GB you bought.**

Internet Value Index (IVI) is an open data platform that quantifies the **real cost, usability, and reliability** of internet access across countries and ISPs.

Inspired by platforms like CoinGecko, IVI provides **transparent, comparable, and model-driven insights** into internet value globally.

---

## 🧠 Overview

Telecom pricing is typically expressed in gigabytes (GB), but users experience the internet in **actions**:

- searching
- streaming
- messaging
- browsing

IVI converts abstract data plans into **real-world usage metrics**, enabling meaningful comparisons across regions and providers.

---

## 🎯 Objective

> Standardize how internet value is measured by combining price, performance, and usability into clear, comparable metrics.

---

## ❗ Problem Statement

In many markets (e.g. Nigeria, India, Brazil), users face:

- **Perceived rapid data depletion** — widely reported but not well quantified  
- **Poor cross-market comparability** — difficult to evaluate value across ISPs or countries  
- **Lack of usage-based metrics** — GB does not reflect real-world usage  
- **Hidden value loss** — due to throttling, expiry, downtime, or QoS variability  

There is currently no widely adopted system that aggregates these into **standardized, comparable indicators**.

---

## 💡 Key Concepts

### 1. Cost per Action
Translate data plans into estimated user actions:

- cost per search  
- cost per minute of video  
- cost per messaging session  

---

### 2. Effective Cost per GB
Adjust advertised pricing based on real-world usability:

Effective $/GB = Price ÷ (Advertised GB × (1 − loss factor))

---

### 3. Value Loss Index
Percentage of paid data that becomes unusable:

Value Loss (%) = (Lost Data ÷ Purchased Data) × 100

---

### 4. Predictability & Transparency Score
Composite indicator based on:

- billing clarity  
- expiry behavior  
- throttling disclosure  
- compensation practices  

---

## 🧪 Modeling Assumptions (MVP)

Initial estimates (subject to refinement):

- Google search: ~0.5–2 KB  
- Text message (e.g. WhatsApp): ~1–5 KB  
- 1 minute video:
  - SD: ~3–5 MB  
  - HD: ~5–10 MB  
- Ping request: ~64 bytes  

> ⚠️ These are approximations. Actual usage varies based on device, app behavior, compression, and network conditions.

---

## 🧩 MVP Scope

### Phase 1 — Core Dataset
- Country + ISP pricing
- Data volume
- Currency normalization (local + USD)
- $/GB baseline
- Basic QoS (speed, latency where available)

---

### Phase 2 — Cost per Action Calculator
User inputs:
- plan price
- data volume

Outputs:
- estimated searches
- video minutes
- messaging capacity

---

### Phase 3 — Basic Scoring
- Cost efficiency ranking
- Preliminary QoS-adjusted value score

---

## 🏗️ Architecture (High-Level)

### Data Sources
- ISP pricing (manual + scraped)
- Exchange rate APIs
- Public QoS datasets
- User-contributed reports (future)

---

### Processing Layer
- Normalize prices → USD
- Compute cost per byte
- Derive cost per action
- Apply adjustment factors:
  - loss factor
  - QoS factor

---

### Output Layer
- Comparison tables
- Rankings
- Dashboards
- Exportable datasets

---

## 📊 Core Metrics

| Metric | Description |
|------|------------|
| $/GB | Price ÷ advertised data |
| Cost per Action | Estimated cost of user actions |
| Effective $/GB | Adjusted for loss and QoS |
| Value Loss Index | % unusable data |
| Predictability Score | Reliability of billing & access |

---

## 🚫 Non-Goals (MVP)

- Real-time packet inspection  
- ISP internal auditing  
- Exact per-user billing verification  

IVI provides **modeled, comparative insights**, not forensic telecom analysis.

---

## 🎯 Target Users

- Consumers — understand plan value  
- Analysts — compare markets  
- Journalists — data-backed reporting  
- Regulators — benchmark performance  

---

## 🚀 Why This Matters

IVI transforms:

| From | To |
|------|----|
| Abstract pricing | Real-world usability |
| Anecdotal complaints | Measurable data |
| Fragmented information | Standardized comparison |

---

## 📁 Repository Structure
internet-value-index/ 
├── data/          # Pricing datasets, exchange rates 
├── models/        # Cost-per-action + adjustment logic 
├── api/           # Computation endpoints ├── web/           # Frontend dashboard ├── scripts/       # Data ingestion / updates 
└── docs/          # Methodology

---

## 🤝 Contributing

We welcome contributions in:

- Data collection (ISP plans)
- Model refinement
- UI/dashboard development

More details in CONTRIBUTING.md (coming soon).

---

## 📄 License

MIT License

---

## 🪧 One-Line Definition

> A platform that quantifies how much real internet value users get for their money.
