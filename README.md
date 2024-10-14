# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The report aims at predicting healthy loans by the assistance of model. 

* Explain what financial information the data was on, and what you needed to predict.

Loan Amount: The size of the loan issued to the borrower.
Interest Rate: The rate at which interest is charged on the loan.
Term of the Loan: The duration for which the loan is taken (e.g., 36 months, 60 months).
Annual Income: The borrower’s reported annual income.
Debt-to-Income Ratio (DTI): A measure of the borrower’s total debt compared to their income, often used to assess their ability to repay the loan.
Credit Score: A numeric representation of the borrower's creditworthiness, based on their credit history.
Loan Purpose: The reason for taking the loan (e.g., debt consolidation, home improvement).
Delinquencies: Information on how many past payments the borrower has missed on any loan.
Employment Length: How long the borrower has been employed at their current job.
Public Records: The number of derogatory public records associated with the borrower, like bankruptcies.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

To understand the target variable we were trying to predict, which is loan_status, we can use the value_counts() method. This method provides the count of unique values in a Series, giving insight into the distribution of loan statuses in the dataset.

* Describe the stages of the machine learning process you went through as part of this analysis.


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithm).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.
Data Collection:

Gathered the lending data, which contains various features related to borrowers and their loans.
Data Preprocessing:

Data Cleaning: Checked for missing values and handled them appropriately (imputation or removal).
Feature Selection: Identified relevant features for predicting loan status and separated the target variable from the features.
Encoding Categorical Variables: If there were categorical variables, they were converted to numerical format using techniques like one-hot encoding or label encoding.
Normalization/Scaling: Normalized or standardized the data to ensure that all features contribute equally to the model, especially important for algorithms like Logistic Regression.
Data Splitting:

Split the data into training and testing sets using train_test_split. This allows for evaluating model performance on unseen data.
Model Selection:

Chose the Logistic Regression model for its interpretability and effectiveness for binary classification problems.
Model Training:

Fit the model on the training data using the fit method, allowing it to learn the relationship between the features and the loan status.
Model Prediction:

Used the trained model to make predictions on the testing set with the predict method.
Model Evaluation:

Evaluated the model using a confusion matrix to assess its performance. Key metrics like accuracy, precision, recall, and F1 score were calculated to measure how well the model predicts both classes (0 for healthy loans and 1 for high-risk loans).
Interpretation of Results:

Interpreted the results to understand the model’s performance and how well it distinguishes between healthy and high-risk loans.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

The 0 label corresponds to healthy loans, which form the majority of the dataset. To assess how well the model predicts healthy loans, we focus on True Negatives (TN) and False Positives (FP).

Precision for 0 (healthy loans): Precision answers the question: "When the model predicts a loan is healthy, how often is it correct?"

Conclusion for Label 0 (Healthy Loan):
The model performs exceptionally well in predicting healthy loans, with both high precision (99.5%) and recall (99.7%).

Conclusion for Label 1 (High-Risk Loan):
The model performs well in predicting high-risk loans, with a precision of 84.7% and recall of 91%. It identifies most high-risk loans correctly but does misclassify some high-risk loans as healthy (56 false negatives).

Overall Model Performance:
The model is excellent at predicting healthy loans (label 0), with very high precision and recall, meaning that it rarely misclassifies healthy loans as high-risk.
For high-risk loans (label 1), the model still performs well but is less perfect. It manages to catch 91% of actual high-risk loans, but around 15% of the time, when it predicts high-risk loans, it is incorrect.

Summary:
The model performs extremely well at identifying healthy loans (0), rarely misclassifying them.
The model is good at identifying high-risk loans (1) with a high recall of 91%, though its precision of 84.7% suggests that it sometimes classifies healthy loans as high-risk. Overall, it does a solid job at distinguishing between the two classes.

If you do not recommend any of the models, please justify your reasoning.