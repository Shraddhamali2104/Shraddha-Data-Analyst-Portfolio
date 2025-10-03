# 💳 Loan Default & Financial Risk Analysis Dashboard (SQL + Power BI)

### 🔗 Project Link
[Access Dashboard (.pbix)](YOUR_LINK_TO_PBIX_FILE)  
[Dataset (Excel/CSV)](YOUR_LINK_TO_DATASET)  

---

## 📂 Dataset

- **Source**: [Loan Data File](YOUR_EXCEL_LINK)  
- **Size**: ~100k+ records  
- **Columns**: Borrower demographics, employment type, loan purpose, income, credit score, loan status (default/non-default), etc.  

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

📸 *Refer to screenshots below for dashboard previews.*  

---

## 📝 Problem Statement  

Banks and financial institutions face increasing **risk of loan defaults**, which impacts profitability and credit management strategies.  
The objective of this project was to build an **interactive Power BI dashboard powered by SQL & DAX** that analyzes:  

- Loan distribution by purpose, age, employment, and income.  
- Trends in loan defaults over time.  
- Financial risk segmentation by credit score, marital status, and income bracket.  
- Applicant demographics & financial profiles influencing defaults.  

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

- **Step 5: DAX Measures & KPIs**  
  - **Loan Amount by Purpose** → SUM of loan amount grouped by purpose.  
  - **Average Income by Employment Type** → AVG income per category.  
  - **Default Rate by Employment Type** → % default per employment type.  
  - **Average Loan by Age Group** → AVG loan by derived age groups.  
  - **Default Rate by Year** → Loan defaults ratio by year.  
  - **YOY Loan Amount Change** → % change vs previous year.  
  - **YOY Default Loan Change** → % change in defaulted loans vs previous year.  
  - **YTD Loan Amount** → Ribbon chart by credit bins & marital status.  
  - **Median Loan by Credit Score** → Median loan per credit category.  
  - **Decomposition Tree** → Loan amount split by income bracket & employment type.  

- **Step 6: Data Validation**  
  - Cross-checked results with:  
    1. **Table visuals** in Power BI.  
    2. **Excel pivot tables** from source dataset.  

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
