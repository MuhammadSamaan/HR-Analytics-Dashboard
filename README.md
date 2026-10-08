# HR Analytics Dashboard — Power BI

A professional, interactive **HR Analytics Dashboard built with Microsoft Power BI** for monitoring workforce structure, employee attrition, compensation, workforce trends, data changes, and HR alerts.

## 📊 Dashboard Overview

The dashboard provides a centralized view of HR analytics through interactive KPI cards, charts, filters, detailed tables, and DAX-driven metrics.

### Main objectives

- Monitor total workforce and employee activity
- Analyze employee attrition and retention
- Understand workforce demographics
- Analyze compensation and income patterns
- Track employee changes
- Identify HR-related alerts and exceptions
- Explore relationships between employee attributes
- Support HR reporting and data-driven decision-making

## 🖥️ Dashboard Pages

### 1. Overview

High-level summary of the organization, including:

- Total Employees
- Active Employees
- Attrition metrics
- Average Age
- Average Tenure
- Average Job Satisfaction
- Department distribution
- Workforce trends
- Income and experience analysis
- HR insights
- Data status/refresh information

### 2. Attrition & Retention Analytics

Focuses on employee turnover and retention.

Key KPIs:

- Attrition
- Attrition Rate
- Active Employees
- Average Tenure
- Average Age

Main analyses:

- Attrition by Department
- Attrition by Job Role
- Attrition by Age Group
- Attrition by Tenure
- Overtime vs Attrition
- Job Satisfaction analysis

### 3. Compensation Analytics

Analyzes employee salary and income patterns.

Key metrics include:

- Median Monthly Income
- Highest Paid Role
- Pay Range
- Average Tenure
- Income vs. Experience
- Compensation by Job Level
- Gender Pay Comparison

### 4. Workforce Analytics

Provides demographic and organizational workforce analysis.

Main areas include:

- Department distribution
- Age group distribution
- Employee demographics
- Workforce composition
- Age-group analysis
- Department-level workforce insights

Age groups used in the dashboard include:

- Under 25
- 25–34
- 35–44
- 45–54
- 55 or Above

### 5. Changes

Provides visibility into changes recorded in the HR data.

Main components include:

- Total Changes
- Change activity
- Change dates
- Change details
- Recent changes
- Change log analysis

### 6. Alerts

Identifies employee records requiring attention based on configurable business rules.

Example conditions include:

- Low Job Satisfaction
- Overtime
- Low Monthly Income
- Salary-related conditions
- Medium / High priority alerts

## 🎨 Design System

The dashboard uses a clean, professional light theme.

Design characteristics:

- Rounded cards
- Clean spacing
- Consistent typography
- Light backgrounds
- Minimal visual clutter
- Interactive filters
- Professional KPI layouts

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop**
- **Power Query**
- **DAX**
- **Microsoft Excel / CSV**
- **Power BI Service**
- **GitHub**

## 📁 Suggested Repository Structure

```text
HR-PowerBI-Dashboard/
│
├── README.md
│
├── PowerBI/
│   └── HR_Analytics_Dashboard.pbix
│
├── Data/
│   └── HR_Data.xlsx
│
├── Screenshots/
│   ├── overview.png
│   ├── attrition.png
│   ├── compensation.png
│   ├── workforce.png
│   ├── changes.png
│   └── alerts.png
│
├── Documentation/
│   └── Dashboard_Documentation.pdf
│
└── LICENSE
```

> **Privacy:** If the source data contains sensitive or personally identifiable employee information, do not publish the raw data publicly. Use anonymized or synthetic data instead.

## 🔄 Data & Refresh Workflow

The dashboard is designed so that the underlying data can be updated and the Power BI report refreshed.

```text
Data Source
    ↓
Excel / CSV / Shared Source
    ↓
Power Query
    ↓
Data Cleaning & Transformation
    ↓
Power BI Data Model
    ↓
DAX Measures
    ↓
Dashboard Visuals
    ↓
Power BI Service
```

For collaborative deployment, a shared **OneDrive or SharePoint** source can be used so authorized users can update the source data and Power BI can refresh the semantic model.

## 🧹 Data Preparation

Power Query is used to prepare the HR dataset before visualization.

