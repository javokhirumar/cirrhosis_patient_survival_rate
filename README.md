# Cirrhosis Survival Prediction

Predict patient survival status for cirrhosis using clinical and lab data with **LightGBM**.

## Dataset

* `train.csv` (15,000 rows), `test.csv` (10,000 rows)
* Target: `Status` (C = alive, D = dead, CL = censored)
* Features: Age, Sex, Drug, lab tests (Bilirubin, Albumin, SGOT, etc.), clinical indicators, Stage

## Steps

1. **EDA** – Checked missing values, duplicates, outliers, and feature distributions
2. **Preprocessing** – Removed `id` & `N_Days`, capped outliers, encoded categorical features
3. **Modeling** – LightGBM (multiclass), handled class imbalance with weights
4. **Evaluation** – Confusion matrix, log loss = 0.4266, confidence ≈ 0.66
5. **Prediction** – Generated probabilities for `Status_C`, `Status_CL`, `Status_D`
