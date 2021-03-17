# Lending Club Loan Approval Optimization
Lending Club is one of the world's largest peer-to-peer lending platform for personal loans.
Its business operation is undermined by the inclusion of delinquent borrowers and the exclusion of responsible borrowers, misrepresented in the loan approval process.
While it is impossible to develop a completely foolproof screening system, utilizing a systematic, data-driven machine learning model will significantly improve the screening process.

## I. Data
The dataset pertaining to 2007-2011 has been acquired from https://data.world/jaypeedevlin/lending-club-loan-data-2007-11.

## II. Data Wrangling
[Data Wrangling Report]()

__1) Data Cleaning__
 * All columns entirely comprised of missing values have been eliminated from the working data.

__2) Feature Selection__
 * Features have been evaluated and selected based on: redundancy, relevance, data leakage, usefulness.
 * Any unnecessary features have been removed from the working data.
 
__3) Feature Modification__
 * Average FICO range of borrower have been derived from upper and lower boundary FICO range of borrower.
 * Target feature (loan_status) has been converted into a binary classification feature.

__4) Target Feature Visualization__
 * It is evident from the pie chart that the given data is imbalanced data.

## III. Exploratory Data Analysis
[Exploratory Data Analysis Report]()

__1) Object Feature Conversion__
 * Object features containing numerical or ordinal values have been converted into numerical features.

__2) Feature Correlations__

__Notable Loan Type Correlations:__
 * grade
 * fico_range_avg
 * revol_util
 * inq_last_6mths

## IV. Preprocessing
[Preprocessing Report]()

__1) Data Processing__
 * Features containing datetime information have been converted into datetime objects, and nominal features have been one-hot encoded.

## V. Modeling
[Modeling Notebook]()

__1) Train Test Split__

__2) Standardize Features__
 * Standardize features using StandardScaler

__3) Resampling__
 * SMOTE has been used to oversample the minority class of the training dataset before the modeling process to resolve the issue of imbalanced data.

__4) Model Evaluation__
 * Hyperparameter tuning with Grid Search
 * F1 score and ROC AUC score were preferred over accuracy, as this project is an imbalanced classification problem.

__Models Tested:__
 * Logistic Regression
 * Random Forest
 * Support Vector Machine
 * XGBoost

Random Forest is the optimal model for the current dataset based on its performance on F1 score and ROC AUC.

__Primary Features of Importance Derived from Random Forest:__
 * last_credit_pull_d
 * grade
 * inq_last_6mths

## VI. Prospective Improvement



