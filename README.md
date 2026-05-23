# 📊 HR Analytics Dashboard (Power BI)

## 📌 Project Overview
This project focuses on analyzing employee data to understand attrition trends and workforce behavior using Power BI. The dashboard provides actionable insights to help organizations improve employee retention and decision-making.

---

## 🎯 Objectives
- Analyze employee attrition patterns  
- Identify key factors affecting employee turnover  
- Perform data cleaning and transformation  
- Build interactive dashboards using Power BI  
- Apply DAX for business calculations  

---

## 🗂️ Dataset
This project uses the IBM HR Analytics dataset.

### Key Columns:
- Age  
- Attrition  
- BusinessTravel  
- DailyRate  
- Department  
- DistanceFromHome  
- Education  
- EducationField  
- EmployeeNumber  

---

## 🧹 Data Cleaning & Transformation
- Removed unnecessary columns  
- Handled missing values  
- Created calculated columns:
  - Age Group  
  - Travel Category  
  - Distance Category  
- Ensured proper data types  

---

## 📊 Key Metrics (DAX Measures)

```DAX
Total Employees = DISTINCTCOUNT(Employee[EmployeeNumber])

Attrition Count = 
CALCULATE(
    COUNT(Employee[EmployeeNumber]),
    Employee[Attrition] = "Yes"
)

Attrition Rate = 
DIVIDE([Attrition Count], [Total Employees]) * 100

Avg Daily Rate = AVERAGE(Employee[DailyRate])
