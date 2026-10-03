# Data Analytics Task 1 — Customer Churn Analysis

## Decision question
Which customer groups should a fictional subscription team contact first to reduce avoidable churn?

## Project contents
- `customer_churn_analysis.ipynb` — complete profiling, cleaning, validation, exploratory analysis, and recommendation.
- `customer_churn_sample.csv` — supplied raw dataset.
- `customer_churn_clean.csv` — cleaned dataset.
- `data_dictionary.csv` — field definitions and quality notes.
- `numeric_summary.csv` — descriptive statistics.
- `outlier_check.csv` — IQR outlier screening.
- `*_churn_summary.csv` — churn summaries by category.
- PNG files — simple exploratory charts.

## Data quality decisions
- 15 rows and 11 columns were supplied.
- No missing values were found.
- No duplicate rows or duplicate CustomerID values were found.
- Text values were trimmed and churn labels standardized.
- Age, tenure, monthly charges, and support-ticket counts were checked for impossible values.
- IQR screening found no extreme outliers.
- `TotalCharges` matched `MonthlyCharges × TenureMonths` within ₹0.01 for every row.
- No rows were silently deleted.

## Initial findings
- 7 of 15 customers churned (46.7%).
- Month-to-month: 7/7 churned (100%).
- One-year: 0/4 churned.
- Two-year: 0/4 churned.
- Basic: 5/7 churned (71.4%).
- Churned customers averaged 4.29 support tickets vs 1.00 for non-churned customers.
- Churned customers averaged 7.0 months tenure vs 29.13 months for non-churned customers.

## Recommendation
**Audience:** fictional retention/support team.

**Decision:** Prioritize month-to-month customers, especially those with short tenure and higher recent support-ticket counts.

**Uncertainty:** This is a very small synthetic sample (15 records). The patterns are descriptive, not causal or predictive, and may not generalize.

**Next measurement:** With a larger real dataset, measure monthly churn by contract type and test whether targeted retention outreach reduces churn.

## How to run
Open `customer_churn_analysis.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab. Keep the CSV in the same folder.
