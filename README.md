# Credit_Risk_Analysis
## Overview of the analysis:
We are building up the skills in the data preparation, statistical reasoning, and machine learning. applying the Machine Learning to solve the real world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we’ll need to employ different techniques to train and evaluate models with unbalanced classes. Using imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company. We will perform:
 - Oversample the data using the RandomOverSampler and SMOTE algorithms.
 - Undersample the data using the ClusterCentroids algorithm.  
 - Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. 
 - Compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.
 
To predict credit risk. Once we’re done, we’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

The following files were used in this project:
[credit_risk_resampling.ipynb](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb)

[credit_risk_ensemble.ipynb](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb)


## Deliverable 1: Use Resampling Models to Predict Credit Risk

In this deliverable using our knowledge of the imbalanced-learn and scikit-learn libraries, we’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, we’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then we’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, we’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.


## Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk

In this deliverable using our knowledge of the imbalanced-learn and scikit-learn libraries, we’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, we’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

Using your knowledge of the imblearn.ensemble library, we’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, we’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Results

RamdomOverSampler model:

![](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/ScreenShots/RandomOverSampler.png)

- The balance accuracy score is 63%.
- The high risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only. 

The Smote Model:

![](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/ScreenShots/Smote.png)

-  The balanced accuracy score is91%  78%.
-  The high risk precision is about 4% with sensitivity 91% which makes the F1 of 7%.

The ClusterCentroids model:

![](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/ScreenShots/ClusterCentroids.png)

- The Balanceda accuracy score is about 51%. 
- The high riskprecision is on 1%
- The sensitivity is at 60% which results F1 of 1%.

The Smoteenn model:

![](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/ScreenShots/SMOTEENN.png)

 - The Balanced accuracy score is about 62%.
 - The high risk precision is still 1%. 
 - The sensitivity is 71% which makes the F1 only 2%.
 - As there is high number of false positives the low sensitivity is 54%


The BalancedRandomForestClassifier model:

![](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/ScreenShots/BalancedRandomForestClassifier.png)

- The balanced accuracy score improved is about 78%.
- The high risk precision is at 4% low.
- The sensitivity is at 67% that makes the F1 at 7%.
- Due to lower number of false positive the low risk sensitivity is at 91% with 100% precision.

The Easy Ensemble Classifier model:

![](https://github.com/urvish7/Credit_Risk_Analysis/blob/main/ScreenShots/EasyEnsembleAdaBoostClassifier.png)

 - The balanced accuracy score is high to 92%.
 - The high risk precision is still low at 7%.
 - The sensitivity is at 91%.
 - The F1 is at 14%.
 - As the number of false positive the low risk sensitivity is at 94% with 99% precision.


## Summary:

Even for sophisticated machine learning algorithms with 93 columns of data to examine, predicting credit risk is a challenging task. It is difficult to determine whether a credit risk is high using any of the models that were used to complete the credit risk analysis. The sensitivity of the high risk credits improved significantly thanks to the Ensemble models. With a recall of 92%, the EasyEnsembleClassifier model can identify nearly all high risk credit. For the total analysis, EasyEnsembleClassifier will run a High-Risk loan precision.
