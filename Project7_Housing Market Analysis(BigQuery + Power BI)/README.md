# 🏡 Housing Market Analysis Dashboard (BigQuery + Power BI)

### 🔗 Project Link:
[Access & Download Dashboard (.pbix)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project7_Housing%20Market%20Analysis(BigQuery%20%2B%20Power%20BI)/Housing_Sales_Analysis.pbix)


### 📂 Dataset:
- [Housing Data (CSV)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project7_Housing%20Market%20Analysis(BigQuery%20%2B%20Power%20BI)/Housing%20Data.csv)  
- [Column Definitions (Excel)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project7_Housing%20Market%20Analysis(BigQuery%20%2B%20Power%20BI)/Housing%2BData%2BColumn%2BDefinitions.xlsx)

The dataset contains **housing market transaction records** along with economic indicators (inflation, yield, interest rates).  
It provides information at the **transaction, regional, and property level** to analyze housing trends.  

**Rows:** 1,00,000 records (transactions)  
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

📸 *Refer to screenshots below for sample dataset preview and data dictionary.* 

![Dataset Preview](https://github.com/user-attachments/assets/a2add68f-61cc-438f-9943-94af25dbd721)


![Column Definitions](https://github.com/user-attachments/assets/0c4a4884-316a-49d4-b73f-0cedec5af8a2)

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

  ![Data in BigQuery](https://github.com/user-attachments/assets/56ab940b-0fba-4211-9ec0-ec855f460a35)

- **Step 2: Data Connection**  
  - Connected **BigQuery** with **Power BI Desktop**.
  ![Connection Image](https://github.com/user-attachments/assets/abcaf4f2-e6e1-4b25-8e02-e60c4b6b2b50)


- **Step 3: SQL Transformations in BigQuery**  
  - Performed initial **data exploration & transformations** using SQL queries.
 
  ![Exploration in SQL](https://github.com/user-attachments/assets/86735fe6-f2b2-41dc-a6b9-42652b9f2d7f)


- **Step 4: Data Cleaning in Power Query Editor**  
  - Handled missing values:  
    - `City` → replaced nulls with `"Unknown"`.  
    - `dk_ann_infl_rate%` → replaced nulls with **1.85** (most frequent value).  
    - `yield_on_mortgage_credit_bonds%` → replaced nulls with **1.47** (most frequent value).  

- **Step 5: Data Enrichment**  
  - Added **Age column** = Difference between transaction date and year_build.  
  - Added calculated field for Offer_Price using purchase price and % change between offer and purchase.  

- **Step 6: DAX Measures & Calculations**  
  - **YOY_Sales_Growth** → % change in sales vs previous year.  
  - **Median Sales Price Change** → YOY % change in median housing price.  
  - **Units Sold in Latest Year & Quarter** → Distinct houses sold.  
  - **Last 12 Months Sales** → Rolling purchase price sum.  
  - **Sales by Region** → Total sales grouped by region.  
  - **TotalYTD Sales** → Year-to-date cumulative sales.  
  - **Average Price per SQM** → Donut chart measure by region.  
  - **Offer-to-SQM Ratio** → Ratio of offer price per sqm.  

  ![Measures](https://github.com/user-attachments/assets/ef3a56f0-b9e1-4d1e-a326-30e503feb56f)


- **Step 7: Visualizations Created**  
  - **Line Chart: YOY Sales Growth by Sales Type**  
  → Shows how housing sales have grown or declined year-over-year, broken down by sales type. Helps identify which types of sales are trending upwards or facing decline.  

  - **Scatter Plot: Offer Price vs Purchase Price**  
  → Displays the relationship between purchase price and offer price. Useful for analyzing negotiation gaps and pricing behavior in the housing market.  

  - **Bar Chart: Median Sales Price Change by Region**  
  → Highlights year-over-year changes in the *median* housing price across regions, showing which regions are experiencing stronger or weaker price growth.  

  - **KPI Cards: Units Sold (Latest Quarter), Last 12 Months Sales**  
  → Quick snapshot of key performance indicators: total houses sold in the latest quarter and the rolling 12-month sales volume. Provides an at-a-glance summary of market performance.  

  - **Ribbon Chart: Sales by Region**  
  → Compares total sales across regions while tracking how regional rankings shift over time. Helps spot consistently strong or emerging regions in housing sales.  

  - **Donut Chart: Average Price per SQM by Region**  
  → Illustrates average housing price per square meter for each region. Useful for comparing affordability and identifying high-priced vs low-priced markets.  

  - **Key Influencer Visual: Purchase Price by Age**  
  → Identifies factors influencing the purchase price, with property *age* being a key driver. Provides insight into how newer vs older homes affect pricing.  

  - **Clustered Bar Chart: Avg Offer/Purchase Price by House Type**  
  → Compares average offer price and purchase price across different house types, showing pricing variations by property category.  

  - **Clustered Bar Chart: Avg Inflation / Interest / Yield by House Type**  
  → Demonstrates how inflation, interest, and bond yield vary across house types. Helps analyze macroeconomic impact on different property categories.  

  - **Clustered Line & Column Chart: Avg SQM & SQM Price by House Type**  
  → Combines line and column visuals to compare average house size (SQM) with price per SQM across property types. Shows trade-offs between property size and per-unit pricing.  

  - **Slicers: Area, Region, City, Sales Type**  
  → Interactive filters that allow users to drill down into specific regions, cities, or sales categories for deeper analysis.  


---

## 📉 Dashboards & Screenshots  

### 📈 House Market Overview 

- Jutland shows positive median sales price growth, while Bornholm records a decline.  
- Units sold in the latest quarter = **77**, with **13bn DKK sales** in last 12 months.  
- Strong correlation between **Offer Price** and **Purchase Price**.  
- YOY Sales Growth: Auction sales grew slightly (+0.29), but Family Sales fell (-0.75). 

![House Market Overview](https://github.com/user-attachments/assets/d1249d76-0612-42e6-9485-f71ea58ec539) 

### 💰 Sales Performance   

- **Regional Sales**: Zealand (95bn) leads, followed by Jutland (81bn).  
- **Average Price per SQM**: Highest in Zealand (~20.8k), lowest in Bornholm (~10.6k).  
- **Age Influence**: Buyers aged **16–45** contribute to lower purchase prices.  
- **Offer to SQM Ratio**: Regular sales (~14.9k) > Family sales (~11.9k).
  
![Sales Performance](https://github.com/user-attachments/assets/ec0b53f3-4cc2-471d-88a9-caa835a1b2d9) 

### 📊 Analysis by House Type

- **Offer vs Purchase Price**: Very close across all house types → strong price alignment.  
- **Financial Indicators**: Yield is consistently higher (3.8–4.6%) than inflation/interest (~1.8–2%).  
- **Average SQM & SQM Price**: Farms have the largest size (~196 sqm) but lowest price per sqm (~13.8k).  
  Apartments & townhouses are denser with higher price per sqm (~19k–28.7k).
- **User Flexibility**: Filters on area, city, region, and sales type allow users to drill down into localized market dynamics, making insights more actionable for targeted business decisions.
    
![House Type Analysis](https://github.com/user-attachments/assets/a5907cf9-02a9-4c87-86a0-fa7f331db597) 

---

## 🔎 Key Insights & Business Impact  

### 📍 Regional Performance  
- **Insight**: Zealand leads sales volume (**95bn DKK**) followed by Jutland (**81bn DKK**), while Bornholm contributes almost negligible.  
- **Business Impact**: Marketing and investment strategies should **prioritize Zealand and Jutland** as primary revenue drivers, while Bornholm may require targeted incentives or subsidies to boost sales.  

### 📍 Median Sales Price Change  
- **Insight**: Jutland shows the highest positive median price growth, while Bornholm shows a decline.  
- **Business Impact**: Investors may expect **higher returns in Jutland**, whereas Bornholm requires **policy support or market interventions** to stabilize property values.  

### 📍 Sales Type Performance  
- **Insight**: Auction sales show slight growth (+0.29 YOY), while Family Sales have sharply declined (-0.75 YOY). Regular and Other sales are also negative.  
- **Business Impact**: Real estate agencies should **explore auction-based strategies** to maximize growth, while rethinking or restructuring **family sales contracts and financing options** to revive interest.  

### 📍 Buyer Demographics  
- **Insight**: Purchases by **buyers aged 16–45** tend to lower average purchase prices.  
- **Business Impact**: Developers should **design affordable housing packages** targeting younger buyers (first-time homeowners), while offering **premium products** to older demographics who can afford higher property values.  

### 📍 Offer Price vs Purchase Price  
- **Insight**: Offer and purchase prices are highly correlated (closely aligned).  
- **Business Impact**: Indicates a **stable and transparent market** — reduces negotiation cycles, speeds up transactions, and allows sellers to set competitive yet realistic prices.  

### 📍 House Type Analysis  
- **Insight**:  
  - Farms → Large size (196 sqm), but lowest price per sqm (~13.8k).  
  - Apartments/Townhouses → Smaller size but highest price per sqm (~19k–28.7k).  
  - Villas → Balanced size and pricing.  
- **Business Impact**: Investors seeking **long-term land appreciation** should target farms, while developers can **maximize per sqm profitability** by focusing on apartments & townhouses in urban centers.  

### 📍 Financial Indicators (Inflation, Interest, Yield)  
- **Insight**: Yield rates (3.8–4.6%) are consistently higher than inflation (~1.9%) and interest (~1.8%).  
- **Business Impact**: Real estate remains an **attractive investment class**, outperforming inflation and mortgage costs. Developers and agencies can **leverage this narrative** to attract investors and buyers.  
 
---

## 🎯 Key Learnings  

- Learned to integrate **BigQuery with Power BI** for scalable cloud-based analytics.  
- Improved skills in **SQL transformations**, **Power Query cleaning**, and **DAX calculations**.  
- Designed advanced Power BI visuals including **ribbon charts, key influencer visuals, and clustered charts**.  
- Enhanced ability to communicate **housing market insights** through KPIs and storytelling dashboards.  

---
## 💡 Special Note
This project showcases my end-to-end data analytics skills — from **data extraction and transformation in Google BigQuery**, to **data cleaning in Power Query**, and building **interactive dashboards with DAX in Power BI**.  
It reflects my ability to not only perform technical implementation but also derive **business-driven insights** that support decision-making.  
I am eager to bring the same problem-solving and analytical approach to real-world business challenges in a professional role.  



