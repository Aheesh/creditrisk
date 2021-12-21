# Credit Risk Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  
  --> The purpose of the analysis is to use historical data to predict the credit worthiness of a customer and predict which customer could potentially end-up defaulting from their loan(s).
  
* Explain what financial information the data was on, and what you needed to predict.
  
  --> The data available captures the borrowers income, details about their debt from total loan , debt to income ratio, and how has their past been in terms of repaying back the loan, also if they have defaulted on their loan(s).
  
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  
  --> We are trying to predict the 'loan status' variable i.e. is the borrower likely to repay ot loan or default on the repayment.
  
* Describe the stages of the machine learning process you went through as part of this analysis.
  --> We followed the basic stages of Model - Fit - Predict using Logistics Regression model. Followed by measuring the accuracy of our prediction. Since the data was imbalanced with small no. of bad-loans in the dataset we Oversampled using RandomOverSampler and repeated the Model - Fit - Predict steps using over_sampled data. 
  
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
  --> As shared above we used Logistics Regression model since this was a binary result type of analysis to predict the quality of loan. The data set represented a small no. of records for bad loans and using Random Over Sampling method we addressed the imbalanced data challenge.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  The Logistic Regression model shows a perfect score in terms of accuracy in prediciting 'Healthy Loan', this could possibly indicate overfitting. The model does how high accuracy of 85% for detecting high-risk loan and a 91% recall value i.e. its good at predicting high-risk loans.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  The logistics regression model retains the 100% accuracy for detecting 'healthy loans' and the accuracy drops 1 basis points for detecting high-risk loans. The recall value for high-risk loan detection goes upto 99% on the oversampled data. Overall oversampling helped improve the recall value for high-risk loan without any significant reduction in accuracy.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best? 
  The Logistics Regression model on Over Sampled data performed best in this case, as it improved the recall score without any downgrade in accuracy of reporting bad-loans.
  
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  Peformance does depend on the problem. In this case of predicting loan/borrower quality the data in general and specifically in this case is imbalanced with smaller number of bad borrowers represented in the data set. From a overall business viability perspective its important for the financial lending company to be able to predict loan defaulters to be able to continue to work with more quality borrowers and make more qualoty loans. 
  
  I recommend the Logistics Regression model using random oversampling to improve the detection of bad borrowers.
  
If you do not recommend any of the models, please justify your reasoning.
 I recommend the Logistics Regression model using random oversampling to improve the detection of bad borrowers.