
# 🛒 SQL Retail Analytics Project

## 📌 Introduction

This project focuses on analyzing retail business data using SQL. The main goal is to understand how a business performs by working with raw transactional data and converting it into meaningful insights.

The dataset represents a retail system where customers purchase products from different stores. By writing structured SQL queries, the project explores how data can be cleaned, analyzed, and used to support business decisions.

Instead of just writing queries, this project follows a step-by-step approach similar to real-world analytics:

* Understanding the data
* Cleaning inconsistencies
* Filtering based on business needs
* Performing aggregations
* Generating insights

---

## 🧠 Project Objective

The objective of this project is to simulate how a data analyst works in a retail environment. It answers key business questions such as:

* How much revenue is generated?
* Which stores perform better?
* What categories sell the most?
* Who are the top customers?
* How discounts affect revenue?

---

## 🗂️ Database Design

The project is built using four main tables:

### 1. Customers

Contains customer details.

* `customer_id`
* `customer_name`

### 2. Stores

Represents store locations.

* `store_id`
* `store_name`

### 3. Products

Stores product category information.

* `product_id`
* `category`

### 4. Sales

Core transactional table.

* `sale_id`
* `customer_id`
* `store_id`
* `product_id`
* `sale_date`
* `amount`
* `quantity`
* `discount`

The **sales table acts as the central table**, connecting customers, stores, and products.

---

## 🔄 Data Generation

The dataset includes:

* 50 customers
* 3 stores
* 4 product categories
* 1000 sales transactions

The sales data is generated using SQL functions like `DBMS_RANDOM` to simulate real-world variability in:

* purchase amounts
* quantities
* discounts

This makes the dataset realistic for analysis.

---

## 🧹 Data Cleaning

Before analysis, the data is cleaned to ensure accuracy.

### Key Issues Identified:

* Missing discount values
* Possible NULL values in quantity and amount

### Fixes Applied:

* NULL discounts replaced with 0
* NULL quantities replaced with 1
* Revenue recalculated as:

👉 **Net Revenue = Amount – Discount**

This step is important because incorrect or missing values can lead to wrong business decisions.

---

## 📊 Data Analysis & Insights

### 1. Overall Business Performance

From the dataset:

* Total Transactions: **1000**
* Total Revenue: **~4.97 million**
* Unique Customers: **50**
* Average Order Value: **~4973**
* Total Quantity Sold: **3000**

👉 Insight:
The business has consistent transaction volume with moderate average order value.

---

### 2. Store Performance

| Store           | Revenue |
| --------------- | ------- |
| Store 1 (CMR)   | ~1.64M  |
| Store 2 (SR)    | ~1.70M  |
| Store 3 (Lucky) | ~1.61M  |

👉 Insight:

* All stores perform almost equally
* Store 2 slightly leads in revenue

This indicates balanced business distribution across stores.

---

### 3. Category Performance

| Category    | Revenue |
| ----------- | ------- |
| Fashion     | ~1.29M  |
| Electronics | ~1.23M  |
| Home        | ~1.22M  |
| Grocery     | ~1.22M  |

👉 Insight:

* Fashion is the top-performing category
* All categories have similar contribution

This shows diversified revenue streams.

---

### 4. Time-Based Analysis

* Monthly revenue shows stable performance across months
* Daily transactions are consistent (~11–12 per day)

👉 Insight:
There is no sudden spike or drop → business is stable.

---

### 5. Customer Behavior

* Some customers contribute significantly higher revenue
* Top customers spend above **100,000**

Customers are categorized as:

* High spenders
* Medium spenders
* Low spenders

👉 Insight:
A small group of customers generates a large portion of revenue.

---

### 6. Discount Analysis

* Around **25% of data has missing discounts** (treated as 0)
* Average discount: ~191

👉 Insight:
Discounts are used selectively, not heavily across all transactions.

---

### 7. Filtering-Based Insights

Using conditions:

* High-value sales (>5000) identified
* Low-quantity transactions detected
* Category-specific and store-specific sales analyzed

👉 Insight:
Filtering helps in identifying specific patterns like premium customers or low-performing sales.

---

### 8. Aggregation Insights

Using GROUP BY:

* Revenue per store
* Revenue per category
* Revenue per customer
* Monthly and daily revenue

👉 Insight:
Aggregation helps break down large data into meaningful summaries.

---

### 9. Advanced Analysis (HAVING, CASE, JOINS)

#### HAVING:

* Identifies top-performing customers and stores

#### CASE:

* Classifies:

  * Customers (High/Medium/Low)
  * Transactions (Big/Small)
  * Stores (High/Medium/Low revenue)

#### JOINS:

* Combines data from multiple tables to get:

  * Customer + Store + Product insights
  * Category-wise revenue
  * Store-wise customer count

👉 Insight:
Combining tables gives a complete business view instead of isolated data.

---

### 10. Window Functions (Advanced)

Used for:

* Ranking customers
* Running totals
* Previous and next transactions

👉 Insight:
Window functions allow advanced analysis without losing row-level detail.

---

## 🔍 Key Learnings

* How to design relational databases
* How to clean real-world messy data
* Writing efficient SQL queries
* Using aggregation and filtering
* Performing business-level analysis
* Understanding customer behavior

---

## 📌 Conclusion

This project demonstrates how raw retail data can be transformed into actionable insights using SQL.

It shows that:

* Data alone is not useful unless analyzed properly
* Small insights (like top customers or best categories) can help improve business decisions
* SQL is powerful enough to perform both basic and advanced analytics

---

## 🚀 Future Improvements

* Add dashboards using Power BI or Tableau
* Use Python for deeper analysis
* Build predictive models (sales forecasting)
* Integrate real-time data

---

## 👨‍💻 Author

**BPS Adithya Vardhan**
B.Tech CSE (AI)

