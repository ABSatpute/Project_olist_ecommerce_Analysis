# 🛒 Olist E-Commerce Data Analysis

This project involves a comprehensive analysis of the Olist dataset (~100k orders) with a focus on two key objectives:

- **Product Demand Prediction**
- **Order Delivery Delay Prediction**

Additionally, an interactive Power BI dashboard is created to visualize key business insights.

---

## 🧠 Approach & Methodology

### 🔹 Part 1: Data Exploration & Preparation

- Loaded all CSV files from the Olist dataset.
- Merged relevant tables using keys like `order_id`, `product_id`, and `customer_id`.
- Cleaned missing values (`review_comment_message`, `product_category_name`, etc.).
- Treated outliers in `freight_value`, `price`, and `shipping_limit_date`.
- Removed duplicates and inconsistent entries.

---

### 🔹 Part 2A: Product Demand Prediction

**Objective:** Identify factors driving product popularity and predict high-demand products.

- Engineered features: total orders per category, average ratings, return rate, etc.
- Created demand classes (High / Medium / Low) using percentile thresholds.
- Models used:
  - Random Forest Classifier
  - XGBoost Classifier
- Evaluation Metrics:
  - Accuracy
  - F1 Score
  - Confusion Matrix
  - ROC-AUC

---

### 🔹 Part 2B: Order Delivery Delay Prediction

**Objective:** Predict whether an order will be delivered late based on customer, product, and logistics features.

- Created new target column: `delay_status` (Late vs On-Time).
- Engineered features: estimated vs actual shipping days, freight value, product category, review score, state distance.
- Models used:
  - Logistic Regression
  - Random Forest Classifier
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - ROC-AUC
  - Confusion Matrix

---

## 📊 Visualizations & Dashboard

**Key Visualizations:**

- Top 10 most demanded product categories
- Delivery delay heatmaps by customer state and seller state
- Rating distribution vs delay
- Feature importance charts

**Interactive Power BI Dashboard Tabs:**

- Sales Trends
- Popular Products
- Delivery Performance
- Delay Distribution by Geography



