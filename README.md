🏠 Boston Housing Price Prediction (Linear Regression)
📌 Project Overview

This project builds a multiple linear regression model to predict median house prices (medv) using the Boston Housing dataset. The workflow covers data cleaning, exploratory data analysis (EDA), feature selection, model training, and evaluation to establish a strong baseline regression model.

📂 Dataset

Name: Boston Housing Dataset

Target Variable: medv (Median house price in $1000s)

Features: Socio-economic, environmental, and housing attributes such as:

rm (average number of rooms)

lstat (% lower status population)

ptratio (pupil–teacher ratio)

nox (pollution level)

tax (property tax rate)

and others

🔍 Exploratory Data Analysis (EDA)

Key EDA steps included:

Univariate analysis: Distribution of individual features

Bivariate analysis: Relationship between key features and house prices

Multivariate analysis: Correlation heatmap to identify important predictors and multicollinearity

Outlier analysis: Identification of extreme values using the IQR method

🧠 Model

Algorithm: Multiple Linear Regression

Train/Test Split: Standard hold-out split

Preprocessing:

Missing value handling

Outlier detection and removal using IQR (for continuous features, excluding medv and chas)

📊 Model Performance
Metric	Value
R² Score	~0.68
Adjusted R²	~0.56
MSE	~10.78
RMSE	~3.28
MAE	~2.30

Interpretation:
The model explains approximately 68% of the variance in house prices. On average, predictions deviate from actual prices by around $3,300, indicating strong baseline performance for a linear regression model on this dataset.

🧪 How to Run

Clone the repository

git clone https://github.com/your-username/boston-housing-regression.git
cd boston-housing-regression


Install dependencies

pip install -r requirements.txt


Run the notebook
Open the Jupyter notebook and run all cells to reproduce the analysis and results.

📁 Project Structure
.
├── data/                  # (optional) dataset files
├── notebooks/             # Jupyter notebooks with EDA & modeling
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
└── results/               # (optional) figures, plots, metrics

🚀 Future Improvements

Apply regularized regression (Ridge, Lasso) to handle multicollinearity

Try non-linear models (Random Forest, XGBoost)

Perform feature engineering and transformations

Cross-validation for more robust evaluation

🙌 Acknowledgements

Dataset: UCI / Scikit-learn Boston Housing dataset

Libraries: NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn

📬 Contact

If you have suggestions or feedback, feel free to open an issue or reach out!
