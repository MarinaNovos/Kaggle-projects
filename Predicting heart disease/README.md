# Heart Disease
## Project Description
Machine learning project focused on predicting the presence of heart disease using clinical and diagnostic data. The goal is to identify high-risk patients and understand the key factors contributing to cardiovascular conditions.

---

## Problem

Cardiovascular diseases are among the leading causes of death worldwide. Early detection is critical for improving patient outcomes and reducing healthcare costs. This project aims to build a predictive model based on patient data and provide interpretable insights into disease risk.

---

## Data

The dataset includes patient-level medical and demographic features:

- Age, Sex  
- Chest pain type  
- Blood pressure, Cholesterol  
- Maximum heart rate  
- Exercise-induced angina  
- ST depression and slope  
- Number of vessels  
- Thallium test results  

Target variable:
- **Heart Disease** (0 — absence, 1 — presence)

---

## Approach

### 1. Data Preprocessing
- Target encoding (categorical → binary)
- Feature grouping (numerical vs categorical)
- Missing value handling using `SimpleImputer`
- One-hot encoding for categorical features
- Feature scaling for numerical variables

### 2. Exploratory Data Analysis
- Distribution analysis (histograms, boxplots)
- Categorical feature analysis (count plots)
- Phik correlation matrix for mixed data types

### 3. Modeling
- Models used:
  - CatBoost (best model)
  - Random Forest
  - Gradient Boosting
- Hyperparameter tuning with `RandomizedSearchCV`
- Stratified cross-validation

### 4. Evaluation
- ROC-AUC (primary metric)
- Accuracy, F1-score
- Confusion matrix

### 5. Model Interpretability
- Feature importance analysis
- SHAP values for global and local explanations

---

## Results

- **Best model:** CatBoost  
- **ROC-AUC:** ~0.95  
- **F1-score:** ~0.88  

Top predictive features:
- Chest pain type  
- Number of vessels  
- Exercise angina  
- ST depression  
- Max heart rate  
- Thallium  

---

## Key Insights

- Clinical indicators related to cardiac stress and vascular condition are the strongest predictors  
- Exercise-induced symptoms and diagnostic test results significantly impact risk  
- Some traditional metrics (e.g., cholesterol, blood pressure) show lower standalone importance  
- Tree-based models effectively capture non-linear relationships in medical data  

---

## Tech Stack

Python • Pandas • NumPy • Scikit-learn • CatBoost • SHAP • Phik • Matplotlib • Seaborn

---

## Future Improvements

- Add feature engineering (interaction features, aggregated indicators)  
- Test advanced models (LightGBM, XGBoost)  
- Validate on external datasets  
- Integrate into a clinical decision-support system  

---
