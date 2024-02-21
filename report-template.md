# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of the analysis is to build a model that can identify the creditworthiness of borrowers based on the historical behavior of lenders and a dataset from a peer-to-peer lending company
* The information contains data on the size of the debt acquired by the client, the interest rate, and the total debt. It also includes the client's income information, the number of accounts that they have, and the loan status. What we need to predict from this information is if the client's loans are at a high risk of defaulting or if the credit is healthy, considering the status of the clients.
* In this data set, there is 30 times more data about the healthy clredit status than the high risk of defaulting. 75036 clients in a healthy situation and 2500 clients in a high risk of defaulting.
* To train this model the data was divided into two sets, the training and the test data sets, one to fit the model and the second to test the result of the work. Then the labels set (y) and the features set (X) were created to better manipulate the data and feed the model. With the data set split a logistic regression model was created and fitted with the X_tran and y_train data sets. After that, the model was fitted with the test data sets and predictions were created resulting in a 100% accuracy in predicting healthy loans and a 91% accuracy in predicting high-risk loans. Considering that there is a big discrepancy in the number of observations in each category the random samples were balanced using the RandomOverSampler module to fit the model with a data set containing the same number of healthy loans and high-risk loans. The accuracy of the general model improved from 99% to 100% and the prediction of high-risk loans improved to 93% while the prediction of healthy loans mantained at 100%
* The LogisticRegression model provides data using an optimization technique to find the coefficients that best separate the classes and is widely used due to its simplicity, interpretability, and effectiveness when the classes are linearly separable. The RandomOverSampler method is used when a variable is highly underrepresented compared to the other biasing the model, this method oversamples the underrepresented variable by randomly duplicating the number of observations in the underrepresented variable, improving the performance of the classification.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 
	- Accuracy = 99%
	- Precision of Healthy loans = 100%
	- Precision of High-risk loans = 91%
	- Recall scores: Healthy = 100%, High risk = 95%.



* Machine Learning Model 2:
  * Description of Model 2
	- Accuracy = 100%%
	- Precision of Healthy loans = 100%
	- Precision of High-risk loans = 93%
	- Recall scores: Healthy = 100%, High risk = 100%.

## Summary

The first logistic regression model appears to be well-fitted to predict healthy loans, the results on the classification report show that the model can predict healthy loans with 100% accuracy. The high-risk loan is predicted with 91% accuracy, looking at the overall accuracy of 99%, we need more samples to train the model on the high-risk loans. Therefore, we created an oversampled logistic regression model, this second model continues to be well-fitted to predict healthy loans, and the results on the classification report show that the model can predict healthy loans with 100% accuracy. Also, this oversampled logistic regression model shows an improvement in predicting high-risk loans with 93% accuracy. The overall accuracy increased to 100%, we have a very good model to predict both healthy and high-risk loans.
* The second model displays an improvement in the accuracy of predicting high-risk loans, a highly under-represented loan status, that why the RandomOverSampler model is better to use in this case.
* In this case we look to have the highest accuracy in predicting the high-risk loans, as are the ones that can affect the lending company directly, and we want to make sure the clients are going to pay the loans in full.
