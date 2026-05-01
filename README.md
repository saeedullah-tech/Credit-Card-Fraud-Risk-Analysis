# Credit Card Fraud Risk Analysis Dashboard

## Project Overview
The **Credit Card Fraud Risk Analysis Dashboard** Transiaction Fraud analysis
This project presents a Power BI dashboard focused on analyzing high-risk financial transactions across different fraud types and industries. The analysis identifies identity theft (24%) as the dominant fraud category, with notable patterns in account takeover and card-not-present transactions. It highlights temporal trends, including peak fraud activity on specific days, and provides insights into sector-based risks such as e-commerce, transportation, and food delivery.
## Dashboard Preview
---
![Image](https://github.com/saeedullah-tech/Credit-Card-Fraud-Risk-Analysis/blob/0e98a4c6766e895b44f97c8a358954351f94e93f/Fraudanalysis-Trim-ezgif.com-video-to-gif-converter.gif)
---


# Dashboard Components

## Key Performance Indicators (KPIs)

The dashboard includes several KPI cards that summarize the overall fraud situation.

| Metric | Description | Value |
|------|-------------|------|
| Fraud Rate | Percentage of fraudulent transactions | 28.60% |
| Fraudulent Transactions | Total number of fraud cases | 286 |
| Critical Risk Transactions | High risk fraud transactions | 10.70 |
| Fraudulent Transaction Amount | Total amount involved in fraud | 3M |

These KPIs provide a quick overview of fraud severity and financial impact.

---

## Filter Panel

The dashboard contains a filter panel that allows users to interact with the data.

### Available Filters
- Fraud Type
- State
- Merchant Name

These filters allow users to explore specific segments of the data and analyze fraud patterns in more detail.

---

# Visualizations

## 1. Total Transaction Amount by Fraud Type and Transaction Category

This stacked horizontal bar chart displays how transaction amounts are distributed across different fraud types and transaction categories.

### Fraud Types
- Card Not Present
- Card Skimming
- Identity Theft
- Account Takeover
- Phishing

### Transaction Categories
- Apparel
- E-commerce
- Electronics
- Food Delivery
- Groceries
- Transportation

### Insights
- Card Not Present fraud shows the highest transaction amounts.
- E-commerce and transportation categories appear frequently in fraud cases.
- This visualization helps identify which transaction categories are more vulnerable to fraud.

---

## 2. Total Transaction Amount by Fraud Risk

The donut chart shows the distribution of transaction amounts by fraud risk level.

| Risk Level | Amount | Percentage |
|-----------|-------|------------|
| High Risk | 5M | 42.42% |
| Medium Risk | 3M | 27.93% |
| Low Risk | 2M | 18.81% |
| Very Low Risk | 1M | 10.85% |

### Insights
High-risk transactions represent the largest share of fraudulent transaction value.

---

## 3. Fraudulent Transactions by State

This bar chart compares the number of fraudulent transactions across different states.

### Top States with Fraud Cases
- Maharashtra – 36
- Karnataka – 34
- Rajasthan – 34
- West Bengal – 33
- Uttar Pradesh – 29
- Tamil Nadu – 28
- Telangana – 27
- Gujarat – 23
- Delhi – 21
- Kerala – 21

### Insights
Certain states experience higher fraud activity, which may indicate regional fraud patterns.

---

## 4. Fraudulent Transactions by Month

This line chart displays fraud trends throughout the year.

| Month | Fraud Cases |
|------|-------------|
| January | 17 |
| February | 18 |
| March | 26 |
| April | 22 |
| May | 22 |
| June | 28 |
| July | 26 |
| August | 29 |
| September | 21 |
| October | 22 |
| November | 21 |
| December | 34 |

### Insights
Fraud activity fluctuates across the year, with the highest number of cases recorded in December.

---

# Dataset Description

The dataset contains information about credit card transactions and fraud risk indicators.

| Column | Description |
|------|-------------|
| Transaction ID | Unique identifier for each transaction |
| Transaction Category | Type of purchase |
| Fraud Type | Type of fraud detected |
| Fraud Risk | Risk level assigned to the transaction |
| Transaction Amount | Value of the transaction |
| State | Location of transaction |
| Merchant Name | Business where the transaction occurred |
| Month | Time period of the transaction |

---

# DAX Measures Used

### Fraud Rate %

```DAX
Fraud Rate % =
DIVIDE(
    [Fraudulent Transactions],
    [Total Transactions],
    0
) * 100
```

### Fraudulent Transactions

```DAX
Fraudulent Transactions =
CALCULATE(
    COUNTROWS('Credit Card Fraud Risk Analysis'),
    'Credit Card Fraud Risk Analysis'[Fraud Risk] = "Fraud"
)
```

### Total Transaction Amount

```DAX
Total Transaction Amount =
SUM('Credit Card Fraud Risk Analysis'[Transaction Amount])
```

---

# Skills Demonstrated

This project demonstrates the following data analytics skills:

- Data Cleaning
- Data Modeling
- Data Visualization
- Dashboard Development
- DAX Calculations
- Fraud Risk Analysis
- Business Insights Generation

---

# Tools and Technologies

- Microsoft Power BI
- DAX (Data Analysis Expressions)
- Data Visualization
- Data Analytics

---

# Key Insights

- Fraudulent transactions account for **28.6% of all transactions**.
- High-risk fraud contributes the **largest financial impact**.
- E-commerce and transportation categories show higher fraud activity.
- Fraud distribution varies across **states and months**.

---

# Project Objective

The objective of this project is to demonstrate how **data visualization and analytics can help detect fraud patterns and support fraud prevention strategies**.

---

# Author

**Saeed Ullah**

Aspiring Data Analyst skilled in:

- Power BI
- SQL
- Excel
- Data Visualization
- Data Analysis
