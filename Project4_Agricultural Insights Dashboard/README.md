# 🌾 Agricultural Data Analysis Dashboard  

### Project Link:  
[Download PBIX File](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project4_Agricultural%20Insights%20Dashboard/Agriculture%20Data%20Analysis.pbix)  

### Project Presentation (PPT) Link:  
[Download Presentation (PPT)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project4_Agricultural%20Insights%20Dashboard/Agricultural-Data-Analytics-Dashboarding-using-Snowflake-and-Power-BI.pptx) 

### Dataset:  
[Download Dataset](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project4_Agricultural%20Insights%20Dashboard/data_season%20(1).csv) 

---

## 📝 Problem Statement  
Agriculture is highly dependent on environmental factors such as rainfall, temperature, and humidity. Farmers and policymakers often lack a **centralized, data-driven system** to evaluate how these parameters influence **crop yield** across years, seasons, and locations.  

This project was designed to:  
- Analyze **rainfall, temperature, humidity, and yield trends**.  
- Understand the impact of **seasonal, regional, and crop-level variations**.  
- Provide actionable insights to improve agricultural planning and resource allocation.  
- Demonstrate **integration of AWS, Snowflake, and Power BI** for scalable analytics.  

---

## ⚙️ Steps Followed  

- **Step 1:** Uploaded raw agricultural dataset into **Amazon S3**.  
- **Step 2:** Configured **IAM Role** for secure **Snowflake integration**.  
- **Step 3:** Established **AWS → Snowflake pipeline** for structured storage and querying.  
- **Step 4:** Performed **data cleaning & transformations** in Snowflake SQL:  
  - Categorized years into custom buckets (`Y1, Y2, Y3`).  
  - Created `Rainfall_Groups` column (Low, Medium, High).  
  - Standardized missing/incorrect values.  
- **Step 5:** Connected **Snowflake with Power BI** for visualization.  
- **Step 6:** Designed dashboards including:  
  - **Rainfall Analysis** – Trends by year, crop, season, and location.  
  - **Temperature Analysis** – Crop-specific and region-specific temperature patterns.  
  - **Humidity Analysis** – Seasonal and spatial humidity impact.  
  - **Yield Analysis** – Relationship between yield and climatic factors.  
- **Step 7:** Published dashboard to **Power BI Service** for end-user accessibility.  

---

## 🚀 Tech Stack  
- **Cloud Storage:** Amazon S3  
- **Data Warehouse:** Snowflake  
- **Data Transformation:** SQL (Snowflake Worksheets)  
- **Visualization:** Power BI  
- **Access Management:** AWS IAM  

---

## 📉 Dashboard  

This Agricultural Insights Dashboard provides a holistic view of how rainfall, temperature, and humidity influence crop yields across regions, years, and seasons.  

### Rainfall Analysis  
![Rainfall Dashboard](https://github.com/user-attachments/assets/94de777c-6dc7-4190-8531-27297d8834e4)

### Temperature Analysis  
![Temperature Dashboard](https://github.com/user-attachments/assets/7685d0a0-eddf-40ec-9d5e-9b00028a7e83)

### Humidity Analysis  
![Humidity Dashboard](https://github.com/user-attachments/assets/9c5ac69c-69f3-493f-afed-b9ef6871c6ec)  

### Yield Analysis  
![Yield Dashboard](https://github.com/user-attachments/assets/838c06fa-dcf3-4020-8141-aed0adf8a8b7)

---

# 🔎 Insights & Business Impact  

🌧 **Rainfall Trends**  
- **Insight:** Bangalore recorded the highest average rainfall (~3.8K), while regions like Kodagu and Raichur averaged ~3.0–3.2K. Paddy crops showed the highest rainfall dependency (~3.5K).  
- **Decision Impact:** Helps farmers and policymakers **plan irrigation and crop placement** based on rainfall intensity. Agri-businesses can forecast **input demand (fertilizers, seeds, irrigation systems)** for rainfall-dependent crops.  

🌡 **Temperature Patterns**  
- **Insight:** Ginger, Tea, and Cashew thrive at higher temperatures (70–79°C), whereas Cotton and Pepper require cooler conditions (~60°C). Bangalore recorded extreme variations (186°C index), far above Mysuru (43°C) or Mangalore (38°C).  
- **Decision Impact:** Supports **climate-smart agriculture planning**, allowing businesses to **identify suitable crops for each region**. Food processing industries can forecast **supply fluctuations** tied to climate variation.  

💧 **Humidity Observations**  
- **Insight:** Humidity remained stable (~55–56%) across years and regions, with slight crop-specific differences (e.g., Cotton and Pepper showing higher dependency).  
- **Decision Impact:** Consistent humidity helps agribusinesses **standardize storage, packaging, and logistics strategies**. Policy makers can **prioritize drought-resistant crops** in areas with marginal humidity changes.  

🌾 **Yield Insights**  
- **Insight:** Cotton had the highest yield (~51K), followed by Coconut (34K) and Ginger (26K). Kodagu and Mysuru emerged as high-yield regions (29K and 28K). Rabi season outperformed Kharif in yield (24.9K vs 20.2K).  
- **Decision Impact:** Enables **resource allocation for high-yield crops** and season-specific crop rotation strategies. Businesses can forecast **market availability and pricing trends**, reducing risk of oversupply or shortage.  

---

## 📈 Key Value Additions  
- Built **interactive Power BI dashboards** for multi-dimensional agricultural analysis.  
- Leveraged **cloud integration (AWS + Snowflake + Power BI)** to ensure scalability.  
- Helps agribusinesses and policymakers design **region-specific agricultural policies** and optimize **supply chain logistics**.  
- Empowers decision makers with **data-backed strategies** for maximizing yield, minimizing risks, and ensuring sustainable farming practices.  
---
