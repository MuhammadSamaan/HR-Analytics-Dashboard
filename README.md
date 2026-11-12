<div align="center">

<img src="HR_Dashboard_Complete_Assets/01_Logos/HR_Intelligence_Logo.png" alt="HR Intelligence logo" width="320">

# HR Intelligence: Workforce Analytics Dashboard

**A six-page, interactive Power BI report that turns 1,470 employee records into answers about attrition, pay, workforce makeup, data changes and HR risk.**

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop%20%26%20Service-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-55%2B%20measures-5B3A92?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-7E57C2?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel%20%2F%20CSV-Data-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Made by](https://img.shields.io/badge/Built%20by-Muhammad%20Samaan-8A2BE2?style=for-the-badge)

### [▶ Open the live interactive dashboard](#-live-dashboard)

</div>

---

<img src="New%20folder/HR%20Analytics%201.JPG" alt="HR Intelligence overview page" width="100%">

---

## Why I built this

Most HR reports I came across were either a wall of Excel tabs or a single pretty chart with no story behind it. I wanted something a non-technical HR manager could open and use in under a minute: click a department, see attrition change; flip to pay, see who is under- or over-paid; open the alert page, see exactly which employees need a conversation this week.

So I built the whole thing from scratch: cleaned the data in Power Query, designed the model, wrote the DAX, drew the layout page by page, and wired up navigation, slicers and insight cards so every page talks to the others.

This is a portfolio project and I put a lot of hours into it. If something here is useful to you, I'm happy.

---

## The dashboard at a glance

| | |
|---|---|
| **Employees analysed** | 1,470 across 3 departments and 9 job roles |
| **Employees who left** | 235, an attrition rate of **15.99%** |
| **Total monthly payroll** | about 9.56M |
| **Average / median monthly income** | 6,503 / 4,919 |
| **Pages** | 6, each with its own filters and a navigation sidebar |
| **DAX measures** | 55+ measures plus calculated columns for age group, tenure group, satisfaction label and alert category |
| **Data model** | `Employees` fact table, `Dim Department`, `Dim Job Role`, and a change-log table |

---

## 🔗 Live Dashboard

> **Power BI report:** `[Add your Power BI Service link here]`

If the link asks you to sign in, the report is shared inside a Power BI workspace. The screenshots below show every page, including the filtered states, so you can see how it behaves without access.

---

## Page by page

### 1. Overview
The landing page. Five KPI cards (total employees, leavers, monthly payroll, average job satisfaction, average income), a department slicer, and charts for headcount, satisfaction mix, attrition and income by role. The **HR Insights** box at the bottom rewrites itself as the filter changes.

<table>
<tr>
<td width="50%"><img src="New%20folder/HR%20Analytics%202.JPG" alt="Overview filtered to Human Resources"><br><sub>Filtered to Human Resources</sub></td>
<td width="50%"><img src="New%20folder/HR%20Analytics%203.JPG" alt="Overview filtered to Research and Development"><br><sub>Filtered to Research & Development</sub></td>
</tr>
<tr>
<td width="50%"><img src="New%20folder/HR%20Analytics%204.JPG" alt="Overview filtered to Sales"><br><sub>Filtered to Sales</sub></td>
<td width="50%"></td>
</tr>
</table>

### 2. Attrition & Retention Analytics
Who leaves, and when? KPIs for attrition count, attrition rate, active employees, average tenure and average age of leavers. Breakdowns by department, job role, age group, tenure group, overtime and job satisfaction. Extra slicers for job role, business travel, overtime and gender let you narrow down to very specific groups.

<img src="New%20folder/HR%20Analytics%205.JPG" alt="Attrition and retention analytics" width="100%">

<table>
<tr>
<td width="50%"><img src="New%20folder/HR%20Analytics%206.JPG" alt="Attrition page with gender, travel and overtime filters"><br><sub>Male, Travel_Rarely, no overtime</sub></td>
<td width="50%"><img src="New%20folder/HR%20Analytics%207.JPG" alt="Attrition page filtered to the Sales job role"><br><sub>Sales role, same filters</sub></td>
</tr>
</table>

### 3. Compensation & Pay Analytics
Salary distribution, pay equity and pay patterns. Average, median and total payroll, highest paid role, pay range, income by role and department, years vs income, and a male/female pay comparison with the gap shown as a percentage. Five dropdown filters (job role, department, gender, job level, overtime) work together.

<img src="New%20folder/HR%20Analytics%207_.JPG" alt="Compensation and pay analytics" width="100%">

<table>
<tr>
<td width="50%"><img src="New%20folder/HR%20Analytics%208.JPG" alt="Compensation page filtered to Sales"><br><sub>Sales only</sub></td>
<td width="50%"><img src="New%20folder/HR%20Analytics%209.JPG" alt="Compensation page with five filters applied"><br><sub>Sales, female, job level 5, overtime</sub></td>
</tr>
</table>

### 4. Workforce Analytics
The shape of the organisation: headcount by department, gender split, age-group distribution, employees by job role, and a workforce structure donut. The **Key Insights** strip writes out the largest department, age group and job level, and the gender ratio in plain sentences.

<img src="New%20folder/HR%20Analytics%2010.JPG" alt="Workforce analytics" width="100%">

<img src="New%20folder/HR%20Analytics%2011.JPG" alt="Workforce analytics with six filters applied" width="100%">

### 5. Data Changes & Updates
A change-tracking page: total changes, new employees, removed employees, updated records and status changes, with a recent-changes table, a trend over time, a department split, and a "recent update by field" chart. A ChangeType filter drives the whole page.

> ⚠️ **The change history on this page is synthetic.** The Kaggle employee file is a single snapshot with no history, so I generated a dummy change log tied to real employee numbers and departments to build and test the page. The structure is real and refresh-ready; the events are not real HR events. More in [Data & Credits](#-data--credits).

<img src="New%20folder/HR%20Analytics%2012.JPG" alt="Data changes and updates, all change types" width="100%">

<table>
<tr>
<td width="50%"><img src="New%20folder/HR%20Analytics%2013.JPG" alt="Changes filtered to Update"><br><sub>Update</sub></td>
<td width="50%"><img src="New%20folder/HR%20Analytics%2014.JPG" alt="Changes filtered to Status Change"><br><sub>Status Change</sub></td>
</tr>
<tr>
<td width="50%"><img src="New%20folder/HR%20Analytics%2015.JPG" alt="Changes filtered to Remove"><br><sub>Remove</sub></td>
<td width="50%"><img src="New%20folder/HR%20Analytics%2016.JPG" alt="Changes filtered to New"><br><sub>New</sub></td>
</tr>
</table>

### 6. HR Alert Center
Turns the data into a to-do list. Counters for high-priority, medium-priority, overtime and low-satisfaction alerts, a critical-alerts panel, alerts by department, and a full table of employees who need attention, filterable by department and alert type.

<img src="New%20folder/HR%20Analytics%2017.JPG" alt="HR alert center" width="100%">

<img src="New%20folder/HR%20Analytics%2018.JPG" alt="HR alert center filtered to Sales high priority" width="100%">
<sub>Filtered to Sales and High Priority</sub>

How the alert counters are built (checked against the data):

| Alert | Rule | Count |
|---|---|---|
| Low satisfaction | Job satisfaction of 1 or 2 | 569 |
| Overtime | OverTime = Yes | 416 |
| Medium priority | Low satisfaction **or** overtime | 832 |
| Long tenure | More than 5 years at the company | 694 |
| High salary | Monthly income of 10,000 or more | 281 |

Thresholds are easy to change in the DAX if your organisation draws the lines elsewhere.

---

## What the data says

A few things that stood out once the dashboard was done (all computed from the 1,470-row dataset):

- **Overtime is the loudest signal.** 30.0% of people who work overtime left, against 10.4% of those who don't.
- **Count and rate tell different stories.** Research & Development loses the most people (132), but Sales (20.4%) and Human Resources (19.0%) lose a bigger share of their teams than R&D (13.7%).
- **One role stands out.** Sales Representatives have a 39.8% attrition rate (33 of 83). Research Directors sit at 2.5%.
- **Pay is skewed.** The median monthly income (4,919) sits well below the average (6,503) because a small group of Managers and Research Directors earn 16K to 17K on average.
- **The workforce is young.** 25 to 34 is the largest age group with 554 people, about 37.7% of everyone.
- **On average, women in this dataset earn slightly more than men** (6.69K vs 6.38K), which shows up as a −4.80% gender pay gap on the compensation page.

---

## How it's built

```
Kaggle CSV / Excel files
        ↓
Power Query: remove unused columns, fix data types, clean names, handle blanks
        ↓
Data model: Employees + Dim Department + Dim Job Role + ChangeLog table
        ↓
DAX: measures and calculated columns
        ↓
Six report pages with slicers, navigation, tooltips and insight cards
        ↓
Power BI Service
```

**Calculated columns** I created: `Age Grouping`, `Tenure Group` (with a sort column), `Job Satisfaction Label` (Low / Medium / High / Very High) and `Alert Category`.

**Age grouping**, as an example of the DAX style:

```dax
Age Grouping =
IF(
    Employees[Age] < 25, "Under 25",
    IF(
        Employees[Age] < 35, "25 - 34",
        IF(
            Employees[Age] < 45, "35 - 44",
            IF(
                Employees[Age] < 55, "45 - 54",
                "55 or Above"
            )
        )
    )
)
```

**Measures** are grouped by purpose:

| Area | Examples |
|---|---|
| Headcount | `Total Employees`, `Active Employees`, `Total Department`, `Emp Count by Job Role` |
| Attrition | `Attrition Employees`, `Attrition Rate`, `Attrition Rate by Department`, `Avg Age of Leavers`, `Overtime Employees` |
| Compensation | `Average Monthly Income`, `Median Monthly Income`, `Total Monthly Payroll`, `Pay Range`, `Highest Paid Role`, `Male avg Income`, `Female Avg Income`, `Gender Pay Gap %` |
| Changes | `Total Changes`, `New Employees`, `Removed Employee`, `Updated Records`, `Status Change %`, `Last Updated` |
| Alerts | `High Priority Alert`, `Medium Priority Alerts`, `Overtime Alert`, `Low Satisfaction Alerts`, `High Salary Alert`, `Long Tenure Alerts` |
| Dynamic text | `HR Insights`, `Largest Dept Insights`, `Largest Age Group Insight`, `Gender Ratio Insights`, `Busiest Change Date Insight` |

---

## 📁 Repository structure

```
HR/
│
├── README.md
├── HR Analytics.pbix                          # The Power BI report (6 pages)
│
├── HR-Employee-Attrition.csv                  # Main employee dataset (1,470 rows x 35 columns)
├── HR_ChangeLog_From_Employee_Data.xlsx       # Workbook: Employees_Current + baseline ChangeLog
├── HR_ChangeLog_From_Employee_Data (1).xlsx   # Duplicate copy of the workbook above
├── HR_ChangeLog_Dummy_Data_Matched.xlsx       # Synthetic change events used by the Changes page
├── ChangeLog.xlsx                             # Small early test change log
│
├── New folder/                                # 19 dashboard output screenshots (used in this README)
│   └── HR Analytics 1.JPG ... HR Analytics 18.JPG (plus 7_.JPG)
├── ss img/                                    # 4 small alert-card icons
│
├── HR_Dashboard_Complete_Assets/              # Main design asset pack
│   ├── 01_Logos/
│   ├── 03_Navigation_Icons/
│   ├── 04_KPI_Icons/
│   ├── 05_Analytics_Icons/
│   ├── 06_Change_Tracking_Icons/
│   ├── 07_Alert_Icons/
│   └── 08_UI_Icons/
├── HR_Analytics_Page2_Complete_Assets/        # Attrition page: sidebar, KPI, analytics and insight cards
├── Compensation_KPI_Purple_Icons/             # Compensation page KPI icons
├── Changes_Page_Purple_Assets/Icons/          # Changes page icons
└── HR_Alert_Center_Individual_Separate_Images/# Alert Center KPI and alert icons
```

---

## 📊 Data & Credits

I want to be straightforward about where everything came from.

| What | Source | Notes |
|---|---|---|
| **Employee data** (1,470 rows, 35 columns) | [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) on Kaggle | A fictional dataset published for learning. Used as the base of the whole model. |
| **Additional data** | Kaggle and a few other public sources | I used extra Excel files to widen the data and test the model with more variety. |
| **Change log** | Generated by me | Synthetic events built from real employee numbers and departments in the dataset. Used to build and test the Changes page. They are **not** verified historical changes. |
| **Icons, logos and backgrounds** | AI-generated image assets | Created for this project, organised into the asset folders above and imported into Power BI. |

Every employee record is public or fictional, and names in the change log are placeholders like "Employee 1469". No real personal or confidential HR data is in this repository.

---

## ✋ Disclaimer

This project is **entirely my own work**. I designed the data model, wrote every DAX measure, built every page and interaction, and did the analysis myself, without a team, a mentor or anyone else's help. The only outside ingredients are the public datasets and AI-generated icon graphics credited above.

The numbers and insights describe a fictional dataset. They do not describe any real company, and they should not be used for real HR decisions without your own data and policies.

---

## 🚀 Run it yourself

1. Download or clone this repository.
2. Open `HR Analytics.pbix` in **Power BI Desktop** (Windows).
3. If Power BI shows a data source error, go to **Transform data → Data source settings** and point each source to the matching file in your local copy.
4. Click **Refresh**, then explore the pages.

To publish: **Power BI Desktop → Publish → Power BI Service → configure refresh → share**.

> A `.pbix` file on GitHub is a project file. It does not turn GitHub into a live dashboard host, which is why the interactive version lives in Power BI Service (see the link at the top).

---

## 🔮 What I'd add next

- Automatic refresh from a shared OneDrive or SharePoint source
- Row-level security so each manager sees only their own team
- Drill-through page for individual employees
- Attrition prediction and HR forecasting
- Email alerts through Power Automate

---

## 👨‍💻 About me

**Muhammad Samaan**, Computer Science graduate from Iqra University, Karachi, working towards entry-level roles in Data Analytics / BI and Full-Stack development.

Power BI · Power Query · DAX · Excel · GitHub

[![GitHub](https://img.shields.io/badge/GitHub-MuhammadSamaan-181717?style=flat-square&logo=github)](https://github.com/MuhammadSamaan)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-muhammad--samaan-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/muhammad-samaan)

If you like the project, a ⭐ on the repo means a lot, and I'm always happy to hear feedback.
