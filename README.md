# Credit Risk Classification

## Project Overview

This project focuses on developing a credit risk classification model using historical lending data to assess borrowers' creditworthiness accurately. The dataset is divided into training and testing sets, and two logistic regression models are constructed: one using the original data and another using resampled training data. The performance metrics, including accuracy, precision, and recall, are evaluated.

## Project Steps

### 1. Splitting the Data

- The dataset is initially split into training and testing sets to facilitate model training and evaluation.
- Labels (y) are created from the "loan_status" column, where 0 represents healthy loans, and 1 indicates high-risk loans.
- The feature set (X) is created from the remaining columns, excluding "loan_status."
- The balance of the labels variable (y) is checked to understand the class distribution.

### 2. Logistic Regression Model with Original Data

- A logistic regression model is trained using the original data (X_train and y_train).
- Model performance is evaluated, including accuracy, confusion matrix, and classification report.
- The model's ability to predict both healthy and high-risk loans is assessed.

### 3. Logistic Regression Model with Resampled Training Data

- To address class imbalance, the training data is resampled using RandomOverSampler.
- A logistic regression model is trained on the resampled data (X_train_resampled and y_train_resampled).
- Model performance is evaluated similarly to the original model.
- The impact of resampling on model predictions for healthy and high-risk loans is analysed.

## Results

Both models perform well in predicting healthy loans, but the resampled data model shows improved performance in identifying high-risk loans. It achieves higher precision, recall, and F1-scores. Based on the results, it is recommended to use the resampled data model for credit risk classification tasks.

## Dependencies

- NumPy
- Pandas
- Scikit-learn
- Imbalanced-learn

## Instructions

1. Clone this repository to your local machine.
2. Open the Jupyter Notebook provided and follow the step-by-step instructions.
3. Execute the code cells in the notebook to perform the analysis.
4. Review the Credit Risk Analysis Report for detailed results and recommendations.

For detailed code and analysis, please refer to the Jupyter Notebook.
