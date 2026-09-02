# Credit Card Fraud Detection

## Project Overview
This project focuses on detecting fraudulent credit card transactions using machine learning. 
The dataset is highly imbalanced, with only a small fraction of transactions being fraudulent. 
The goal is to build a predictive model that can accurately identify fraud while minimizing false positives.

Key highlights of the project:
- Data preprocessing and feature engineering
- Handling class imbalance with SMOTE
- Training models including XGBoost with hyperparameter tuning
- Model evaluation using metrics suitable for imbalanced datasets (Precision, Recall, F1-score, ROC-AUC)
- Model interpretation using feature importance and SHAP values

## Dataset
The dataset used in this project is available on Kaggle:

[Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data?select=creditcard.csv)

**Note:** To run this code, you need to download the dataset manually from Kaggle and place `creditcard.csv` in the same directory as the notebook.

## Setup
1. Create and activate a virtual environment (optional but recommended).
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Download `creditcard.csv` from Kaggle (see above) and place it in the project root, or set the `CREDITCARD_CSV` environment variable to its path.
4. Open and run `Credit Card Fraud Detection Project.ipynb` top to bottom.

## Results
Using an XGBoost classifier trained on SMOTE-resampled data:

| Metric (fraud class) | Score |
|---|---|
| Precision | 0.74 |
| Recall | 0.86 |
| F1-score | 0.80 |
| ROC-AUC | 0.98 |
