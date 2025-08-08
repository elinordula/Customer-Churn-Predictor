# Customer-Churn-Predictor

#Overview
This project is a simple machine learning-based tool that predicts whether a customer is likely to churn (leave the service) or stay, based on a few input features. It uses the Telco Customer Churn dataset and is built using Python libraries such as pandas, scikit-learn, and Gradio.

A clean user interface is provided using Gradio so that anyone can interact with the trained model without writing any code.

#Dataset Used
The dataset used in this project is the Telco Customer Churn dataset, which is available on Kaggle.

It contains customer-level information such as:

Gender

Whether they are a senior citizen

Tenure (how long they’ve been with the service)

Monthly charges

Type of contract (monthly, yearly, etc.)

And more…

The target column is Churn, which indicates whether the customer has left the company.

Features Used in the Prediction
The current model uses the following features from the dataset for making predictions:

gender (0 = Female, 1 = Male)

SeniorCitizen (0 = No, 1 = Yes)

tenure (in months)

MonthlyCharges

Contract (0 = Month-to-month, 1 = One year, 2 = Two year)

These features were chosen because they are simple and still give a good prediction performance.

#How It Works
Data Cleaning

Removed missing or inconsistent values

Converted total charges to numeric format

Removed non-informative columns like customer ID

Label Encoding

Converted categorical variables to numeric format so they can be used in a machine learning model.

Train/Test Split

Split the dataset into training and testing sets (80% training, 20% testing).

Feature Scaling

Applied standardization to numeric features to make the model training more efficient.

Model Training

Used a Random Forest Classifier with 100 decision trees.

Model accuracy reached around 79% on test data.

Evaluation

Evaluated the model using accuracy, precision, recall, and confusion matrix.

Also plotted feature importances.

Gradio Interface

Built a simple web UI where users can enter values for the five selected features and get a prediction:

"Will Churn"

"Will Stay"

#Example Inputs
Gender	SeniorCitizen	Tenure	MonthlyCharges	Contract	Output
0	0	2	95	0 (Month-to-Month)	Will Stay
1	1	1	105	0	Will Churn

#Tools and Libraries Used
Python

Pandas

NumPy

Scikit-learn

Matplotlib & Seaborn (for visualization)

Gradio (for interactive UI)
Improve the user interface for better clarity

