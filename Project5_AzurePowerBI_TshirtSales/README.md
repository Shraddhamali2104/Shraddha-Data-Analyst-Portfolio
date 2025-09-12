# 👕 Men’s T-Shirt Sales Insights Dashboard  

### 📌 Project Link  
[Download PBIX File](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/TshirtSales_AzurePowerBI/Tshirts%20Brands.pbix)  


### 📂 Dataset  
[View or Download Dataset](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/TshirtSales_AzurePowerBI/Men%2BTshirt.csv)  

This dataset contains **Men’s T-Shirt sales data** including:  
- **Brand Name** – The brand of the t-shirt.  
- **Title** – Product name/description.  
- **Original Price** – Listed price before discount (may contain NULL values).  
- **Sale Price** – Final selling price after discount.  

  The dataset was cleaned to handle **missing values**, create **derived columns** (e.g., Marked Price, Discount %, Profit %), and prepare it for **brand-level sales & profitability insights**.
---

## 📝 Problem Statement  
Retail companies often struggle to track **pricing accuracy, discount effectiveness, and profit margins** across multiple brands and product varieties.  
This project aims to:  
- Analyze **brand-wise performance** in terms of sales, profit, and discount patterns.  
- Identify **top & bottom performing brands** by various KPIs.  
- Enable **decision-makers** to optimize pricing, discounts, and inventory planning.  
- Demonstrate **end-to-end data integration** using Azure SQL Database and Power BI.

---

## ⚙️ Steps Followed  

### 🔧 Step 1: Database Setup on Azure  
- Created an **Azure SQL Database** and configured **server firewall rules** to allow secure access.  
- Connected to the database using **SQL Server Management Studio (SSMS)** with credentials (server name, username, password).
    
 ![Database_Setup](https://github.com/user-attachments/assets/7ab88b56-de90-4d6d-bc62-8287c0262550) 

---

### 📥 Step 2: Data Import & Cleaning in Azure SQL  
- Imported **flat file dataset** into SQL database table.
- Cleaned data with SQL:  
**Data View Before cleaning the data**
![Data_View Before](https://github.com/user-attachments/assets/417ebccc-a808-466e-a526-e623361851bc)

**Data View After cleaning the data**
![Data View After](https://github.com/user-attachments/assets/ed6772b6-aa80-4759-b67e-4ec0e62ebec6)

---

### 🔗 Step 3: Connecting Power BI to Azure SQL  
- Used **Database Connector** in Power BI to connect live to Azure SQL Database.   

---

### 🧹 Step 4: Data Cleaning and Transformation in Power BI  
- Removed rows with **all NULL values**.  
- Handled NULLs in `Original_Price` column by:  
    - Creating a conditional column:  
      - If `Original_Price` is NULL → `factor = 1.5` else `factor = 0`.  
    - Creating a custom column: `Sales * factor`.
    - Creating a "Marked Price" column in Power Query using:
      if [Original_Price] = "NA" then [Sales*Factor] else [Original_Price]
      
    ![Added_Columns](https://github.com/user-attachments/assets/91c0c3cf-2926-44bd-a9b9-3b6d612243e5)
    
- Replacing missing `Original_Price` with calculated value → `Marked Price`.  
- Dropping temporary columns (`factor`, `Sales*factor`, old `Original_Price`).
      
  **Data View After cleaning the data**
  ![Data View After](https://github.com/user-attachments/assets/ef1f1cab-a29c-4f21-a2db-a75983b63aed)
- Performed additional cleaning using Power Query (where required).  
- Created new DAX columns:  
  - `Discount % = (Marked Price - Sale Price) / Marked Price`  
  - `Cost Price = Sale Price * (1 - Profit %)` *(assuming profit % between 2–17%)*  
  
![DAX_MEASURES](https://github.com/user-attachments/assets/bbb05d9a-3b62-4592-8dac-a7e5bdc6b6fd)

---

### 📊 Step 5: Dashboard Design  
Created a **multi-page Power BI report** with interactive visuals:  

- Brands Overview Page:
Displays all available brands and introduces the dashboard with a **clean, minimal design** for easy navigation.  

- 📉 Top 5 Brands by Average Discount %  
Highlights brands offering the **highest average discounts**, helping assess promotional strategies.  

- 💰 Top 5 Brands by Highest Average Profit %  
Identifies **most profitable brands**, guiding focus on high-margin products.  

- 🛒 Top 5 Brands by Highest Number of Varieties  
Shows brands with **widest product variety**, helping in inventory and assortment planning.  

- 💵 Top 5 Brands by Highest Average Sales Price  
Compares brands with **premium pricing**, useful for luxury vs. mid-range product analysis.  

- 📉 Bottom 5 Brands by Average Profit %  
Pinpoints **low-margin brands** to review pricing, cost, or discounting strategies.  


---

## 🚀 Tech Stack  
- **Cloud Database:** Azure SQL Database  
- **Data Cleaning & Transformation:** SQL (Azure + SSMS)  
- **Visualization:** Power BI  
- **Language:** DAX, SQL  

---

## 📉 Dashboard Preview  
![Dashboard1](https://github.com/user-attachments/assets/16360d34-0fae-47ef-9ad6-9e487661235e)

![Dashboard2](https://github.com/user-attachments/assets/fb1bd11e-352a-4834-8a9d-92572b791f76)

---

# 🔎 Insights & Business Impact  

📌 **Discount Optimization**  
- **Insight:** The Indian Garage Co. offers the highest average discount (~72%), followed by British Club and The Bear House.  
- **Business Impact:** Helps marketing teams review **discount strategies** to balance customer attraction with profitability.  

📌 **Profitability Analysis**  
- **Insight:** NVOC, Thinc, and Choiceit achieved the highest profit margins (~17%). Some brands like Urbano Fashion and Maniac have very low profit % (~11–12%).  
- **Business Impact:** Enables management to **prioritize high-margin brands** and take corrective actions (price revisions, vendor negotiations) for low-margin brands.  

📌 **Variety Planning**  
- **Insight:** The Indian Garage Co. leads with the highest number of varieties (51), followed by U.S. Polo Assn. and Netplay.  
- **Business Impact:** Assists inventory planners in **stock allocation** and helps identify **gaps or over-representation** in brand assortment.  

📌 **Pricing Strategy**  
- **Insight:** ARMANI EXCHANGE and BROOKS BROTHERS have the highest average selling prices (~6.1K and 5.1K respectively), showing they cater to the premium segment.  
- **Business Impact:** Enables differentiation of **premium vs. mass-market brands**, helping design **tiered pricing and promotional campaigns**.  

📌 **Bottom Performers**  
- **Insight:** Brands like Urbano Fashion, Be Active X AG, and Maniac are among the bottom 5 in profit %.  
- **Business Impact:** These insights trigger **cost control measures** or **discontinuation reviews** for consistently low-margin SKUs.  

📌 **Overall Brand Health**  
- **Insight:** Combination of metrics (discount %, profit %, varieties, sales price) gives a **360° view of brand performance**.  
- **Business Impact:** Equips decision-makers with a **data-driven approach** to manage brand partnerships, discount budgets, and pricing models.  


---

## 📈 Key Value Additions  
- Built a **cloud-powered, scalable BI solution** using Azure + Power BI.  
- Automated **data cleaning and transformation pipeline** using SQL and DAX.  
- Designed **interactive dashboards** to drive brand-level decision making.    

---

## 🎯 Future Scope  
- Implement **scheduled refresh** to get real-time insights.  
- Add **forecasting models** for sales and profit prediction using Power BI AI visuals.  
- Integrate **Azure Synapse Analytics** for big data scalability.  

