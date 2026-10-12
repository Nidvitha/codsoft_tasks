# Titanic Survival Prediction 🚢

## 1. Project Overview

The Titanic Survival Prediction project uses machine learning
to predict whether a passenger survived the Titanic disaster.

The model uses passenger information such as age, gender,
ticket class, fare, and family relationships to predict
survival.

This project demonstrates the complete machine learning
workflow, including data preprocessing, exploratory data
analysis, model training, and evaluation.

## 2. Objectives

- Perform exploratory data analysis (EDA).
- Handle missing values and preprocess the dataset.
- Visualize patterns in passenger survival.
- Build classification models using Python.
- Evaluate and compare machine learning models.
- Identify important features influencing predictions.

## 3. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- VS Code

## 4. Dataset

The Titanic dataset was obtained from Kaggle.

It contains passenger information, including:

- Passenger class
- Age
- Gender
- Number of siblings and spouses aboard
- Number of parents and children aboard
- Ticket fare
- Port of embarkation
- Survival status

Dataset: https://www.kaggle.com/competitions/titanic/data

The training dataset contains 891 passenger records
and 12 columns.

## 5. Project Workflow

### Exploratory Data Analysis

- Examined the dataset structure and statistical summaries.
- Identified missing values.
- Analyzed survival rates by gender and passenger class.
- Investigated the relationship between age, fare,
  and survival.
- Created visualizations using Matplotlib and Seaborn.

### Data Preprocessing

- Removed unnecessary columns for the initial models.
- Handled missing values in Age and Embarked.
- Used median imputation for Age.
- Used mode imputation for Embarked.
- Applied one-hot encoding to categorical variables.
- Separated the features and target variable.
- Split the data into training and testing sets.

### Model Development

Two classification algorithms were implemented:

1. Logistic Regression
2. Random Forest Classifier

The dataset was split into 80% training data
and 20% testing data.

### Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Five-fold cross-validation was also performed
for the Random Forest model.

## 6. Model Performance

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 80.45% | 81.56% |
| Survivor Precision | 79% | 78% |
| Survivor Recall | 67% | 72% |
| Survivor F1-score | 72% | 75% |

The Random Forest model achieved 81.56% accuracy
on the test dataset.

Its five-fold cross-validation mean accuracy
was 81.37%.

## 7. Feature Importance

The Random Forest model identified the following
features as important for its predictions:

| Feature | Importance |
|---|---:|
| Fare | 27.85% |
| Sex | 26.32% |
| Age | 25.24% |
| Passenger Class | 7.95% |
| SibSp | 5.35% |
| Parch | 4.10% |
| Embarked_S | 2.32% |
| Embarked_Q | 0.87% |

Fare, gender, and age had the highest feature
importance in the trained Random Forest model.

Feature importance indicates predictive contribution
within this model and does not establish causation.

## 8. Project Structure

Titanic-Survival-Prediction/
│
├── Titanic_Survival_Prediction.ipynb
├── Titanic-Dataset.csv
└── README.md

## 9. Conclusion

This project demonstrates how machine learning
can be used to predict passenger survival.

Exploratory data analysis helped identify patterns
in the dataset, while preprocessing prepared
the data for model training.

Logistic Regression achieved 80.45% test accuracy,
and Random Forest achieved 81.56%.

The project provided practical experience in
data analysis, data preprocessing, classification,
model evaluation, and cross-validation.

## 10. Future Improvements

- Perform more extensive feature engineering.
- Use preprocessing pipelines to prevent data leakage.
- Apply hyperparameter tuning.
- Explore additional classification algorithms.
- Evaluate models using repeated cross-validation.
- Improve model performance through systematic
  experimentation.