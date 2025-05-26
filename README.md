# Customer Churn Prediction with Machine Learning
This project focuses on developing a machine learning model to predict customer churn based on a real-world customer dataset. The goal is to proactively identify customers who are likely to churn, enabling targeted retention strategies.

Data:
The dataset used in this project originates from a public source (please insert the specific source here if you have it, e.g., "Kaggle's Telco Customer Churn dataset"). It contains anonymized information about various customer attributes, including:

CreditScore: Customer's creditworthiness

Geography: The country where the customer resides

Gender: Customer's gender

Age: Customer's age

Tenure: The number of years the customer has been with the company

Balance: Customer's account balance

NumOfProducts: The number of products the customer utilizes

HasCrCard: Indicates if the customer possesses a credit card (Yes/No)

IsActiveMember: Indicates if the customer is an active member (Yes/No)

EstimatedSalary: Customer's estimated annual salary

Exited: The target variable – indicating whether the customer churned (1) or not (0)

Complain: Whether the customer filed a complaint

Satisfaction Score: A numerical score reflecting customer satisfaction

Card Type: The type of customer's card (e.g., DIAMOND, GOLD)

Point Earned: Points accumulated by the customer


Methodology:
This project followed a systematic approach to build an effective churn prediction model.

Data Preparation
This critical phase transformed raw data into a usable format for machine learning.

Column Selection: 
We removed irrelevant columns like RowNumber, CustomerId, and Surname which had no predictive value.
Handling Missing Data: We ensured the dataset was complete, with no missing values.
Encoding Categorical
Data:
Text-based columns such as Gender (converted to 0/1) and Geography, Card Type (converted using One-Hot Encoding into new binary columns) were transformed into numerical formats for the model.
Addressing Data Leakage: An initial 100% accuracy pointed to data leakage. We identified and removed Complain and Satisfaction Score from the features, as these columns contained information too directly correlated with churn, ensuring realistic model predictions.
Model Training
Data Split: 
The prepared data was divided into 80% for training and 20% for testing the model.
Model Choice: A Logistic Regression model was selected as our primary algorithm for predicting churn.
Model Evaluation
We assessed the model's performance using standard metrics: Accuracy, Precision, Recall, F1-Score, and a Confusion Matrix.