Typical preparation steps include:

- Removing unnecessary columns
- Removing duplicate records
- Cleaning column names
- Correcting data types
- Handling missing values
- Creating calculated categories
- Preparing data for the Power BI model

## 📐 DAX & Analytics

The dashboard uses DAX measures and calculated columns for HR analysis.

### Average Tenure

```DAX
Average Tenure =
AVERAGE(Employees[YearsAtCompany])
```

### Age Grouping

```DAX
Age Grouping =
IF(
    Employees[Age] < 25,
    "Under 25",
    IF(
        Employees[Age] < 35,
        "25 - 34",
        IF(
            Employees[Age] < 45,
            "35 - 44",
            IF(
                Employees[Age] < 55,
                "45 - 54",
                "55 or Above"
            )
        )
    )
)
```

### Example Alert Logic

The alert system can use business rules such as:

- Job Satisfaction ≤ 2
- Overtime = Yes
- Monthly Income below a defined threshold

These are configurable examples and should be adjusted to the organization's HR policies.

## 🔍 Interactivity

The dashboard supports Power BI features such as:

- Date filters
- Department filters
- Job Role filters
- Employee-level filtering
- Cross-filtering
- Drill-down
- Tooltips
- Interactive charts
- KPI cards

## 🚀 Publishing & Deployment

### Power BI

Typical workflow:

```text
Power BI Desktop
       ↓
Publish
       ↓
Power BI Service
       ↓
Configure Refresh
       ↓
Share / Embed Report
```

### GitHub

GitHub can host the project documentation, PBIX/project files where appropriate, screenshots, sample data, and supporting resources.

GitHub is the project repository; it does **not** replace Power BI Service as the interactive dashboard hosting platform.

Recommended setup:

```text
GitHub
  ├── README
  ├── PBIX / project files
  ├── screenshots
  ├── documentation
  └── sample/anonymized data

Power BI Service
  └── Published interactive dashboard
```

## 🌐 Live Dashboard

**Power BI Dashboard:**  
`[Add your Power BI report link here]`

**Live Demo / Website:**  
`[Add your deployed website URL here]`

## 📸 Dashboard Preview

After adding screenshots to the `Screenshots` folder, use:

```markdown
## Dashboard Preview

![Overview](Screenshots/overview.png)

![Attrition Analytics](Screenshots/attrition.png)

![Compensation Analytics](Screenshots/compensation.png)

![Workforce Analytics](Screenshots/workforce.png)

![Changes](Screenshots/changes.png)

![Alerts](Screenshots/alerts.png)
```

## 🔐 Data Privacy

For a public GitHub repository:

- Remove employee names
- Remove employee IDs
- Remove email addresses
- Remove phone numbers
- Remove addresses
- Remove confidential salary information where required
- Remove other personally identifiable information
- Use anonymized or synthetic data for demonstrations

Do not publish confidential HR records or proprietary company information without authorization.

## 📌 Important Deployment Note

A `.pbix` file stored on GitHub does not automatically become a publicly interactive Power BI dashboard.

The normal architecture is:

```text
GitHub
   ↓
Project files / Documentation
   ↓
Power BI Service
   ↓
Interactive Report
```

Users who need to **view** the interactive report should receive the appropriate Power BI access or a properly configured public/embed link.

Users who need to **update the data** should normally receive controlled access to the underlying shared data source rather than edit access to the GitHub repository.

## 📈 Future Improvements

Possible future enhancements:

- Automated data refresh
- OneDrive / SharePoint integration
- Automated HR alerts
- Email notifications
- Row-level security
- Role-based access
- Employee drill-through pages
- HR forecasting
- Attrition prediction
- Automated data-quality checks
- Power BI Service deployment
- Web embedding
- Power Automate integration

## 👨‍💻 Project Author

**Muhammad Samaan**

**Power BI • Power Query • DAX • Excel • GitHub**

## 📄 License

Choose a license appropriate for your intended use. For a portfolio project, an MIT License is one common option.

## ⭐ Project

This project demonstrates how Power BI can be used to transform HR data into an interactive analytics solution for workforce monitoring, attrition analysis, compensation analysis, change tracking, and HR alerts.
