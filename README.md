# MMA---Loan-Default-Prediction

1. Objective: Build a robust machine learning model to predict loan defaults, enabling a digital lending company to minimize financial risks and improve profitability.

2. Steps Taken:
     a) Business Understanding: The main objective here is to identify high-risk loans using customer demographic and previous loan data and focus on minimizing defaults by accurately classifying loans as "Good" (1) or "Bad" (0).
     b) Data Understanding: Explored datasets containing customer demographics, loan performance, and previous loan details. These were some of the key findings. Savings accounts dominated the customer base (78%), while students exhibited the highest default rates (27%). Smaller loans had higher default rates compared to larger ones.

3. Data Preparation:
   a) Merged multiple datasets using the primary key customerid. As the next step, data cleaning was performed by removing the duplicates and filling missing values with mean, median, and mode. The previous loan data was aggregated for future creation.
   b) Engineered new features such as repayment ratios, loan durations, and approval timelines.
   c) Encoded categorical variables and normalized numerical data.

4. Modeling:
  a) 3 models were compared and these were Logistic Regression, Random Forest, and XGBoost.
  b) The method of hyperparameter tuning was adopted using Grid Search and Optuna to improve the model's performance.
  c) Logistic regression emerged as the best model with an accuracy of 91.72%, precision of 100% with no false positives for flagged defaulters, and a recall of 92% which implied that it missed 120 out of 1450 defaulters. 

5. Evaluation:
   a) Insights: Students and permanent employees had the highest default rates. The model effectively flagged high-risk loans while maintaining a balance between accuracy and precision. Missed defaults highlighted the need for additional external features like credit scores.

6. Key Results: The Logistic Regression model outperformed others, making it a reliable tool for risk assessment. Hyperparameter tuning with Optuna improved accuracy by 2.72%.

7. Recommendations:
   a) Introduce a pre-screening process for students applying for loans.
   b) Use external data (e.g., credit scores) to improve predictions.
   c) Employ class imbalance techniques to further enhance recall.
