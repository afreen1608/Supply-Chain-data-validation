# Supply-chain-data-validation
AI based Project for data validation and standardization in supply chain systems.

Overview

This project focuses on validating and standardizing supply chain data using an eCommerce dataset sourced from Kaggle. The aim is to ensure clean, consistent, and accurate data across key areas like order processing, delivery timelines, and inventory handling. Machine learning techniques are applied to predict delivery performance and flag inconsistencies, supporting better decision-making in supply chain operations.

Dataset

The dataset includes files like:
df_Orders.csv
df_Customers.csv
df_Products.csv
df_Payments.csv
df_OrderItems.csv

We primarily used the orders data, which contains details about purchase, approval, delivery, and estimated delivery timestamps.
Data Validation and Standardization Converted timestamp columns to datetime objects.
Validated data types and handled missing values using errors='coerce'.

Engineered features:
delivery_days: Number of days taken to deliver an order.
late_delivery: Boolean column indicating whether delivery was late.
Checked for anomalies like negative delivery times or unrealistic values.

Machine Learning Model
Goal: Predict whether an order will be delivered late.
Model: Logistic Regression
Input Features: delivery_days, order_status, etc.
Target: late_delivery column

Model Performance
Accuracy: 95.29%
Precision (on-time orders): 96%
Recall (late orders): 54%
F1-score (late orders): 64%

The model performed well on identifying on-time deliveries but showed lower recall for late deliveries, suggesting further improvement with additional features or balancing techniques.

Conclusion

This project demonstrates the use of AI for data validation and predictive analytics in supply chain management. Clean data and accurate delivery predictions can help companies optimize logistics and improve customer satisfaction.
