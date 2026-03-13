# Kaggle House Prices - Advanced Regression Techniques

This repository contains my solution for the Kaggle competition:

https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

## Result

- **Public Leaderboard Score:** 0.12242  
- **Rank:** 497 / 4063  
- **Date:** 2026-03-11

## Overview

The goal of this competition is to predict the final sale price of residential homes using various features describing the property.

This project builds a regression pipeline that includes data preprocessing, feature engineering, and model ensembling.

The final prediction is generated using an ensemble of:

- Lasso Regression
- Ridge Regression
- LightGBM

These models were selected to combine the strengths of regularized linear models and gradient boosting trees.

---

## Approach

### Data Preprocessing

The following preprocessing steps were applied:

- Removal of extreme outliers based on `GrLivArea`
- Log transformation of `SalePrice`
- Missing value imputation based on feature semantics
- One-hot encoding for categorical variables

### Models

Three models were trained and combined using weighted averaging.

**Lasso Regression**

- Uses L1 regularization
- Performs implicit feature selection
- Works well with high-dimensional one-hot encoded data

**Ridge Regression**

- Uses L2 regularization
- Handles multicollinearity between features
- Provides stable linear predictions

**LightGBM**

- Gradient boosting tree model
- Captures nonlinear relationships and feature interactions
- Complements linear models in the ensemble

### Ensemble

The final prediction is generated using a weighted average of the three models.

Combining linear models and gradient boosting improves robustness and generalization.

## Data

Download the dataset from Kaggle:

https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data

## License

This repository is for educational purposes.  
The dataset belongs to the Kaggle competition and must be downloaded from Kaggle.