# Credit-Risk-Prediction-using-Machine-Learning

 Project Overview:  
This project focuses on building a machine learning system to predict whether a customer is a high credit risk (likely to default) or low credit risk (likely to repay). The goal is to help financial institutions make better lending decisions and reduce financial losses.
The project applies multiple machine learning models and compares their performance using business-relevant metrics such as Recall, Precision, and ROC-AUC.

 Objectives:
Predict customer credit risk (Good vs Bad)
Handle imbalanced data effectively
Maximize detection of high-risk customers
Compare multiple ML models fairly
Select the best model for real-world deployment

 Dataset:
The dataset contains customer financial and demographic information, including:
Age
Job
Housing status
Credit amount
Loan duration
Account information
Purpose of loan

 Key Challenge:
Imbalanced dataset (fewer risky customers)
Higher cost of misclassifying risky customers

 Project Workflow:
1. Data Preprocessing
Handling missing values
Feature engineering (e.g., credit ratios, burden metrics)
Outlier treatment using percentile capping
Encoding categorical variables
2. Feature Selection
Correlation analysis
Removal of redundant features
Selection of high-impact variables
3. Data Transformation
Scaling numerical features using StandardScaler
Skewness correction using log transformations
4. Handling Imbalance
Applied SMOTE to balance training data
5. Model Building
The following models were trained and evaluated:
Logistic Regression
Support Vector Machine (SVM)
Random Forest
K-Nearest Neighbors (KNN)
XGBoost
6. Model Optimization
Hyperparameter tuning (GridSearchCV)
Threshold tuning (business-driven decision threshold = 0.35)

 Model Performance:
  Model	             Accuracy	       Precision (Risk=1)	         Recall (Risk=1)	        F1-score	      ROC-AUC
Logistic Regression	  0.625	              0.434	                     0.817	               0.566	         0.786
  SVM	                0.715	              0.516	                     0.783	               0.623	         0.751
Random Forest	        0.640	              0.445	                     0.817	               0.576	         0.765
  KNN	                0.665	              0.466	                     0.800	               0.589	         0.762
XGBoost	              0.665	              0.466	                     0.800	               0.589	         0.762

 Key Insights:
Logistic Regression achieved the best overall performance with the highest ROC-AUC and strong recall
High recall ensures most risky customers are correctly identified
Precision is lower due to intentional bias toward catching more risky customers
Threshold tuning significantly improved business relevance

 Final Model Selection:

Logistic Regression was selected as the final model because:

Highest ROC-AUC (best overall discrimination)
Strong recall for risky customers
High interpretability (important for financial decisions)
Stable and reliable performance

 Visualizations:

The project includes:
Model comparison bar charts
ROC-AUC comparison
Recall comparison

 Business Impact:
Reduces loan default risk
Improves credit approval decisions
Balances risk vs opportunity
Provides explainable predictions

 Future Improvements:
Advanced hyperparameter tuning
Cost-sensitive learning
Probability calibration
Deployment as a web app/API

 Conclusion:

The project demonstrates that a well-tuned Logistic Regression model can effectively predict credit risk, achieving strong recall and ROC-AUC. The model prioritizes identifying high-risk customers, making it suitable for real-world financial applications.

 Tech Stack:
Python
Pandas, NumPy
Scikit-learn
XGBoost
Matplotlib

 Contact:

If you have any questions or feedback, feel free to reach out.
