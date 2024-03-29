# credit-risk-model-stability
This project is for the Kaggle competition: Home Credit - Credit Risk Model Stability. This is a group project between Carlos Martinez Abrego, Jacob Lam and Ramon Mora

## Research

Before starting this project, we had to conduct research on credit risk, we need to figure out what are some important metrics that is used when considering whether someone would likely to default.

From initial research, I discovered that the 5C's of Credit is very important in predicting the probability of whether or not a borrower would default on his debt. The 5C's are listed below.

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

## Project Overview

## Challenges

