## Bank-Term-Deposit-Prediction
Data Analysis and model building to predict if a particular customer will choose to subscribe a term deposit plan in bank or not.

## Problem Statement
### Business Use Case
There has been a revenue decline for a Portuguese bank and they would like to know what actions to take. After investigation, they found out that the root cause is that their clients are not depositing as frequently as before. Knowing that term deposits allow banks to hold onto a deposit for a specific amount of time, so banks can invest in higher gain financial products to make a profit. In addition, banks also hold better chance to persuade term deposit clients into buying other products such as funds or insurance to further increase their revenues. As a result, the Portuguese bank would like to identify existing clients that have higher chance to subscribe for a term deposit and focus marketing efforts on such clients.

### Stakeholders
* Bank Manager/Marketing Head
* Marketing team

### Data Science Problem Statement
Predict if the client will subscribe to a term deposit based on the analysis of the marketing campaigns the bank performed. Predicting potential customers would help marketing team to target on them and make marketing proedures more efficient.

### Evaluation Metric
In our given objective it will be great to have high recall value rather than accuracy or precision.

If we get a higher recall, it indicates higher chances of classifying customers who aren't intereted in Term deposit(Negative outcome) but at the same time it will increases the chances of covering all customer who will be ineterested in deposit(positive outcome).

When we have Greater precision it decreases the chances of wrongly classifying not interested ones to be the interested one. But it also decreses the likelihood of correctly predciting the customer who are more likely to subscribe.

So we need a high Recall model since we don't want to miss any potential customers, but precision should not be too low.So we will be using Recall & Precision to evaluate the model.Alongwith,we will be using AUC - Probability to discriminate between subscriber and non-subscriber.

## Understanding the dataset
### Data Set Information

* The data is related to direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be subscribed ('yes') or not ('no') subscribed.

* dataset: train.csv with all examples (32950) and 14 inputs including the target feature,  very close to the data analyzed in [Moro et al., 2014

*Goal:- The classification goal is to predict if the client will subscribe (yes/no) a term deposit (variable y).

### Features

Feature	         Feature_Type	         Description
age	      :       numeric	           :    age of a person

job	      :       Categorical,nominal:   type of job ('admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed, 'services',                                                                'student', 'technician','unemployed','unknown')


marital	         categorical,nominal	   marital status ('divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
education	       categorical,nominal	   ('basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
default	         categorical,nominal	   has credit in default? ('no','yes','unknown')
housing	         categorical,nominal	   has housing loan? ('no','yes','unknown')
loan	           categorical,nominal	   has personal loan? ('no','yes','unknown')
contact	         categorical,nominal	   contact communication type ('cellular','telephone')
month	           categorical,ordinal	   last contact month of year ('jan', 'feb', 'mar', ..., 'nov', 'dec')
day_of_week	     categorical,ordinal	   last contact day of the week ('mon','tue','wed','thu','fri')
duration	       numeric	               last contact duration, in seconds . Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no')
campaign	       numeric	               number of contacts performed during this campaign and for this client (includes last contact)
poutcome	       categorical,nominal	   outcome of the previous marketing campaign ('failure','nonexistent','success')

* Target variable (desired output):
y	               binary	                 has the client subscribed a term deposit? ('yes','no')
