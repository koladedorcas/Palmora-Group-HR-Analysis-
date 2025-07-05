#  Palmora Group HR Analytics | Power BI Dashboard

This repository contains an HR analytics project built using **Power BI**, focused on analyzing gender distribution, salary structure, and performance at **Palmora Group**, a fictional manufacturing company based in Nigeria.

## Objective
To help Palmora address gender inequality concerns, pay gap issues, and minimum wage compliance across its regional operations.

---

## Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Tools Used](#-tools-used)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Power BI Report Features](#-power-bi-report-features)
- [Key Questions Answered and their visualization](#-key-questions-answered-and-their-visualization)
- [Dashboard Preview](#-dashboard-preview)
- [Key Insights](#-key-insights)
- [What I Learned](#-what-i-learned)
  

---

## Project Overview

Palmora Group has been under scrutiny for potential gender inequality and a visible gender pay gap in its three regional offices. This project provides a data-driven review of the company’s HR data to assist in informed decision-making by:

- Identifying gender distribution per region and department
- Measuring performance ratings by gender
- Analyzing the salary structure and identifying pay gaps
- Checking for minimum wage compliance ($90,000 threshold)
- Calculating employee bonuses based on performance

---

## Dataset Description

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

![Cleaned Palmoria employee dataset](https://github.com/user-attachments/assets/2a1e5e36-547e-464f-9a6b-1fd4466581aa)
---
![Cleaned palmoria bonus rule dataset](https://github.com/user-attachments/assets/72ae5bec-9cab-498a-9bd3-453f7bfa4c78)
---

## Power BI Report Features

- **Donut Chart**: Gender distribution
- **Clustered Bars**: Gender by Region & Department
- **Stacked Columns**: Rating distribution by gender
- **Matrix/Table**: Avg salary by Gender, Region, and Department
- **Bar Charts**: Salary Band groupings, location and gender
- **KPI Cards**: Total Employees, % gender count
- **Slicers**: Gender | Region | Department | Rating

---

## Key Questions Answered and their visualization

1. What is the gender distribution across regions and departments?
![Palmoria 1](https://github.com/user-attachments/assets/c3bebe09-0327-488e-b3c2-696cb9e1aec1)
---
2. How are ratings distributed by gender?
![Palmoria 2](https://github.com/user-attachments/assets/b3ffc919-0f37-4f16-b89b-9ee7ba6b8562)
---
3. Is there a gender-based salary gap across the organization?
![Palmoria 3](https://github.com/user-attachments/assets/71d2ae40-b6b0-41bd-8cfc-61ea42aac6aa)
---
4. Does Palmora comply with the new $90,000 minimum salary regulation?
![Palmoria 4](https://github.com/user-attachments/assets/e97f3352-63a5-46d7-94a8-e5e6ee6eba9e)

---
5. What is the distribution of employees across salary bands?
![Palmoria 4](https://github.com/user-attachments/assets/e97f3352-63a5-46d7-94a8-e5e6ee6eba9e)
---

## Dashboard Preview
![Palmoria group Dashboard](https://github.com/user-attachments/assets/a3ffd330-347a-4f96-8b02-6148b1ae5135)

-----

## Key Insights
### Palmoria Group: Gender and HR Data Analysis
In this project, I analyzed HR data from Palmoria Group to uncover gender-related insights and assess salary compliance across three regions in Nigeria.

- Total employees: 972

- Minimum wage compliance: ✅ 303 employees meet the $90,000 threshold

- Gender split: 49% Male, 46.5% Female, 4.4% Undisclosed

- Top-paying departments: Accounting (Female), Engineering (Male)

- Kaduna leads in female representation; Lagos is male-dominant

- Most ratings fall under “Good” and “Average”, with females excelling in “Very Good” ratings

## Lessons Learned:
- Effective use of Power Query for data cleaning and merging bonus rules

- Built interactive dashboards with slicers for flexible exploration

- Used Cards, pie charts, and bar visuals to communicate findings clearly

This project showcases my ability to translate HR data into actionable insights for decision-makers.

---






