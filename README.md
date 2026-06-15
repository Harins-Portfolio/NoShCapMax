# Operational Capacity Optimization Audit: Business Intelligence & Exploratory Data Architecture

[![Project Status: Completed Audit](https://img.shields.io/badge/Project%20Status-Completed%20Audit-blue.svg)](https://github.com/your-username/no-show-audit)
[![Core Stack: Python](https://img.shields.io/badge/Stack-Python%20%7C%20Pandas%20%7C%20Seaborn-blue.svg)]()
[![Methodology: CRISP-DM](https://img.shields.io/badge/Methodology-CRISP--DM%20%2F%20DAMA--5-orange.svg)]()
[![Language: Spanish Codebase](https://img.shields.io/badge/Language-Spanish%20Codebase-red.svg)]()

---

## ⚠️ Language & Execution Notice / Nota de Idioma
> **Note for Recruiters & Clients:** The architectural overview and documentation are written in English. However, the source code, inline notebook commentary, and underlying data-canvas artifacts are completely developed in **Spanish**, matching the native enterprise operational framework utilized during this executive business audit.

---

## 1. Executive Commercial Executive Summary
Unscheduled appointment vacancies result in severe operational capacity wastage, underutilized medical personnel, and artificially inflated patient wait times. When **20.2%** of an organization's booking volume fails to materialize without prior notification, it directly leaks predictable revenue windows.

**Important Project Scope Clarification:** This repository does *not* deploy predictive machine learning classification models. Instead, it serves as a rigorous, end-to-end **Data Exploration & Business Optimization Audit (CRISP-DM Phases 1–3)**. It focuses on transforming a messy database of over 110,000 bookings into clean, structural, and actionable evidence loops that decision-makers can read in under 30 seconds.

---

## 2. Core Project Milestones & Directory Map

The analytical lifecycle travels through a strict step-by-step evolution across the folders:

* **📁 `core_notebooks/` (Classroom Analytical Blueprint):**
  * **S01 - Problem Framing:** Translating organizational losses into a measurable KPI matrix and initial PECO hypotheses.
  * **S02 - Tabular Foundations:** Opening the framework at scale with `pandas` to expose initial structural behaviors.
  * **S03 - Data Preparation:** Encapsulating messy, ad-hoc transformations into reproducible pipelines.
  * **S04 - Visual Storytelling:** Grouping tabular metrics into target visual patterns for executive presentation.
* **📁 `docs/` (Strategic Iteration Canvas):**
  * Tracks the evolutionary growth of the `Project Canvas` (v1 to v3), documenting how business assumptions shifted as raw numbers surfaced.
* **📁 `production_scripts/` (Independent Validation Asset):**
  * **`EDA_NoShow_Harins_Final.ipynb`**: My individual, unguided technical assessment executed on an entirely fresh subset of 20,050 real-world entries, proving end-to-end extraction autonomy.

---

## 3. Structural Data Quality Discoveries (DAMA-5 Framework)
Before conducting any diagnostic visualization, the raw dataset was audited against strict enterprise data governance guidelines, revealing critical structural vulnerabilities:

1. **Validez (Validity Errors):** Identified chronological logic anomalies where `AppointmentDate` timestamps occurred *prior* to their corresponding registration `ScheduledDate` entries. These entries were dynamically isolated to avoid calculating distorted waiting times.
2. **Consistencia (Inverted Formats):** Fixed the target vector variable `No-show` (`"Yes"` structurally indicated non-attendance/absence), transforming it into a clean, normalized evaluation metric.

---

## 4. Key Diagnostic Insights & Strategic Action Loops
By isolating variables on the independent assessment dataset, the following core behavioral drivers were uncovered:

* **The Administrative Lag Boundary:** Patients forced to navigate booking windows exceeding **14 days** exhibited a dramatic spike in absenteeism, resulting in an approximate **32.7% No-Show rate** compared to just **16.0%** for immediate-response slots.
* **The Demographics Variance:** Absenteeism is highly clustered by demographic lines; adolescent and young adult brackets represent high-risk windows (~26.6%), whereas senior cohorts stabilize at a highly reliable ~15.5% marker.

### Executive Recommendation Loop:
Instead of throwing capital at unsegmented automated alert notifications, the enterprise should execute a tiered mitigation plan: deploy targeted, confirmation-mandatory SMS alert sequences and priority manual phone follow-ups exclusively for high-risk cohorts (adolescent demographics crossing the 14-day administrative wait threshold).

---

## 5. Environment & Technical Dependencies
* **Engine Environment:** Python 3.10+ | Jupyter Notebooks / Google Colab Environment
* **Core Core Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`

---
## 6. Contact & Consulting Strategy
Developed by **Nikhil Harins** — Madrid, ES.  
* **LinkedIn:** [linkedin.com/in/nikhilharins](https://linkedin.com/in/nikhilharins)
* **Portfolio Hub:** [Link to your Reflex App Website]
