# Data Dictionary

Source file: `data/HR_Attrition_Analysis_Dashboard.xlsx` (sheet `Employee_Data`), also available as `data/employee_data.csv`.

> Synthetic dataset created for practice/portfolio use. All names and values are fictional.

## Raw columns

| Column | Description |
|---|---|
| Employee_ID | Unique employee ID |
| Name | Employee name (fictional) |
| Age | Age in years |
| Gender | Male / Female |
| Marital_Status | Single / Married / Divorced |
| Education | Diploma, Bachelor's, Master's, MBA, Doctorate |
| Department | Sales, HR, R&D, IT, Finance, Operations |
| Job_Role | Designation |
| City | Work location |
| Joining_Date | Date of joining |
| Exit_Date | Date of leaving (blank if still working) |
| Years_at_Company | Tenure till exit date, or till 01-Oct-2026 if still working |
| Monthly_Salary_INR | Monthly gross salary in INR |
| Last_Hike_Percent | Last salary hike % |
| Job_Satisfaction | 1 = Low, 2 = Medium, 3 = High, 4 = Very High |
| Work_Life_Balance | 1 = Bad, 2 = Good, 3 = Better, 4 = Best |
| Performance_Rating | 1 = Low to 5 = Outstanding |
| Overtime | Yes / No |
| Trainings_Last_Year | Number of trainings attended last year |
| Attrition | Yes = employee left, No = still working |
| Exit_Reason | Reason for leaving (only where Attrition = Yes) |

## Calculated columns (Excel formulas)

| Column | Logic |
|---|---|
| Attriton_Flag | 1 if Attrition = "Yes", else 0 (column name keeps the original spelling used in the workbook) |
| Age_Group | Under25, 25-34, 35-44, 45-54, 55+ |
| Salary_Band | Low: below 40,000; Medium: 40,000 to 60,000; High: above 60,000 (monthly INR) |
| Satisfaction_Level | Low: Job_Satisfaction 1-2; Medium: 3; High: 4 |

## KPI formulas (`Calculation` sheet)

| KPI | Formula |
|---|---|
| Total employees | `=ROWS(HR_Attrition[])` |
| Total attrition | `=SUM(HR_Attrition[Attriton_Flag])` |
| Attrition rate | Total attrition / Total employees |
| Average age | `=AVERAGE(HR_Attrition[Age])` |
| Average job satisfaction | `=AVERAGE(HR_Attrition[Job_Satisfaction])` |
