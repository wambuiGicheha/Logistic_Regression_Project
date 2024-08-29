# Logistic_Regression_Project

## Overview
In this project, I developed and evaluated two machine learning models—Logistic Regression and Decision Tree—to predict customer churn. The primary goal was to identify patterns and features that contribute to customer attrition, enabling the business to take proactive measures to retain customers.

I began by building a baseline logistic regression model, which showed reasonable accuracy but exhibited limitations in recall, indicating that it struggled to correctly identify customers who would churn. To address this, we introduced a decision tree classifier, which offered a more balanced performance, particularly in terms of recall, and provided clearer insights into the key features driving churn.

By comparing the results of both models, I was able to recommend the most effective approach for predicting customer churn, considering both the accuracy and interpretability of the models. This analysis is intended to guide the business in implementing targeted retention strategies, while also identifying areas for further model refinement.

## Business and Data Understanding

SyriaTel, a telecommunications company, is facing the challenge of customer churn — customers leaving the service, resulting in lost revenue. Retaining customers is crucial for the company’s profitability and growth, as acquiring new customers often costs more than keeping existing ones. The company needs to identify customers who are likely to stop doing business with them so that targeted retention strategies can be implemented.

## Data Understanding

 The data for this project has been sourced from <a href="https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset"> Kaggles Website</a> and it relates to the data analysis questions since it has the information that is needed to predict the churn of customers in the company. 
The data represent customer information for a telecommunications company, specifically focused on customer churn behavior. The sample includes individual customers, with each row representing a single customer. The variables included in the dataset capture a variety of customer attributes and usage patterns, which are crucial for predicting whether a customer is likely to churn.

The variables are as follows.

Customer Demographics:

* Area Code: The geographical area code where the customer is located.
* International Plan: Whether the customer has an international calling plan (Yes/No).
* Voice Mail Plan: Whether the customer has a voicemail plan (Yes/No).
Usage Statistics:

* Total Day Minutes: The total number of minutes the customer used during the day.
* Total Day Calls: The total number of calls the customer made during the day.
* Total Day Charge: The total charge for day usage.
* Total Eve Minutes: The total number of minutes the customer used during the evening.
* Total Eve Calls: The total number of calls the customer made during the evening.
* Total Eve Charge: The total charge for evening usage.
* Total Night Minutes: The total number of minutes the customer used during the night.
* Total Night Calls: The total number of calls the customer made during the night.
* Total Night Charge: The total charge for night usage.
* Total Intl Minutes: The total number of minutes the customer used for international calls.
* Total Intl Calls: The total number of international calls the customer made.
* Total Intl Charge: The total charge for international usage.

Customer Service Interaction:

* Customer Service Calls: The number of calls the customer made to customer service.

Target Variable:

* Churn: Indicates whether the customer churned (True) or stayed (False).

## stakeholder audience and dataset choice 
Marketing and Customer Retention Teams:

These teams are responsible for designing and executing strategies to retain customers. They need insights into which customers are at risk of churning and the factors driving this behavior to create targeted campaigns and personalized offers.
Product Management Team:This team can use the insights from the model to improve product features, pricing, or service offerings. Understanding the reasons behind customer churn helps them to refine the product and reduce churn risk.

Customer Support Team: As the frontline of customer interaction, the support team can benefit from knowing which customers are likely to churn. They can prioritize outreach and provide high-quality support to these customers, potentially mitigating churn.

Executive Leadership:Executives need a high-level understanding of customer churn to make informed strategic decisions. They are interested in the overall impact of churn on the business and the effectiveness of the strategies in place to mitigate it.

Data Science and Analytics Team:This team is responsible for building and maintaining the churn prediction models. They need detailed insights into the model's performance and limitations to continue refining and improving it.

#### Dataset Choice
The dataset used in this analysis consists of customer information from SyriaTel, a telecommunications company. The dataset includes various features that could influence customer churn, such as:

Usage Patterns: Total day minutes, total night minutes, and other usage metrics that indicate how frequently and in what ways customers are using the service.
Billing Information: Data related to the billing cycle, charges, and payment history, which might influence a customer's decision to stay or leave.
Customer Service Interactions: Records of customer service calls as these can be critical in determining customer satisfaction.
Demographic Data: Information such as customer location and account tenure, which can provide context for churn patterns.

## Modeling
The modeling approach for predicting customer churn involves several key steps, from data preprocessing to model evaluation and selection. Here’s a detailed outline of the approach:

1. Data Preprocessing
* Data Cleaning: Handle missing values, outliers, and incorrect data entries. Ensure that all the features are in the correct format.
* Feature Engineering: Create new features that might help the model, such as interaction terms, ratios, or derived metrics. Consider transforming categorical variables into numerical ones using techniques like one-hot encoding.
* Scaling: Standardize or normalize numerical features to ensure that the model treats them equally, especially when using algorithms like logistic regression.
* Balancing the Dataset: Since the dataset is imbalanced (with more non-churn cases than churn cases), apply techniques like SMOTE (Synthetic Minority Over-sampling Technique) to balance the class distribution in the training data.

2. Model Selection
Approach
Data Preprocessing:

Cleaned the data and handled missing values.
Encoded categorical variables and scaled numerical features.
Applied SMOTE to balance the dataset.
Model Selection:

Logistic Regression: Aimed for simplicity and interpretability. Tuned hyperparameters using cross-validation.
Decision Tree: Chosen for its interpretability and ability to handle non-linear relationships.
Training:

Trained models on the balanced dataset.
Used various hyperparameters to optimize performance.

## Evaluation
Metrics
Models were evaluated using:

Accuracy: Measures the overall correctness of the model.
Precision: Indicates the proportion of true positives among predicted positives.
Recall: Measures the proportion of true positives among actual positives.
F1 Score: Balances precision and recall.
ROC-AUC: Assesses the model’s ability to distinguish between classes.
AUC-PR: Evaluates performance with respect to the positive class.
* Results
Logistic Regression: Achieved an ROC AUC Score of 0.6788 and an AUC-PR of 0.2834.
Decision Tree: Provided competitive results with high interpretability.

## Conclusion
The decision tree model offers a clear advantage in interpretability, showing how different features influence churn decisions. While the logistic regression model provides robust performance metrics, the decision tree’s visual nature allows for more straightforward explanations to stakeholders.

Recommendations
Implementation: Deploy the model that best fits the business needs, considering both accuracy and ease of interpretation.
Retention Strategies: Use model insights to identify at-risk customers and implement targeted retention measures.
Ongoing Evaluation: Regularly update and monitor the model to ensure it continues to provide accurate predictions as customer behavior evolves.