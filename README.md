# Credit_Risk_Analysis_Module_12_Challenge

Objective: To create financial analysis tool using Python Coding to use Data reparation for a logistic regression model to compare 2 different versions of the main loan dataset.  One of the datasets will be the one provided for the challenge and the other will be a resample of the original data using the RandonSmapler module.  We will then compare the accuracy and summary reports for both datasets to determine which is better.

The jupyter notebook containing the code is named credit_risk_resampling.ipynb

The data deals with determining as our Y target variable if a loan is a healthy one (0) or an at risk one (1).  The X variables are all other columns in the dataset and provide different categories of data that will need to be assessed in predicting Y.
One main concern with this type of supervised learning models is that it requires that we feed the correct data to the models so they may produce good predictions.  For this challenge the Supervised Learning will be using a Logictic Regression Model to determine if a loan is healthy of at risk which is a prediction of a binary outcopme from data.

The Logistic Regression Modeling is divided into 4 steps.  The code starts by preprocessing the data which includes the splitting of the data into training and testing sets.  The second steps is to trai the model where we use our label data and allow the model to recognize classification patters.  The Next step is validation which uses our test data to assess how well the model predicts the label. Finally, we use the model to predict labels for unclassified date.
  
## Results
The code will use the 2 data sets to and produce a scoring feature to help determine accuracy, precision and recall metrics.
Description of Accuracy, Precision, and Recall scores for the original dataset (Model 1) and the Oversampled Dataset (Model 2).
### Accuracy: Ratio of correctly predicted observations to the total number of observations. However, it an be susceptible to imbalanced datasets.  
* Machine Learning Model 1:  0.99
* Machine Learning Model 2: 0.99
Both model s have a very high degree of accuracy, so we will need to look at other metrics to determine if the dataset may be imbalanced.

### Precision: Precision is the ratio of correctly predicted positive observations to the total predicted positive observations. In the case of the dataset it would be understood as for those loans that were classified at risk, that were actually at risk.  
* Machine Learning Model 1:  Healthy: 1.00; At Risk: 0.86
* Machine Learning Model 2: Healthy: 1.00; At Risk: 0.84
For both models the precision is very high for the Healthy loans and not high for the at risk. For model one, we can see that the data is very imbalanced with a value count of 75,036 samples of healthy loans (0) and just 2,500 of At risk loans (1). It also appears that even after resampling the data, the precision for the at Risk loans worsen.

### Recall is the ratio of correctly predicted positive observations to all predicted observations for that class. all of the actual loan samples, how many were correctly classified as healthy or at risk?
* Machine Learning Model 1: Healthy 0.99; At Risk 1.00
* Machine Learning Model 2: Healthy 0.969. at risk 0.99

## Summary
Neither model is precise enough for the at risk loans (1).  The data appears to be too imbalanced and the Oversampling approach may not have improved precision for the At Risk (1) class.   It may be needed to use Undersampling or obtain a new data set with better “At Risk Loan” samples to create a stronger model in training.
In the case of a prediction of a healthy loan or an at risk one, I believe determining those that are at Risk is more important since they present the bigger risk of default.  IN the case of  these datasets, none of the models could improve their precision of this class.  I would recommend using a different resampling approach such as under sampling or to obtain a better data set representative of both healthy and at risk loans.

#### Resources
Fintech bootcamp class materials and in class examples
Tutoring session 3/14/24 

