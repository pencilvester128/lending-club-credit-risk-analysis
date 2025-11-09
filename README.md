# lending-club-credit-risk-analysis
Weekend sprint: Predicting loan defaults using historical data from 2.26M loans
# Credit Risk Analysis: Predicting Loan Defaults

Credit risk analysis using 2.26M real loans to predict defaults and quantify financial losses. Built as a resource-conscious (real busisness constraint always) weekend sprint with actionable recommendations and clear next steps for iteration.

## 📊 Project Overview

**Business Question:** Can we predict which borrowers will default on their loans?

**Key Findings:**
- Borrowers with 2+ prior delinquencies show 2.2 percentage points higher default rates
- **$1.2B+ in losses** identified across loans with 1-2 prior delinquencies
- Employment length showed weak predictive power and was deprioritized

**Dataset:** 2.26M loans from Lending Club (2007-2018)  
**Tools:** Python (Pandas, Matplotlib, Seaborn), Jupyter Notebook  
**Methodology:** CRISP-DM framework

---

## 🎯 Key Results

### Financial Impact
- **1 delinquency:** $939M in total losses (35K loans)
- **2 delinquencies:** $296M in total losses (11K loans)
- **Combined exposure:** $1.235B from just the 1-2 delinquency segments

### Recommendations
1. Use delinquency history as key decision factor for borderline approval cases
2. Implement risk-based pricing tiers for applicants with 1-2 delinquencies
3. Develop multi-variable risk model combining delinquency + DTI + income

---

## 📁 Repository Structure
```
├── notebooks/
│   └── credit_risk_analysis.ipynb    # Full analysis with commentary
├── scripts/
│   └── credit_risk_analysis.py       # Clean Python script
├── visualizations/
│   └── chart1_default_risk_pattern.png
│   └── chart2_business_impact_focused.png
│   └── chart3_risk_volume_tradeoff.png
└── README.md
```

---

## 📂 Data Source

**Dataset:** Lending Club Loan Data (2007-2018)  
**Download:** [Kaggle - Lending Club Loan Data](https://www.kaggle.com/datasets/wordsforthewise/lending-club)

*Note: Due to GitHub file size limits, the dataset is not included in this repository. Download from Kaggle and place in a `/data` folder to reproduce the analysis.*

---

## 🚀 Quick Start

1. Download the dataset from Kaggle (link above)
2. Clone this repository
3. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn`
4. Open `notebooks/credit_risk_analysis.ipynb` in Jupyter
5. Update the data path in the notebook to point to your downloaded CSV

---

## 🔍 Methodology

**Framework:** CRISP-DM (Cross-Industry Standard Process for Data Mining)

**Process:**
1. **Business Understanding:** Defined hypothesis around debt behavior predicting defaults
2. **Data Understanding:** Assessed 145 variables for quality and completeness
3. **Data Preparation:** Cleaned data, calculated loss metrics, created segments
4. **Analysis:** Statistical analysis of risk patterns
5. **Evaluation:** Quantified business impact in dollar terms
6. **Insights:** Generated actionable recommendations

**Note on Failed Hypothesis:** Initially tested employment length as a predictor. Found weak signal (1.5pp spread) and made resource-conscious decision to deprioritize. This mirrors real-world data science where not every hypothesis pans out.

---

## 📈 Future Iterations

- Build predictive model (logistic regression with multiple variables)
- Calculate actual vs. estimated losses (account for payments before default)
- Analyze income-to-loan ratio interactions with delinquency
- Clean and categorize employment titles by industry/stability
- A/B test risk-based pricing strategies

---

## 👤 About

This project was completed as a weekend sprint to demonstrate:
- Business-focused data analysis
- Resource-conscious iteration and prioritization
- Clear communication of technical findings to non-technical stakeholders
- Professional documentation and code organization

**Author:** CJ Watkins  
**LinkedIn:** (https://www.linkedin.com/in/cwatkins128/) 
**Contact:** cjw@leadwithic.com

---

## 📄 License

MIT License - feel free to use this project as a learning resource or portfolio template.
