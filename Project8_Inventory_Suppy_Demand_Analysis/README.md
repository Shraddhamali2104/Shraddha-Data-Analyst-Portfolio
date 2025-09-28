# 📊 Inventory Demand & Supply Analysis Dashboard  

## 📌 Project Overview  
This project focuses on **analyzing and visualizing inventory demand and supply data** as a **learning exercise** to understand data pipelines, database integration, and Power BI reporting.  
The main goal was to practice building reports starting from a **test environment**, validating data, and then **transitioning to a production environment** while maintaining data quality and consistency.  

---

## 🗂️ Datasets  
- **Test Environment Datasets** – Demand, availability, and order-level data used for initial report development.  
- **Products Dataset** – Product metadata used to enrich the test data.  
- **Production Environment Dataset** – Cleaned and validated dataset for final reporting.  

---

## 🔧 Steps Followed  
1. **Data Import & Cleaning**  
   - Imported two datasets into SQL Server (Test Environment).  
   - Combined them using **LEFT JOIN** queries.  
   - Imported the combined table into Power BI.  
   - Cleaned and validated data, corrected data types.  

2. **Power BI Report Development**  
   - Added custom background canvas for report pages.  
   - Created key **DAX measures**:  
     - Total Number of Days  
     - Total Demand & Total Availability  
     - Average Demand & Availability per Day  
     - Total Supply Shortage  
     - Total Profit, Total Loss, Average Loss per Day (USD)  
   - Added slicers for **Product Name** and **Order Date** for interactive filtering.  

3. **Transition to Production Environment**  
   - Imported Production Environment dataset & Products dataset.  
   - Fixed data quality issues (wrongly mapped product IDs).  
   - Combined and replaced data source in Power BI to connect to the production table.  

4. **Integration with MySQL**  
   - Replicated transformations and joins in MySQL.  
   - Created equivalent SQL queries for compatibility with Power BI.  
   - Connected Power BI to MySQL and validated that visuals match expected results.  

---

## 🎯 Key Learnings  
- ✅ **Test vs. Production Environment** – Understanding their purpose in analytics workflows.  
- ✅ **Data Quality First** – Ensuring accuracy before visualization.  
- ✅ **Data Source Transition** – Using Power Query Advanced Editor for smooth migration from SQL Server to MySQL.  
- ✅ **Working with Multiple Databases** – Combining MS SQL Server and MySQL as sources.  
- ✅ **Building KPI-Driven Dashboards** – Creating meaningful measures for business insights.  

---

## 🛠️ Tools & Technologies Used  
- **SQL Server** – Data import, joins, and transformations.  
- **MySQL** – Production-level data storage and query optimization.  
- **Power BI** – Visualization, DAX, and interactive dashboard creation.  
- **Power Query (M Language)** – For data shaping and source transitions.  

---

## Dashboards
### 📊 Page 1 – Demand & Supply Overview  
This page highlights **key operational KPIs** to monitor inventory demand and availability.  
- **Average Demand per Day (48.65)** – Tracks how much demand is generated daily on average.  
- **Average Availability per Day (24.70)** – Measures how much supply is available per day on average.  
- **Total Supply Shortage (61K)** – Shows the gap between demand and availability, helping stakeholders identify unmet demand.  

**Purpose:** This page helps decision-makers quickly assess whether supply is keeping up with demand and plan procurement or production adjustments accordingly.  

![Dashboard1](https://github.com/user-attachments/assets/144dc3bf-bbcf-4113-9789-9cdfa52e319e)

---

### 💰 Page 2 – Profitability & Loss Analysis  
This page focuses on the **financial impact** of demand-supply imbalances.  
- **Total Profit (301K)** – Shows cumulative profit over the selected period.  
- **Total Loss (8M)** – Represents cumulative losses incurred (e.g., due to unmet demand or overstocking costs).  
- **Average Daily Loss (2.97K)** – Highlights the average daily financial loss, enabling management to prioritize corrective actions.  

**Purpose:** This page is designed to quantify the financial outcomes of operational decisions and help minimize losses while maximizing profit.  

![Dahboard2](https://github.com/user-attachments/assets/cc236800-87d4-4340-8ba1-39fbdf0b90ff)

---

## 📌 Summary  

This project showcases a **complete learning workflow**:  
importing data → cleaning and combining datasets → developing KPIs → switching from test to production environment → connecting to MySQL → validating in Power BI.  

It reflects my ability to handle **end-to-end data analytics projects** while focusing on **data quality, reproducibility, and interactivity**.  
