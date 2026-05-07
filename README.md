# Home Loan Default Prediction (Banking Risk Analytics)

[span_1](start_span)[span_2](start_span)This capstone project involves building a predictive model to identify factors and customer segments eligible for home loans while minimizing default risk[span_1](end_span)[span_2](end_span).

##  Project Overview
[span_3](start_span)[span_4](start_span)Lending institutions aim to identify potential defaulters to reduce financial risk[span_3](end_span)[span_4](end_span). [span_5](start_span)[span_6](start_span)[span_7](start_span)This project uses historical application data, credit bureau records, and previous loan applications to predict the target variable (Defaulter vs. Non-Defaulter)[span_5](end_span)[span_6](end_span)[span_7](end_span).

##  Data Sources Used
- **[span_8](start_span)application_train.csv**: Main dataset containing client's static data and loan status[span_8](end_span).
- **[span_9](start_span)[span_10](start_span)bureau.csv**: Client's previous credits reported by other financial institutions[span_9](end_span)[span_10](end_span).
- **[span_11](start_span)[span_12](start_span)previous_application.csv**: History of previous applications for Home Credit loans[span_11](end_span)[span_12](end_span).

##  Data Engineering & Cleaning
- **[span_13](start_span)[span_14](start_span)Joins & Aggregation**: Merged millions of records from bureau and previous application tables using `SK_ID_CURR` as a unique key[span_13](end_span)[span_14](end_span).
- **Missing Value Treatment**: Used **Median Imputation** for numerical features and **Mode Imputation** for categorical features.
- **Encoding**: Applied **One-Hot Encoding** to convert categorical text data into a format suitable for machine learning models.

##  Models & Performance
[span_15](start_span)We compared multiple models to determine the best performance[span_15](end_span):
1. **Logistic Regression**: High baseline accuracy (91.95%) and good ROC-AUC (0.7556).
2. **Decision Tree Classifier**: Fast execution and comparable accuracy (91.62%).

## 📝 Challenges Faced & Techniques Used
- **[span_16](start_span)Memory Management**: Handled large-scale data by using **10% Random Sampling** for visualization to prevent system freezing[span_16](end_span).
- **[span_17](start_span)[span_18](start_span)Data Complexity**: Managed complex one-to-many relationships by implementing **Groupby Aggregation**[span_17](end_span)[span_18](end_span).
- **[span_19](start_span)[span_20](start_span)Class Imbalance**: Addressed the challenge where only ~8% of users were defaulters by evaluating models using ROC-AUC scores[span_19](end_span)[span_20](end_span).
-
