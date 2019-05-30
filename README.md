# Synthetic Minority Oversampling Technique (SMOTE) – Bank Marketing

## A. Goal  
In the dataset on Amazon Alexa reviews, we observed that imbalance in the dataset reduced the models’ accuracy to predict minority class (1 star ratings). In this exercise, we will use SMOTE to deal with an unbalanced dataset – to improve our models’ accuracy in predicting minority class.

## B. Data Source  
https://www.kaggle.com/henriqueyamahata/bank-marketing

## C. Summary  
We have used a dataset on the results of marketing calls for term deposit, made by a Portuguese bank. The data has a total of 41188 rows, of which only 4640 are 1; thus, our dataset is unbalanced. Initially, we created decision tree and logistic regression models and evaluated their performances (accuracy, sensitivity, and specificity), and then we compared these results with those of the models built on SMOTEd data.  
We used SMOTE to create a balanced dataset: we oversampled (synthetically generated more data points) the minority class and under-sampled the majority class.

