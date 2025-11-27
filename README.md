# 🏦 Bank Customer Churn Prediction

## 📌 Project Overview
This project aims to predict whether a bank customer will leave the bank (churn) or stay, based on their demographic and financial data. Customer Churn is a critical metric for banks, and predicting it helps in retaining valuable customers by offering them proactive incentives.

The model is built using **Support Vector Machine (SVM)** and handles imbalanced data using **Random Over Sampling (ROS)** to achieve high accuracy.

## 📂 Dataset
The dataset contains **10,000 records** of bank customers with the following features:
- **Demographics:** Geography, Gender, Age.
- **Financial Details:** Credit Score, Balance, Estimated Salary.
- **Account Info:** Tenure, Number of Products, Has Credit Card, Is Active Member.
- **Target Variable:** `Churn` (1 = Left, 0 = Stayed).

## 🛠️ Tech Stack & Libraries
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-Learn (SVM, GridSearchCV)
- **Data Balancing:** Imbalanced-learn (ROS)

## 🚀 Key Steps in the Project
1. **Data Preprocessing:**
   - Handled missing values (if any).
   - **One-Hot Encoding** for categorical variables (`Geography`, `Gender`).
   - **Feature Scaling** using `StandardScaler` to normalize numerical data (crucial for SVM).
   
2. **Handling Imbalance:**
   - The original dataset was biased towards customers who stayed.
   - Used **Random Over Sampling (ROS)** to balance the dataset, ensuring the model learns equally from both 'Churn' and 'No Churn' classes.

3. **Model Building:**
   - Implemented **Support Vector Classifier (SVC)**.
   - Why SVM? It works well with higher-dimensional data and finds the optimal boundary between classes.

4. **Hyperparameter Tuning:**
   - Used **GridSearchCV** to find the best parameters (`C`, `Gamma`, `Kernel`) for the SVM model to improve performance.

## 🚀 Results
After balancing the data and tuning hyperparameters, the model achieved the following performance:

- **Accuracy:** ~92%
- **Recall (Churn Class):** High recall ensures we don't miss customers who are likely to leave.
- **Precision:** Balanced precision to avoid false alarms.
