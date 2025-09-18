# Churn-Predict-for-Video-Streaming-Service
This churn prediction project demonstrates ML models such as  Logistic Regression, Random Forest, XGBoost, LightGBM, ans CatBoost

## Overview

- This project addresses customer churn prediction for a subcription-based video streaming service.
- This is part of my challenge project from Coursera https://www.coursera.org/projects/data-science-challenge
- Applying ML models to forecast which users are likely to cancal their subcriptions.
- Freature include acount demographics, billing details, viewing habits, and target churn (1 = churned, 0 = retained)
- The goal is to predict churn probability via ROC-AUC to enable targeted interventions

## Approach
- Loaded data with Pandas, visualized distributions and correlations via Seaborn and Matplotlib
- Handled categoricals with encoding, scaler with nummerical features.
- Split data 80/20 with stratification to manage class imbalance (about 18% churn rate)

## Model to development:
- Baselines: Logistic Regestion and Random Forest.
- XGBoost, LightGBM, and CatBoost

## Evaluation 

Metrics: ROC-AUC, precision-recall, f1-score on train and validation sets.

Feature importance:

<img width="747" height="453" alt="Image" src="https://github.com/user-attachments/assets/f57a3ddf-342b-4c40-b27a-28784cf932ea" />

## Conclusion

The CatBoost model shows good performance on the training set, indicating a strong ability to distinguish between churned and non-churned subscriptions. AUC=0.76 on train and 0.75 on validation. Compared to other models, CatBoost achieves a better recall for the churned class (1), with a balanced f1-score on both training and validation sets. The model performs well across various threshold settings, with high sensitivity (recall) at lower thresholds and high specificity at higher thresholds. Depending on business needs, the cutoff threshold can be adjusted to optimize for precision or recall. Churned subscriptions can be better identified with this model compared to others. Importance of detecting churned subscriptions is prioritized, the cutoff can be lowered to improve recall further.

The most important features in the CatBoost model for predicting churn are:
* EngagementScore
* AvgMonthlyCharge
* AccountAge
* PricePerContentDownload

## Contact
* Name: Thanh Xuyen, Nguyen
* LinkedIn: https://www.linkedin.com/in/xuyen-thanh-nguyen-0518/
* Email: thanhxuyen.nguyen@outlook.com
