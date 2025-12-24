## 📂 Project Workflow
This project is divided into 4 main notebooks to ensure modularity and reproducibility:

| Notebook | Description | Key Outcome |
| :--- | :--- | :--- |
| **1.0 Import Libraries & EDA** | Initial data loading, understanding data distribution, and checking target imbalance. | Insight on data quality & anomaly detection. |
| **2.0 Data Cleaning & FE** | Merging 7 datasets, handling missing values, and generating aggregated features (Feature Engineering). | Integrated dataset with **100+ new predictive features**. |
| **3.0 Feature Selection** | Removing multicollinear features and selecting top features using importance scores to reduce noise. | Optimized feature set for modeling. |
| **4.0 Training & Model Selection** | Training models (Logistic Regression, Random Forest, XGBoost, LightGBM) and evaluation. | Final **XGBoost model** with **0.76 AUC-ROC**. |
