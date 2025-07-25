# Credit Default Prediction – XGBoost & Power BI Dashboard 📊

This project tackles the challenge of predicting **loan defaults** — a critical task in financial risk assessment.  
It combines **machine learning (XGBoost with SMOTE)** to handle imbalanced data and a **Power BI dashboard** to provide actionable insights for stakeholders.

---

## 🚀 Project Highlights

### **1. Machine Learning Pipeline**
- **Data Preprocessing**  
  - Smart null value imputation using **Gemini API**
  - Feature scaling and encoding  
  - Train-test split with stratification

- **Class Imbalance Solution**  
  - **SMOTE (Synthetic Minority Oversampling Technique)** applied on the training set

- **Model Training & Tuning**  
  - **XGBoost Classifier**  
  - **Hyperparameter tuning** via `GridSearchCV`:
    - `max_depth`, `n_estimators`, `learning_rate`, `subsample`, `colsample_bytree`
  - **Threshold optimization** to balance **recall** and **precision** for the minority class (defaults)

- **Model Performance (Test Set)**  
  - **ROC AUC**: 0.9361  
  - **Default Class Precision**: 0.81  
  - **Default Class Recall**: 0.61  
  - **F1-score**: 0.69  

> These metrics highlight the trade-off between precision and recall in imbalanced datasets, ensuring that more defaults are correctly identified (high recall), even if it means a few false positives.

---

### **2. Business Intelligence Dashboard (Power BI)**

To complement the ML results, an interactive **Power BI dashboard** was built for stakeholders to monitor portfolio health.

#### **Dashboard Features**
- **KPIs:**
  - High Risk Client Rate
  - Overdue Client Rate
  - Average PDN (Probability of Default)
  - Average Debt-to-Income Ratio
- **Visuals:**
  - Risk Category breakdown by Age Group, Industry, and Family Status
  - Debt Pressure Index analysis
  - Client demographics (Sex, Education, Family Status)
  - Geographic analysis by `LV_AREA` and `LV_SETTLEMENTNAME`
- **Interactive Filters (Slicers):**
  - AgeGroup, RiskCategory, Industry, Location

🔗 **[View the Interactive Power BI Report](PUT-YOUR-POWER-BI-PUBLIC-LINK-HERE)**

---

## 📂 Repository Structure
