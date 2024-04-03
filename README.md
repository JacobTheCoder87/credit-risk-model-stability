###Credit-Risk-Model-Stability
This project is for the Kaggle competition: Home Credit - Credit Risk Model Stability. This is a group project between Carlos Martinez Abrego, Jacob Lam and Ramon Mora

![Approving Credit Loan](images/Home_Credit_Background.png)

## Project Overview

In this Home Credit - Credit Risk Model Stability project we are tasked with analyzing a person's ability to repay their loans with little to no credit history. This way people who have been traditionally denied from a loan based on their credit history have access to being approved for a loan. 

In our group project, we first approached the project by researching about loans and the different ways that people are evaluated when applying for a loan. We specifically used the 5C's of Credit as a framework for selecting each column from our dataset. The 5C's of Credit stands for Capacity, Conditions, Character and Collateral. With that knowledge we used it to help us select the columns from the large dataset that were given. We narrowed it down to 24 columns in total that we will use to train our data. Next we split up the work between the three of us. Each of us were responsible for locating 8 columns from the dataset and also merging them together into one dataset. Once each of us have our own merged dataset, we merged all three dataset into one dataset. We actually faced some challenges during this data merging process. We discovered some of our columns especially from our collateral columns there were many values that were either error or masked where it would be very difficult to extract any meaningful data from them. In the end we decided to drop those columns.

Once we merged our dataset into a main_train dataset, we decided to start with the EDA process by discovering patterns, outliers, columns to drop and created visualizations in order to better understand the relationships between our data.

## Research

Before starting this project, we had to conduct research on credit risk, we need to figure out what are some important metrics that is used when considering whether someone would likely to default.

From initial research, I discovered that the 5C's of Credit is very important in predicting the probability of whether or not a borrower would default on his debt. The 5C's are listed below with the related columns from the datasets provided by Kaggle below.

1) Capacity

This consists of income earned, stability of employment, cash flow.

From the feature_definitions: amount_416A: Deposit Amount (Cash flow), amtdebitincoming_4809443A: Incoming debit card transactions amount. (Cash flow),amtdebitoutgoing_4809440A: Outgoing debit card transactions amount. (Cash flow), amtdepositbalance_4809441A: Deposit balance of client. (Cash flow), amtdepositincoming_4809444A: Amount of incoming deposits to client's account. (Income Earned),
amtdepositoutgoing_4809442A: Amount of outgoing deposits from client's account. (Cash flow),
annuity_780A: Monthly annuity amount. (Cash flow)
cntincpaycont9m_3716944L: Number of incoming payments in the past 9 months. (Cash flow),
cntpmts24_3658933L: Number of months with any incoming payment in last 24 months. (Stability of employment)
commnoinclast6m_3546845L: Number of communications indicating low income in the last six months. (Income earned or Cash flow)
empl_employedtotal_800L: Employment length of a person. (Stability of employment)
empl_industry_691L: Employment Industry of the person. (Stability of employment)
equalityempfrom_62L: Flag indicating a sudden change in the client's length of employment. (Stability of employment)
maininc_215A: Client's primary income amount. (Income earned)

2) Capital

This consists of savings or investment account balances. 

From the feature_definitions: 
downpmt_116A: Amount of downpayment. (Investment account balances)

3) Conditions

This consists of the financial reasons for taking on the debt. (More subjective, evaluated mostly qualitatively.)

4) Character

This consists of the borrower's reputation. This may include a review of applicant's credit history or credit score. Old or past behaviors will be used as the predictor for future behavior. (Includes both qualitative and quantitative methods)

From the feature_definitions: avgdbddpdlast24m_3658932P: Average days past or before due of payment during the last 24 months. (Credit history)
avgdbddpdlast3m_4187120P: Average days past or before due of payment during the last 3 months. (Credit history)
education_927M: Education level of the person. (Measure of character)

5) Collateral

Consists of personal assets that are pledged by borrowers as security for loans. Examples includes savings, vehicles or homes.

From the feature definition: collater_typofvalofguarant_298M: Collateral valuation type (active contract) (Collateral),
collater_typofvalofguarant_407M: Collateral valuation type (closed contract). (Collateral),
collater_valueofguarantee_1124L: Value of collateral for active contract. (Collateral),
collater_valueofguarantee_876L: Value of collateral for closed contract. (Collateral),
collaterals_typeofguarante_359M: Type of collateral that was used as a guarantee for a closed contract. (Collateral),
collaterals_typeofguarante_669M: Collateral type for the active contract. (Collateral),

6) Misc

From the feature_definitions:

Lets exclude applicant's previous application history. We will exclude those columns from our data.

Thanks to Investopedia for this source. https://www.investopedia.com/ask/answers/040115/what-most-important-c-five-cs-credit.asp 

Note to self to join data together review the TKH slides on joining tables with Pandas for Phase 2: "2_26 Data Engineering Pandas I"

## Challenges

Navigating through various datasets presented several challenges, including:

- Understanding Column Significance:
    - Initially, understanding the significance of each column required background research into financial terminology. To streamline this process, we evaluated the columns with the 5C’s of credit. This framework helped us prioritize which columns to select, ensuring they were relevant to our model.

- Data Integration:
    - After identifying the most important columns, merging all the data together posed a new challenge. Merging columns from different datasets into a main file presented complexities such as handling missing data, identifying and eliminating irrelevant columns, and reconciling datasets with overlapping information.

- Identification of Target Join Columns:
    - Case ID: Serving as the target column for joining datasets together.
    - Target Column: Crucial for model building.

- Handling Large Datasets:
    - Working with large datasets had significant strain on our local resources. Insufficient RAM capacity impeded our ability to execute code seamlessly. To counteract this limitation, we adopted a strategic approach of pruning unnecessary columns, optimizing storage while retaining essential data integrity.