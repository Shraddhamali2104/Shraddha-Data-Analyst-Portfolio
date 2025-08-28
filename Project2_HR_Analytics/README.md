
# 📊 HR Analytics Dashboard  
 
### Project Link:
[Access Dashboard (.pbix)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project2_HR_Analytics/HR%20Analytics%20.pbix)

### Detailed Documentation Link: 
https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project2_HR_Analytics/HR_Analytics_Dashboard_Documentation.pdf

### Dataset:
[Download Dataset](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project2_HR_Analytics/Attendance%20Sheet%202022-2023_Masked.xlsx)

## 📝 Problem Statement 
This dashboard was developed to analyze employee attendance behaviors across multiple dimensions including work-from-home trends, sick leave patterns, and overall presence rates.
The objective is to provide actionable insights to HR and management regarding:

- Which employees or teams have the highest and lowest presence and work-from-home percentages.

- How sick leave incidence fluctuates over time and across the organization.

- Which days (e.g., Mondays, Fridays) are most commonly chosen for remote work.

- Identifying potential wellness issues signaled by spikes in sick leave.

- Understanding weekly and monthly trends to improve workforce planning, event scheduling, and hybrid office strategies.

The dashboard equips decision makers with a single-view attendance tool to enhance HR policy-making, space management, and proactive employee wellness interventions.




## ⚙️ Steps Followed  

- **Step 1:** Imported monthly attendance sheets from Excel, each containing employee records with daily attendance codes.
- **Step 2:**  Unpivoted the data so all dates appear in a single column, standardized column names and data types, and removed summary or non-relevant rows. 
- **Step 3:**  Created a parameter template and implemented the GetData function, allowing the same transformation to be dynamically applied across all monthly sheets. 
- **Step 4:**  Invoked the transformation function on all sheets and combined them into a single, unified attendance table for analysis. 
- **Step 5:**  Developed DAX measures for key HR metrics, including WFH Count, Total Working Days, Present Days, Presence %, WFH %, SL Count, and SL %. 
- **Step 6:**  Designed an interactive Power BI dashboard with:
      -  card visuals for key KPIs
      -  tables/matrices for employee-level insights
      -  area charts for trend analysis
      -  day-of-week visuals
      -  slicers for flexible time-range selection.  
- **Step 7:**  Designed visualizations:  
  Used the dashboard to capture trends in leaves, remote work, and attendance, generating actionable insights to support HR planning and management.



  ## 📉 Dashboard  

### Employee Attendance & Work Preference Insights 



![Dashboard]("https://github.com/user-attachments/assets/e2e1416d-8465-49e0-bc25-16b5a35aae5b")  

  

---
