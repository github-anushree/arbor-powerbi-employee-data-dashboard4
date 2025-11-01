Employee Insights Dashboard | Analyzing Workforce Trends with Power BI
📘 Project Overview

This Power BI project transforms raw Excel employee data into a fully interactive HR Analytics Dashboard.
It provides key insights into employee distribution, salary trends, bonus ratios, tenure analysis, and workforce diversity — empowering data-driven HR decisions.

🧩 Key Objectives

Clean, transform, and model employee data in Power Query

Create dynamic calculated columns and DAX measures

Visualize salary, tenure, department, and gender insights

Build an interactive and executive-friendly dashboard

🧠 Tech Stack

Tool: Microsoft Power BI

Data Source: Excel (arbor-powerbi-employee-data.xlsx)

Language: DAX, Power Query (M Language)

Model Type: Single table (Employee Data)

Data Transformations: Data cleaning, removing duplicates, type conversion, date/time logic

⚙️ Data Transformation Steps

Performed in Power Query Editor:

Data Cleaning: Removed blanks, errors, and duplicate records using Remove Duplicates and Filter Rows.

Date Operations: Extracted Joining Month, Joining Year, and calculated TenureDays using

TenureDays = Duration.Days(DateTime.LocalNow() - [Joining Date])


Feature Engineering: Created Month-Year column for time-based analysis.

Validation: Used Group By to ensure no duplicate Employee IDs.

🧮 DAX Measures Created
KPI	DAX Formula (Simplified)
Total Employees	DISTINCTCOUNT(UniqueEmpID)
Total Salary	SUM(Salary)
Total Bonus	SUM(Bonus)
Average Salary	AVERAGE(Salary)
Average Bonus	AVERAGE(Bonus)
Bonus % of Salary	DIVIDE([Total Bonus], [Total Salary])
Total Tenure (Years)	SUMX(Employee, Employee[TenureDays]/365)
Average Tenure	AVERAGE(TenureDays)
📊 Dashboard Highlights

✅ KPI Cards: Total Employees, Avg Salary, Avg Bonus, Avg Tenure
📈 Charts:

Department-wise Employees

Country-wise Avg Salary

Gender Distribution (Donut Chart)

Avg Tenure by Department

Salary Trend (Line Chart over Month-Year)
🌍 Location Metrics: Country-level salary averages

🎯 Key Insights

HR department has the highest employee count.

Average employee tenure is around 2,000+ days, reflecting good retention.

Bonus constitutes nearly 9% of total salary.

Canada and France lead with the highest average salaries.

🪄 What Makes This Dashboard Stand Out

Clean, minimalistic design using corporate yellow and gray theme

Completely dynamic — filters by Department, Country, Gender

Built using DAX measures only (no hardcoded values)

Ready for HR Managers or Business Leaders to use for real insights

📁 File Structure
📂 Arbor-Employee-Insights
 ┣ 📊 Employee_Insights_Dashboard.pbix
 ┣ 📈 arbor-powerbi-employee-data.xlsx
 ┣ 🧾 README.md
 ┗ 📸 dashboard-preview.png

🏁 Conclusion

This project demonstrates how raw Excel HR data can be transformed into strategic insights using Power BI’s analytical power — from data cleaning to storytelling visuals.
