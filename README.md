# Community Happiness & Life Satisfaction Analysis

**R case study combining multiple linear regression and logistic classification**

## Executive Summary
This project uses community survey data to examine two related questions: how neighborhood quality and years of residence relate to current happiness, and whether safety walking at night plus neighborhood quality can help classify high life satisfaction.

The original coursework fit and evaluated the logistic model on the same observations. The cleaned portfolio preserves the original model specification but adds a **reproducible train/test evaluation extension** so classification performance is assessed on held-out data.

## Methods Demonstrated
- Survey-data preparation
- Multiple linear regression
- Regression diagnostics
- Binary outcome creation
- Logistic regression
- Train/test validation
- Confusion matrix
- Accuracy
- Sensitivity/recall
- Specificity
- Precision
- ROC curve and AUC

## Data Note
The original `happinessSurvey.csv` was not included in the uploaded repository. The notebook expects it at `data/happinessSurvey.csv`. Specific AUC/accuracy values should be added only after rerunning the analysis.

## Interview Talking Point
> I used the same survey dataset for two different analytical questions: a linear regression for a continuous happiness outcome and logistic regression for a binary high-life-satisfaction outcome. I then extended the original coursework by evaluating the classifier on held-out data because evaluating on the training observations can overstate performance.

## Limitation
Survey relationships are observational. Regression coefficients and predictive performance should not be interpreted as proof that neighborhood characteristics cause happiness.
