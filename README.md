# Lending Club Loan Approval Optimization
## 1. Data
Lending Club is one of the world's largest peer-to-peer lending platform for personal loans.
The dataset pertaining to 2007-2011 has been acquired from https://data.world/jaypeedevlin/lending-club-loan-data-2007-11.

## 2. Data Wrangling
Data Wrangling Report

__Problem 1:__ Feature Selection
 * Features have been selected based on: redundancy, relevance, data leakage, usefulness
 * Any unnecessary features have been removed from the working data
 
__Problem 2:__ Feature Modification
 * Average FICO range of borrower have been derived from upper and lower boundary FICO range of borrower
 * Target feature (loan_status) has been converted into binary classification feature
