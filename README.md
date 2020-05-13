# Machine_learing

## Project Overview
Utilizing the machine learning technology to predict low and high risk loans. Testing machine leaning models and their accuracy in making the prediction

## Module challenge

### Objective
Comparing performance of various machine learning models on heavily unbalanced sample.

### Results 
Due to heavily unbalanced samples all basic models (oversampled, under sampled, smote and combined) have the same precision scores: extremely high, 1.0 for low risk loans and extremely low, 0.01 for high risk investments. So, all the models might falsely identify large number of low risk investments as high risk which makes them poor models. 
Alternatively we can use Balanced Random Forest model which outperforms the other models.  It provides superior precision in predicting for both low risk (1.0) and high risk investments 0.83 (see confusion matrix and imbalanced classification report). So chance of having low risk investment classified as high risk is minimized. The cost of random forest model is low sensitivity to high risk investments,0.35. That means there is increased chance for high risk investment going under the radar. However, given that there is ~100x less high risk investments than low risk investments this model is sufficient. 
### Definitions 
* Sensitivity / Recall measures how sensitive positive classification is. It shows how many true positive (TP) instances were detected out of the whole population of positives i.e. true positive (TP) plus false negative (FN):  p = TP/(TP+FN). For example, how many true high-risk credits were detected out of all high-risk credits i.e. true high plus falsely identified low. 

* Precision measures how accurate the model is in detecting true positives (TP) out of whole population of items identified as positives i.e. true positive (TP) plus false positive (FP): TP/(TP+FP). For example, how many low risk credits were correctly identified as true low risk (TP) out of true low risk (TP) plus falsely identified low risk (FP).
*Balanced accuracy score (F1): measures the accuracy of how often the classifier is correct with the model weighing each class. It is combination of precision and recall (or precision of true positive and precision of true negative).
 

## Resources

- Technologies used: Python, sklearn package, samplers (RandomOverSampler, SMOTE, RandomUnderSampler, SMOTEENN), ML models ( LogisticRegression, BalancedRandomForestClassifier)
- Programs: credit_risk_resampling.ipynb
- Resources: Resources/LoanStats_2019Q1.zip 
- User must download credit_risk_challenge_TO file and Resources folder to the same location

