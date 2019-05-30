# Synthetic Minority Oversampling Technique (SMOTE) – Bank Marketing

## A. Goal  
In the dataset on Amazon Alexa reviews, we observed that imbalance in the dataset reduced the models’ accuracy to predict minority class (1 star ratings). In this exercise, we will use SMOTE to deal with an unbalanced dataset – to improve our models’ accuracy in predicting minority class.

## B. Data Source  
https://www.kaggle.com/henriqueyamahata/bank-marketing

## C. Summary  
We have used a dataset on the results of marketing calls for term deposit, made by a Portuguese bank. The data has a total of 41188 rows, of which only 4640 are 1; thus, our dataset is unbalanced. Initially, we created decision tree and logistic regression models and evaluated their performances (accuracy, sensitivity, and specificity), and then we compared these results with those of the models built on SMOTEd data.  

We used SMOTE to create a balanced dataset: we oversampled (synthetically generated more data points) the minority class and under-sampled the majority class.

- Function

**SMOTE(y ~ ., data, perc.over = 100, perc.under = 200)**  
  
The number of minority class rows are decided as follows.  
**New no. of minority class rows = Original no. of minority class rows X [1 + (perc.over/100)]**
  
The number of majority class rows are decided as follows.  
**New no. of majority class rows = [New no. of minority class rows - Original no. of minority class rows] X (perc.under/100)**  
  
We were able to see improvement in the sensitivities of the models, which is a key metric for us – as we want to predict 1s with accuracy; however, usage of SMOTE resulted in a slight decline in the specificities and thus in the overall accuracy.  
  
We will apply SMOTE function on the training data; thus, we need to split the data before using SMOTE.  

_Variable Description_

INPUT
**age:** Client age  
**job:** Job Type  
marital: Marital status  
education: Education level  
default: Whether the client has defaulted  
housing: Whether the client has housing loan  
loan: Whether the client has a personal loan  
contact: Type of communication  
month: Last month of the contact  
day_of_week: Last contact day of the week  
duration: Duration of last contact (seconds)  
campaign: Number of times client contacted in the campaign  
pdays: Number of days since the client was last contacted  
previous: Number of times the client was contacted in earlier campaigns  
poutcome: Outcome of the previous marketinig campaign  
emp.var.rate: Employment variation rate  
cons.price.idx: Consumer price index  
cons.conf.idx: Consumer confidence index  
euribor3m: Euribor 3 month rate  
nr.employed: Number of employees  
