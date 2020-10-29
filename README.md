# Project Fraudulent Activities

This project is based on Supervised Machine Learning model. 
The goal was to develop a predictive model to help a company to detect fraudulent activities when customers purchase on its website.


## A 3-step project

### Step 1
For the first results, I developped a classic Logistic Regression model in order to begin with some basic metrics. I decided to keep all features except signup_time and purchase_time.

Results are not good mainly because the data is imbalanced.

### Step 2
With the exact same features, I developped a Random Forest model which I boosted with a GridSearchCV.

The results are correct and can be release. However, F1_score for test data could be improved. 

### Step 3
Eventually I developped a GridSearchCV-tuned Random Forest model with only few countries in the dataset. I observed that 'US', 'Unknown' and 'China' countries represent 80% of total countries so I kept the same feature that always but only 'US', 'Unknown' and 'China' for countries.

The results are not very interesting because these features create an over-fitted model. All results are very good on train dataset but bad on test dataset.

## Improvement
I did not use the two time features. I am sure they could improve my model, particularly by using the delta time between the signup time and the purchase time.
