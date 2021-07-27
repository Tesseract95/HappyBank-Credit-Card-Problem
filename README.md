# Analytics-Vidhya Jobathon

The below problem statement belongs to the Jobathon dataset that has been conducted by analytics-Vidhya in MAY 2021. I fall in the top 10% range in the competition.
Overall Rank:823 out of 8141.

# HappyBank customer credit card lead prediction.
Happy Customer Bank is a mid-sized private bank that deals in all kinds of banking products, like Savings accounts, Current accounts, investment products, credit products, among other offerings. The bank also cross-sells products to its existing customers and to do so they use different kinds of communication like telecasting, e-mails, recommendations on net banking, mobile banking, etc. In this case, the Happy Customer Bank wants to cross-sell its credit cards to its existing customers. The bank has identified a set of customers that are eligible for taking these credit cards. Now, the bank is looking for your help in identifying customers that could show higher intent towards a recommended credit card.

# Dataset Description
## Train Data:
| Column_Name   | Description | 
| ------------- |:-------------:| 
| ID            | Customer_ID | 
| Gender        | Gender of the Customer      |  
| Age           | Age of the Customer    | 
| Region_Code   | Region From which the Customer Belongs     |  
| Occupation    | Occupation of the customer    | 
|  Channel_Code | Channel Code for the customer                               |
|   Vintage            | vintage  measures the performance of a portfolio in different periods of time after the loan (or credit card) was granted.|
| Credit_Product       | whether the customer has credit_product or not on the credit card.|
| Avg_Account_Balance  |  Average Acoount balance of the customer.|
|Is_Active| Whether the credit-card is active or not.|
|Is_Lead(Target)| Whether the customer will intent towards credit-card or not.|

## Test Data
| Column_Name   | Description | 
| ------------- |:-------------:| 
| ID            | Customer_ID | 
| Gender        | Gender of the Customer      |  
| Age           | Age of the Customer    | 
| Region_Code   | Region From which the Customer Belongs     |  
| Occupation    | Occupation of the customer    | 
|  Channel_Code | Channel Code for the customer                               |
|   Vintage            | vintage  measures the performance of a portfolio in different periods of time after the loan (or credit card) was granted.|
| Credit_Product       | whether the customer has credit_product or not on the credit card.|
| Avg_Account_Balance  |  Average Acoount balance of the customer.|
|Is_Active| Whether the credit-card is active or not.|


# Evaluation Metrics:
ROC-AUC value for class1.

# Approach:
## EDA & Preprocessing
i) Missing values in Credit_Product.

ii) Transformation of Age column.

iii)Analyzing the Avg_Account_Balance.

## Feature Enginnering:
i) Statistical Feature of Avg_Account_Balance,Vintage(Skewness,Kstats,Kurtosis,Mean)

ii) Binning and KBinsDiscretizer

iii)Lable and Frequency Encoding

## Model Building
i) Experimented with LogisticRegression,XGBOOST,LGBM,CATBOOST.

ii) Stacked Average method of all the models.

## Model Evaluation:
i) Highest ROC value is on Stacked Average Method(i.e. 0.8499951406)
