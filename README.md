# credit_risk_classification
## Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Credit Analysis

## Instructions
The instructions for this Challenge are divided into the following subsections:

1. Split the Data into Training and Testing Sets

    Create a Logistic Regression Model with the Original Data

2. Write a Credit Risk Analysis Report

# Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:

1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
  
2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
  
   NOTE
   A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
  
3. Split the data into training and testing datasets by using train_test_split.

# Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:

1. Fit a logistic regression model by using the training data (X_train and y_train).
    
2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

# Evaluate the model’s performance by doing the following:

1. Generate a confusion matrix.
    
2. Print the classification report.

# Answer the following question: 
How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Write a Credit Risk Analysis Report
The purpose of this analysis is to evaluate whether borrowers are ‘at-risk’ or ‘credit-worthy’ to lend to.

I imported data reading the loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt. These were the features, while the label was the loan status. Using the features, we needed to predict whether borrowers were credit worthy to lend to or not. The label was a confirmation whether borrowers received a loan or not.  

Once I had the feature and labels saved in X and y variables, I then ran a “train-test-split” from sklearn which gave me my training data to train the model on, and the testing data to then test the model. 

I instantiated a Logistic Regression model and fit it with the training data to train the model. Using the ‘X-test’ data, I then had the model make predictions for the labels. This is where the machine predicts whether the borrower would receive a loan or not. These predicted labels were then ran against the actuals labels.

To analyze the results of the model, I generated a confusion matrix and printed a confusion matrix.

## Results

Using bulleted lists, describe the balanced accuracy score and the precision and recall scores of the machine learning model.
•	The accuracy score of the Logistic Regression model is 94%
•	Both the precision and recall for predicting healthy loans is 100%
•	The precision for predicting high-risk loans is 87%
•	The recall for predicting high-risk loans is 89%

## Summary

For this data set it is most important to predict the high-risk loans and this model did have a lower precision and recall score for predicting these borrowers. When evaluating the confusion matrix, it was found that with a testing sample size of 2,384, there were 80 false positives and 67 false negatives given by the model. That means that 80 borrowers were predicted to provide loans to when they were high-risk borrowers.

I would want to develop a model with a higher precision and recall ratings on predicting at-risk borrowers.   

