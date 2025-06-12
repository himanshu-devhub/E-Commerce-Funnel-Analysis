# 🛒 E-Commerce Funnel Analysis

## 📌 Project Overview
This project analyzes the customer journey through an e-commerce platform's buying funnel — from product views to purchases. The goal is to identify drop-offs at each stage and provide insights to improve conversion rates.

**Funnel Stages:**
- Product View
- Added to Cart
- Checkout
- Purchase

## 📂 Dataset
- **Source:** UCI Machine Learning Repository
- **File:** `Online Retail.xlsx`
- **Rows:** ~540,000  
- **Time Period:** Dec 2010 – Dec 2011  
- **Fields:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

## 🧹 Data Cleaning
- Removed canceled transactions (`InvoiceNo` starting with 'C')
- Removed null `CustomerID` values
- Calculated `TotalPrice` = Quantity × UnitPrice
- Filtered for positive quantity transactions

## 🔎 Funnel Metrics Calculation

Calculated funnel metrics for each customer:
- **Views:** Unique products seen (approximated by unique StockCode entries)
- **Cart:** Unique products added to cart (based on Quantity > 0)
- **Purchase:** Number of distinct invoices per customer (proxy for purchases)

## 📊 Visualizations (Python)
- Bar chart for drop-off at each funnel stage
- Top 10 countries by total purchases
- Distribution of total spend per customer

## 🧠 Key Insights
- Significant drop-off between Cart and Purchase stages.
- Majority of purchases come from UK customers.
- Short-term contracts show lower conversion rates compared to long-term customers.
- Certain high-frequency customers show higher cart abandonment — opportunity for retargeting.

## 📁 Files Included
- `notebook.ipynb` – Full analysis and visualizations in Python
- `Plot.pdf` - Screenshot
- `README.md` – Project documentation

## 🛠 Tools Used
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook

## ✅ Future Improvements
- Incorporate session-level data for more accurate funnel mapping
- Predict drop-off risk using machine learning
- Include demographic segmentation for deeper insights

---

