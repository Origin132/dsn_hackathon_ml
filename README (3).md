# DSN Bootcamp Qualification Hackathon 2026 — ML Track

Machine-learning solution for the DSN Bootcamp Qualification Hackathon 2026 ML Track. The task is to predict `total_sales` for product-store records using the supplied product and store features.

## Project Overview

This project covers:

- Data loading and inspection
- Data cleaning and preprocessing
- Categorical normalization and encoding
- Missing-value handling
- Exploratory data analysis (EDA)
- Feature engineering
- Log transformation of the target variable
- XGBoost regression
- LightGBM regression
- Validation RMSE comparison
- Prediction ensembling
- Final test-set prediction
- Kaggle submission-file generation

## Files

| File | Description |
|---|---|
| `DSN_Hackathon_ML.ipynb` | Complete Jupyter/Kaggle notebook containing the analysis and modelling workflow |
| `submission.csv` | Final prediction file generated from the notebook; contains `id` and `total_sales` |

## Modelling Results

The validation results recorded in the notebook are:

| Model | Validation RMSE |
|---|---:|
| XGBoost | 1135.9101 |
| LightGBM | 1121.3602 |
| 60/40 XGBoost–LightGBM ensemble | 1128.5394 |

The validation target was evaluated on the original `total_sales` scale after reversing the `log1p` transformation.

## Final Test Predictions

The notebook recorded the following range and mean for the final ensemble predictions:

- Minimum prediction: 50.57
- Maximum prediction: 5747.48
- Mean prediction: 1952.60
- Test rows: 1,705

## Reproducing the Analysis

The notebook was developed in a Kaggle/Jupyter environment. To reproduce it:

1. Open `DSN_Hackathon_ML.ipynb` in Jupyter, Kaggle, or another compatible notebook environment.
2. Place the competition `train.csv` and `test.csv` files in the expected input location.
3. Install/import the required Python packages, including `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`, and `lightgbm`.
4. Run the notebook from the beginning so that preprocessing, feature engineering, model training, prediction, and submission generation occur in sequence.

## Submission Format

The submission file contains exactly two columns:

```text
id,total_sales
```

and 1,705 prediction rows.

## Note

The notebook contains the modelling workflow and the outputs captured during the Kaggle run. If the model parameters are changed, the notebook should be rerun before treating the resulting metrics or submission file as corresponding to the new configuration.

## Competition

DSN Bootcamp Qualification Hackathon 2026 — Machine Learning Track.
