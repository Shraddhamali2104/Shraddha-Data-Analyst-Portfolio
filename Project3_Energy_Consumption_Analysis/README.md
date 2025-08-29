# ⚡ Energy Consumption Dashboard  

### Project Link:  
[Access Dashboard (Tableau Cloud)](https://public.tableau.com/) <!-- replace with actual Tableau Cloud link -->  

### Project Presentation (PPT) Link:  
[Download Presentation (PPT)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project3_Energy_Consumption_Analysis/Energy-Consumption-Dashboarding-using-Snowflake-and-Tableau.pdf) 

### Dataset:  
[Download Dataset](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project3_Energy_Consumption_Analysis/Renewable_Energy_Usage_Sampled.csv)  

---

## 📝 Problem Statement  
This project was designed to analyze **renewable and non-renewable energy consumption patterns** across different regions, countries, and income levels.  

The main objectives were to:  
- Monitor **monthly usage trends** segmented by region, country, and energy source.  
- Analyze **impact of income levels** on energy usage and cost savings.  
- Provide decision-makers with **insights into sustainable energy adoption** and opportunities for cost optimization.  
- Develop a **cloud-integrated pipeline** from raw dataset to interactive dashboard for scalable analytics.  

---

## ⚙️ Steps Followed  

- **Step 1:** Created an **Amazon S3 bucket** and uploaded the raw dataset.  
- **Step 2:** Configured an **IAM Role** with proper trust policy for secure Snowflake integration.  
- **Step 3:** Established **S3 → Snowflake integration** using external stage object.  
- **Step 4:** Loaded the dataset into **Snowflake (SQL Worksheet)** for further processing.  
- **Step 5:** Performed **data analysis & transformations** in Snowflake:  
  - Increased **monthly usage** depending on income level:  
    - +10% for Low income  
    - +20% for Middle income  
    - +30% for High income  
  - Adjusted **cost savings** inversely:  
    - -10% for Low income  
    - -20% for Middle income  
    - -30% for High income  
- **Step 6:** Connected Snowflake with **Tableau Desktop**
- **Step 7:** Designed dashboards including the following visuals :
              -   
- **Step 7:** Published dashboards to **Tableau Cloud** for wider accessibility.  

---

## Architectural Diagram


## 📉 Dashboards  

### 🌍 Energy Usage by Region & Country  
Visualizes monthly consumption trends segmented by region, country, and energy source to identify high-usage areas and compare renewable adoption.  

![Energy Dashboard1](https://github.com/user-attachments/assets/placeholder1)  

### 📊 Income Level Impact Analysis  
Analyzes how different income levels influence energy usage growth and cost-saving potential.  

![Energy Dashboard2](https://github.com/user-attachments/assets/placeholder2)  

### 🔋 Energy Source Mix  
Breakdown of renewable vs. non-renewable energy usage, highlighting sustainable adoption trends.  

![Energy Dashboard3](https://github.com/user-attachments/assets/placeholder3)  

---

# 🔎 Insights  

From the dashboard, the following key insights were observed:  

⚡ **Usage Trends**  
- High-income groups show **greater energy consumption growth**, but **lower relative cost savings** due to adjusted scaling.  
- Low-income regions adopt renewables at a **slower pace**, highlighting policy intervention needs.  

🌍 **Regional Observations**  
- Certain countries exhibit **sharp renewable adoption trends**, while others remain reliant on non-renewables.  
- Regions with higher GDP generally have a **diverse energy mix** compared to single-source dependency in developing countries.  

💰 **Cost Savings Patterns**  
- Savings decline as income levels rise, despite higher overall consumption → signals potential inefficiency in energy subsidy allocation.  

📈 **Sustainability Opportunities**  
- Countries with high renewable adoption align with **global sustainability goals**, while lagging regions indicate **growth potential** for clean energy investments.  

---

## 🚀 Tech Stack  
- **Cloud Storage:** Amazon S3  
- **Data Warehouse:** Snowflake  
- **Data Transformation:** SQL (Snowflake Worksheets)  
- **Visualization:** Tableau Desktop + Tableau Cloud  
- **Access Management:** AWS IAM  

---

