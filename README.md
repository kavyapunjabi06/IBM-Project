# IBM - Project (BM 380)
# Customer Churn Analysis

## Project Description
This project analyses a customer dataset (`Churn Modelling.csv`) to understand who is leaving the bank, where, and why. The same dataset is explored through three tools, each with a different purpose:

| Tool | What it does |
| :--- | :--- |
| **Excel** | Tabular insights: churn percentage by different categories (geography, age group, gender, etc.) |
| **Python** | Visualization of the analysis in the form of charts (`pandas` + `matplotlib`) |
| **Power BI / BI tool** | A summed-up, insightful dashboard of the whole dataset for quick decision-making |

The goal is to find the baseline churn rate, spot high-risk customer segments, and shortlist the factors worth investigating first so that retention efforts can be targeted.

---

## Dataset
* **File:** `Churn Modelling.csv`
* **Target column:** `Exited` (0 = customer stayed, 1 = customer left)
* **Key columns used:** `Geography`, `Age`, `Balance`, and other numeric fields
* A helper column `Churn_Status` is created in Python (0 -> Not Exited, 1 -> Exited) so charts show labels instead of numbers.

---

## Project Structure

```text
├── Churn Modelling.csv                                   # Dataset
├── churn_analysis.py                                     # Python script (charts)
├── churn_analysis.xlsx                                   # Excel: churn by category
├── churn_dashboard.pbix                                  # BI dashboard
├── Line_by_Line_Code_Guide_and_Chart_Applications.pdf
└── README.md
### Team  
Kavya Punjabi  
Mohammed Sadiq Siddique  
Asad Usman  
Mohd Sajjad Ansari
