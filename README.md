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

Our best iteration so far was a Random Forest with a class_weight balance to deal with our class imbalance issue, as well as 300 n-estimators and a max_depth of 10. It is very possible that with more iterations and tweaking, our model would perform even better. Sadly, due to time, life and computer constraints, this was the best model we could present in the time given.

## Conlusion and Next Steps

In conclusion, while the model itself may have been somewhat lackluster, the overall theory has been proven - it is possible to feed a random forest model customer data and predict whether or not a customer will churn. It is not possible to overstate the benefits of such a model, as it would allow companies to effectively churn back time on their customer expiration. A company using this model could effectively earmark customers that the model thinks will churn "soon" and take steps to prevent that behavior, such as reaching out to make a special offer or simply to check in with a customer that might be lost soon. Furthermore, it is possible to tease out the feature importance from this model and determine which "features" are most impactful as relates to "churn", thereby making edits to their business strategy in regard to those features.

## Repo Structure
```
├── data
├── images
├── README.md
├── ChurnDown.pdf
└── Final.ipynb
```
