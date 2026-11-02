# HR Attrition Analysis Dashboard (Excel)

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?logo=microsoft-excel&logoColor=white)
![Focus](https://img.shields.io/badge/Focus-HR%20Analytics-blue)
![Dataset](https://img.shields.io/badge/Dataset-Synthetic%20(80%20employees)-lightgrey)

An interactive Excel dashboard that analyses **why employees leave** and **who is most at risk of leaving**, built with Pivot Tables, Pivot Charts, Slicers and formula-driven KPIs.

> **Why this project?** Employee turnover is one of the most expensive and visible problems in HR. This project shows how raw HR data can be turned into clear, actionable retention insights, the kind of analysis an HR Executive / HR Analyst supports every day.

---

## Dashboard Preview

![HR Attrition Dashboard](images/dashboard_preview.png)

*The full interactive version (with slicers) is in [`data/HR_Attrition_Analysis_Dashboard.xlsx`](data/HR_Attrition_Analysis_Dashboard.xlsx). Download it and open it in Microsoft Excel.*

---

## Business Problem

The company (a fictional organisation, "ABC Co.") is losing a large share of its workforce. HR leadership wants to know:

1. What is the overall attrition rate?
2. Which departments, job roles and employee groups are losing the most people?
3. What reasons do employees give for leaving?
4. Which factors (overtime, satisfaction, work-life balance, hike, tenure) are linked to attrition?
5. What can HR do to improve retention?

## Objectives

- Build a clean, structured HR dataset with calculated helper columns
- Create headline KPIs for quick leadership reporting
- Analyse attrition across department, role, education, age group, gender, marital status, performance, satisfaction and work-life balance
- Analyse exit reasons to understand the "why" behind resignations
- Present the findings in an interactive dashboard and recommend HR actions

---

## Dataset

| Item | Detail |
|---|---|
| Records | 80 employees |
| Columns | 25 (21 raw + 4 calculated) |
| Departments | Sales, HR, IT, Finance, Operations, R&D |
| Period | Joining dates up to 2026; tenure measured till exit date, or till 01-Oct-2026 for active employees |
| Type | **Synthetic (fictional) data created for practice/portfolio use.** All names and values are made up. |

Calculated columns added in Excel: `Attriton_Flag` (1/0), `Age_Group`, `Salary_Band`, `Satisfaction_Level`.

Full column descriptions: [`docs/data_dictionary.md`](docs/data_dictionary.md). A plain CSV copy is available at [`data/employee_data.csv`](data/employee_data.csv).

---

## Tools & Excel Skills Used

- **Excel Tables** with structured references (e.g. `HR_Attrition[Age]`)
- **Formulas:** `ROWS`, `SUM`, `AVERAGE`, nested `IF` (to create age groups, salary bands and satisfaction levels)
- **13 Pivot Tables** (summarised on the `Calculation` sheet)
- **Pivot Charts** (bar, column, pie, doughnut) on the `CHARTS` sheet
- **Slicers** for interactive filtering
- **Dashboard design:** KPI cards, consistent colour theme, chart layout

## Workbook Structure

| Sheet | Purpose |
|---|---|
| `Data_Dictionary` | Meaning of every column |
| `Employee_Data` | Cleaned dataset + calculated columns |
| `Calculation` | KPI formulas and all pivot tables |
| `CHARTS` | Pivot charts |
| `DASHBOARD` | Final one-page interactive dashboard |

---

## Headline KPIs

| KPI | Value |
|---|---|
| Total employees | **80** |
| Employees who left | **34** |
| Active employees | **46** |
| **Attrition rate** | **42.5%** |
| Average age | 33.7 years |
| Average job satisfaction (scale 1-4) | 2.6 |

---

## Key Insights

> These insights describe patterns in this dataset. With only 80 records, treat them as indicators to investigate further, not proven causes.

**1. Poor work-life balance is the #1 exit reason.**
15 of the 34 leavers (44%) cited it, followed by Conflict with Manager (7, 21%) and Job Dissatisfaction (6, 18%). Lack of Career Growth (3), Better Salary Elsewhere (2) and Relocation (1) were minor reasons, so **pay alone is not what is driving exits.**

**2. Overtime is strongly linked to attrition.**
74% of employees who work overtime left (20 of 27), compared with 26% of those who do not (14 of 53). 10 of the 15 "poor work-life balance" exits were overtime employees.

**3. Most people leave early.**
53% of leavers left within their first year and 71% within two years (median tenure of leavers: under 1 year). This points to onboarding and early-engagement gaps.

**4. Some departments are hit harder.**

| Department | Attrition rate |
|---|---|
| Operations | 60% (6 of 10) |
| Sales | 50% (9 of 18) |
| Research & Development | 44% (7 of 16) |
| IT | 39% (7 of 18) |
| Finance | 30% (3 of 10) |
| Human Resources | 25% (2 of 8) |

**5. Younger employees are more likely to leave.**
58% of employees under 25 left (7 of 12), versus 17% in the 45-54 group (1 of 6).

**6. Low satisfaction and low hikes go together with exits.**
Employees with a "Low" satisfaction level had a 55% attrition rate (18 of 33), versus 32% for "Medium". Employees who received a hike under 5% left at 72% (13 of 18) versus 34% for those with 5% or more. Leavers also averaged fewer trainings (2.9 vs 3.4) and a lower last hike (8.1% vs 9.8%).

**7. Qualification and marital status patterns.**
MBA and Master's holders left at 55% each (12 of 22), versus 28% for Bachelor's holders. Divorced employees had the highest rate by marital status (55%, 11 of 20). Gender showed little difference (female 40%, male 45%).

---

## Recommended HR Actions

| Finding | Suggested action |
|---|---|
| Work-life balance and overtime | Review workloads and overtime policy, introduce flexible hours / comp-offs, track overtime hours monthly |
| Early exits | Strengthen onboarding, assign buddies/mentors, run 30-60-90 day check-ins |
| Conflict with manager | Manager-effectiveness training, skip-level meetings, anonymous upward feedback |
| High-attrition departments (Operations, Sales) | Run stay interviews and pulse surveys, review targets and team structure |
| Low satisfaction and low hikes | Regular engagement surveys, transparent hike criteria, recognition for high performers |
| Highly qualified staff leaving | Define career paths and growth opportunities for MBA/Master's hires |

---

## HR Skills Demonstrated

- HR / People Analytics and workforce reporting
- Attrition and retention analysis
- Exit-interview data analysis
- Employee engagement and satisfaction analysis
- Data cleaning, structuring and KPI design
- Translating data into business recommendations

---

## Repository Structure

```
HR-Attrition-Analysis-Dashboard/
├── README.md
├── data/
│   ├── HR_Attrition_Analysis_Dashboard.xlsx   # full interactive workbook
│   └── employee_data.csv                      # raw data (CSV copy)
├── docs/
│   └── data_dictionary.md
└── images/
    └── dashboard_preview.png
```

## How to Use

1. Download `data/HR_Attrition_Analysis_Dashboard.xlsx`.
2. Open it in **Microsoft Excel (2013 or later)**, since slicers need Excel to work.
3. Go to the **DASHBOARD** sheet and use the slicers to filter.
4. Explore `Calculation` for the pivot tables and `Employee_Data` for the source data.

## Limitations & Future Improvements

- Small, synthetic dataset (80 rows), so results are illustrative.
- Correlation does not prove causation; findings should be validated with real exit interviews.
- Next steps: add a Power BI version, build an attrition-risk score, and add cost-of-attrition analysis.

---

## About Me

**[Your Full Name]**, BBA graduate looking for **entry-level HR roles** (HR Executive / HR Generalist / Recruitment / HR Analytics).

- LinkedIn: [your LinkedIn URL]
- Email: [your email]
- GitHub: [@roshniarya938-hash](https://github.com/roshniarya938-hash)

---

*Disclaimer: The dataset is entirely fictional and created for learning and portfolio purposes. It does not represent any real company or individual.*
