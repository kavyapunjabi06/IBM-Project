# IBM - Project (BM 380)
# Customer Churn Analysis

## Project Description
This project analyses a customer dataset (`Churn Modelling.csv`) to understand who is leaving the bank, where, and why[cite: 1]. The same dataset is explored through three tools, each with a different purpose[cite: 1]:

| Tool | What it does |
| :--- | :--- |
| **Excel** | Tabular insights: churn percentage by different categories (geography, age group, gender, etc.)[cite: 1] |
| **Python** | Visualization of the analysis in the form of charts (`pandas` + `matplotlib`)[cite: 1] |
| **Power BI / BI tool** | A summed-up, insightful dashboard of the whole dataset for quick decision-making[cite: 1] |

The goal is to find the baseline churn rate, spot high-risk customer segments, and shortlist the factors worth investigating first so that retention efforts can be targeted[cite: 1].

---

## Dataset
- **File:** `Churn Modelling.csv`[cite: 1]
- **Target column:** `Exited` (0 = customer stayed, 1 = customer left)[cite: 1]
- **Key columns used:** `Geography`, `Age`, `Balance`, and other numeric fields[cite: 1]
- A helper column `Churn_Status` is created in Python (0 -> Not Exited, 1 -> Exited) so charts show labels instead of numbers[cite: 1].

---

## Project Structure

```text
├── Churn Modelling.csv                                   # Dataset
├── churn_analysis.py                                     # Python script (charts)
├── churn_analysis.xlsx                                   # Excel: churn by category
├── churn_dashboard.pbix                                  # BI dashboard
├── Line_by_Line_Code_Guide_and_Chart_Applications.pdf
└── README.md
```
*(Rename files to match your actual project.)*[cite: 2]

---

## Python Charts and Their Use Cases
The script produces a 2×2 figure (Plots 1–4) and one separate chart (Plot 5)[cite: 2].

### Plot 1: Overall Churn (Bar chart)
- **Question it answers:** What share of customers is leaving?[cite: 2]
- **Use case:** Gives the baseline retention rate and shows the class imbalance in the data, before digging into reasons[cite: 2]. Important when building prediction models, since a model can look accurate just by always guessing "stays"[cite: 2].

### Plot 2: Churn by Geography (Grouped bar chart)
- **Question it answers:** Where is churn worst?[cite: 2]
- **Use case:** Geographic segment analysis[cite: 2]. If one country's Exited bar is disproportionately high versus its own Not Exited bar, the problem is local (competitors, service, pricing) and not company-wide[cite: 2].

### Plot 3: Age Distribution by Churn Status (Overlapping histograms)
- **Question it answers:** Which age groups are leaving?[cite: 2]
- **Use case:** Demographic profiling[cite: 2]. If leavers are older, use relationship-led retention offers; if younger, focus on engagement and onboarding[cite: 2].

### Plot 4: Account Balance by Churn Status (Box plot)
- **Question it answers:** Are we losing high-value clients?[cite: 2]
- **Use case:** Shows the financial impact of churn[cite: 2]. A higher box for "Exited" means leavers hold more money, so they are the top priority for personal outreach by relationship managers[cite: 2].

### Plot 5: Correlation of Features with Churn (Horizontal bar chart)
- **Question it answers:** Which factors drive churn?[cite: 2]
- **Use case:** Driver analysis for executives[cite: 2]. Bars pointing right increase churn, bars pointing left decrease it[cite: 2]. Longer bar = stronger relationship[cite: 2]. Ignore ID-style columns (row number, customer ID) and remember that correlation is not causation[cite: 2, 3].

---

## Summary

| Chart | Type | Business use |
| :--- | :--- | :--- |
| **Overall Churn** | Bar | Sets baseline retention target[cite: 3] |
| **By Geography** | Grouped bars | Targets regional fixes and campaigns[cite: 3] |
| **Age** | Overlapping histograms | Shapes marketing and retention offers[cite: 3] |
| **Balance** | Box plot | Prioritizes personal outreach[cite: 3] |
| **Correlation** | Horizontal bars | Guides where to investigate first[cite: 3] |

---

## Key Takeaways
- Establish the overall churn rate first, then segment it by geography, age, and balance[cite: 3].
- Focus retention effort on the segments with the highest churn and highest balances[cite: 3].
- Use the correlation chart to decide which variables to study in more depth[cite: 3].

---

## Team
**- Kavya Punjabi**\
**- Mohammed Sadiq Siddique**\
**- Asad Usman**\
**- Mohd Sajjad Ansari**
