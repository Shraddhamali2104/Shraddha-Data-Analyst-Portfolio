# 🏡 Housing Market Analysis Dashboard (BigQuery + Power BI)

### 🔗 Project Link:
[Access Dashboard (.pbix)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project2_Housing_Analysis/Housing_Market_Analysis.pbix)


### 📂 Dataset:
- [Housing Data (CSV)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project2_Housing_Analysis/Housing%20Data.csv)  
- [Column Definitions (Excel)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project2_Housing_Analysis/Housing+Data+Column+Definitions.xlsx)

### 📂 Dataset Description  

The dataset contains **housing market transaction records** along with economic indicators (inflation, yield, interest rates).  
It provides information at the **transaction, regional, and property level** to analyze housing trends.  

**Rows:** ~XX,XXX records (transactions)  
**Columns:** 15+ features (property, sales, and macroeconomic variables)  

#### Key Columns:  

- **date (MM/DD/YY)** → Transaction date of the house purchase.  
- **region** → Region/area where the property is located.  
- **city** → City of the property (null values handled → replaced with `"Unknown"`).  
- **sales_type** → Type of sales (e.g., mortgage, freehold, etc.).  
- **purchase_price** → Actual transaction price of the property.  
- **offer_price** → Price offered compared to purchase price.  
- **sqm** → Size of the property in square meters.  
- **year_build** → Year in which the property was built.  
- **age** → Derived column = (Transaction Year – Year Built).  
- **dk_ann_infl_rate%** → Annual inflation rate (nulls replaced with 1.85).  
- **yield_on_mortgage_credit_bonds%** → Yield rate on mortgage bonds (nulls replaced with 1.47).  
- **interest_rate%** → Interest rate during the transaction period.  

#### Additional Notes:  
- The dataset combines **real-estate property data** with **economic indicators** to capture both micro and macro perspectives.  
- Missing values were imputed with the **most frequent value** for numeric features and `"Unknown"` for categorical.  
- Enriched with **calculated fields** like *Age, Offer-to-SQM ratio, YOY Sales Growth,* etc.  

📸 *Refer to screenshots below for sample dataset preview and data dictionary.*  
![Dataset Preview](https://github.com/user-attachments/assets/a2add68f-61cc-438f-9943-94af25dbd721)

![Column Definitions]()  


---

## 📝 Problem Statement  

The housing market is influenced by multiple factors like region, city, inflation, interest rates, and housing age.  
The goal of this project was to design an **interactive Power BI dashboard** powered by **Google BigQuery** to analyze housing sales trends, median prices, inflation/interest rate impacts, and other key drivers.  

This equips decision-makers (real-estate investors, analysts, policy makers) with insights on:  
- 📈 Sales trends over time (YOY, YTD, Last 12 Months).  
- 🌍 Regional and city-wise housing sales performance.  
- 💸 Impact of inflation, yield, and interest rates on housing prices.  
- 🏘️ Housing affordability through price per SQM and Offer-to-SQM ratios.  
- 🔑 Key influencers of purchase price (e.g., house age, region, sales type).  

---

## ⚙️ Steps Followed  

- **Step 1: Data Loading**  
  - Uploaded housing dataset into **Google Cloud BigQuery**.  

- **Step 2: Data Connection**  
  - Connected **BigQuery** with **Power BI Desktop**.  

- **Step 3: SQL Transformations in BigQuery**  
  - Performed initial **data exploration & transformations** using SQL queries.  

- **Step 4: Data Cleaning in Power Query Editor**  
  - Handled missing values:  
    - `City` → replaced nulls with `"Unknown"`.  
    - `dk_ann_infl_rate%` → replaced nulls with **1.85** (most frequent value).  
    - `yield_on_mortgage_credit_bonds%` → replaced nulls with **1.47** (most frequent value).  

- **Step 5: Data Enrichment**  
  - Added **Age column** = Difference between transaction date and year_build.  
  - Added calculated fields for sales price, Offer_Price, and ratios.  

- **Step 6: DAX Measures & Calculations**  
  - **YOY_Sales_Growth** → % change in sales vs previous year.  
  - **Median Sales Price Change** → YOY % change in median housing price.  
  - **Units Sold in Latest Year & Quarter** → Distinct houses sold.  
  - **Last 12 Months Sales** → Rolling purchase price sum.  
  - **Sales by Region** → Total sales grouped by region.  
  - **TotalYTD Sales** → Year-to-date cumulative sales.  
  - **Average Price per SQM** → Donut chart measure by region.  
  - **Offer-to-SQM Ratio** → Ratio of offer price per sqm.  

- **Step 7: Visualizations Created**  
  - Line chart: YOY Sales Growth by Sales Type.  
  - Scatter plot: Offer Price vs Purchase Price.  
  - Bar chart: Median Sales Price Change by Region.  
  - KPI Cards: Units Sold (latest quarter), Last 12 Months Sales.  
  - Ribbon chart: Sales by Region.  
  - Donut chart: Average Price per SQM by Region.  
  - Key Influencer visual: Purchase Price by Age.  
  - Clustered bar charts: Avg Offer/Purchase Price by House Type, Inflation/Interest/Yield by House Type.  
  - Clustered Line & Column chart: Avg SQM & SQM Price by House Type.  
  - Slicers: Area, Region, City, Sales Type.  

---

## 📉 Dashboards & Screenshots  

### 📈 YOY Sales Growth  
Line chart analyzing yearly growth in sales across different sales types.  
![YOY Sales Growth](ADD_SCREENSHOT_LINK_HERE)

### 💰 Offer Price vs Purchase Price  
Scatter plot showing correlation between purchase price and offer price.  
![Offer Price Scatter](ADD_SCREENSHOT_LINK_HERE)

### 📊 Regional Median Price Change  
Bar chart showing YOY change in median housing prices by region.  
![Median Price Change](ADD_SCREENSHOT_LINK_HERE)

### 🏘️ Regional Sales Overview  
Ribbon chart showing sales dominance across different regions.  
![Sales by Region](ADD_SCREENSHOT_LINK_HERE)

### 📌 KPI Cards  
Latest Units Sold, Last 12 Months Sales, and YTD Sales KPIs.  
![KPI Cards](ADD_SCREENSHOT_LINK_HERE)

### 🔎 Key Influencer Analysis  
Factors influencing purchase price with **Age of property** being a major driver.  
![Key Influencer](ADD_SCREENSHOT_LINK_HERE)

---

# 🔎 Key Insights  

📊 **Sales Trends**  
- Consistent YOY growth, with fluctuations tied to inflation/interest rate variations.  
- YTD sales show a strong cumulative performance trend.  

🌍 **Regional & City Analysis**  
- Certain regions dominate sales volume, while others show stronger price growth potential.  
- "Unknown" cities still represent a significant share → opportunity to enrich data sources.  

💸 **Price & Affordability**  
- Offer-to-SQM ratio highlights affordability issues in specific regions.  
- Median housing price change shows a divergence between affordable and premium markets.  

🏠 **House Type & Age Factors**  
- Newly built houses have higher purchase prices, but older houses often provide better SQM value.  
- Clustered bar charts reveal that house type significantly impacts price sensitivity to inflation/yield.  

---

## 🎯 Key Learnings  

- Learned to integrate **BigQuery with Power BI** for scalable cloud-based analytics.  
- Improved skills in **SQL transformations**, **Power Query cleaning**, and **DAX calculations**.  
- Designed advanced Power BI visuals including **ribbon charts, key influencer visuals, and clustered charts**.  
- Enhanced ability to communicate **housing market insights** through KPIs and storytelling dashboards.  

---



