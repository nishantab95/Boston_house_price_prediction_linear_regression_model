# 🏠 Boston Housing Price Prediction (Linear Regression + Random Forest)

## 📌 Project Overview

This project builds and compares multiple regression models to predict median house prices (`MEDV`) using the Boston Housing dataset.  

The workflow includes:

- Data cleaning  
- Exploratory Data Analysis (EDA)  
- Feature selection  
- Baseline Linear Regression modeling  
- Random Forest modeling  
- Hyperparameter tuning with GridSearchCV  
- Model evaluation and comparison  

The goal was to establish a strong baseline model and then improve performance using nonlinear methods and hyperparameter optimization.

---

## 📂 Dataset

- **Name:** Boston Housing Dataset  
- **Target Variable:** `MEDV` (Median house price in $1000s)  
- **Features:** Socio-economic, environmental, and housing attributes such as:

  - `RM` – Average number of rooms  
  - `LSTAT` – % lower status population  
  - `PTRATIO` – Pupil–teacher ratio  
  - `NOX` – Pollution level  
  - `TAX` – Property tax rate  
  - and others  

---

## 🔍 Exploratory Data Analysis (EDA)

Key EDA steps included:

- **Univariate analysis** – Distribution of individual features  
- **Bivariate analysis** – Relationship between key features and house prices  
- **Multivariate analysis** – Correlation heatmap to identify
- **Outlier analysis** – Identification using IQR method  
- **Feature scaling** (for linear models)

---

## 🧠 Models Implemented

### 1️⃣ Multiple Linear Regression (Baseline)

- Standard train/test split  
- Missing value handling  
- Outlier removal (IQR method for continuous variables)  
- Feature scaling applied  

#### 📊 Performance

| Metric | Value |
|--------|--------|
| R² | ~0.70 |
| Adjusted R² | ~0.62 |
| RMSE | ~3.19 |
| MAE | ~2.25 |

**Interpretation:**  
The linear model explains ~70% of the variance in house prices. It provides a strong and interpretable baseline but is limited by linear assumptions and multicollinearity.

---

### 2️⃣ Random Forest Regressor (Default)

Tree-based model to capture nonlinear relationships and feature interactions.

#### 📊 Performance

| Metric | Value |
|--------|--------|
| R² | ~0.73 |
| RMSE | ~3.00 |
| MAE | ~2.10 |

**Improvement:**  
Better performance than linear regression due to ability to model nonlinear patterns.

---

### 3️⃣ Random Forest (Hyperparameter Tuned with GridSearchCV)

Hyperparameters tuned:

- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`
- `max_features`

Cross-validation: **5-fold CV**  
Scoring metric: **R²**

#### ✅ Best Parameters Found

```python
{
 'max_depth': 10,
 'max_features': 'sqrt',
 'min_samples_leaf': 1,
 'min_samples_split': 2,
 'n_estimators': 100
}
