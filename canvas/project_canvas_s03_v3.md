# Analytical Project Canvas: Operational Capacity Optimization
> **Artifact Version:** v3.0 (Data Preparation & Operational Enrichment)  
> **Course Module:** Data Science Applied to Business (Session S03)  
> **Author:** Nikhil Harins | **Date:** May 24, 2026

---

## 1. Business Problem Statement
*(No changes from v1.0/v2.0; baseline absenteeism is locked at 20.2%)*

---

## 2. Metric Architecture & Baseline Performance
* **Primary KPI:** Appointment No-Show Rate ($tasa\_no\_show$)  
* **Operational Performance Baseline:** **20.2%** across 110,521 valid observations.

---

## 3. Engineering a Reproducible Pipeline (CRISP-DM: Data Prep)
Instead of relying on isolated, manual steps, all data transformations from Session S02 were consolidated into a single, automated, and production-ready function: `prepare_basic(df)`.

* **Structural Dimensions Expanded:** The dataset was expanded from 14 raw variables to **24 processed columns**.
* **Patient Volume Tracking:** Isolated **62,298 unique patients** across the 110,521 scheduled events, unlocking future capability to track repeat-offender behavioral patterns.
* **Feature Engineering Inventions:**
  1. `LongWait`: A binary flag ($0$ or $1$) dividing wait vectors exactly at the 14-day administrative boundary.
  2. `AgeGroup`: Categorical clustering of raw age integers into specific life stages (`Children`, `Adolescents`, `Adults`, `Seniors`).
  3. `Neighbourhood_NoShowRate`: An advanced feature that groups rows by geographic location and calculates the historical regional baseline rate.

---

## 4. Empirical Evidence & Multi-Variable Hotspots
With the feature engineering pipelines fully deployed, data aggregation queries revealed concrete demographic and geographic patterns:

### H1: The Age-Cohort Risk Distribution
* **Adolescents Segment:** Exhibits the absolute highest behavioral risk, with an alarming **26.6% No-Show rate**.
* **Seniors Segment:** Represents the most stable corporate anchor, dropping to a highly reliable **15.5% No-Show rate**.

### H2: Geographic Risk Mapping (The "Neighborhood Effect")
To prevent small sample sizes from distorting corporate strategy, an enterprise filtering rule was applied: **Minimum sample size of 50 bookings ($min\_n \ge 50$)** with an absenteeism threshold set at **22%**.
* **The Discovery:** Isolated exactly **16 geographic hotspot neighborhoods** operating with systemic, high-risk absence rates well above the clinic network's average baseline.

---

## 5. Prioritized Hypotheses for Visual Validation
These multi-variable discoveries dictate our visual strategy for the upcoming milestone (Session S04):

| ID | Targeted Operational Hypothesis | Tabular Base Evidence (S03) | Proposed Visual Plot Type (S04) |
| :--- | :--- | :--- | :--- |
| **H1** | Wait windows heavily accelerate capacity waste. | 16.0% (Agile) vs 32.7% (Long Wait). | Bar Chart (By WaitingBin arrays) |
| **H2** | Age modulates risk, but administrative wait determines outcome. | 26.6% (Adolescents) vs 15.5% (Seniors). | Matrix Heatmap (`AgeGroup` x `WaitingBin`) |
| **H3** | High-risk hotspots require targeted operational intervention. | 16 statistically reliable hotspot areas found. | Horizontal Ranking Bar Chart ($min\_n \ge 50$) |

---

## 6. Evolving B2B Solution Logic & Operational Limits
* **Refined Strategic Recommendation:** The clinic must stop treating its calendar uniformly. We recommend implementing high-touch manual confirmation sequences and priority telephone routing rules targeted explicitly at **Adolescent cohorts booking appointments in the 16 identified geographic hotspots with wait times exceeding 7 days**.
* **Milestone Limitation:** These insights are built on observational data combinations. Because the current SMS reminder deployment strategy is heavily biased (reactive rather than proactive), we cannot definitively prove causality without clean visual charts and statistical significance modeling.
