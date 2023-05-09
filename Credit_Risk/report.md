# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis is to automate the classification process for calculating the risk of providing loans to people, based on a number of different numerical metrcis.

The data in this financial model consists of; loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt. And the column to predict is loan status, where a value of 0 indicates low risk, and 1 indicates high risk.

The variable in which this model is trying to predict is "loan status" to use this data to possibly make predictions on whether or not an individual should be approved for a loan. In the training data there were 75,036 instances where loans were approved (low risk), and only 2500 cases where loans were denied (high risk).

 First data was sepparated into the label category, represented as "y", in this case the loan_status column, and the variables "X", which represent the data with which to train the model. Then the data was then assessed and split into training data and test data, and stratified, so as to ensure that both groups were representitive of the total population. The model was trained and produced a score of 99 percent accuracy. This may however have been due to the relatively small sample group of high risk loans, which had a relatively poor recall of 89%. To improve on this, the data was oversampled, so that it was trained with data containing 56277 low risk and an equal number of high-risk datapoints.
 
After re-training the model, the recall of both high risk and healthy loans were 100%

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
                precision    recall  f1-score   support

healthy_loan       1.00      1.00      1.00     18759
high-risk_loan     0.87      0.89      0.88       625
accuracy                               0.99     19384

Although accuracty was high, there were only 625 samples in the high risk category to train on, and the recall was only 0.9, suggesting the model has overtrained on healthy loan data, and will opt to select healthy_loan, as statistically it will generally be the correct answer.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
                precision    recall  f1-score   support

healthy_loan         1.00      1.00      1.00     18759
high-risk_loan       0.87      1.00      0.93       625

      accuracy                           1.00     19384

When oversampling the data, the model has performed better, obtaining 100% recall for both options, and the overall accuracy has improved to 100%

## Summary

 The second model performed best, as although there isn't much difference in the accuracy between the two models, the second model is more accurate at predicting high risk loans, which overall are more likely at causing the company to lose money (making them more impoptant to predict correctly). The second model, after training on equal amounts of healthy and riskly loan data, has achieved an accuracy of 100 percent and perfect recall for both categories, suggesting it would be an adequate model to employ to speed up the classification process.

