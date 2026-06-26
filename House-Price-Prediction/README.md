# California Housing Price Prediction

## Project Overview

This project predicts California housing prices using supervised machine learning regression techniques.

The primary objective was to build a complete end-to-end machine learning workflow starting from raw data exploration to a final predictive model capable of estimating median house values.

The project covers every major stage of a real-world machine learning pipeline, including:

- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Cleaning
- Data Preprocessing
- Baseline Model Development
- Model Comparison
- Cross Validation
- Hyperparameter Tuning
- Model Evaluation
- Feature Importance Analysis
- Residual Analysis
- Prediction System

---

## Dataset

The project uses the California Housing Dataset.

Source:

https://www.kaggle.com/code/hassaan2580/california-housing-dataset

The dataset contains 20,640 observations collected from the 1990 California Census.

### Original Features

- Longitude
- Latitude
- Housing Median Age
- Total Rooms
- Total Bedrooms
- Population
- Households
- Median Income
- Ocean Proximity

### Engineered Features

To improve model performance, three additional features were created:

- Rooms per Household
- Bedrooms per Room
- Population per Household

### Target Variable

- Median House Value

---

## Project Workflow

Feature Engineering

↓

Exploratory Data Analysis (EDA)

↓

Train-Test Split

↓

Feature Preprocessing Pipeline

↓

Baseline Model

↓

Model Comparison using Cross Validation

↓

Hyperparameter Tuning

↓

Final Model Training

↓

Model Evaluation

↓

Feature Importance Analysis

↓

Residual Analysis

↓

Prediction System

---

## Exploratory Data Analysis

The exploratory data analysis focused on understanding the dataset before model development.

The analysis included:

- Dataset overview
- Missing value analysis
- Duplicate value detection
- Descriptive statistics
- Distribution analysis
- Outlier detection
- Correlation analysis
- Feature relationship analysis

Several important observations were made:

- Only the **total_bedrooms** feature contained missing values.
- The target variable is right-skewed and capped near \$500,000.
- Several numerical features contain genuine high-value outliers.
- Median Income showed the strongest positive correlation with house prices.
- High multicollinearity existed among room and population-related variables.

---

## Data Preprocessing

A preprocessing pipeline was built using Scikit-Learn's Pipeline and ColumnTransformer.

The preprocessing steps included:

### Numerical Features

- Median Imputation
- Standard Scaling

### Categorical Features

- Most Frequent Imputation
- One-Hot Encoding

The preprocessing pipeline ensured that identical transformations were applied during both training and prediction.

---

## Models Evaluated

The following regression algorithms were evaluated:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- HistGradientBoosting Regressor

Model performance was compared using 5-Fold Cross Validation.

Evaluation metrics:

- RMSE
- MAE
- R² Score

---

## Hyperparameter Tuning

The best-performing model, HistGradientBoostingRegressor, was further optimized using GridSearchCV.

The following hyperparameters were tuned:

- Learning Rate
- Maximum Depth
- Maximum Leaf Nodes
- Minimum Samples per Leaf
- L2 Regularization

The optimized model achieved improved cross-validation performance compared to the default configuration.

---

## Final Model Performance

The final tuned HistGradientBoostingRegressor achieved the following performance on the test dataset:

| Metric | Score |
|----------|--------|
| RMSE | 44,401.13 |
| MAE | 29,503.81 |
| R² Score | 0.852 |

---

## Feature Importance

Permutation Importance was used to determine which variables contributed most to the model's predictions.

The most influential features were:

- Latitude
- Longitude
- Median Income
- Population per Household
- Ocean Proximity

The analysis showed that geographic location and neighborhood income are the strongest predictors of California housing prices.

---

## Residual Analysis

Residual plots were generated to evaluate model errors.

The residual distribution indicated that prediction errors were centered around zero without significant systematic patterns, suggesting that the model generalizes well on unseen data.

---

## Prediction System

A reusable prediction function was developed that accepts housing characteristics as input and returns the estimated median house value.

The function automatically performs feature engineering before generating predictions using the trained model.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn

---

## Machine Learning Concepts Demonstrated

This project demonstrates practical implementation of:

- Feature Engineering
- Data Cleaning
- Missing Value Imputation
- Pipeline
- ColumnTransformer
- StandardScaler
- One-Hot Encoding
- Cross Validation
- Hyperparameter Tuning
- Model Comparison
- Permutation Feature Importance
- Residual Analysis
- Regression Evaluation Metrics

---

## Key Learnings

Through this project, I learned how to:

- Build end-to-end machine learning workflows.
- Engineer meaningful features to improve predictive performance.
- Create reusable preprocessing pipelines.
- Compare multiple regression algorithms using cross-validation.
- Optimize models using GridSearchCV.
- Interpret model behavior using permutation feature importance.
- Evaluate regression models using RMSE, MAE, and R² Score.
- Build a prediction system suitable for future deployment.
