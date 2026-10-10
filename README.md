# IBM - Project (BM 380)

# Customer Churn Analysis

## Project Description

This project analyses a customer dataset (`Churn Modelling.csv`) to understand who is leaving the bank, where, and why. The same dataset is explored through three tools, each with a different purpose:

| Tool | What it does | 
| ----- | ----- | 
| **Excel** | Tabular insights: churn percentage by different categories (geography, age group, gender, etc.) | 
| **Python** | Visualization of the analysis in the form of charts (`pandas` + `matplotlib`) | 
| **Power BI / BI tool** | A summed-up, insightful dashboard of the whole dataset for quick decision-making | 

The goal is to find the baseline churn rate, spot high-risk customer segments, and shortlist the factors worth investigating first so that retention efforts can be targeted.

## Dataset

* **File:** `Churn Modelling.csv`

* **Target column:** `Exited` (0 = customer stayed, 1 = customer left)

* **Key columns used:** `Geography`, `Age`, `Balance`, `NumOfProducts`, `IsActiveMember`, and other numeric fields

* A helper column `Churn_Status` is created in Python (0 -> Not Exited, 1 -> Exited) so charts show labels instead of numbers.

## Project Structure

```
├── Churn Modelling.csv                    # Dataset
├── churn_analysis.ipynb                   # Python script (charts)
├── churn_analysis.xlsx                    # Excel: churn by category
├── churn_dashboard.pbix                   # BI dashboard
├── Churn_Dashboard_Report.pdf             # Executive Power BI analysis report
└── README.md

```

## Problem Statement

The institution manages **10,000 retail banking accounts** representing **₹76.49 Crore** in total deposit capital, with an aggregate attrition rate of **20.37% (2,037 exited accounts)**.

The primary business challenge is that attrition is heavily skewed toward high-value and specific demographic cohorts rather than being uniformly distributed:

* **Severe Capital Outflow:** Exited accounts carried higher average balances (₹91,108.54) than retained accounts (₹72,745.30), generating an aggregate liquidity drain of **₹18.56 Crore** (24.26% of all portfolio deposits).

* **Extreme Multi-Product Backlash:** Customers holding 3 or 4 products churn at **82.71%** and **100.00%**, respectively, pointing to severe bundling friction and fee fatigue.

* **Regional Disparity:** Customers in Germany experience an acute churn rate of **32.44%**—almost double the rates observed in France (16.15%) and Spain (16.67%)—representing 48% of all lost capital.

* **Mid-Life Wealth Attrition:** Customer attrition escalates rapidly among mature demographics, hitting **33.97%** for ages 41–50 and **56.21%** for ages 51–60.

* **Inactivity Risk:** Inactive accounts exhibit nearly double the churn rate of active accounts (**26.85% vs. 14.27%**), accounting for **₹11.78 Crore** of the lost capital.

## Solution Statement

To arrest the ₹18.56 Crore capital outflow and drive the institutional churn rate from 20.37% down toward top-quartile benchmarks ($\le$ 13.50%), the solution pairs a multi-tool diagnostic pipeline with a targeted, 4-pillar retention framework:

1. **Interactive Analytics & Risk Intelligence:** Leverage Power BI (`churn_dashboard.pbix`) with dedicated Executive, Diagnostic, and Operational drill-through pages to isolate high-risk customer cohorts in real time.

2. **Product De-Cluttering & Bundling Alignment:** Shift focus from aggressive 3+ product cross-selling to the institutional "2-Product Golden Rule" (which exhibits the lowest portfolio churn rate at **7.58%**).

3. **Regional & Wealth Segment Remediation:** Deploy competitive deposit yields and fee waivers in Germany, along with dedicated Relationship Managers and wealth preservation instruments for customers aged 41–60.

4. **Automated CRM Early-Warning System (EWS):** Configure proactive 30- and 45-day inactivity alerts and retention concessions to re-engage dormant accounts before formal exit occurs.

## Team

* **Kavya Punjabi**

* **Mohammed Sadiq Siddique**

* **Asad Usman**

* **Mohd Sajjad Ansari**
