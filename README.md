🧠 Approach & Methodology


🔸 Part 1: Data Exploration & Preparation
Loaded all CSV files from Olist dataset (~100k orders).

Merged relevant tables using keys like order_id, product_id, customer_id.

Cleaned missing values (review_comment_message, product_category_name, etc.).

Treated outliers in freight_value, price, shipping_limit_date.

Removed duplicates and inconsistent entries.



🔸 Part 2A: Product Demand Prediction
Objective: Identify factors driving product popularity and predict high-demand products.

Feature engineered total orders per product category, average ratings, return rate, etc.

Created demand classes (high/medium/low) based on percentile thresholds.

Used classification models:

Random Forest Classifier

Gradient Boosting (XGBoost Classifier)

Evaluated using Accuracy, F1 Score, Confusion Matrix, ROC-AUC.



🔸 Part 2B: Order Delivery Delay Prediction
Objective: Predict whether an order will be delivered late based on customer, product, and logistics features.

Engineered a new target column delay_status (late vs on-time).

Modeled using:

Logistic Regression

Random Forest

Metrics: Accuracy, Precision, Recall, ROC-AUC, Confusion Matrix

Important features: Estimated vs actual shipping days, freight value, product category, review score, state distance.



📊 Visualizations & Dashboard
Key Visualizations:
Top 10 most demanded product categories

Delivery delay heatmaps by customer state and seller state

Rating distribution vs delay

Feature importance graphs for both models

Interactive Dashboard:
Built with Power BI

Tabs for:

Sales Trends

Popular Products

Delivery Performance

Delay Distribution by Geography

📍 File: dashboard/olist_dashboard.pbix

