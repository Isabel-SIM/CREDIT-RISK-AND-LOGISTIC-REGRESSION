# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

    The analysis aims to develop machine learning models for predicting the creditworthiness of borrowers using historical data from a peer-to-peer lending services company.

* Explain what financial information the data was on, and what you needed to predict.

    The dataset includes various financial information about borrowers, such as credit scores, income, and debt-to-income ratio, as well as loan-related details. 
    The primary goal is to distinguish healthy loans (0 label) from high-risk loans (1 label).

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

    The variable being predicted in this analysis is the 'loan_status' variable, which indicates the status of the loan. It is a binary variable with two possible values: 0 for healthy loans and 1 for high-risk loans. To gain insight into the distribution of loan status in the dataset, I used the value_counts function.

* Describe the stages of the machine learning process you went through as part of this analysis.

    - Data preparation.
    - Data analysis: The labels were checked using value_counts(), and the data was split into training and testing sets using train_test_split.
    - Logistic regression: The original training data (X_train and y_train) was used to fit the logistic regression model. Predictions were made on the testing data (X_test), and the model's performance was evaluated using metrics such as accuracy score, confusion matrix, and classification report.
    - Logistic regression with resampled data: To address the class imbalance issue, where high-risk loans were underrepresented, the data was resampled using RandomOverSampler. The logistic regression model was then fitted using the resampled training data (X_train_resampled and y_train_resampled), and predictions were made on the testing data. The model's performance was evaluated using metrics like accuracy score, confusion matrix, and classification report.


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

    To predict the loan status, I employed logistic regression as the machine learning algorithm. Logistic regression is a widely adopted method specifically designed for binary classification tasks, making it a suitable choice for accurately predicting the two loan status categories. 
    Additionally, to address the class imbalance issue in the dataset, I used the RandomOverSampler resampling method to generate synthetic samples - to achieve a more balanced training set.

# Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

    Model 1: Logistic Regression Model with Original Data
    Balanced accuracy score: 0.9521352751368186
    
    Label 0 (healthy loan):
    - Precision: 1.00
    - Recall: 1.00
    - F1-score: 1.00
    
    Label 1 (high-risk loan):
    - Precision: 0.86
    - Recall: 0.91
    - F1-score: 0.88

    Machine Learning Model 2:
    Accuracy Score: 0.9941749445500477

    Label 0 (healthy loan):
    - Precision: 1.00
    - Recall: 0.99
    - F1-score: 1.00

    Label 1 (high-risk loan):
    - Precision: 0.85
    - Recall: 0.99
    - F1-score: 0.92


# Summary:

    Both models performed well in predicting healthy loans (0 label) with high accuracy, precision, recall, and F1-scores. However, they differ in their performance for high-risk loans (1 label).

    - Model 1 accurately identifies a significant portion of high-risk loans but has lower precision compared to healthy loans.

    - Model 2, which uses resampled data, demonstrates improved performance for high-risk loans with higher precision and balanced F1-score.

    Considering the goal of accurately identifying high-risk loans and achieving a balance between precision and recall, Model 2 with resampled data is recommended. (Achieving a balance between precision and recall, is crucial for making informed lending decisions.)