# Smart Borrower Risk & Recovery System

A real-world, ML-powered solution to optimize loan recovery by profiling borrowers, detecting early risk signals, and dynamically assigning cost-effective recovery strategies.

---

##  Table of Contents

- [Overview](#overview)
- [Business Problem](#business-problem)
- [Dataset Description](#dataset-description)
- [Project Architecture](#project-architecture)
- [Key Steps](#key-steps)
- [Insights](#insights)
- [ML Modeling](#ml-modeling)
- [Borrower Segmentation](#borrower-segmentation)
- [Recovery Strategy Design](#recovery-strategy-design)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Conclusion](#conclusion)

---

## Overview

Loan defaults impact the financial health of lending institutions. This project builds a **Smart Borrower Risk & Recovery System** that:
- Uses ML to **predict repayment risks**
- Segments borrowers based on financial behavior
- Recommends **dynamic, cost-sensitive recovery strategies**

---

## Business Problem

Financial institutions face:
- Rising loan defaults
- Ineffective one-size-fits-all recovery efforts
- High cost of legal and manual collections

We built a system to:
1. Profile borrower risk early
2. Segment customers using K-Means
3. Use ML (Random Forest) to predict high-risk defaults
4. Tailor recovery strategy by borrower risk segment

---

## Dataset Description

The dataset simulates 500 borrower records and includes:

| Feature | Description |
|---------|-------------|
| `Borrower_ID` | Unique ID of borrower |
| `Age` | Borrower age |
| `Gender` | Male/Female |
| `Employment_Type` | Salaried/Self-employed |
| `Monthly_Income` | Monthly earnings in dollars |
| `Num_Dependents` | Number of dependents |
| `Loan_Amount` | Principal loan amount |
| `Loan_Tenure` | Tenure in months |
| `Interest_Rate` | Annual interest rate (%) |
| `Collateral_Value` | Value of pledged asset |
| `Outstanding_Loan_Amount` | Balance yet to be paid |
| `Monthly_EMI` | Monthly installment |
| `Payment_History` | On-Time, Delayed, etc. |
| `Num_Missed_Payments` | Count of missed EMIs |
| `Days_Past_Due` | Total days overdue |
| `Recovery_Status` | Fully/Partially/Not recovered |
| `Collection_Attempts` | Recovery calls/actions made |
| `Collection_Method` | Calls, Legal, Settlement, etc. |
| `Legal_Action_Taken` | Yes/No |

---

## Project Architecture


---

## Key Steps

1. **Step 1: Data Import & Initial Exploration**
2. **Step 2: Descriptive Statistics & Cleaning**
3. **Step 3: EDA & Distribution Analysis**
4. **Step 4: Payment History & Missed Payments Impact**
5. **Step 5: Income vs Recovery Analysis**
6. **Step 6: K-Means Clustering to Segment Borrowers**
7. **Step 7: Segment Interpretation & Labeling**
8. **Step 8: Train ML Model (Random Forest) for Risk Detection**
9. **Step 9: Assign Dynamic Recovery Strategy**

---

## Insights

- Most loans cluster around \$5K–\$15K with a few outliers > \$100K
- Borrowers with **0–2 missed payments** are mostly recovered
- High-income groups show better repayment behavior
- Borrower Segments reveal:
  - Segment 0: Moderate Income, High Loan Burden
  - Segment 1: High Income, Low Default Risk
  - Segment 2: Balanced Risk
  - Segment 3: High Loan, Higher Default Risk

---

## ML Modeling

- Target: `High_Risk_Flag` based on risky segments
- Model: `RandomForestClassifier`
- Features used: Income, loan size, EMI, missed payments, DPD
- Output: Risk Score for each borrower

---

## Recovery Strategy Design


* Risk Score > 0.75 → Aggressive Recovery
* 0.5 – 0.75       → Settlement Offers
* < 0.5            → Automated Reminders

## Tech Stack
Python, Pandas, NumPy

Plotly for visualizations

Scikit-learn (KMeans, RandomForest)

Git + GitHub

Google Colab + VS Code


## Conclusion

* This project simulates how modern financial institutions can:

* Identify risky borrowers before default occurs

* Reduce legal costs using early segmentation

* Boost repayments via targeted strategy

This is a production-ready framework that can be enhanced with real-time APIs and deeper behavior signals.

