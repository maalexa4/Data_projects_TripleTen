
# Customer Churn Prediction Project

## Project Overview

This project focuses on predicting customer churn for a telecom company. The goal is to build a machine learning model that can accurately predict whether a customer is likely to churn based on various customer attributes. The final model needs to achieve a high AUC-ROC score while also maintaining interpretability.

## Dataset

The project utilizes multiple datasets:

- **Contract Data:** Contains information about the customer's contract, such as the contract type, payment method, monthly charges, and total charges.
- **Internet Data:** Includes internet usage details like the amount of data used.
- **Phone Data:** Contains details on whether the customer has multiple phone lines.
- **Personal Data:** Includes demographic information such as gender, age, and whether the customer has dependents.

The datasets were merged on the `customerID` field to create a comprehensive dataset for modeling.

## Data Preprocessing

- **Handling Missing Values:** 
  - `TotalCharges` was converted to a numeric type, and missing values were imputed using the median.
  - Missing values in categorical features were treated as a separate category (`_nan`).

- **Feature Engineering:**
  - Created a `Churn` feature by converting the `EndDate` to a binary variable (1 for churned, 0 for not churned).
  - Added a `ContractLength` feature to capture the duration of the customer’s contract.

- **One-Hot Encoding:**
  - Categorical features such as `Type`, `PaperlessBilling`, `PaymentMethod`, `gender`, `Partner`, `Dependents`, and `MultipleLines` were one-hot encoded.

## Exploratory Data Analysis (EDA)

EDA revealed important insights, such as:

- **Churn Distribution:** Customers with month-to-month contracts are more likely to churn compared to those with longer-term contracts.
- **Payment Method:** Customers using electronic checks as a payment method have a higher churn rate.
- **MonthlyCharges & TotalCharges:** Monthly charges had a relatively uniform distribution, while total charges were positively skewed.

## Modeling

### Logistic Regression

- **Model:** Logistic Regression with class weighting to address class imbalance.
- **Performance:**
  - AUC-ROC: 0.997
  - Accuracy: 98.5%

### Random Forest Classifier

- **Model:** Random Forest with hyperparameter tuning using GridSearchCV.
- **Performance:**
  - AUC-ROC: 0.998
  - Accuracy: 98.97%
- **Feature Importance:** The model identified the most important features contributing to churn, such as `PaymentMethod`, `ContractLength`, and internet usage (`mb_used`).

## Final Model

The **Random Forest** model was selected as the final model due to its slightly better performance compared to Logistic Regression. However, Logistic Regression remains valuable for its interpretability.

## Conclusion

The project successfully developed a highly accurate model for predicting customer churn. The Random Forest model demonstrated excellent performance, achieving an AUC-ROC of 0.998. Future work could involve exploring more advanced imputation methods and experimenting with additional model types like XGBoost.
