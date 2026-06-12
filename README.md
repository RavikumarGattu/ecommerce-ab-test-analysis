# E-Commerce A/B Test Analysis
## Does Q4 Holiday Season Drive Higher Purchasing Behavior?

**Author:** Ravikumar Gattu  
**Dataset:** UCI Online Retail II (UK-based retailer, 2009-2011)  
**Tools:** Python, pandas, scipy, statsmodels, matplotlib, seaborn

---

## Project Overview
This project analyzes purchasing behavior differences between 
Q4 (holiday season) and non-Q4 customers for a UK-based 
online retailer using an A/B test framework.

**Key Finding:** Q4 customers generate **75.5% more revenue 
per customer per month** than non-Q4 customers — confirmed 
with 99.98% statistical confidence (p=0.0002).

---

## Business Question
Does the Q4 holiday season drive significantly higher 
purchasing behavior compared to Q1-Q3?

## Hypothesis
- **H0:** Q4 customers spend the same as non-Q4 customers
- **H1:** Q4 customers spend more than non-Q4 customers

## A/B Groups
- **Control:** Customers who purchased in Q1, Q2, Q3
- **Test:** Customers who purchased in Q4

---

## Key Results

| Metric | Control (Q1-Q3) | Test (Q4) | Winner |
|---|---|---|---|
| Raw Avg Revenue/Customer | £2,322 | £1,584 | Control |
| Avg Order Value | £468 | £500 | Test ✅ |
| Avg Orders/Customer | 4.95 | 3.17 | Control |
| **Revenue/Customer/Month** | **£129** | **£226** | **Test ✅** |
| **Monthly Lift** | | | **+75.5%** |

**Statistical Test Results:**
- T-statistic: 3.78
- P-value: 0.0002
- Confidence: 99.98%
- Result: SIGNIFICANT ✅ — Reject H0

---

## Key Insights
1. Raw revenue comparison was misleading due to different 
   time windows (18 vs 7 active months)
2. After normalization Q4 generates 75.5% more per month
3. Q4 customers place higher value orders (£500 vs £468)
4. 52% customer retention rate across seasons
5. 1,038 customers shop exclusively in Q4 — re-engagement opportunity

---

## Business Recommendations
1. Re-engage 1,038 Q4-only customers in Q1-Q2
2. Launch loyalty program with coupons and discounts
3. Increase Q4 inventory investment — 75.5% revenue premium justifies it
4. Protect wholesale relationships — 52% retention shows loyalty

---

## Data Source
Download the dataset from Kaggle:
https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci

Save as `data/online_retail_II.csv` before running notebook.

---

## Setup

```bash
pip install -r requirements.txt
```

## Run Analysis
Open and run all cells in:notebooks/ab_test_analysis.ipynb

---

## Repository Structure

ecommerce-ab-test-analysis/
├── data/                    — dataset (not tracked in git)
├── notebooks/
│   └── ab_test_analysis.ipynb  — main analysis notebook
├── README.md
├── requirements.txt
└── .gitignore

---

## Skills Demonstrated
- A/B test design and hypothesis framework
- Data cleaning and quality validation
- Confounding variable identification and correction
- Statistical significance testing (T-test, p-value)
- Business insight generation and recommendations
- Data visualization with matplotlib and seaborn