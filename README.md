# 🏦 Bank Loan Analysis Dashboard

An end-to-end Power BI project analyzing **38,576 loan applications** to track lending performance, portfolio risk, and repayment health for a consumer lending business.

![Dashboard Summary](images/dashboard_summary.png)

## 📊 Project Overview

This dashboard answers the core questions a lending business asks every month:
- How many loans are we issuing, and how much capital is deployed?
- What share of the book is **good** (fully paid / current) vs **bad** (charged off)?
- How do interest rate, DTI, and repayment differ by loan term?
- Where geographically, and for what purposes, is loan demand concentrated?

The report is built as a two-page interactive Power BI dashboard (`bank_dashboard.pbix`) on top of a single loan-level dataset (`Financial_loan_data.xlsx`, 38,576 rows × 23 columns).

## 🔑 Key Metrics (Summary Page)

| Metric | Value |
|---|---|
| Total Loan Applications | 38,576 |
| Total Funded Amount | $435.8M |
| Total Amount Received | $473.1M |
| Average Interest Rate | 12.05% |
| Average DTI Ratio | 13.33% |
| Good Loan % | 86.18% |
| Bad Loan % (Charged Off) | 13.82% |

## 🖼️ Dashboard Pages

### Summary
KPI cards, good vs. bad loan breakdown, and funded amount / interest rate / DTI split by loan term.

![Dashboard Summary](images/dashboard_summary.png)

### Overview
Monthly application trend, loan term mix, home ownership, loan purpose, and top states by volume.

![Dashboard Overview](images/dashboard_overview.png)

> Note: these PNGs are static exports recreated from the underlying data for portfolio viewing (e.g. on GitHub/LinkedIn, which can't render `.pbix` files). Open `bank_dashboard.pbix` in Power BI Desktop for the live, interactive version with slicers and drill-through.

## 🗂️ Repository Structure

```
├── bank_dashboard.pbix        # Power BI report (open in Power BI Desktop)
├── Financial_loan_data.xlsx   # Source dataset
├── images/
│   ├── dashboard_summary.png
│   └── dashboard_overview.png
└── README.md
```

## 🛠️ Tools & Skills Used

- **Power BI Desktop** — data modeling, DAX measures, report design
- **DAX** — KPI cards, good/bad loan classification, term-based aggregations
- **Excel** — source data (loan-level records: term, grade, purpose, state, income, DTI, interest rate, payments)

## 📈 Data Dictionary (selected columns)

| Column | Description |
|---|---|
| `LOAN_STATUS` | Fully Paid / Current / Charged Off |
| `TERM` | 36 or 60 month loan term |
| `INT_RATE` | Interest rate on the loan |
| `DTI` | Borrower debt-to-income ratio |
| `LOAN_AMOUNT` | Amount funded |
| `TOTAL_PAYMENT` | Total amount repaid to date |
| `PURPOSE` | Stated reason for the loan |
| `HOME_OWNERSHIP` | Rent / Mortgage / Own |
| `ADDRESS_STATE` | Borrower's US state |

## 🚀 How to Explore

1. Clone this repo
2. Open `bank_dashboard.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
3. Use the slicers on the left and the page navigator at the top to move between **Summary** and **Overview**

## 📌 Insights

- The book is healthy overall: **86.2%** of applications are good standing (fully paid or current).
- 36-month loans dominate volume (28,237 loans, $273M funded) vs. 60-month loans (10,339 loans, $163M funded).
- **Debt consolidation** is by far the largest use of funds (~$232M), more than 4x the next largest purpose (credit cards, ~$59M).
- California, New York, and Florida are the top three states by application volume.
- Application volume grows steadily through the year, peaking in Q4 (Oct–Dec).

---

