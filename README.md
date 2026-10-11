# Telco Customer Churn — Data Cleaning and Preprocessing

**Course:** Data Science — Assignment No. 2  
**Name:** Afifa Jabbar
**Roll No:** SU92-BSCSM-F25-012

## Dataset
- **Title:** Telco Customer Churn
- **Source:** https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- **Size:** 7,043 rows × 21 columns
- **Objective:** Predict whether a telecom customer will leave (churn).

## What this project does
| Stage | Work done |
|---|---|
| Data cleaning | hidden missing values, duplicates, inconsistent categories, wrong data types, outliers |
| Preprocessing | feature/target split, variable types, encoding (binary, ordinal, one-hot), standardization, log transform for skewed data, feature engineering |
| Leakage prevention | train-test split **before** fitting any scaler or encoder |

## Key findings
- `TotalCharges` was stored as text and had 11 hidden blank values (all new customers with tenure 0) → converted to numeric and filled with 0.
- "No internet service" / "No phone service" were merged into "No".
- `TotalCharges` was right-skewed → `log1p` transformation.
- New features created: `AvgMonthlySpend`, `NumServices`, `HasFamily`.

## Files
- `telco-churn-data-cleaning.ipynb` — the full notebook with code, outputs and explanations
- `processed_data/` — cleaned and preprocessed output files (optional, if uploaded)

## How to run
Open the notebook on Kaggle or Google Colab, add the dataset (or upload the CSV), and run all cells.

