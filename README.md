# Asset Pricing & Machine Learning: Factor Zoo

## Objective
Predict future stock returns using a wide array of explanatory variables ("factor zoo") by applying both linear and machine learning models. The goal is to identify robust predictive signals and evaluate their out-of-sample performance.

## Project Structure

```
.
│
├── README.md                  # Project description
├── data/
│   ├── raw/                   # Original data (Fama-French, Yahoo)
│   └── processed/             # Final dataset with features + target
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_linear.ipynb
│   ├── 04_model_ml.ipynb
│   └── 05_evaluation.ipynb
├── models/
│   └── pricing_model.py       # Model classes
├── utils/
│   └── data_loader.py         # Functions for downloading and cleaning data
└── requirements.txt
```

## Models
- OLS Linear Regression (baseline)
- Lasso / Ridge Regression
- Random Forest Regressor
- XGBoost Regressor
- Evaluation with R², MAE, Information Coefficient

## Data
- **Financial factors**: Kenneth French (Size, Value, Momentum, etc.)
- **Price data**: Yahoo Finance (via yfinance)
- **Fundamentals**: Alpha Vantage, Kaggle (e.g. ROE, leverage, P/E)

## Data frequency
- Monthly, panel format (stock-month): one row per stock per month

## Target
- One-month-ahead realized return (`return_next_month`)

## Tech Stack
- Python, pandas, sklearn, xgboost, matplotlib, seaborn, statsmodels
- Jupyter Notebook

---
