# DSCI 552 Homework 5

Decision trees as interpretable models on the UCI Acute Inflammations data set, and LASSO / ridge / PCR / L1-penalized boosting for regression on the UCI Communities and Crime data set.

## Structure

```
.
├── Homework 5 Data/
│   ├── diagnosis.data          # Acute Inflammations (UTF-16, tab-separated)
│   ├── diagnosis.names
│   ├── communities.data        # Communities and Crime
│   └── communities.names
├── notebook/
│   └── Agudanmu_Danmu_HW5.ipynb
└── requirements.txt
```

## How to run

```bash
pip install -r requirements.txt
cd notebook
jupyter notebook Agudanmu_Danmu_HW5.ipynb
```

The notebook reads the data with the relative path `../Homework 5 Data/`, so it should be run from the `notebook/` folder. Running all cells takes about a minute, mostly the cross-validation for PCR and XGBoost.

## Contents

- **Problem 1** — Label powerset decision tree on the whole data set, IF-THEN rules, and cost-complexity pruning with 5-fold CV.
- **Problem 2** — Median imputation, correlation matrix, coefficient of variation, scatter/box plots of the 11 highest-CV features, and test MSE of least squares, ridge, LASSO (raw and standardized), PCR and an L1-penalized XGBoost tree (`reg_alpha` chosen by 10-fold CV).
