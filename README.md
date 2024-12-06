# Predicting Loan Interest Rates Using Machine Learning: A Model Comparison and Evaluation

This project focuses on predicting the interest rate assigned to a loan based on various financial and personal factors. The goal was to clean, prepare, and model the loan dataset, using machine learning techniques to create a robust model and evaluate its performance.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Cleaning and Preparation](#data-cleaning-and-preparation)
3. [Modeling Techniques](#modeling-techniques)
4. [Testing and Evaluation](#testing-and-evaluation)
5. [Findings and Results](#findings-and-results)
6. [Conclusion](#conclusion)
7. [Files and Code](#files-and-code)

## Project Overview

In this project, I worked with a loan dataset where the goal was to predict the interest rate assigned to each loan. The project involved several steps including data cleaning, model building, and testing on a holdout dataset. The model performance was evaluated using Root Mean Squared Error (RMSE) on a holdout test set.

## Data Cleaning and Preparation

The dataset contained missing values and irrelevant features that needed to be cleaned and prepared for analysis. The cleaning steps included:
- **Identifying Missing Values**: I calculated the percentage of missing values for each column.
- **Handling Missing Data**: Based on the distribution of missing values, I decided to drop certain columns that either had too many missing values or were not relevant to the prediction task. These included columns like `loan_reason`, `months_since_last_delinq`, and `months_since_last_public_record`.
- **Data Transformation**: Numerical features were retained and transformed as necessary, while categorical features were encoded appropriately.


## Modeling Techniques

I built several machine learning models to predict the interest rate of loans, including:

- **Linear Regression**: A baseline model to evaluate the impact of linear relationships between features and the target variable.
- **Random Forest Regressor**: A more complex model to capture non-linear patterns in the data.
- **Gradient Boosting Machine (GBM)**: A high-performing model that works well for structured data by combining multiple weak learners.
  
Each model was built using Python and evaluated based on its performance on the holdout dataset.

## Testing and Evaluation

I evaluated the final model on the "Holdout for Testing" dataset, using RMSE as the evaluation metric. The results were saved in a separate CSV file.

## Findings and Results
After evaluating different models, the Random Forest Regressor yielded the best performance with an RMSE of 1.3412. The model effectively captured complex relationships in the dataset that simpler models like Linear Regression could not.

Key findings:

- Feature Importance: The most important features influencing the interest rate were annual_income, loan_amount_funded, and debt_to_income_ratio.
- Data Challenges: Missing data in some columns required careful handling, but the results showed that dropping certain columns did not significantly hurt the model's performance.

## Conclusion
This project demonstrated the process of cleaning, modelling, and testing a machine learning model to predict loan interest rates. The Random Forest Regressor provided the most accurate predictions, and the results were stored in a CSV file for further analysis.

## Files and Code

loan_interest_rate_model.pkl: Saved model after training.

Results_from_ArushiMakraria.csv: Final predictions on the test set.

data_cleaning.py: Code for cleaning and preparing the data.

modeling.py: Code for building and evaluating the models.


Feel free to explore the repository for more details!



