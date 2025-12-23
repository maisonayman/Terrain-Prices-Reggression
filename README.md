# Terrain Prices Regression – Kaggle Competition

This repository contains my solution for the **Terrain Prices Regression** Kaggle competition.

## Competition Overview
The objective of this competition is to predict terrain prices based on a mix of:
- Numerical features
- Categorical features (such as terrain type, land use, zoning, etc.)

The task is a **regression problem**, where the target variable represents the terrain price.

Competition link:  
https://www.kaggle.com/competitions/terrain-prices-reggression

---

## Approach
To solve this problem, I used a machine learning pipeline that handles preprocessing and modeling in a clean and reproducible way.

### Key steps:
1. Data loading and basic exploration
2. Separation of features and target variable
3. Handling categorical features using encoding
4. Training and evaluating regression models
5. Generating predictions for the test dataset
6. Creating a submission file for Kaggle

---

## 🤖 Model Used
- **Gradient Boosting Regressor** (scikit-learn)

This model was chosen due to its strong performance on structured tabular data and its ability to capture non-linear relationships.

---

## Preprocessing
Preprocessing is handled using a `Pipeline` and `ColumnTransformer`:

- **Numerical features**:
  - StandardScaler
- **Categorical features**:
  - One-Hot Encoding (`handle_unknown="ignore"`)

This ensures consistent preprocessing during training and prediction.

---

## Evaluation Metric
- **R² Score**

Model performance was evaluated using a validation split before generating final predictions.

