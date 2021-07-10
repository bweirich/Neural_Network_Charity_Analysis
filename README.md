# Neural_Network_Charity_Analysis

## Overview

This analysis used neural networks to build a model to predict which charities would most benefit from funding.  This will help to better allocate available funds to maximize the impact it will have.

## Results

### Data Preprocessing

For this dataset the target variable is the "IS_SUCCESSFUL" field as this is the determining factor we are attempting to predict with the model.  The variables that were removed as they were deemed unnecessary to the model performance are the identification features:
- EIN
- NAME
The remaining variables became our feature variables which include:
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT

The features "APPLICATION_TYPE" and "CLASSIFICATION" were preprocessed using buckets to decrease the noise to hopefully improve accuracy.

In further optimization of the model the 'ASK_AMT" feature was also preprocessed using buckets and dummy values to improve accuracy.

### Compiling, Training and Evaluation the Model

In the original model 2 hidden layers were used in the neural network model with 80 neurons and 30 neurons respectively.  The Rectified Linear Unit (ReLU) function was used as the activation function in both hidden layers and the Sigmoid function was used in the output layer.  With this model the accuracy score achieved was 73%.

![alt_text](https://raw.githubusercontent.com/bweirich/Neural_Network_Charity_Analysis/main/Images/Original.PNG)

In order to try to increase the accuracy of the model we increased the hidden layers to 3 and increased the neurons to 100, 50 and 10 respectively.  The Sigmoid function was used for the second and third hidden layers instead of the ReLU function.  With the preprocessing optimizations and the model optimizations the accuracy score achieved was 

![alt_text](https://raw.githubusercontent.com/bweirich/Neural_Network_Charity_Analysis/main/Images/Optimization.PNG)

## Summary

Overall the accuracy results of the optimized model did not improve on the initial model indicating further analysis would be needed to improve the model.  Since there was little to no change in the accuracy score with changes to the model a neural network or deep learning model may not be the most effective model.  A RandomForest or LogisticRegression model might have similar or improved results while using less processing power and less run time.  
