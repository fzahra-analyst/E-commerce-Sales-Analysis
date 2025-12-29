# 📄 E-commerce Data Analysis Project

📘 Available Languages:  
🇬🇧 English | 🇫🇷 [Français](README_FR.md)

## 📌 Project Overview
This project analyzes a large Brazilian e-commerce dataset (Olist).  
The goal is to understand:

- customer behavior  
- sales performance  
- product characteristics  
- shipping efficiency  

The project includes:
- Data Cleaning  
- Feature Engineering  
- Exploratory Data Analysis (EDA)  
- Customer Analysis  
- Shipping Analysis  
- Product Insights  
- Geographical Analysis  

This work is part of my **Data Analysis Portfolio**.

---

## 🚀 1. Data Cleaning

### Key Steps:
- Removed duplicates  
- Handled missing values (products, reviews, geolocation…)  
- Fixed inconsistent data types  
- Merged multiple datasets into one order-level dataset  
- Removed invalid shipping values:  
  - negative delivery times  
  - unrealistic outliers (> 90 days)

---

## 🧱 2. Feature Engineering

### Time-based Features
- `order_year`  
- `order_month`  
- `order_weekday`  

### Customer Features
- `customer_order_count`  
- `customer_total_spent`  
- `is_repeat_customer`  

### Shipping Features
- `delivery_time_days`  
- `delays_days` (actual delivery − estimated delivery)  
- `shipping_ratio` (freight_value / price)  

### Product Features
- `product_volume_cm3`  
- `product_density`  

These new features enabled deeper and more meaningful insights.

---

## 📊 3. Exploratory Data Analysis (EDA)

### Sales Insights
- Sales are highly concentrated in major cities:  
  **São Paulo**, **Rio de Janeiro**, **Belo Horizonte**
- Top-selling categories:  
  - `bed_bath_table`  
  - `health_beauty`  
  - `sports_leisure`
- Highest average price categories:  
  - `computers_accessories`  
  - `watches_gifts`  
  - `auto`
- Monthly sales show seasonal patterns  
- Most orders contain **only one item**

---

## 👥 4. Customer Analysis
- Most customers are **one-time buyers**  
- Repeat customers represent a small segment but generate high revenue  
- Top spenders contribute substantially to total revenue  
- Customer distribution is heavily concentrated in South and Southeast Brazil  
- `customer_order_count` confirms that most buyers order **once or twice**

---

## 🚚 5. Shipping & Delivery Analysis
- **Average delivery time ≈ 13 days**  
- Some orders arrive after the estimated date  
- Longer geographical distances result in longer delivery times  
- Large/heavy products →  
  - higher shipping costs  
  - more delays  
- `shipping_ratio` is highest for large-volume categories (furniture, decor)

---

## 📦 6. Product Analysis
- Product volume and density strongly influence delivery time  
- Large products (furniture, decor, luggage) → slower delivery  
- Small products (beauty, accessories, toys) → faster and cheaper shipping  

---

## 🔍 7. RFM Analysis (if applied)
- Most customers fall under **Low Frequency – Low Monetary**  
- High-value customers are rare but important  
- Recency analysis shows seasonal purchasing behavior  

---

## 🌍 8. Geographical Analysis
- Top-performing states by number of orders: **SP**, **RJ**, **MG**, **PR**  
- Northern and interior states show longer delivery durations (distance + logistics constraints)

---

## 🧩 9. Final Insights Summary
- ✔ Sales are concentrated in major cities  
- ✔ Best-selling categories differ from the highest-priced categories  
- ✔ Customer loyalty is low  
- ✔ Average delivery time is 13 days and depends heavily on geography  
- ✔ Larger products lead to higher shipping costs and delays  
- ✔ Feature engineering significantly improved the analysis  

---

## 📊 Power BI Dashboard

An interactive dashboard built using **Power BI Desktop** to analyze e-commerce sales and customer behavior.

### Key Insights:
- Sales and revenue trends over time
- Repeat vs one-time customers
- Top-performing states and regions
- Order distribution by customer segment

### Files:
- `powerbi/ecommerce_dashboard.pbix` – Power BI Desktop file
- `powerbi/dashboard_preview.png` – Dashboard preview image

> 🔍 To explore the dashboard, download the `.pbix` file and open it using **Power BI Desktop** (free).

---

## 🛠️ 10. Tools & Libraries
- Python  
- Pandas  
- Numpy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  
- (Optional) GeoPandas  

---
## 📊 Data Source

This project is based on the **Brazilian E-Commerce Public Dataset (Olist)**, which contains real-world commercial data from multiple sellers and customers.

The original dataset includes:
- Orders
- Customers
- Products
- Payments
- Reviews
- Sellers
- Geolocation data

To optimize analysis and performance, the raw data was cleaned, transformed, and engineered into new datasets used throughout this project.

🔗 Dataset source:  
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## 📁 Project Structure

E-commerce-Sales-Analysis/
│
├── data/
│   ├── cleaned_dataset.csv
│   ├── engineered_dataset.csv
│   ├── orders_full.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_customer_analysis.ipynb
│   ├── 04_rfm_analysis.ipynb
│   ├── 05_geographical_analysis.ipynb
│
├── results/
│   ├── customer_summary.csv
│   ├── rfm_segments.csv
│   └── graphs/
│       ├── 1.png
│       ├── 2.png
│       ├── 3.png
│       └── ...
│
├── src/
│   ├── data_cleaning.py
│   ├── eda.py
│   └── utils.py
│
├── README.md
└── requirements.txt


---

## 🎯 12. Conclusion
This project demonstrates a complete and professional end-to-end analysis of real-world e-commerce data.  
It highlights customer behavior, sales trends, product characteristics, and logistical performance powered by strong feature engineering.

---

## 💼 Author
**Fatima Zahra**
Data Analysis
