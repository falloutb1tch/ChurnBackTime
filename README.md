# If I Could Churn Back Time
## Overview

For my capstone project, I have chosen to continue in a similar vein to my Phase 3 project with entirely different data. Churn, which is what it is called when a customer stops doing business with a company, is one of the largest issues facing almost every industry today. In context of subscription industries, for example, "churn" is a massive ongoing issue, as it is infinitely cheaper to keep existing customers than to lure in new ones.

## Business Understanding

Therefore, establishing a procedure to keep customers from "churning" is of the utmost importance. The first step in this process is identifying the reasons behind customer churn, such as dissatisfaction, area of service provided, quality of service, and other such considerations. Following that, we will build a model that will accurately predict whether or not a customer will churn, and thereby provide the limitlessly valuable opportunity for a company to prevent that churn.

## Data Understanding

The data we've used for this endeavor comes to us from IBM, and is a publicly available dataset created for this exact purpose - to help deal with churn problems, and allow students like me to cut our teeth on such before we enter the wider world of data science. This sample data module tracks a fictional Telco company's customer churn based on a variety of possible factors, such as gender, monthly charges, and usage information, as well as whether the customer churned or not. Due to the nature of the data we used, any location based features were excluded because the data was all centered in California specifically. There is also a class imbalance present, meaning that 73% of customers have not churned and 26% have, so our data is "imbalanced" from the start.

## Data Preparation

The data was pared down to necessary columns and split into train and test sets to prepare for modeling. Numeric columns were scaled whilst categorical columns were ordinally or OneHotEncoded as needed. We also employed label encoding for our target column to allow for modeling. There were also some minor steps needed such as merging dataframes and changing column names to facillitate that merge.

## Model Recommendation


## Conlusion and Next Steps


## Repo Structure
```
├── data
├── images
├── README.md
├── ChurnDown.pdf
└── Final.ipynb
```
