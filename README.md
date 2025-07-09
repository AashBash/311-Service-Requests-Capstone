# NYC 311 Service Requests Capstone Project

Welcome to my final capstone project for the Springboard Data Science Career Track. This project analyzes NYC 311 service request data to uncover trends in complaint types, agency performance, and geographic disparities — and builds a predictive model to identify complaints likely to face delays.

## Project Objective

The main goal of this project is to:
- Understand trends in 311 complaint volumes and resolution times
- Highlight underserved areas and slow-performing agencies
- Provide actionable insights to help city officials improve service delivery

This project fits into a broader effort to use business intelligence tools to enhance urban governance, accountability, and resident satisfaction.

## Exploratory Data Analysis (EDA)

EDA was performed using Tableau to create insightful visualizations on:
- Complaint type frequency
- Borough-wise complaint volumes and delays
- Agency performance and seasonal patterns

Key findings:
- **Noise - Residential** was the most common complaint
- **Queens** generated the highest number of requests and had the most delays
- **NYPD** was the slowest-performing agency
- **Brooklyn** also showed signs of needing more agency attention

## Data Preprocessing

- Removed unnecessary columns
- Converted timestamps to `datetime` format
- Engineered `Response Time (Hours)` and `Is Closed` features
- Standardized categorical variables
- Focused on top 3 boroughs by volume
- Removed duplicate entries

## Modeling

A **logistic regression model** was developed to predict whether a complaint would be delayed. The model aThe logistic regression model performed strongly in classifying whether a 311 service request would receive a slow or fast response, showing improvements after data cleaning. It achieved an accuracy of 89% and an excellent ROC AUC score of 0.95, reflecting its strong ability to distinguish between fast and slow complaints. The model achieved a precision of 0.82 and a recall of 0.82 for slow responses, meaning it correctly identified the majority of delayed cases while keeping false alarms relatively low. The F1-score for slow responses was 0.82, demonstrating a strong balance between precision and recall. According to the confusion matrix, out of 7,896 actual slow complaints, the model correctly predicted 6,505 and misclassified 1,391 as fast. Similarly, it correctly identified 15,787 out of 17,198 fast complaints, misclassifying only 1,411. These results indicate that the model is a reliable tool for flagging service delays in NYC’s 311 system, offering valuable support for improving agency responsiveness and prioritizing high-risk complaint types.

## ✅ Recommendations

Based on the analysis and model results, here are three actionable recommendations:

1. **Reallocate agency resources** to improve NYPD response times, especially for noise complaints.
2. **Target boroughs like Queens and Brooklyn** for improved complaint resolution workflows.
3. **Implement a predictive dashboard** to prioritize incoming 311 requests likely to be delayed.

