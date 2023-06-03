# deep-learning-challenge

## Overview
In this challenge, we were tasked with processing and scaling data in order to train a neural network to perform a binary classification on whether or not an organization applying for funding might be successful. This involved binning large categories as well as creating dummy variables for all non-numeric categories. For the machine learning half, we were tasked with playing with variables and inputs in order to attempt to get an accuracy score over 75%.

## Results
### Data Preprocessing
The variables used as a target for my model was the "IS_SUCCESSFUL" column as we are attempting to form a decision on whether new applicants might be successful or not. In terms of features, I narrowed down the scope to using the following columns: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, and ASK_AMT. I dropped the following columns in my final version of the model in order to attempt better accuracy: EIN, NAME, SPECIAL_CASE.

### Compiling/Training/Evaluating the Modeel
In terms of neurons/layers/activation functions, I went with roughly double the number of columns (minus one) along with two hidden layers and relu functions, narrowing down the neurons with each hidden layer. My thought was that increasing the number of hidden layers an appropriate amount as well as gradually decreasing the neurons with each step would provide a better fit. As I am still unfamiliar with the different sorts of functions, I stayed with simply using the relu function.
In the end I was unable to meet the target model performance of 75% despite increasing the bin size of the APPLICATION_TYPE "Other" category as well as dropping the SPECIAL_CASE column that I deemed unneccessary due to the rare chance that it changes from a No to a Yes.

## Summary
Overall, the results of this deep learning model was unsatisfactory and I would recommend playing more with different activation functions and possibly less columns in order to refine the process. Another recommendation would be to choose a regular machine learning estimator such as the SGD Classifier or other algorithm based on one of the many flowcharts available for deciding on an algorithm.
