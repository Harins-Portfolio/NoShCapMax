# Analytical Project Canvas: Operational Capacity Optimization
> **Artifact Version:** v1.0 (Initial Alignment Framework)  
> **Course Module:** Data Science Applied to Business (Session S01)  
> **Author:** Nikhil Harins | **Date:** May 23, 2026

---

## 1. Business Problem Statement
An estimated 20.2% of patients booking appointments across the localized clinic network fail to show up for their scheduled slots without prior notice. This systemic absenteeism creates massive clinical capacity wastage, leaves expensive medical personnel underutilized, and artificially inflates waiting lists for patients in critical need of immediate care.

---

## 2. Metric Architecture & Baseline Performance
* **Primary KPI:** Appointment No-Show Rate ($tasa\_no\_show$)
* **Mathematical Formula:** $$\text{No-Show Rate} = \frac{\text{Non-Attended Appointments}}{\text{Total Scheduled Appointments}}$$
* **Historical Benchmark Baseline:** **20.2%** (22,319 missed slots out of 110,527 raw records).

---

## 3. Structural Data Inventory
* **Unit of Observation:** A single scheduled clinical appointment event.
* **Target Vector ($Y$):** `No-show` (Categorical String: `"Yes"` structurally maps to a non-attendance outcome).
* **Critical Candidate Attributes:** `Age` (Patient age), `ScheduledDate` (Log entry timestamp), `AppointmentDate` (The actual visit date), `SMS_received` (Text alert confirmation flag).
* **Proposed Derived Vector:** `waiting_days` (Administrative wait delta: `AppointmentDate` minus `ScheduledDate`).
* **Strategic Missing Dimensions Requested:** Patient-to-clinic commute distance (km), historical patient cancellation logs, and macro weather conditions on the appointment date.

---

## 4. Enterprise Data Governance Risks (DAMA-5)
* **Validity Dimension Risk:** Preliminary inspection suggests chronological anomalies where an `AppointmentDate` could be registered *prior* to its `ScheduledDate`, leading to a corrupt negative waiting delta. These rows must be isolated.
* **Consistency Dimension Risk:** The native target vector is counterintuitively encoded (`No-show = "Yes"` indicates an absence). This requires strict normalization in early pipeline stages to protect downstream business logic.

---

## 5. Structured Operational Hypothesis (PECO Framework)
* **P (Population):** Active patients booking appointments within the clinical facility network.
* **E (Exposure Delta):** Prolonged administrative booking delays exceeding a critical window (`waiting_days > 14`).
* **C (Comparison Base):** Agile, short-term scheduling turnaround windows (`waiting_days <= 14`).
* **O (Expected Outcome):** A statistically significant expansion in absenteeism relative to the historical baseline.

> **Unified Synthesis Statement:** We will evaluate whether scheduling clinical appointments with a lag exceeding 14 days causes a dramatic spike in absenteeism compared to agile booking cycles of under two weeks, isolating `waiting_days` as our primary candidate feature.

---

## 6. Candidate Operational Decision & Boundaries
* **Proposed Action:** If empirical evidence validates the threshold, administrative routing rules will automatically trigger mandatory telephone confirmation loops and high-priority SMS sequences exclusively for accounts crossing the 14-day delay margin.
* **Milestone Limitation:** At this initial stage (S01), the project scope is purely descriptive on paper. No data processing pipelines or probabilistic correlations have been validated in code.
