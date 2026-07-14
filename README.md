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

1. Clone the repository:
   ```bash
   git clone https://github.com/ailinwu520/CreditCardFraudDetection.git
   cd CreditCardFraudDetection
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download `creditcard.csv` from the [Kaggle dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data?select=creditcard.csv) and place it in the project directory (or point to it via the `CREDITCARD_CSV` environment variable).

## Usage

Launch Jupyter and open the notebook:
```bash
jupyter notebook "Credit Card Fraud Detection Project.ipynb"
```

Run the cells top to bottom to reproduce the full pipeline.

## Results

The final Optuna-tuned XGBoost model achieves the following on the held-out test set:

| Metric | Value |
| --- | --- |
| ROC-AUC | ~0.98 |
| Recall (fraud class) | ~0.86 |
| Precision (fraud class) | ~0.74 |
| F1-score (fraud class) | ~0.80 |

These metrics prioritize catching fraudulent transactions (recall) while keeping false positives at a reasonable level, which is the appropriate trade-off for a highly imbalanced fraud-detection problem.


