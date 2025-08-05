# Risk-Client-Engagement-Analytics
# Credit Risk & Client Engagement Analytics Dashboard

A comprehensive Power BI dashboard project designed to analyze client engagement, loan exposure, and deposit behavior across multiple banking entities. This solution supports data-driven credit risk evaluation and operational decision-making for financial institutions.

---

## 🧩 Problem Statement

To develop a risk analytics solution in the banking domain that helps minimize the risk of lending by using client data to determine the likelihood of loan repayment.

---

## 💡 Solution Overview

- Built an end-to-end interactive dashboard using Power BI, with data modeling, transformation, and visualization capabilities.
- Helped identify high-risk clients by analyzing engagement history, estimated income, loan amounts, and deposit types.
- Created KPI-driven visual reports for Loan Analysis, Deposit Analysis, and Client Summary.

---

## 🗂️ Dataset Description

The dataset includes multiple interconnected tables:
- `Clients-Banking`
- `Banking Relationship`
- `Investment Advisor`
- `Gender`
- `Period`

Relationships were defined using primary and foreign keys.

---

## 🧹 Data Cleaning & Feature Engineering

- Created `Engagement Timeframe` and `Engagement Days` to track how long clients have been associated with the bank.
- Segmented `Estimated Income` into bins: Low (< 100000), Mid (< 300000) as `Income Band`.
- Introduced `Processing Fees` based on `Fee Structure`.

---

## 🧮 Key DAX Calculated Measures

| Metric | Description |
|--------|-------------|
| **Total Clients** | `DISTINCTCOUNT('Clients - Banking'[Client ID])` |
| **Bank Loan** | `SUM('Clients - Banking'[Bank Loans])` |
| **Business Lending** | `SUM('Clients - Banking'[Business Lending])` |
| **Total Deposit** | `[Bank Deposit] + [Savings Account] + [Foreign Currency Account] + [Checking Accounts]` |
| **Total Fees** | `SUMX('Clients - Banking', [Total Loan] * [Processing Fees])` |
| **Engagement Days** | `DATEDIFF('Clients - Banking'[Joined Bank], TODAY(), DAY)` |

---

## 📊 KPIs Included

- Total Clients  
- Total Loan  
- Total Deposit  
- Total Fees  
- Engagement Length  
- Credit Card Balance  
- Savings, Checking, and Foreign Currency Account Balances

---

## 📈 Dashboards/Visualizations

- **Home Page Overview**
- **Loan Analysis**: View loan types, amounts, and repayment risks
- **Deposit Analysis**: Understand client deposit behaviors
- **Client Summary**: Engagement length, income band, and credit behavior

---

## 🏁 Conclusion

This Power BI solution supports banks in evaluating client profiles effectively and enables better risk management decisions. The model provides transparency in lending operations and identifies high-risk clients proactively.

---

## 🔭 Future Enhancements

- Add predictive analytics for loan default risk
- Integrate time-series trends across quarters
- Include comparison across nationalities and banking institutions

---

## 💻 Tech Stack

**Tools & Languages:** Power BI, DAX, SQL, Python, Excel  
**Focus Areas:** Data Cleaning, KPI Modeling, Credit Risk Analytics, Data Visualization, Reporting

---

