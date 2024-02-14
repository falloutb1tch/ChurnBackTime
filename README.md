# If I Could Churn Back Time
## Overview

For my capstone project, I have chosen to continue in a similar vein to my Phase 3 project with entirely different data. Churn, which is what it is called when a customer stops doing business with a company, is one of the largest issues facing almost every industry today. In context of subscription industries, for example, "churn" is a massive ongoing issue, as it is infinitely cheaper to keep existing customers than to lure in new ones. Therefore, establishing a procedure to keep customers from "churning" is of the utmost importance. The first step in this process is identifying the reasons behind customer churn, such as dissatisfaction, area of service provided, quality of service, and other such considerations. Following that, we will build a model that will accurately predict whether or not a customer will churn, and thereby provide the limitlessly valuable opportunity for a company to prevent that churn.

## Business Understanding

As previously stated, it is much cheaper to keep existing customers than to continually lure new customers in. In other words, the longer a customer stays with a company, the more money that company stands to make from them. It seems fairly simple in that context, right? So it also follows that if there was a way to accurately predict whether or not a customer would churn, that method would be likely to save a company a boatload of money. And no, "boatload" in this case is not an exaggeration - the data we are using today comes from a fictional telecommunications company, but the very real company known as Verizon walked away from 2023 with $134 billion in total operating revenue. So our goal here was quite simple - build a model that could accurately predict when a customer would stop doing business with a company, and provide that company an opportunity to stop that customer from churning, thereby saving them money.

## Data Understanding

The data we've used for this endeavor comes to us from IBM, and is a publicly available dataset created for this exact purpose - to help deal with churn problems, and allow students like me to cut our teeth on such before we enter the wider world of data science. This sample data module tracks a fictional Telco company's customer churn based on a variety of possible factors, such as gender, monthly charges, and usage information, as well as whether the customer churned or not. Due to the nature of the data we used, any location based features were excluded because the data was all centered in California specifically. There is also a class imbalance present, meaning that 73% of customers have not churned and 26% have, so our data is "imbalanced" from the start.

## Data Preparation

we will remove any columns that are unnecessary or contain information that we already have in our other two available dataframes. This way, we will prevent overlapping of information and inaccurate feature impact on our modeling later. Once again there are many columns in this dataframe that were repeated in the first (or second) dataframe, and therefore are unnecessary. Furthermore, any of the quarter or count information isn't relevant to our modeling process. These things have nothing to do with whether or not a customer churned, because no consumer is keeping track of fiscal quarters of their cellphone company to plan to cut their service, but gender or tenure with company might very well be relevant. Now, throughout all this data exploration and preparation, we have created three separate dataframes with one common column ("Customer ID"), 7043 entries that correspond to each other in each of the three dataframes, and various information on their services, plans, and habits. At this point, we must weld together those three separate dataframes into one usable one, and then begin the analysis process.

## Model Recommendation

![RFCMTune2](https://github.com/falloutb1tch/ChurnBackTime/assets/149413838/7071a1ac-2e39-43de-aee7-e69fae9599fc)

After what hypertuning that life, time, and computer constraints would allow, we have arrived at the conclusion that our second attempt had our highest recall, and therefore is the best model that we could be using for this purpose. Our second model was a Random Forest, hypertuned with the parameters class_weight, max_depth and n_estimators. This model displayed 84% recall and 77% accuracy.

## Conlusion and Next Steps

In conclusion, it is entirely possible and very beneficial to employ a similar predictive model for the purpose of customer churn issues on a real-world scale. With what limited time and resources I had available, I was able to properly tune a model that was 77% accurate and had 84% recall, and I'm sure that those numbers could be tweaked and increased with further time and resources applied. Earlier in this notebook, I mentioned that Verizon had clocked something to the tune of $134 billion in revenue in 2023; I do not know what Verizon is doing to solve any churn problems they may be having, but imagine if a company like Verizon could successfully stop customers leaving whenever possible - it could increase their revenue even further, and therefore, this model (and its kin) is priceless. After further tweaking and perfecting of the hypertuning process, a telecommunications company could use this model in order to accurately predict whether a customer will churn soon and then take steps to reach out and prevent that customer from doing so. For example, the number of referrals and contract type seemed to be very important factors as to whether or not a customer would churn, and so perhaps a telecommunications company could apply a special bonus to increase the number of referrals each customer has or a specific deal for a certain contract type.

## Repo Structure
```
├── data
├── images
├── README.md
├── ChurnDown.pdf
└── Final.ipynb
```
