# StreamPro – User Engagement & Drop-off Analysis

This repository contains a take-home data analysis assignment for the **StreamPro** video-streaming platform.

The goal of the analysis is to understand early user engagement, identify drop-off points in the first session, and evaluate whether engagement issues are driven by content, device, or app version.

---

## 📌 Business Questions

The analysis answers the following questions:

1. **Q1:** What percentage of new users reach at least **30 seconds of watch time** in their **first session**?
2. **Q2:** Which factors (device, content genre) correlate with higher first-session engagement?
3. **Q3:** Is there a particular **device OS or app version** where early drop-off is abnormally high?

---

## 🗂 Data Sources

The notebook uses four input datasets:

- `events.jsonl` – raw user event logs (session_start, watch_time, reactions, session_end)
- `users.csv` – user attributes (signup date, subscription tier, demographics)
- `videos.csv` – video metadata (genre, duration)
- `devices.csv` – device metadata

---

## 🏗 Approach & Design

- Analysis is implemented in a **single Jupyter Notebook** for clarity and reproducibility
- Data is processed using a simplified **Bronze → Silver → Gold** pattern:
  - **Bronze:** raw data loading and inspection
  - **Silver:** data cleaning, typing, and enrichment
  - **Gold:** session-level metrics and analytical models
- Emphasis is placed on:
  - correctness of metrics
  - transparency of assumptions
  - honest handling of sparse data

---

## 📊 Key Findings (Summary)

- Only **~2% of users** reach 30 seconds of watch time in their first session
- Median first-session watch time is under **10 seconds**, indicating very early disengagement
- Engagement differences by device are minor
- App-version-level analysis is **inconclusive** due to very small sample sizes per version
- Early drop-off appears to be a **systemic onboarding or content issue**, not tied to a specific platform

---

## ⚠️ Data Limitations

- High-engagement first sessions (≥30s) are rare, limiting statistical power
- App version analysis is constrained by sparse data
- Results should be interpreted as directional rather than causal

---

## ▶️ How to Run

1. Clone the repository
2. Install dependencies (Anaconda / pandas / matplotlib)
3. Open the notebook in Jupyter
4. Run all cells top-to-bottom

---

## 📁 Repository Structure

```
.
├── data/
│   ├── events.jsonl
│   ├── users.csv
│   ├── videos.csv
│   └── devices.csv
└── notebook/
    └── streampro_assignment.ipynb
```

---

## ✅ Notes

This project focuses on **analytical thinking and data modeling decisions**, not production infrastructure.
