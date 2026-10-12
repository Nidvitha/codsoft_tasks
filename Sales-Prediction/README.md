# Sales Prediction Using Python

## 1. Project Overview

This project uses machine learning to predict product sales based on advertising expenditure across TV, radio, and newspaper platforms.

The objective is to analyze the relationship between advertising investments and sales and develop regression models to predict sales accurately.

Two machine learning algorithms, Linear Regression and Random Forest Regression, were implemented and evaluated.

## 2. Objectives

- Perform exploratory data analysis (EDA).
- Analyze the relationship between advertising expenditure and sales.
- Visualize data using Matplotlib and Seaborn.
- Build regression models to predict sales.
- Evaluate and compare different machine learning models.
- Identify important features using feature importance.
- Apply cross-validation to assess model performance.

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

The project uses the Advertising dataset, which contains 200 observations.

The dataset includes the following features:

| Feature | Description |
|---|---|
| TV | Advertising expenditure on TV |
| Radio | Advertising expenditure on radio |
| Newspaper | Advertising expenditure on newspapers |
| Sales | Product sales (target variable) |

Dataset source: 
https://www.statlearning.com/resources-python

## 5. Project Workflow

### Exploratory Data Analysis (EDA)

- Examined the dataset structure and statistical summaries.
- Checked for missing values and duplicate records.
- Analyzed the distribution of sales and advertising expenditure.
- Created histograms and scatter plots.
- Calculated correlations between advertising expenditure and sales.
- Visualized correlations using a heatmap.

### Data Preprocessing

- Separated independent and dependent variables.
- Selected TV, Radio, and Newspaper as input features.
- Selected Sales as the target variable.
- Split the dataset into training and testing sets.

### Model Development

Implemented two regression algorithms:

1. Linear Regression
2. Random Forest Regressor

The dataset was split into 80% training data and 20% testing data.

### Model Evaluation

The models were evaluated using the following metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

Five-fold cross-validation was also performed to evaluate model consistency.

## 6. Exploratory Data Analysis Results

The correlation analysis revealed the following relationships with sales:

| Feature | Correlation with Sales |
|---|---:|
| TV | 0.90 |
| Radio | 0.35 |
| Newspaper | 0.16 |

TV advertising showed the strongest linear correlation with sales.

## 7. Model Performance

Both models were evaluated on the same test dataset.

| Metric | Linear Regression | Random Forest |
|---|---:|---:|
| MAE | 1.275 | 0.918 |
| MSE | 2.908 | 1.437 |
| RMSE | 1.705 | 1.199 |
| R² Score | 90.59% | 95.35% |

Random Forest achieved a higher R² score and lower prediction errors on the test dataset.

## 8. Cross-Validation Results

Five-fold cross-validation was used to evaluate model performance.

| Metric | Linear Regression | Random Forest |
|---|---:|---:|
| Mean R² Score | 89.54% | 94.17% |
| Standard Deviation | 0.0314 | 0.0211 |

Random Forest achieved a higher mean R² score and lower variation across the five folds.

## 9. Feature Importance

The Random Forest model identified the following feature importance values:

| Feature | Importance |
|---|---:|
| TV | 84.54% |
| Radio | 13.66% |
| Newspaper | 1.80% |

TV advertising had the highest feature importance in the trained model, followed by radio and newspaper advertising.

Feature importance represents the model's use of each feature and does not establish a causal relationship with sales.

## 10. Conclusion

This project demonstrates the application of machine learning regression techniques to predict product sales using advertising expenditure.

Exploratory data analysis revealed that TV advertising had the strongest correlation with sales.

Two models, Linear Regression and Random Forest Regression, were developed and evaluated.

Linear Regression achieved a test R² score of 90.59%, while Random Forest achieved 95.35%.

Five-fold cross-validation produced mean R² scores of 89.54% for Linear Regression and 94.17% for Random Forest.

The results show that Random Forest performed better across the evaluated metrics on this dataset.

The project provided practical experience in data analysis, visualization, regression modeling, feature importance, and model evaluation.

## 11. Future Improvements

- Perform hyperparameter tuning.
- Experiment with additional regression algorithms.
- Use pipelines to organize preprocessing and model training.
- Evaluate models on additional unseen data.
- Investigate nonlinear relationships between advertising expenditure and sales.

## 12. Project Structure

```text
Sales-Prediction/
│
├── Sales_Prediction.ipynb
├── Advertising.csv
└── README.md
```

## 13. How to Run the Project

1. Clone or download this repository.
2. Install the required libraries.
3. Open `Sales_Prediction.ipynb` in Jupyter Notebook or VS Code.
4. Ensure `Advertising.csv` is in the project directory.
5. Run the notebook cells sequentially.

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```