#  Palmora Group HR Analytics | Power BI Dashboard

This repository contains an HR analytics project built using **Power BI**, focused on analyzing gender distribution, salary structure, and performance at **Palmora Group**, a fictional manufacturing company based in Nigeria.

## Objective
To help Palmora address gender inequality concerns, pay gap issues, and minimum wage compliance across its regional operations.

---

## Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Key Questions Answered](#-key-questions-answered)
- [Tools Used](#-tools-used)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Power BI Report Features](#-power-bi-report-features)
- [Key Insights](#-key-insights)
- [Bonus Calculation Logic](#-bonus-calculation-logic)
- [Dashboard Preview](#-dashboard-preview)
- [What I Learned](#-what-i-learned)
- [How to View or Use the File](#-how-to-view-or-use-the-file)

---

## Project Overview

Palmora Group has been under scrutiny for potential gender inequality and a visible gender pay gap in its three regional offices. This project provides a data-driven review of the company’s HR data to assist in informed decision-making by:

- Identifying gender distribution per region and department
- Measuring performance ratings by gender
- Analyzing the salary structure and identifying pay gaps
- Checking for minimum wage compliance ($90,000 threshold)
- Calculating employee bonuses based on performance

---

## 📂 Dataset Description

| Column         | Description                                  |
|----------------|----------------------------------------------|
| Name           | Employee's full name                         |
| Gender         | Gender of employee (some missing)            |
| Department     | Assigned department (some NULL values)       |
| Salary         | Monthly/Annual salary                        |
| Location       | Region (Lagos, Abuja, Kaduna)                |
| Rating         | Performance rating (Very Good to Poor)       |

A second dataset was used for mapping bonus percentage by rating.

---

## Key Questions Answered

1. What is the gender distribution across regions and departments?
2. How are ratings distributed by gender?
3. Is there a gender-based salary gap across the organization?
4. Does Palmora comply with the new $90,000 minimum salary regulation?
5. What is the distribution of employees across salary bands?
6. How much bonus should each employee receive based on rating?
7. What is the total compensation (salary + bonus) per region?

---

## Tools Used

- [Power BI Desktop](https://powerbi.microsoft.com)
- Power Query (for data cleaning)
- DAX (for calculated columns and measures)
- Excel (initial dataset)

---

## Data Cleaning & Preparation

- Replaced blank genders with `Undisclosed`  
- Removed rows with NULL departments  
- Filtered out employees without salary values  
- Ensured correct data types (text, numeric)  
- Created new columns for Salary Band, Bonus Amount, and Total Compensation  

---

## Power BI Report Features

- **Donut Chart**: Gender distribution
- **Clustered Bars**: Gender by Region & Department
- **Stacked Columns**: Rating distribution by gender
- **Matrix/Table**: Avg salary by Gender, Region, and Department
- **Bar Charts**: Salary Band groupings, Bonus Allocation
- **KPI Cards**: Total Employees, Minimum Wage Compliance Count
- **Slicers**: Gender | Region | Department | Rating

---

## Key Insights

- Over 58% of employees earn **below** the $90,000 compliance threshold.
-  Women have **lower average salaries** than men across all regions.
- Abuja has the **highest total compensation** after bonus allocations.
- Gender distribution is nearly balanced overall, but department-level bias exists.
- Male employees received **all the “Very Good” ratings**.

---

## Bonus Calculation Logic

| Rating       | Bonus % |
|--------------|---------|
| Very Good    | 20%     |
| Good         | 10%     |
| Average      | 5%      |
| Poor         | 0%      |
| Not Rated    | 0%      |

## DAX Calculations
```DAX
Bonus Amount = Salary * LOOKUPVALUE('BonusRules'[Bonus %], 'BonusRules'[Rating], Rating)
Total Compensation = Salary + Bonus Amount
