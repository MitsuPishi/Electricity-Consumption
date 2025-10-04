# Electricity Consumption Prediction – Quera FinAi Competition

This repository contains my solution for the **FinAi competition on Quera.org**, where the task is to predict **electricity consumption (kWh)** based on given features.
The dataset is provided by Quera and includes training and test sets.

* **train.csv** – Training data with electricity consumption labels
* **test.csv** – Test data for final predictions (without labels)
* **electricity_consumption.ipynp** – Main training & optimization code
* **submission.csv** – Example output file for competition submission

---

## Approach

The solution explores two main models:

1. **XGBoost Regressor**

   * Hyperparameter tuning with **Optuna** (Bayesian optimization)
   * Cross-validation based on R² score
   * Final model trained on full training set

2. **Linear Regression with Polynomial Features**

   * Pipeline including optional scaling & polynomial feature expansion
   * Hyperparameter tuning with **Optuna** (degree and scaler usage)
   * Serves as a baseline comparison

The final competition submission uses the **XGBoost model** with the best parameters found during optimization.

---

## Submission Format

The submission file must include:

* `electricity_consumption_kWh` (predicted values)

Example:

```csv
 electricity_consumption_kWh
123.45
150.67
98.32
...
```

---

## Results

* Best model: **XGBoost Regressor**
* Evaluation metric: **R² Score**
* Validation R²: ~ (varies depending on split and tuning)

---

## Notes

* This repository is for educational and competition purposes.
* Data files are not included here due to competition rules. Please download them directly from Quera FinAi.
* [Dataset Link](https://quera.org/contest/assignments/4367/download_problem_initial_project/287260/)
---

## Acknowledgements

* [Quera.org](https://quera.org/) for hosting the FinAi competition
* [Optuna](https://optuna.org/) for hyperparameter optimization
* [XGBoost](https://xgboost.readthedocs.io/) for gradient boosting
