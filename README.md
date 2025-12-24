# 🏦 Home Credit Indonesia: Credit Risk Scoring Model

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Library](https://img.shields.io/badge/Library-XGBoost%20%7C%20Pandas%20%7C%20Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
**Credit Scoring** is a statistical analysis used by lenders and financial institutions to assess a person's creditworthiness. This project aims to solve a classic classification problem: **predicting whether a loan applicant will be able to repay their loan or will encounter difficulties (default).**

This project was developed as part of the **Project-Based Virtual Internship : Data Scientist at Home Credit Indonesia x Rakamin Academy**.

## 💼 Business Understanding
* **Problem:** Non-Performing Loans (NPL) or defaults significantly impact the company's profitability and liquidity.
* **Goal:** Develop a machine learning model to predict the probability of default for each applicant.
* **Impact:** By accurately identifying high-risk customers, the company can minimize financial losses while optimizing loan approval rates for credible applicants.

## 📊 Dataset & Features
The dataset consists of **7 heterogeneous tables** encompassing customer behavior and transactional history:
* `application_{train|test}.csv`: Main table (static data).
* `bureau.csv` & `bureau_balance.csv`: Customer's previous credits provided by other financial institutions.
* `POS_CASH_balance.csv`: Monthly balance snapshots of previous POS (Point of Sales) and cash loans.
* `credit_card_balance.csv`: Monthly balance snapshots of previous credit cards.
* `previous_application.csv`: History of previous applications at Home Credit.
* `installments_payments.csv`: Repayment history for previously disbursed credits.

**Feature Engineering Highlights:**
* Aggregated data from transactional tables to create a comprehensive customer view.
* Generated **100+ predictive features** to capture financial stability patterns.

## 🛠️ Methodology
1.  **Exploratory Data Analysis (EDA):** Showing the imbalanced targets and default risk based on external score.
2.  **Data Preprocessing:** Handling outliers, imputing missing values, and encoding categorical variables (One-Hot & Label Encoding).
3.  **Feature Engineering:** Creating domain-specific features (e.g., `debt_to_income_ratio`, `credit_utilization`).
4.  **Feature Selection:** Removing high-collinearity features to optimize model performance.
5.  **Modeling:** Training models (Logistic Regression, Random Forest, XGBoost, LightGBM) and evaluation.
6.  **Evaluation:** Using **AUC-ROC (Area Under the Receiver Operating Characteristic Curve)** as the primary metric.
7.  **Model Selection** Choosing XGBoost as the final modal due to its performance.

## 📈 Key Results
The final model : XGBoost achieved robust performance on the validation dataset:

| Metric | Score |
| :--- | :--- |
| **AUC-ROC** | **0.7601** |
| **Training Accuracy** | **0.7120** |

> **Insight:** An AUC score of **0.76** indicates that the model has a strong capability to distinguish between "Good" and "Bad" borrowers, exceeding the baseline for reliable predictive modeling in this context.


## 📂 File Structure
```text
├── notebooks/             # Jupyter Notebooks for analysis
│   ├── 1.0-import-libraries-and-eda.ipynb
│   ├── 2.0-data-cleaning-and-feature-engineering.ipynb
│   ├── 3.0-feature-selection.ipynb
    └── 4.0-training-and-model-selection.ipynb
  
├── images/                # Charts and visualizations
    ├── final-feature-importances.png    
├── src/                   # Source code for preprocessing
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
