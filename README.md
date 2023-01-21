# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis

Good loans tend to outnumber risky loans significantly. This makes credit risk an inherently unbalanced classification problem. Hence one needs to employ different techniques to train and evaluate models with unbalanced classes. This is the ask for this project- to use imbalanced-learn and scikit learn libraries to build and evaluate models using resampling. To oversample the data, RandomOverSampler and SMOTE algorithms are used and to undersample, ClusterCentroids algorithm is used. A 
Good loans tend to outnumber risky loans significantly. This makes credit risk an inherently unbalanced classification problem. Hence one needs to employ different techniques to train and evaluate models with unbalanced classes. 

This is the ask for this project- to use imbalanced-learn and scikit learn libraries to build and evaluate models using resampling. To oversample the data, RandomOverSampler and SMOTE algorithms are used and to undersample, ClusterCentroids algorithm is used. A 
combinatorial approach of over- and undersampling using the SMOTEENN algorithm is then used. Finally comparison is made between machine learning models that reduce bias,the BalancedRandomForestClassifier and EasyEnsembleClassifier. 

## Results

The step by step analysis is provided in https://github.com/ashrs03/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb and 
https://github.com/ashrs03/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb

 - Naive Random oversampling 

![image](https://user-images.githubusercontent.com/42523379/213842536-67bc4044-202b-4f4b-a6b4-224ccf46d589.png)

Precision - high_risk loan status 0.01 | low_risk loan status 1.0
Recall - high_risk loan status 0.64  | low_risk loan status 0.69
Accuracy 0.67

  - SMOTE oversampling 
  
  ![image](https://user-images.githubusercontent.com/42523379/213842703-6abbbb6b-d5d1-4b38-8c09-bbe135ecd8f4.png)

Precision - high_risk loan status 0.01 | low_risk loan status 1.0
Recall - high_risk loan status 0.61 | low_risk loan status 0.64
Accuracy -0.63

- ClusterCentroids Undersampling 

![image](https://user-images.githubusercontent.com/42523379/213842755-3ecd94fb-4f89-4bbc-a0ee-a607d0b7becc.png)

Precision - high_risk loan status 0.01 | low_risk loan status 1.0
Recall - high_risk loan status 0.59 | low_risk loan status 0.43
Accuracy - 0.50

 -  SMOTEENN combination oversampling and undersampling 
 
![image](https://user-images.githubusercontent.com/42523379/213842785-9d1a8f1c-5c64-4449-a584-1212de32b295.png)

Precision - high_risk loan status 0.01 | low_risk loan status 1.0
Recall - high_risk loan status 0.59 | low_risk loan status 0.43
Accuracy -0.50

  - Balanced Random Forest classifier 
  
![image](https://user-images.githubusercontent.com/42523379/213842868-1b488b77-b883-4f6f-8afa-f3aa8c238b0d.png)

Precision - high_risk loan status 0.04 | low_risk loan status 1.0
Recall - high_risk loan status 0.67 | low_risk loan status 0.91
Accuracy- 0.78

  - Easy Ensemble AdaBoost classifier 
  
 ![image](https://user-images.githubusercontent.com/42523379/213842900-cf09bdb5-136c-4236-907e-8c9a72a0c863.png)

Precision - high_risk loan status 0.07 | low_risk loan status 1.0
Recall - high_risk loan status 0.91 | low_risk loan status 0.94
Accuracy- 0.93

## Summary
Based on the results the Easy Ensemble AdaBoost Classifier has the best accuracy at 0.93 and is the best model in terms of accuracy. The precision of all the models were comparable and were low for high risk loan status and at 1.0 for the low_risk loan status. In terms of recalls too, when the value is closer to 1 that makes it a better model and with the high_risk/ low_risk recall values at 0.91 | 0.94 respectively for the Easy Ensemble AdaBoost classifier, this is again better than other models for recall. Overall the Easy Ensemble AdaBoost classifier should be chosen as the model for further credit risk analysis. 

