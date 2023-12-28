# Customer Spending Score Prediction

This repository contains code for predicting customer spending scores based on various customer attributes. The dataset used for this project is the "Customers.csv" dataset, which includes information about customers such as age, annual income, gender, profession, work experience, and family size.

## Setup

Before running the code, make sure you have installed the necessary libraries and downloaded the dataset. You can set up your environment by following these steps:

1. Install the Kaggle library and configure it with your Kaggle API credentials. Ensure you have a Kaggle account and generate your API token as `kaggle.json`.

```python
! pip install kaggle
```

2. Download the dataset from Kaggle using the Kaggle CLI:

```python
! kaggle datasets download -d datascientistanna/customers-dataset
```

3. Unzip the downloaded dataset:

```python
! unzip customers-dataset.zip
```

4. Remove unnecessary files:

```python
! rm customers-dataset.zip
```

## Data Exploration and Preprocessing

The code begins with data exploration and preprocessing steps, including:

- Loading the dataset and inspecting its structure.
- Handling missing values (using the most frequent value for profession in this case).
- Visualizing the distribution of features and target variable.
- Creating new features based on domain knowledge.

## Feature Engineering

Feature engineering is a crucial part of preparing the dataset for modeling. In this project, the code creates new features like "Income_by_Experience," "Experience_per_member," "Income_per_member," and others based on domain-specific knowledge.

## Model Building

The code implements various regression models for predicting customer spending scores, including:

- Random Forest Regressor
- Support Vector Regressor (SVR)
- Extra Trees Regressor
- AdaBoost Regressor
- XGBoost Regressor
- LightGBM Regressor

Each model is trained and evaluated using root mean squared error (RMSE) as the evaluation metric.

## Stacking Models

The key focus of this project is on stacking models. Stacking is an ensemble learning technique that combines predictions from multiple models to achieve better predictive performance. The code demonstrates stacking by training a Random Forest Regressor on the predictions of the individual models (SVM, Extra Trees, AdaBoost, XGBoost, LightGBM).

## Conclusion

This repository provides a comprehensive example of how to approach a customer spending score prediction problem using machine learning and stacking techniques. You can use this code as a starting point for your own projects and explore ways to improve model performance and feature engineering.

If you have any questions or suggestions, please feel free to reach out. Happy modeling!