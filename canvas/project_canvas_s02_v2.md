# Analytical Project Canvas: Operational Capacity Optimization
> **Artifact Version:** v2.0 (Tabular Evidence Update)  
> **Course Module:** Data Science Applied to Business (Session S02)  
> **Author:** Nikhil Harins | **Date:** May 23, 2026

---

## 1. Business Problem Statement
*(No changes from v1.0)*

---

## 2. Metric Architecture & Baseline Performance
* **Primary KPI:** Appointment No-Show Rate ($tasa\_no\_show$)  
* **Historical Baseline Status:** Confirmed at **20.2%** across the verified operational subset.

---

## 3. Structural Data Inventory & Audit (DAMA-5 Execution)
Following high-scale database execution using `pandas`, the row-by-row data profiling yielded concrete figures, eliminating initial uncertainty:

* **Raw Total Volume:** 110,527 appointments.
* **Clean Analyzable Volume (`df_analysis`):** 110,521 rows (6 critical anomalies programmatically dropped).
* **DAMA-5 Data Quality Rectifications:**
  * **Validity Failures (Age):** Isolated 1 row showing a negative age value (`Age < 0`).
  * **Validity Failures (Chronology):** Isolated 5 rows displaying corrupted timestamps where the appointment preceded the booking action (`WaitingDays < 0`).
  * **Consistency Normalization:** Programmatically converted the native categorical column into a boolean vector mapping directly to absolute business states.

---

## 4. Empirical Tabular Evidence (Testing the Framework)
Using localized aggregation queries (`groupby`), your initial business hypotheses were exposed to direct tabular validation:

### H1: Administrative Lag (The Booking Window Effect)
* **Agile Windows ($\le$ 14 days delay):** Yields a reliable **16.0% No-Show rate**.
* **Prolonged Windows (> 14 days delay):** Absenteeism spikes heavily to a **32.7% No-Show rate**.
* **Tabular Insight:** Crossing the 14-day boundary results in a massive **+16.7 percentage point increase** in unfulfilled operational capacity.

### H2: The Communication Leak Paradox (SMS Analysis)
* **No Reminder Sent (`SMS_received = 0`):** Results in a **16.7% No-Show rate**.
* **Reminder Sent (`SMS_received = 1`):** Results in a **27.6% No-Show rate**.
* **Critical Discovery Alert:** This counterintuitive shift exposes a classic corporate **Selection Bias**. Reminders are not failing; management is systematically sending text alerts to long-wait bookings that already possess an inherently high baseline risk of skipping their appointment.

---

## 5. Refined Operational Hypothesis (PECO v2)
* **Unified Statement:** Long wait delays (>14 days) represent the core structural driver of clinic underutilization (+16.7 p.p. risk over agile slots). Automated SMS distribution systems currently follow a reactive deployment path that masks true behavioral performance, requiring a controlled multi-variable matrix analysis in upcoming cycles.

---

## 6. Evolving Decision Logic & Boundaries
* **Strategic Pivot:** Instead of evaluating the entire database uniformly, administrative actions must be split. The 14-day scheduling threshold is now mathematically validated as a business danger zone.
* **Milestone Limitation:** While our tabular slices confirm heavy variance, we have not built visual distribution charts or calculated neighborhood geographic effects. Recommending a hard system configuration rewrite is restricted until data preparation steps are fully locked in.
