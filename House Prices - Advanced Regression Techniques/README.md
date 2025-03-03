# House Prices
## Project Description
When asked to describe their dream home, most buyers focus on the number of bedrooms, the size of the backyard, or perhaps a charming white-picket fence. 
However, real estate pricing is far more intricate, influenced by dozens of subtle yet critical factors—many of which buyers might never consider.
This dataset provides an extensive look into the complexities of home valuation. 
With 79 explanatory variables, it captures nearly every aspect of residential properties in Ames, Iowa—from the type of road access and basement quality to the year of construction and even proximity to railroads.
It is our ob to predict the sales price for each house. For each Id in the test set, you must predict the value of the SalePrice variable.

## Libraries Used
To conduct the analysis, the following libraries were used:

Standard Libraries:
- pandas, numpy: For data manipulation and numerical operations.

Data Visualization:
- matplotlib, seaborn: For data visualization, including distribution plots and correlation heatmaps.

Machine Learning & Data Processing:
- sklearn: For preprocessing, model training, and evaluation, including:
- train_test_split, RandomizedSearchCV, cross_val_score (Model selection & evaluation)
- OneHotEncoder, StandardScaler (Feature engineering)
- SimpleImputer (Handling missing values)
- Pipeline, ColumnTransformer (Data transformation pipelines)
- mean_squared_error(Model performance metrics)


Gradient Boosting Models:
- RandomForestRegressor, GradientBoostingRegressor, CatBoostRegressor: For efficient model training and performance optimization.

## Findings and Recommendations
The project was aimed at predicting house prices using advanced regression techniques. 
The goal was to analyze various factors influencing property values and develop machine learning models to make accurate predictions. 
During the analysis, it was established that many variables, such as LotArea, MasVnrArea, BsmtFinSF1, TotalBsmtSF, GarageArea, and SalePrice, exhibited right-skewed distributions, suggesting the need for log transformation before modeling. 
Features like OverallQual, OverallCond, Fireplaces, KitchenAbvGr, and GarageCars were identified as categorical and processed using One-Hot Encoding. 
Year-based features (YearBuilt, YearRemodAdd, GarageYrBlt, YrSold) showed an increasing trend in new houses over time, aligning with real estate market dynamics. Additionally, variables such as FullBath, HalfBath, and TotRmsAbvGrd revealed standard housing layouts based on their modal values. 
To predict house prices, multiple machine learning models were employed, including CatBoost, RandomForest, and GradientBoosting. 
The preprocessing pipeline included missing value imputation, scaling for numerical features, and encoding for categorical variables. 
Hyperparameter tuning was conducted using RandomizedSearchCV to optimize model performance. As a result, the best-performing model was CatBoost with the following parameters: learning_rate = 0.05, l2_leaf_reg = 3, iterations = 500, depth = 6, and border_count = 64. 
This model achieved the best score of -27163.79 in terms of negative root mean squared error. Other models, including RandomForest and GradientBoosting, also performed well but had slightly higher error values. 
The RMSE (Root Mean Squared Error) of the best model on the test set was 25,449.22. 
Feature importance analysis revealed that the most significant factor in the model was OverallQual (23.07), followed by GrLivArea (12.94), BsmtFinSF1 (5.26), 1stFlrSF (4.95), and TotalBsmtSF (4.51). 
Other influential features included LotArea, GarageCars, Fireplaces, YearBuilt, and GarageArea. Some categorical features, such as KitchenQual and ExterQual, also had noticeable impacts on the model’s predictions. 
Meanwhile, features like MoSold, YrSold, and Street had minimal influence, indicating that temporal factors had little effect on property values. In conclusion, the project successfully developed predictive models for house prices, with CatBoost emerging as the best model based on its predictive accuracy. 
The analysis provided valuable insights into the factors affecting house prices, highlighting the importance of structural quality, living area, and additional amenities in determining property value. 
Future improvements may include further feature engineering, handling outliers more effectively, and exploring additional modeling techniques to enhance prediction accuracy. 
On the Kaggle platform, the results on the test data showed a Score : 0.13353, further confirming the effectiveness of the model