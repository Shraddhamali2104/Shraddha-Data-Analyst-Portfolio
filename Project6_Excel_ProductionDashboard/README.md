# 🏭 Production Analysis & Manager Performance Dashboard  

### 📌 Project Link  
📂[Download Excel File](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project6_Excel_ProductionDashboard/Excel_Production_Dashboard.xlsx)
 
This Excel file contains updated data, visuals and dashboard.
 
---

### 📂 Dataset   

This dataset contains **production and manager-level data** with:  
- 👩‍💼 **Manager Details:** Name, Gender (NULLs handled), Age (standardized using first recorded value)  
- 🌍 **Region** – Production site location  
- 📦 **Production Data:** Product Type, Units Produced, Production Cost, Year, Month  

Data was cleaned and transformed in Excel to create derived columns such as **Age Group** and **Production Cost per Unit** for better analysis.

---

## 📝 Problem Statement  
Manufacturing teams often struggle with:  
- Tracking **manager performance & workload distribution**  
- Identifying **high-cost product lines**  
- Understanding **seasonality in production trends**  

This project solves these pain points by:  
✅ Analyzing production costs by product type  
✅ Highlighting workload imbalance across managers  
✅ Visualizing monthly production patterns  
✅ Enabling interactive decision-making with filters  

---

## ⚙️ Project Workflow  

### 1️⃣ Data Understanding & Cleaning  
- Replaced missing Gender values with `"Unknown"`  

**Data View Before Cleaning :**

![Data View](https://github.com/user-attachments/assets/a439e6d3-9485-4a21-88d7-a3036616ef46)

**Data View After Cleaning :**

![Data View](https://github.com/user-attachments/assets/675cbad9-d42a-43bf-bc04-0f5cf611a7ef)

### 2️⃣ Data Transformation  
- Standardized Manager Age using `VLOOKUP` (kept first recorded value) :
  - Each manager was having different ages.Set the first entry of age according to production date as the true age uisng vlookup function.
**Before:**
![Screenshot](https://github.com/user-attachments/assets/8a3192be-2965-4fc8-b895-67aa573fed28)
**After**
![Screenshot](https://github.com/user-attachments/assets/2d6c715e-8f56-454f-8de3-63d7fc9aad73)  

- Created **Age Group** column using Nested `IF`  
- Calculated **Production Cost per Unit** = Total Cost ÷ Units Produced

![Screenshot](https://github.com/user-attachments/assets/90ead1f5-60cd-4437-b90b-4d348b9fdf48)

### 3️⃣ Visualization  
Designed key charts in Excel:  
- 📊 **3D Column Chart:** Total Production Cost by Product Type
  ![Column Chart](https://github.com/user-attachments/assets/defe9f16-79aa-4f09-96ac-66abadf9e649)
  
- 📊 **3D Bar Chart:** No. of Tasks by Manager
  ![Bar Chart](https://github.com/user-attachments/assets/bf66586a-623f-4586-8dac-fb3bbdb170e5)
  
- 📈 **3D Line Chart:** Units Produced by Year & Month
  ![Line Chart](https://github.com/user-attachments/assets/f3096d6c-8a72-442a-b51b-a79511b99106)
  
- 🥧 **3D Pie Chart:** Average Production Cost per Unit by Product Type
  ![Pie Chart](https://github.com/user-attachments/assets/05c9a9b8-e27d-47a6-a521-4a530bc26fb2)

### 4️⃣ Dashboard Design  
- Combined all charts into a **single interactive Excel dashboard**  
- Added **Slicers** for filtering by Region, Gender, Age Group, and Quarter


---

## 🚀 Tools & Skills Used  
- **Tool:** Microsoft Excel  
- **Key Functions:** VLOOKUP, IF, Nested IF, Math Formulas  
- **Visuals:** 3D Column, 3D Bar, 3D Line, 3D Pie  
- **Interactivity:** Slicers  

---

## 📉 Dashboard Preview  
![Dashboard](https://github.com/user-attachments/assets/cfc31385-b4bd-4335-af6d-adbd0fdfdbaf)

---

# 🔎 Insights & Business Impact  

📌 **Production Cost Analysis**  
- **Insight:** Automobiles have the highest total production cost (₹11.52L), followed by Machinery (₹9.10L).  
- **Impact:** Helps focus cost optimization efforts on high-spend product lines.  

📌 **Manager Workload Distribution**  
- **Insight:** Nancy Grey (2,190 tasks) and Jane Smith (1,164 tasks) handle significantly higher workloads.  
- **Impact:** Supports workload balancing to improve team efficiency and avoid burnout.  

📌 **Production Trend Over Time**  
- **Insight:** Peak production occurred in Nov 2023 (4,803 units) and Mar 2024 (4,127 units), with declines in later months.  
- **Impact:** Enables proactive planning for high-demand periods.  

📌 **Cost per Unit Efficiency**  
- **Insight:** Furniture has the highest cost per unit (₹180.44), while Electronics & Machinery are most cost-efficient (~₹108).  
- **Impact:** Helps optimize production methods for high-cost product lines.  

📌 **Interactive Decision-Making**  
- **Insight:** Dashboard slicers allow quick deep dives by region, quarter, or age group.  
- **Impact:** Enables agile, data-driven decision-making at management level.  

---

## 📈 Key Highlights  
✅ Automated **data standardization** (Manager Age)  
✅ Designed a **single-page interactive dashboard**  
✅ Delivered **actionable insights** with visual storytelling  
✅ Enabled **filter-driven exploration** for managers  

--- 

---

> **⭐ Tip** This project demonstrates **end-to-end Excel-based analytics** — from raw data cleaning to interactive dashboard creation — showcasing strong skills in **data analysis, business insights, and visualization.**

