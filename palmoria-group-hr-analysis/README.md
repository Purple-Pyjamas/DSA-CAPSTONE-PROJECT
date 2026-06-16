# Palmoria Group HR Analysis
 
> Analyzing gender distribution, pay gaps, and performance ratings across Palmoria Group's regions to reveal inequality insights as regards salary distribution across genders, and drive fair, data-backed management decisions.

---

## 📖Project Overview

This project was completed as part of the DSA Data Analysis Capstone requirements, where I took on the role of an HR Analytics Expert recruited by the Palmoria Group, a Nigerian manufacturing company facing public scrutiny over gender inequality.  
In this project, I analyse the Palmoria Group company’s HR data to generate insights and reveal problem areas, especially regarding gender related issues across the 3 regions of the company, and come up with evidence based recommendations for the management’s attention. 
As a secondary task, I also allocated the annual bonuses to be paid out to each employee based on their performance rating, and I visusalized my findings neatly using PowerBi.

---

## ❓Problem Statement

The Palmoria Group was publicly called out by the media as "The Manufacturing Patriarchy" due to concerns about gender inequality. HR needs a data-driven internal report to understand:
1. The gender distribution in the organization, by region and by department
2. Variations of performance ratings based on gender 
3. The company’s salary structure. Is there is a gender pay gap? If yes, in what department and regions?
4. A recent regulation was adopted which requires manufacturing companies to pay 
employees a minimum of $90,000 
 - Does Palmoria meet this requirement?
 -  What is the pay distribution of employees grouped by a band of $10,000 across the 3 regions of the company?
As a secondary task, HR wants a newly computed salary for individual employees in the company, and handed me another data set that contains rules for making bonus payments, requiring me to:
1. Calculate the amount to be paid as a bonus to individual employees
2. Calculate the total amount to be paid to individual employees (salary inclusive of bonus)
3. Calculate the total amount to be paid out per region and company-wide

---

## 🔨Tools

| Tool | Purpose |
|------|---------|
| Power BI | Interactive dashboard and data visualization, new groups |
| Power Query| Data transformation: removing nulls, promote headers, changed data type, pivot columns |
| DAX | Calculated measures, calculated columns |
| Formulas | `Total Compensation = 'Palmoria Group emp-data'[Salary] + 'Palmoria Group emp-data'[Bonus Amount]`; `Bonus Amount = VAR EmpDept = 'Palmoria Group emp-data'[Department] VAR EmpRating = 'Palmoria Group emp-data'[Rating] VAR BonusPct = CALCULATE(MAX('bonus lookup table'[Value]), 'bonus lookup table'[Department] = EmpDept, 'bonus lookup table'[Attribute] =EmpRating) RETURN 'Palmoria Group emp-data'[Salary] * BonusPct`
         
---

## 📂 Dataset

| Field | Details |
|-------|---------|
| **Source** | Internal, HR data provided by Palmoria Group (via DSA) |
| **Scope** | All company employees across 3 regions and multiple departments |
| **Key Columns** | [Employee ID, Gender, Region, Department, Salary, Performance Rating] |
| **Data Privacy** | All personal data has been anonymized, no real employee identities disclosed |
| **Supplementary data** | Contains rules for bonus allocation (rating-to-bonus percentage mapping) |

---

## 🔍 Methodology

### Step 1: Data Cleaning
- Removed duplicate rows
- Handled missing values using 
- Standardized date formats 
- Renamed columns for consistency
- Deleted useless column

### Step 3: Exploratory Data Analysis (EDA)

- Showed the total number of employees, average salary, and minimum salary using cards on dashboard
- Analysed the gender distribution across departments using tables on the dashboard
- Tramsformed data in power query: promoted headers, pivotted columns, changed data types, filtered rows, replaced rows
- Used DAX functions and measured columns to analyse and identify gender disparities in pay, ratings, and representation

### Step 4: Created calculated columns

| Column | Logic |
|--------|-------|
| Salary Band | Grouped into $10,000 bands: $20k–$30k, etc. 
| Bonus amount for each employee |Pivoted the bonus rules table, created new calculated columns from it: Bonus Amount = VAR EmpDept = 'Palmoria Group emp-data'[Department] VAR EmpRating = 'Palmoria Group emp-data'[Rating] VAR BonusPct = CALCULATE(MAX('bonus lookup table'[Value]), 'bonus lookup table'[Department] = EmpDept, 'bonus lookup table'[Attribute] =EmpRating) RETURN 'Palmoria Group emp-data'[Salary] * BonusPct |
| New salary | Total Compensation = 'Palmoria Group emp-data'[Salary] + 'Palmoria Group emp-data'[Bonus Amount] |

### Step 5: Visualization & Dashboard

- Key KPIs displayed include:
  - Average salary across employees
  - Gender distribution in the company and across regions, department and salary range
  - Salary disribution across regions and then across departments in the company
  - Insights on the performance ratings of employees, categorized by their gender
- Chart types used include: clustered bar chart, clustered column chart, donut chart, and cards as well
- Filters/slicers for more precise information

---

## 💡 Key Findings & Insights

👩‍🦱 Gender Distribution: Female employees represent 46.62% of the workforce overall, with lagos being the most imbalanced area. In general however, there is no significant difference. Non-binary employees represent only a 4.23% of the workforce, which is significantly low.
📊 Ratings Gap: Male employees received "Average" ratings at 22 percentage points higher than female employees in the company, despite similar role distributions.
💸 Pay Gap: A gender pay gap of approximately $6230 exists on average. Pay gap is most pronounced in the Human resource and Sales departments, and in Lagos state, with deficits of up to 12% of the average salary.
⚖️ Regulation Compliance: More than 70% of employees currently earn below the $90,000 minimum salary threshold — concentrated in Kaduna
🎁 Bonus Payout: Total bonus obligations amount to $2,200,000 company-wide, with Kaduna accounting for the largest share at $825,911.78.

---

## 📊 Dashboard / Visualizations

<img width="632" height="353" alt="palmoria1" src="https://github.com/user-attachments/assets/a3412d4a-111f-4431-aace-b98bd1aa0739" />

<img width="638" height="362" alt="palmoria2" src="https://github.com/user-attachments/assets/1f40765d-2ce1-4d0f-bf5b-f58ce88dddef" />

---

## 🚀 How to Use This Project

### To view the Power BI Dashboard:
1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
2. Clone or download this repository
3. Open `palmoria hr analysis.pbix` in Power BI Desktop
4. Explore using the slicers and filters on the report pages

---

## Limitations

- Employees who did not disclose gender were classified as "Non binary". They were only excluded from gender-specific interpretations, but not the initial analysis, and may cause skewed results.
- This analysis is based on a static HR snapshot. Attrition and promotions after the data cut-off are not reflected.
- The minimum salary regulation ($90,000) is applied uniformly, and a regional "cost of living" differences were not factored in.

---

## Future Improvements

- Build a Power BI dashboard with drill-through by employee level and tenure
- Add trend analysis where multi-year HR data becomes available
- Automate bonus calculation using Python for scalability

---

## 📬 Contact

**Uchechukwu Okwudili**  
📧 [ucokwudili27@gmail.com]  
💼 [www.linkedin.com/in/uchechukwu-okwudili-a7437933a]  

---
