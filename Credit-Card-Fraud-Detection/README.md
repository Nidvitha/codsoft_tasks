# Credit Card Fraud Detection

## Project Overview

This project uses machine learning to identify potentially fraudulent
credit card transactions. It explores data analysis, class imbalance,
model training, evaluation, and classification threshold tuning.

Two machine learning algorithms were implemented:
- Logistic Regression
- Random Forest

## Dataset

The project uses the Credit Card Fraud Detection dataset from Kaggle.

- Transactions: 284,807 (before removing duplicates)
- Features: 30
- Target: Class
- 0: Legitimate transaction
- 1: Fraudulent transaction

After removing 1,081 duplicate rows, the dataset contained
283,726 transactions, including 473 fraudulent transactions.

Dataset:
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Project Workflow

1. Data loading and exploration
2. Missing-value and duplicate analysis
3. Exploratory data analysis
4. Feature and target separation
5. Stratified train-test split
6. Feature scaling
7. Logistic Regression model training
8. Random Forest model training
9. Model evaluation
10. Precision-Recall curve analysis
11. Classification threshold tuning
12. Feature importance analysis
13. Model serialization

## Exploratory Data Analysis

The original dataset contained 284,807 transactions.

- Legitimate transactions: 284,315
- Fraudulent transactions: 492
- Missing values: 0
- Duplicate rows: 1,081

The dataset was highly imbalanced, with fraudulent transactions
representing approximately 0.17% of the original data.

After removing duplicate rows, the dataset contained 283,726
transactions.

## Models

### 1. Logistic Regression

Logistic Regression was trained using StandardScaler for the
Time and Amount features.

Class weighting was used to account for class imbalance.

### 2. Random Forest

A Random Forest classifier with 100 decision trees was trained.
The balanced_subsample class-weighting strategy was used.

## Model Evaluation

The dataset was divided into training and testing sets using
an 80:20 split with stratified sampling.

The following metrics were used:

- Accuracy
- Precision
- Recall
- F1-score
- Average Precision
- Confusion Matrix

### Results

| Model | Threshold | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.5 | 97.52% | 5.62% | 87.37% | 10.57% |
| Random Forest | 0.5 | 99.95% | 97.10% | 70.53% | 81.71% |
| Random Forest | 0.2 | 99.95% | 92.59% | 78.95% | 85.23% |

The Random Forest model achieved an Average Precision of 0.7977
at the initial model evaluation.

### Threshold Tuning

The classification threshold was adjusted from 0.5 to 0.2
using a validation set.

At the 0.2 threshold, the final Random Forest model achieved:

- Precision: 92.59%
- Recall: 78.95%
- F1-score: 85.23%

On the test set, it correctly detected 75 of 95 fraudulent
transactions and produced 6 false positives.

Threshold selection was performed using validation data.
The test set was also used for earlier model comparisons,
so the final results should be interpreted accordingly.

## Feature Importance

The most influential features in the final Random Forest model
were:

1. V14
2. V10
3. V4
4. V12
5. V17

These are PCA-transformed features, so their original
transaction-level meanings are not directly interpretable.

Feature importance measures model reliance, not causation.

## Project Structure

Credit-Card-Fraud-Detection/
│
├── Credit_Card_Fraud_Detection.ipynb
├── README.md
├── requirements.txt
├── threshold.json
└── fraud_detection_model.pkl

The dataset and trained model are not required to reproduce
the project if the dataset is downloaded and the notebook
is executed.

## How to Run

1. Clone this repository.
2. Download the dataset from Kaggle.
3. Place creditcard.csv in the project directory.
4. Install the required dependencies:

   pip install -r requirements.txt

5. Open the notebook:

   Credit_Card_Fraud_Detection.ipynb

6. Run the notebook cells in order.

## Future Improvements

- Experiment with additional classification algorithms.
- Explore resampling techniques for imbalanced data.
- Optimize the classification threshold using business costs.
- Evaluate models using cross-validation.
- Develop a web application for fraud prediction.

## Author

Nidvitha Adidala