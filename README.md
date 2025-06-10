# Predicting Customer Churn at SyriaTel Company


**Author**: [Sharon Leonida Aoko](mailto:sharon.aoko@student.moringaschool.com)

## Overview

Syriatel is a private mobile provider based in Syria. They would like to predict whether a customer will soon unsubscribe or stop doing business with them.
This project focuses on customer churn, which is a critical challenge for telecom companies as it directly impacts the revenue and growth of such companies. 
With increasing competition, companies need targeted retention strategies to save significant costs compared to acquiring new customers
     
## Business Problem
SyriaTel’s Customer Retention Team is the stakeholder.

SyriaTel would like to predict whether a customer will soon unsubscribe or stop doing business with them. This project focuses on customer churn, 
which is a critical challenge for telecom companies as it directly impacts the revenue and growth of such companies. With increasing competition,
companies need targeted retention strategies to save significant costs compared to acquiring new customers.
The main problem is the reduction of how much money will be lost because of customers who don't stick around very long, thus leading to lost revenue. 

## Data Source

The dataset is in CSV format, it has 3,333 rows of customers’ data. It contains the following fields:
                                                                                                                                                
 1. Account info: state, account length, area code
                                                                                                                                                
 2. Usage metrics: total day minutes, international calls, number of customer service calls
                                                                                                                                                
 3. Plan details: international plan (yes/no), voice mail plan
                                                                                                                                                
Main target is: churn (True/False)   

Kaggle. https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset

## Objectives

The main objective is to develop a predictive model that identifies SyriaTel customers at high risk of churning, enabling proactive retention 
strategies to reduce revenue loss.
    
The key questions focus on this analysis are :

1. To predict which customers are most likely to churn using machine learning

2. Identify what the key factors are driving churn, such as service calls or  international plans, from the dataset

3. Identify  the recommended actionable strategies to retain high-risk customers

## Logistic Regression Modeling and evaluation

For "Not Churn" Customers (False):    
   
1. 96% Precision: When the model says a customer won’t leave, it’s correct 96% of the time.

2. 77% Recall: the model misses 23% of loyal customers that means it wrongly flags them as "about to leave".

For "Will Churn" Customers (True):       
 
1. 37% Precision: When it predicts a customer will leave, it’s wrong 63% of the time.
        
2. 81% Recall: the model catches 81% of actual churners this is good, but with many false alarms.

## Decision Tree Modeling and evaluation

From the decision tree above we identified the top 3 drivers of customer churn in your telecom dataset:    

1. International Plan (32.5% impact) 
       
Customers with international plans are 3× more likely to churn.
        
Action: Stakeholder need to review international plan pricing/quality. Offer targeted retention deals. 
   
2. Customer Service Calls (32.2% impact)  
      
Each additional service call increases churn risk dramatically. 
       
Action: The stakeholder needs to improve first-call resolution. Flag customers who make ≥3 calls.
    
3. Daytime Charge (27.2% impact)   
     
High daytime charges correlate with churn. 
       
Action: The stakeholder needs to analyze if competitors offer better daytime rates.



## Conclusions

From the analysis done for SyriaTel’s Customer Retention Team, the model predicted that:

1. For International Plan Users:

Higher entropy means they're harder to predict

They need more nuanced retention strategies

2. For Domestic-Only Users:

Lower entropy makes them easier to manage

They need standard retention offers that may work well

3. For Feature Priorities:

They should Focus on high-information-gain features first that is international_plan → customer_service_calls → total_day_charge


### Recommendations

From the analysis done the model gives a prediction of the likelihood of the customers to leave if:
1. They have an international plan.

2. They Called customer service 3+ times

3. Have high daytime charges

Due to this limitations, the stakeholders should Prioritize retention offers such as discounts, special perks for these customers.

They could also train support teams to handle international plan issues better.

The stakeholders should not focus on features such as Night/weekend call usage, how long they’ve had the account and whether they have voicemail



## For More Information

See the full analysis in the [Jupyter Notebook](./AnalysisOnAircraftRisk.ipynb) or 

review this [presentation](./Shamilz_Aviation_Corporation_fleet_expansion_Analysis.pdf).

For additional info, contact Sharon Leonida Aoko at (mailto:sharon.aoko@student.moringaschool.com)


## Repository Structure

```
├── data
├── images
├── README.md
├── Predicting_CustomerChurn_at_SyriaTel_Company.pdf
└── Predicting_CustomerChurn_at_SyriaTel_Company.ipynb
```
