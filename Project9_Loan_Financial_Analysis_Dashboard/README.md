# 💳 Loan Default & Financial Risk Analysis Dashboard (SQL + Power BI)

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
 

- **Data Validation**  
  - Cross-checked each visual's results with:  
    1. **Table visuals** in Power BI.  
     The image indicates that the result in the actual visual and the table visual used for data validation are same.
    
    ![Validation](https://github.com/user-attachments/assets/7f97e786-7daa-4deb-9077-294a136bf87a)
  

    2. **Excel pivot tables** from main dataset Source.  
   
    
---

## 📊 Dashboards & Visuals  

### 🔹 Loan Default & Overview  
- Loan amount distribution by purpose.  
- Average income by employment type.  
- Default rate across employment types.  
- Loan amounts by age groups.  
- Year-wise loan default trends.  

![Loan Default Overview](YOUR_SCREENSHOT_LINK_1)  

---

### 🔹 Financial Risk Matrices  
- YOY loan amount & default changes.  
- YTD loan amount by credit score bins & marital status.  
- Decomposition tree: Income Bracket vs Employment Type.  

![Financial Risk](YOUR_SCREENSHOT_LINK_2)  

---

### 🔹 Applicant Demographics & Financial Profile  
- Median loan amount by credit category.  
- Loan distribution by education, marital status, dependents.  
- Average loan for high credit applicants by age group & marital status.  

![Demographics Profile](YOUR_SCREENSHOT_LINK_3)  

---

## 🔎 Key Insights & Business Impact  

- **Default Risk**: Unemployed borrowers have the **highest default rate (3.39%)**, while full-time employees show the lowest (~2.36%).  
- **Age Influence**: Adults & middle-aged borrowers take the **highest average loans (~127k)**, while teens take significantly less.  
- **Credit Score Effect**: Applicants with **Medium & High credit scores** account for the majority of loans, while low credit borrowers still secure significant amounts (~1.1bn).  
- **YOY Trends**: 2015–2016 saw the **highest loan growth & defaults**, whereas 2017 showed a dip.  
- **Marital Status**: Married & divorced applicants account for higher loan volumes compared to singles.  

---

## 🎯 Key Learnings  

- Stronger understanding of **SQL + Power BI integration** for end-to-end reporting.  
- Implemented **advanced DAX measures**: YOY, YTD, ratios, and decomposition trees.  
- Learned **financial risk profiling** using credit score bins, income brackets, and loan purpose.  
- Validated business intelligence dashboards against raw **Excel pivots** for accuracy.  

---

## 💡 Special Note  

This project demonstrates my ability to create **risk-focused financial dashboards** that combine **data cleaning, SQL transformations, DAX measures, and business storytelling**.  
It provides actionable insights for **credit analysts, risk managers, and banks** to make informed lending decisions.  

---
