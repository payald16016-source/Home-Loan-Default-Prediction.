# Home Loan Default Prediction (Banking Risk Analytics)

This capstone project involves building a predictive model to identify factors and customer segments eligible for home loans while minimizing default risk.

## Project Overview
Lending institutions aim to identify potential defaulters to reduce financial risk. This project uses historical application data, credit bureau records, and previous loan applications to predict the target variable (Defaulter vs. Non-Defaulter).

## Data Sources Used
* **application_train.csv**: Main dataset containing client's static data and loan status.
* **bureau.csv**: Client's previous credits reported by other financial institutions.
* **previous_application.csv**: History of previous applications for Home Credit loans.

## Data Engineering & Cleaning
* **Joins & Aggregation**: Merged millions of records from bureau and previous application tables using **SK_ID_CURR** as a unique key.
* **Missing Value Treatment**: Used Median Imputation for numerical features and Mode Imputation for categorical features.
* **Encoding**: Applied One-Hot Encoding to convert categorical text data into a format suitable for machine learning models.

## Models & Performance
We compared multiple models to determine the best performance:
1. **Logistic Regression**: High baseline accuracy (91.95%) and good ROC-AUC (0.7556).
2. **Decision Tree Classifier**: Fast execution and comparable accuracy (91.62%).

## 📝 Challenges Faced & Techniques Used
* **Memory Management**: Handled large-scale data by using 10% Random Sampling for visualization to prevent system freezing.
* **Data Complexity**: Managed complex one-to-many relationships by implementing Groupby Aggregation.
* **Class Imbalance**: Addressed the challenge where only ~8% of users were defaulters by evaluating models using ROC-AUC scores.
*
