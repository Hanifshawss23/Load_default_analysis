# 📊 Loan Default Risk Analysis

## 📌 Project Overview
This project analyzes a loan portfolio for "Horizon Financial Group" to identify key risk factors driving a high default rate (~25%). The goal is to provide data-driven insights to improve the underwriting process and help the company meet its target default rate of 12%.

## 🛠️ Tech Stack
- **Python**: Pandas, NumPy, Matplotlib, Seaborn
- **Jupyter Notebook**: For exploratory data analysis (EDA) and visualization
- **Data Handling**: Data merging, binning, and statistical aggregation

## 🔑 Key Findings & Recommendations
Based on the exploratory data analysis, three primary levers were identified to improve the credit scoring model:
1. **Credit Score**: Implement a minimum threshold of **650**. (Default rates drop significantly from ~29% to ~16% above this point).
2. **Debt-to-Income (DTI) Ratio**: Implement a maximum DTI threshold of **50%**. (Default rates double once DTI exceeds this level).
3. **Employment Stability**: Require a minimum of **2 years of continuous employment**. (Default rate is ~34.5% for <2 years vs. ~17.5% for 2-5 years).

## 🚀 How to Run This Project
1. Clone this repository:
   ```bash
   git clone https://github.com/Hanifshawss23/load_default_analysis.git
