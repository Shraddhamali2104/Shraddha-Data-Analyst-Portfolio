# 📊 Sales Performance Dashboard  
 
### Project Link:
Project1_Sales_Analysis/Sales_data_analysis.pbix

### Detailed Documentation Link: 
https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project1_Sales_Analysis/Sales_Data_Analysis_Documentation.pdf


## 📝 Problem Statement  
This dashboard was developed to analyze store sales performance across multiple dimensions such as products, regions, customers, and promotions.  
The objective is to provide actionable insights to management regarding:  

-  Which products generate the highest sales, profit, and volume.  
-  Which cities/regions are outperforming or underperforming in terms of revenue.  
- How promotional strategies are influencing discounts, sales, and profit.  
- Identifying seasonal patterns in sales and profitability.  
- Monitoring risks of over-discounting where excessive discounts reduce profit margins.  

The dashboard equips decision makers with a **single-view performance tool** to guide pricing, marketing, and product placement strategies.  

---

## ⚙️ Steps Followed  

- **Step 1:** Loaded structured dataset (SQL Server + Excel imports) into Power BI Desktop.  
- **Step 2:**  Used Power Query Editor for data cleaning — removed duplicates, standardized dates, filled missing profit values, normalized product category names.  
- **Step 3:**  Verified data model integrity by linking:  
  - `Fact_Sales` (transactions)  
  - `Dim_Customers` (customer demographics, city, state, region)  
  - `Dim_Product` (product IDs, category, price)  
  - `Dim_Promotion` (promotion IDs, type, discount strategy)  
- **Step 4:**  Transformed numerical fields, created calculated columns for Net Sales, Discount Value, and Profit.  
- **Step 5:**  Applied consistent color theme, slicers, and drill-through navigation to enhance user interactivity.  
- **Step 6:**  Created key measures using DAX functions for KPIs:  
  -  Total Sales  
  -  Total Profit  
  -  Net Sales (post discount)  
  -  Average Discount %  
  -  Quantity Sold  
- **Step 7:**  Designed visualizations:  
  -  KPI cards for overall Sales, Profit, Quantity.  
  -  Bar & Column charts for Top/Bottom products, Regional performance, Promotion impact.  
  -  Line charts for time-series / quarterly trend analysis.  
  -  Pie/Donut charts for customer segment and product share.  

---

## 📉 Dashboards  

### 🔝🔻 Top and Bottom 5 Analysis  
Comparison of top and bottom 5 products by sales, quantity, and profit to identify best and worst performers.

![Sales Dashboard](https://github.com/user-attachments/assets/681cb6d5-0d8c-4f20-94e0-074436de0917)  

### 🎯 Sales & Promotions Impact Analysis  
An interactive Power BI dashboard analyzing sales across Indian cities with insights on order volume, profit vs. net sales correlation, promotional discount impact, and sales trends over time.  

![Sales Dashboard2](https://github.com/user-attachments/assets/f4453950-7a3a-469b-b0fe-605d1dff5064)  

### ⚖️ Comparison of Sales/Profit/Quantity  
This dashboard visual enables users to compare total sales, profit, and quantity sold between two custom date ranges, allowing for dynamic, side-by-side performance analysis.  

![Sales Dashboard3](https://github.com/user-attachments/assets/868cc627-8210-4223-a67c-b69aafc70932)  

### 🗂️ Sales Transactions with Dynamic Filters  
This matrix visual displays detailed transaction data and can be dynamically filtered by date, customer, product, and promotion for targeted analysis.

![Sales Dashboard4](https://github.com/user-attachments/assets/d2171a9f-b96e-4140-ba35-ce87c48415c4)  

---

# 🔎 Insights  

From the dashboard, the following key insights were observed:  

📦 **Top Product Performance**  
  - Apple iPhone 14 is the best-performing product across Net Sales, Profit, and Quantity.  
  - Other top products also contribute heavily to revenue, whereas bottom products show potential for replacement or repricing.  

🌍 **City / Region Analysis**  
  -  Kanpur generated the highest Net Sales among all cities.  
  -  Bangalore recorded the lowest Net Sales, signaling areas for potential growth.  

🎯 **Promotions Analysis**  
  -  Summer Sale promotion offered the highest total discount amount, raising concerns about profitability impact.  
  -  Some promotions delivered high discounts but very low profit gains → over-discounting risks.  

📈 **Trend Analysis**  
  -  Quarterly Sales Trends revealed strong seasonal spikes during holiday/festival periods linked to discounts & promotions.  
  -  Sales and Profit exhibit a strong positive correlation, meaning scaling revenue generally boosts profitability.  

💸 **Discount Observations**  
  - In several categories, average discounts exceeded intended thresholds, negatively affecting net profitability.  

🏙️ **Regional Insights**  
  - Higher order volumes in a city didn’t always translate to highest profits → efficiency in regional marketing and operations matters.  

---
