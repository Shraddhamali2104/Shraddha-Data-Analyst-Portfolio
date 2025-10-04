# 💳 Loan Default & Financial Risk Analysis Dashboard(SQL + Power BI)

### 🔗 Project Link
[Access & Download Dashboard (.pbix)](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project9_Loan_Financial_Analysis_Dashboard/Loan_Default_analysis.pbix)  

---

## 📝 Problem Statement  

Banks and financial institutions face increasing **risk of loan defaults**, which impacts profitability and credit management strategies.  
The objective of this project was to build an **interactive Power BI dashboard powered by SQL & DAX** that analyzes:  

- Loan distribution by purpose, age, employment, and income.  
- Trends in loan defaults over time.  
- Financial risk segmentation by credit score, marital status, and income bracket.  
- Applicant demographics & financial profiles influencing defaults.

---

## 📂 Dataset

- **Source**: [Loan Data File](https://github.com/Shraddhamali2104/Shraddha-Data-Analyst-Portfolio/blob/main/Project9_Loan_Financial_Analysis_Dashboard/Loan%2BDataset%2BLink.xlsx)  
- **Size**: ~2,55,347 records  

#### Key Columns:  
- `LoanID` → Unique identifier of each loan  
- `LoanAmount` → Approved loan amount  
- `Purpose` → Purpose of loan (Home, Business, Education, Auto, etc.)  
- `EmploymentType` → Borrower’s employment category (Full-time, Part-time, Self-employed, Unemployed)  
- `Income` → Annual income of borrower  
- `CreditScore` → Numeric score (binned into categories: High, Medium, Low, Very Low)  
- `AgeGroup` → Derived column (Teen, Adults, Middle Age Adults, Senior Citizens)  
- `MaritalStatus` → Borrower’s marital status (Single, Married, Divorced)  
- `Education` → Education level of borrower  
- `LoanStatus` → Defaulted or Non-defaulted loan  
- `LoanDate` → Issue date (used for year-based analysis)  

![Dataset](https://github.com/user-attachments/assets/0275e41c-5117-4e3f-942f-88f062f4d83c)


---

## ⚙️ Steps Followed  

- **Step 1: Data Loading**  
  - Loaded loan dataset into **MS SQL Server**.  

- **Step 2: Data Connection**  
  - Imported data from SQL Server to **Power BI Desktop**.  

- **Step 3: Data Profiling & Cleaning**  
  - Adjusted data types (Date, Numeric, Categories).  
  - Handled null values and verified with Excel source pivots.  

- **Step 4: Feature Engineering**  
  - Created **derived columns**: `Year`, `AgeGroup`, `Credit Score Bins`, `Income Bracket`.
  
  ![Derived column and dax measures](https://github.com/user-attachments/assets/eb515d1f-8919-46d9-8e82-99b721cabaea)
  
  
## 📌 Step 5: DAX Measures & KPIs  

### 📊 Page 1 – Loan Default Overview  
- **Average Income by Employment Type** → AVG borrower income segmented by employment categories (Full-time, Self-employed, etc.).  
- **Average Loan by Age Group** → AVG loan amount segmented by borrower age groups (Teens, Adults, Middle Age, Seniors).  
- **Default Rate by Employment Type** → % of defaults segmented by employment categories.  
- **Default Rate by Year** → Annual ratio of defaults to total loans (yearly portfolio risk trend).  
- **Loan Amount by Purpose** → SUM of loan amounts grouped by loan purpose (Home, Business, Auto, Education, etc.).  

---

### 📊 Page 2 – Applicant Demographics & Financial Profile  
- **Average Loan Amount (High Credit)** → AVG loan size only for *High Credit Score* borrowers (financial strength indicator).  
- **Median Loan by Credit Score Bins** → Median loan amount grouped by credit score bins (High, Medium, Low, Very Low).  
- **Total Loan (Adults) by Credit Bins** → SUM of loans taken by adult borrowers segmented into credit bins.  
- **Total Loan (Middle Age Adults)** → SUM of loan amounts for middle-aged borrowers (loan exposure concentration).  
- **Total No. of Loans by Education Type** → COUNT of loans segmented by borrower education levels (School, Graduate, Postgraduate, etc.).  

---

### 📊 Page 3 – Financial Risk & Time Analysis  
- **YOY Default Loan Change** → Year-over-year % change in loan defaults (default trend tracker).  
- **YOY Loan Amount Change** → Year-over-year % change in total loan disbursements (growth/decline tracker).  
- **YTD Loan Amount** → Year-to-date loan disbursement (running total of loans issued in the current year).


## Data Validation
  - Cross-checked each visual's results with:  
    1. **Table visuals** in Power BI.  
     The image indicates that the result in the actual visual and the table visual used for data validation are same.
    
    ![Validation](https://github.com/user-attachments/assets/7f97e786-7daa-4deb-9077-294a136bf87a)
  

    2. **Excel pivot tables** from main dataset Source.  
    The images indicates that the result in the actual visual and the pivot table used for data validation are same.
    
   <p align="center">
  <img src="https://github.com/user-attachments/assets/3b4e5e83-c514-4d3f-8e56-025d150869e1" alt="Page 1 Dashboard" width="45%" />
  <img src="https://github.com/user-attachments/assets/58416363-5118-4151-85c7-ae918286adbe" alt="Page 2 Dashboard" width="45%" />
   </p> 
---

## 📊 Dashboards & Visuals  

### 🔹 Loan Default & Overview  
This dashboard provides an overview of borrower risk and loan distribution patterns. It highlights average income by employment type, loan amount distribution by purpose, and default rates across employment types and years. The focus is on identifying which categories of borrowers are more prone to defaults and how defaults have trended over time. 

![Loan Default Overview](https://github.com/user-attachments/assets/aeea2695-cf22-4f32-a012-9f3979706412)  

---

### 🔹 Financial Risk Matrices  
This dashboard tracks loan growth and default changes over time. It uses measures like **YOY loan amount change**, **YOY default loan change**, and **YTD loan disbursement** to analyze business growth and portfolio risk. Additionally, a **Decomposition Tree** is included to drill down into loan distribution by different borrower attributes (such as income brackets and employment type), providing deeper insights into the key factors driving loan performance. Overall, the dashboard helps identify whether the financial institution is lending more responsibly and if defaults are reducing or rising year-over-year.


![Financial Risk](https://github.com/user-attachments/assets/20426a36-f974-4748-8f69-c5964c588e02)  

---

### 🔹 Applicant Demographics & Financial Profile  
This dashboard analyzes borrower demographics and financial strength. It showcases insights like average and median loan amounts segmented by credit scores, loan distribution across age groups, and number of loans by education type. The goal is to understand how borrower background (education, credit, age) influences loan exposure.

![Demographics Profile](https://github.com/user-attachments/assets/093f957b-9afa-4acd-b848-8f000c5ef583) 

---

## 📊 Key Insights & Business Impact  

### 🔹 Page 1 – Loan Default Overview  
- **Average Income vs Employment Type** → Full-time employees have the **highest average income (~₹50K)** compared to self-employed (~₹35K). However, default rates for self-employed are **10% higher**, showing income stability matters more than raw income.  
- **Loan Amount by Purpose** → The **largest loan segment is Home Loans (~₹3.5M total)**, followed by Business and Auto Loans. Education loans are **lowest but show higher default rates (~18%)**, indicating higher risk in lending to students/young borrowers.  
- **Default Rate by Year** → Defaults have declined from **15% in 2018 to 9% in 2022**, showing better risk controls and improved credit policies.  
- **Business Impact** → Focus lending more towards **low-risk employment categories** and maintain strong **credit checks on self-employed & education loans**.  

---

### 🔹 Page 2 – Applicant Demographics & Financial Profile  
- **Average Loan by Credit Score** → Borrowers with **High Credit Scores take larger loans (~₹200K avg)**, but default less. Low credit borrowers take **smaller loans (~₹80K avg)** but default at a much higher rate (~22%).  
- **Median Loan by Credit Score Bin** → Median loans steadily rise with credit quality, validating the credit scoring system as a strong predictor of risk.  
- **Total Loans by Age Group** → Middle-aged borrowers (30–45 yrs) account for **~55% of total loan volume**, showing they are the core business segment.  
- **Loans by Education Type** → Graduates hold the majority share (~60% of loans), while postgraduates take fewer loans but at higher average amounts.  
- **Business Impact** → Bank should **prioritize lending to high-credit middle-aged borrowers** (high volume, low risk) while placing **strict caps/interest premiums on low credit score borrowers** to reduce NPAs (non-performing assets).  

---

### 🔹 Page 3 – Financial Risk & Time Analysis  
- **YOY Loan Amount Change** → Loan disbursements have grown steadily at **12–15% YoY**, showing strong demand.  
- **YOY Default Loan Change** → Defaults have reduced YoY from **+10% growth in 2019 to –5% in 2022**, meaning risk control strategies are working.  
- **YTD Loan Amount** → Current year YTD loans have crossed **₹1.8M**, tracking ahead of last year’s pace.  
- **Business Impact** → Growth is sustainable with reducing default ratios. The bank can **expand loan products to high-credit customers** while continuing to monitor risk-heavy categories (students, self-employed, low credit scores).  


---

## 🎯 Key Learnings  

- Stronger understanding of **SQL + Power BI integration** for end-to-end reporting.  
- Implemented **advanced DAX measures**: YOY, YTD, ratios, and decomposition trees.  
- Learned **financial risk profiling** using credit score bins, income brackets, and loan purpose.  
- Validated business intelligence dashboards against raw **Excel pivots** for accuracy.  

---
### ℹ️ Why Custom DAX Measures Were Created  

You might be wondering why some of the measures were created even though Power BI provides built-in features to showcase them.  
The main purpose was to **understand and implement different DAX functions** such as:  

- `DATEYTD`  
- `CALCULATE`  
- `CUMULATIVE`  
- `ALLEXCEPT`  
- `ALL`  
- `COUNTROWS`  
- `FILTER`  
- `NOT`  
- `ISBLANK`  
- `MEDIANX`  
- `AVERAGEX`  
- `SUMX`  

Additionally, each measure and visual was **validated after creation**, since ensuring accuracy holds huge importance in data analysis.  

---
## 💡 Special Note  

This project demonstrates my ability to create **risk-focused financial dashboards** that combine **data cleaning, SQL transformations, DAX measures, and business storytelling**.  
It provides actionable insights for **credit analysts, risk managers, and banks** to make informed lending decisions.  

---
