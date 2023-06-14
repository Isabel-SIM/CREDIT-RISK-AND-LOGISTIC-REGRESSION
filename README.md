<h1>Credit Risk Classification</h1><br>

This project develops a credit risk classification model using historical lending data to accurately identify borrowers' creditworthiness. The dataset is split into training and testing sets, and two logistic regression models are created: one using the original data and another using resampled training data. Performance metrics, including accuracy, precision, and recall, are evaluated.<br><br>

The project involved the following steps:<br><br>

<b>1.</b> Splitting the Data: The dataset was divided into training and testing sets.<br><br>

<b>2.</b>  Logistic Regression Model with Original Data: A logistic regression model was trained and evaluated using the original data. Performance metrics, such as accuracy, confusion matrix, and classification report, were calculated.<br><br>

<b>3.</b>  Logistic Regression Model with Resampled Training Data: The training data was resampled using RandomOverSampler to address class imbalance. A logistic regression model was trained on the resampled data and evaluated on the testing set.<br><br>

<b>4.</b>  Credit Risk Analysis Report: A summary report was provided, comparing the performance of both models. The analysis was based on the accuracy, precision, and recall scores.<br><br>

Both models perform well in predicting healthy loans, but the resampled data model shows improved performance in identifying high-risk loans. It achieves higher precision, recall, and F1-scores. Based on the results, it is recommended to use the resampled data model for credit risk classification tasks.
