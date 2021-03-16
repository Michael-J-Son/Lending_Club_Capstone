# Lending Club Loan Approval Optimization
Lending Club is one of the world's largest peer-to-peer lending platform for personal loans.
Its business operation is undermined by the inclusion of delinquent borrowers and the exclusion of responsible borrowers, misrepresented in the loan approval process.
While it is impossible to develop a completely foolproof screening system, utilizing a systematic, data-driven machine learning model will significantly improve the screening process.

## 1. Data
The dataset pertaining to 2007-2011 has been acquired from https://data.world/jaypeedevlin/lending-club-loan-data-2007-11.

## 2. Data Wrangling
[Data Wrangling Report]()

__Feature Selection__
 * Features have been evaluated and selected based on: redundancy, relevance, data leakage, usefulness.
 * Any unnecessary features have been removed from the working data.
 
__Feature Modification__
 * Average FICO range of borrower have been derived from upper and lower boundary FICO range of borrower.
 * Target feature (loan_status) has been converted into a binary classification feature.

__Target Feature Visualization__
 * It is evident from the pie chart that the given data is imbalanced data.

## 3. Exploratory Data Analysis
[Exploratory Data Analysis Report]()

__Feature Correlations__

__Notable Loan Type Correlations:__
 * grade
 * fico_range_avg
 * revol_util
 * inq_last_6mths

## 4. Preprocessing
[Preprocessing Report]()

Columns containing datetime information have been converted into datetime objects, and nominal features have been one-hot encoded.

## 5. Modeling
[Modeling Notebook]()

SMOTE has been used to oversample the minority class of the training dataset before the modeling process to resolve the issue of imbalanced data.

Models tested:
 * Logistic Regression
 * Random Forest
 * Support Vector Machine
 * XGBoost



Random Forest Classifier has been selected

metrics: ROC AUC score, F1 scores

Primary features of importance:
 * last_credit_pull d
 * grade
 * inq last 6mths


