# Housing Price Prediction

## Project Overview

This project predicts house prices using machine learning techniques.

The goal was to build a complete regression workflow including:

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Preprocessing
- Model Comparison
- Cross Validation
- Hyperparameter Tuning
- Final Model Evaluation

---

## Dataset

The project uses the California Housing Dataset. 

Source : https://www.kaggle.com/code/hassaan2580/california-housing-dataset

Features include:

- Longitude
- Latitude
- Housing Median Age
- Total Rooms
- Total Bedrooms
- Population
- Households
- Median Income

Target Variable:

- Median House Value

---

## Project Workflow

```text
EDA
↓
Train-Test Split
↓
Preprocessing Pipeline
↓
Model Comparison
↓
Cross Validation
↓
Hyperparameter Tuning
↓
Final Model Selection
```

---

## Models Evaluated

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- HistGradientBoosting Regressor

---

## Best Model

HistGradientBoosting Regressor achieved the best cross-validation performance.

Evaluation Metrics:

- RMSE
- MAE
- R² Score

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn

---

## Key Learnings

Through this project I learned:

- Building preprocessing pipelines using Pipeline and ColumnTransformer
- Handling numerical and categorical features separately
- Comparing multiple machine learning models
- Using Cross Validation for model evaluation
- Performing hyperparameter tuning using GridSearchCV

---
