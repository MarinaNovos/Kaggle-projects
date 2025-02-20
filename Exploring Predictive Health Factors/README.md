# Polycystic Ovary Syndrome (PCOS) Lifestyle Impact Analysis
## Project Description
Polycystic ovary syndrome (PCOS) is a common endocrine disorder that affects the reproductive health and quality of life of millions of women worldwide. 
Research has shown that lifestyle choices such as diet, exercise, stress management, etc. have a significant impact on the pathogenesis and symptom relief of PCOS. 
However, there are still many gaps in research on the relationship between lifestyle and PCOS, especially in terms of individual differences and comprehensive lifestyle interventions.
In order to promote research progress in this field, we are organizing the "Polycystic Ovary Syndrome (PCOS) Lifestyle Impact Research Competition". 
The aim is to use data-driven methods to deeply analyze the impact of lifestyle choices on PCOS, and provide scientific basis for clinical intervention and health management.


## Libraries Used
To conduct the analysis, the following libraries were used:

Standard Libraries:
- pandas, numpy: For data manipulation and numerical operations.

Data Visualization:
- matplotlib, seaborn: For data visualization, including distribution plots and correlation heatmaps.

Machine Learning & Data Processing:
- sklearn: For preprocessing, model training, and evaluation, including:
- train_test_split, RandomizedSearchCV, cross_val_score (Model selection & evaluation)
- OneHotEncoder, StandardScaler, LabelEncoder (Feature engineering)
- SimpleImputer (Handling missing values)
- Pipeline, ColumnTransformer (Data transformation pipelines)
- f_classif, mutual_info_classif (Feature selection)
- roc_auc_score, roc_curve, confusion_matrix, precision_recall_curve (Model performance metrics)

Imbalanced Data Handling:
- imblearn: For oversampling techniques, including SMOTE.

Gradient Boosting Models:
- XGBoost, LightGBM, CatBoost: For efficient model training and performance optimization.

## Findings and Recommendations
Our analysis revealed significant correlations between PCOS and various factors, including:
- Hyperandrogenism
- Insulin resistance
- Hormonal imbalance
- Hirsutism
- Difficulties with conception

To develop predictive models, we used gradient boosting algorithms, including LGBM, XGBoost, and CatBoost. 
Hyperparameter tuning was performed to optimize model performance. Additionally, feature selection techniques, such as feature importance analysis and SHAP interpretation, were applied to enhance the model's transparency.
The study confirms that lifestyle factors significantly influence the development and progression of PCOS. However, additional research is required to assess the impact of specific lifestyle parameters such as physical activity frequency and sleep duration.
The developed approach, incorporating data balancing, model interpretability, and feature selection, can be used to identify high-risk groups and tailor personalized recommendations for patient management. 