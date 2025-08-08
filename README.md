# Customer Churn Predictor

## Overview

This project is a simple machine learning-based tool that predicts whether a customer is likely to **churn** (leave the service) or **stay**, based on a few input features. It uses the **Telco Customer Churn** dataset and is built using Python libraries such as **pandas**, **scikit-learn**, and **Gradio**.

A user-friendly interface is provided using **Gradio**, so anyone can interact with the trained model without writing any code.

---

## Dataset Used

The dataset used in this project is the **Telco Customer Churn** dataset, available on Kaggle.

It contains customer-level information such as:

- Gender  
- Whether the customer is a senior citizen  
- Tenure (how long they’ve been with the service)  
- Monthly charges  
- Type of contract (monthly, yearly, etc.)  
- And more...

The target column is **Churn**, which indicates whether the customer has left the company.

---

## Features Used in the Prediction

The current model uses the following features for making predictions:

- `gender` (0 = Female, 1 = Male)  
- `SeniorCitizen` (0 = No, 1 = Yes)  
- `tenure` (in months)  
- `MonthlyCharges`  
- `Contract` (0 = Month-to-month, 1 = One year, 2 = Two year)

These features were selected because they are simple and effective.

---

## How It Works

### 1. Data Cleaning
- Removed missing or inconsistent values  
- Converted total charges to numeric format  
- Dropped non-informative columns like customer ID

### 2. Label Encoding
- Converted categorical variables to numeric values

### 3. Train/Test Split
- Split the dataset into 80% training and 20% testing sets

### 4. Feature Scaling
- Standardized the numeric features using `StandardScaler`

### 5. Model Training
- Trained a **Random Forest Classifier** with 100 decision trees  
- Achieved around **79%** accuracy on test data

### 6. Evaluation
- Evaluated the model using metrics like accuracy, precision, recall, and confusion matrix  
- Visualized the most important features

### 7. Gradio Interface
- Created a simple interactive UI using Gradio  
- Users enter values for five features and get a prediction:  
  - `Will Churn`  
  - `Will Stay`

---

## Example Inputs

| Gender | SeniorCitizen | Tenure | MonthlyCharges | Contract           | Output     |
|--------|----------------|--------|----------------|--------------------|------------|
| 0      | 0              | 2      | 95             | 0 (Month-to-Month) | Will Stay  |
| 1      | 1              | 1      | 105            | 0 (Month-to-Month) | Will Churn |

---

## Tools and Libraries Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib and Seaborn  
- Gradio

---
