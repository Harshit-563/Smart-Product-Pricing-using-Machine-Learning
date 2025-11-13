ML Challenge 2025: Smart Product Pricing Solution

Team Name: ML_Hustler
Team Members: Harshit Maurya, Abhishek Patel, Rachit Mishra
Submission Date: 12 oct 2025

1. Executive Summary

Our project focuses on predicting the most suitable price for products using the provided dataset of historical sales and product information. We explored multiple machine learning models and found that gradient boosting–based approaches (LightGBM and XGBoost) performed best. The final model combines strong feature engineering with careful tuning to achieve consistent and reliable predictions.

2. Methodology Overview
2.1 Problem Analysis

We treated the challenge as a supervised regression task aimed at predicting the optimal product price. During exploratory data analysis, we noticed that factors such as product category, brand, and customer ratings strongly influenced pricing. There were also clear differences in pricing behavior across different product groups.

Key Observations:

Higher-rated products usually maintained higher but more stable prices.

Brand and category turned out to be among the most important predictors.

Several numerical features were skewed, so we applied log transformations.

Some correlated features were removed to avoid redundancy.

2.2 Solution Strategy

Approach Type: Ensemble Regression Model (LightGBM/XGBoost with baseline comparisons)
Core Idea: Capture the non-linear relationship between demand, ratings, and pricing through gradient boosting, supported by well-engineered interaction features.

We started with simple linear and random forest models as baselines and then moved to boosting algorithms for better generalization and performance.

3. Model Architecture
3.1 Architecture Overview

The overall pipeline consists of:

Data Cleaning → Feature Engineering → Model Training → Evaluation → Price Prediction

3.2 Model Components

Tabular Feature Pipeline:

Preprocessing: Filled missing values, log-transformed skewed variables, and encoded categorical features.

Model Type: Gradient Boosting Regressor (LightGBM/XGBoost).

Key Parameters: learning_rate = 0.05, n_estimators = 1000, max_depth = 8, subsample = 0.8, colsample_bytree = 0.8.

Validation: 5-fold cross-validation with early stopping to prevent overfitting.

4. Model Performance
4.1 Validation Results

SMAPE Score: 48.8172

Other Metrics: RMSE = 0.658399

Gradient boosting showed the most stable and accurate predictions compared to linear regression and random forest baselines.

5. Conclusion

In this project, we learned that well-designed feature transformations and ensemble models can significantly improve pricing predictions. Our final model achieved a strong balance between accuracy and interpretability, while strictly following all competition rules and avoiding any use of external data.

Appendix
A. Code Artefacts

The complete notebook (smart_product_pricing_full.ipynb) includes preprocessing, model training, and prediction steps.

B. Additional Results

Additional plots such as feature importance and validation curves are included in the notebook for reference.