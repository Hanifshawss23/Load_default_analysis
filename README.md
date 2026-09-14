# 📊 Horizon Financial Group: Loan Default Risk Analysis

**Author:** [Hanif Kung'unde](https://github.com/Hanifshawss23)  
**Role:** Data Analyst / Researcher  

---

##  Project Overview
Horizon Financial Group has issued over 600 personal loans across 2024 and 2025. The company has noticed that roughly **1 in 4 loans are defaulting (24.3%)**, which is well above their target of 12%. The VP of Risk has asked the data team to analyze the existing loan book and borrower data to identify the key risk factors driving these defaults. The insights from this analysis will directly inform changes to their credit scoring model and loan approval thresholds.

## 🎯 Objectives
1. Calculate the overall default rate and break it down by credit score range.
2. Examine the relationship between a borrower’s Debt-to-Income (DTI) ratio and the likelihood of defaulting.
3. Identify which loan purposes have the highest default rates.
4. Assess how employment status and years employed affect default risk.

## 🛠️ Tech Stack
- **Python** (Pandas, NumPy)
- **Data Visualization** (Matplotlib, Seaborn)
- **Environment** (Jupyter Notebook)

---

## 🔍 Key Findings & Exploratory Data Analysis (EDA)

### 1. Credit Score (Highest Impact Risk Factor)
Credit score is the single strongest predictor of default. Borrowers in the lowest bucket (520–599) default at nearly **50%**, while those scoring 750+ default at only ~12%.

![Default Rate by Credit Score Range]
(![creditscore.png](https://share.jotbird.com/images/ed2081b3-cbe4-4a30-95ac-8c426d77a9da.png))
*Figure 1: Default rates drop significantly once the credit score crosses the 650 threshold.*

### 2. Debt-to-Income (DTI) Ratio
Default rates **double** once the DTI ratio crosses 50%, jumping from ~17% (25–49 range) to ~36% (50–74 range). The scatter plot below confirms that defaulted borrowers cluster heavily at higher DTI values.

![Default Rate by DTI Ratio Range]
(![dtiratio.png](https://share.jotbird.com/images/5762a1e2-1504-4079-9b87-c9818553e34d.png))
*Figure 2: Default rate spikes dramatically for DTI ratios above 50%.*

![DTI Ratio vs. Default Status]
(![defaultornot.png](https://share.jotbird.com/images/a7ccddf7-cbce-4474-b4fe-469c4db086f2.png))
*Figure 3: Scatter plot showing the spread of DTI ratios for defaulted vs. non-defaulted loans.*

### 3. Loan Purpose Distribution
The distribution of loan purposes (Home Improvement, Major Purchase, Medical Expenses, etc.) was relatively balanced. While some purposes had slightly higher volumes, no single purpose stood out as a dominant default driver compared to credit score or DTI.

![Distribution of Loan Purposes]
(![loanpurpjpg.png](https://share.jotbird.com/images/33be0606-589e-4f3c-b74b-ef0dac601997.png))
*Figure 4: Count of loans issued by purpose.*

### 4. Employment Stability
While general *Employment Status* (Full-Time, Part-Time, Self-Employed) did not show massive disparities in default rates, **Years Employed** was a highly significant factor. Borrowers with **less than 2 years** at their current job default at **34.5%**, compared to just **17.5%** for those with 2–5 years of tenure.

![Default Rate by Employment Status]
(![yearsemployed.png](https://share.jotbird.com/images/82efeb41-485d-4ade-a6d6-af8976b88637.png))
*Figure 5: Default rates across different employment statuses.*

---

## ✅ Final Recommendations for Underwriting

Based on the data analysis, here are the top 3 recommended threshold adjustments for the credit scoring model to help Horizon Financial Group meet its 12% default target:

| # | Risk Factor | Finding | Recommended Threshold | Expected Impact |
|---|-------------|---------|----------------------|-----------------|
| 1 | **Credit Score** | ~50% default rate below 600 | **Minimum 650** | Drops default cohort from ~29% to ~16% |
| 2 | **DTI Ratio** | Default rate doubles above 50% | **Maximum 50%** | Removes over-leveraged borrowers |
| 3 | **Employment Stability** | 34.5% default rate for <2 years tenure | **Minimum 2 years continuous employment** | Filters out job-instability risk |

---
