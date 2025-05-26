# Customer Churn Prediction with Machine Learning
This project focuses on developing a machine learning model to predict customer churn based on a real-world customer dataset. The goal is to proactively identify customers who are likely to churn, enabling targeted retention strategies.

Data:
The dataset contains various customer attributes, including demographics, financial details, and service usage. Key features include CreditScore, Age, Balance, EstimatedSalary, and the target variable, Exited (churned or not).

Methodology:
We followed a structured approach:

Data Preparation: Cleaned and transformed raw data. This involved removing irrelevant columns (RowNumber, CustomerId, Surname) and encoding categorical features (Gender, Geography, Card Type) into numerical format. Crucially, we identified and resolved data leakage by removing Complain and Satisfaction Score, which initially led to unrealistically high accuracy.
Model Training: The prepared data was split 80/20 into training and testing sets. A Logistic Regression model was trained to predict churn.
Model Evaluation: Performance was assessed using Accuracy, Precision, Recall, F1-Score, and a Confusion Matrix.
Results
After addressing data leakage, the model achieved an accuracy of 81%.

The Confusion Matrix ([[1545 62], [308 85]]) showed:

Strong performance in identifying non-churning customers (1545 correctly predicted).
Room for improvement in predicting actual churners (only 85 correctly predicted), with 308 churners being missed (False Negatives). This highlights the need to improve Recall for the churn class.
Future Improvements
Potential enhancements include feature scaling, exploring alternative models (e.g., Random Forest, Gradient Boosting), and addressing class imbalance to better predict the minority (churning) class.

Technologies Used
Python
Jupyter Notebooks
Pandas
scikit-learn
