# Excel-All-Project
# 🏢 NDRI HR Analytics Dashboard
### Workforce Intelligence | Attendance | Overtime | Payroll | Employee Performance

**An End-to-End HR Analytics Project using Python, SQL, Excel & Power BI**

---

## 📌 Project Overview

Human Resource Management is not just about maintaining employee records. It is about understanding workforce availability, attendance patterns, overtime requirements, payroll distribution, and operational efficiency.

This project focuses on building an interactive **HR Analytics Dashboard for an NDRI-inspired workforce environment**, helping HR teams and management monitor employee-related KPIs, identify workforce patterns, and make data-driven operational decisions.

The dashboard transforms HR data into actionable insights through data cleaning, analytical queries, KPI development, and interactive visualizations.

> **Project Mission:** Turn workforce data into meaningful insights that support better staffing decisions, attendance monitoring, overtime analysis, and payroll visibility.

---

## 🎯 Business Problem

Managing a large workforce can become challenging when employee, attendance, overtime, and payroll information is spread across multiple spreadsheets or reports.

Without a centralized analytical view, HR teams may face several problems:

- **Attendance visibility:** Difficulty identifying attendance trends and absence patterns.
- **Overtime monitoring:** Limited visibility into departments or shifts with higher overtime hours.
- **Payroll transparency:** Challenges in comparing salary distribution and overtime-related costs.
- **Workforce planning:** Difficulty understanding employee availability across departments and shifts.
- **Operational efficiency:** Time-consuming manual reporting and limited access to consolidated HR KPIs.

### Key Business Question

**How can HR analytics help management monitor workforce availability, understand overtime patterns, improve attendance visibility, and make more informed staffing and payroll decisions?**

*Scope note: This is an analytics portfolio project inspired by an NDRI-style workforce environment. It does not imply access to official NDRI employee records or endorsement by NDRI.*

---

## 🛠️ Tools & Technologies

| Technology | Application |
|---|---|
| Python | Data cleaning and exploratory data analysis |
| Pandas & NumPy | Data transformation and calculations |
| SQL | Workforce queries, aggregations, and comparisons |
| Power BI | Interactive HR dashboard |
| DAX | HR KPI calculations and analytical measures |
| Excel | Data inspection and preliminary reporting |

---

## 📊 Dashboard Features

### 1. Workforce Overview
- Total Employees
- Present Employees
- Absent Employees
- Attendance Percentage
- Total Overtime Hours
- Total Salary / Payroll

### 2. Attendance Analytics
- Daily and monthly attendance trends
- Present versus absent employee comparisons
- Department-wise attendance patterns
- Attendance percentage by shift, where shift data is available

### 3. Overtime Analytics
- Total overtime hours
- Department-wise overtime comparison
- Employee-level overtime distribution
- Identification of recurring high-overtime patterns

### 4. Payroll Analytics
- Total payroll expenditure
- Average salary per employee
- Department-wise salary distribution
- Overtime cost analysis, where reliable overtime payment data is available

### 5. Department & Workforce Analysis
- Employee distribution by department
- Workforce composition
- Department-level attendance and overtime comparisons
- Filters for department, date, shift, and employee category, depending on available fields

---

## 🔍 Analytical Methodology

### Step 1 — Data Cleaning with Python

- Inspected data structure and column types.
- Checked missing values and duplicate records.
- Standardized relevant dates, employee identifiers, and categorical values.
- Validated attendance and overtime records.
- Prepared consistent data for further analysis.

### Step 2 — SQL-Based HR Analysis

Used SQL aggregations, filtering, joins, conditional logic, and window functions where appropriate to analyze:

- Department-wise employee counts
- Attendance and absence patterns
- Overtime distribution
- Payroll comparisons
- Employee and department-level rankings

### Step 3 — KPI Development in Power BI

Created analytical measures and interactive visualizations to consolidate important workforce indicators into a single reporting experience.

### Step 4 — Business Interpretation

Connected dashboard metrics to practical HR questions, such as where staffing review may be needed, which departments show higher overtime, and how attendance patterns vary over time.

---

## 💡 Business Questions This Project Answers

1. How many employees are recorded in the workforce dataset?
2. What percentage of scheduled employee-days are marked present?
3. Which departments have higher recorded absence rates?
4. Which departments or shifts record the most overtime?
5. How is payroll distributed across departments?
6. Are there recurring overtime patterns that deserve further investigation?
7. Which workforce indicators should HR monitor regularly?
8. How can centralized reporting reduce dependence on manual spreadsheet reviews?

---

## 📈 Business Impact & Recommendations

The following are potential outcomes the analysis is designed to support. They are not claims of measured improvements.

| HR Finding to Investigate | Potential Business Value | Recommended Action |
|---|---|---|
| Repeated absence patterns in a department | Better visibility into staffing gaps | Review scheduling, leave patterns, and coverage requirements |
| Consistently high overtime in a shift | Earlier identification of workload pressure | Evaluate staffing levels and shift allocation |
| Significant differences in departmental payroll | Improved payroll cost visibility | Compare headcount, salary structure, and overtime costs |
| Attendance information spread across reports | Faster access to workforce KPIs | Centralize reporting in Power BI |
| Recurring overtime across particular periods | Better understanding of operational demand | Compare overtime trends with workload and staffing data |

### Expected Business Benefits

- Improved visibility into workforce attendance.
- More structured overtime monitoring.
- Better-informed staffing and shift-planning discussions.
- Clearer payroll and departmental cost reporting.
- Reduced manual effort in recurring HR reporting, if the dashboard replaces existing manual processes.
- More consistent, evidence-based workforce decisions.

**Impact measurement:** Any claimed improvement in reporting time, overtime cost, or attendance should be measured against a documented baseline before and after implementation.

---

## 📐 Important HR KPI Definitions

| KPI | Calculation |
|---|---|
| Total Employees | Distinct count of employee IDs |
| Present Employee-Days | Count of valid present employee-day records |
| Absent Employee-Days | Count of valid absent employee-day records |
| Attendance Rate | Present scheduled employee-days ÷ Total scheduled employee-days × 100 |
| Total Overtime Hours | Sum of valid overtime hours |
| Average Salary | Total salary ÷ Number of employees in the relevant payroll population |
| Overtime Cost | Overtime hours × applicable hourly overtime rate, if the rate is available |


*Update the filenames to match the files actually included in your repository. Never upload confidential employee information.*

---

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Install Python and the required libraries.
3. Open the notebook to review data cleaning and exploratory analysis.
4. Run the SQL queries against the appropriately configured database.
5. Open the Power BI `.pbix` file in Power BI Desktop.
6. Explore the dashboard using the available filters and review the business insights.

Install the Python dependencies:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## 🔐 Data Privacy & Responsible Analytics

Employee data is sensitive. This project should use synthetic, anonymized, or properly authorized data.

- Do not publish employee names, IDs, phone numbers, salaries, or attendance records that could identify real individuals.
- Use aggregated metrics for public dashboard screenshots.
- Apply appropriate access controls to confidential HR data.
- Treat overtime and absence indicators as signals for investigation, not proof of poor employee performance.

---

## 🧠 Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- SQL querying and aggregation
- HR KPI development
- Power BI dashboard design
- DAX calculations
- Workforce and overtime analysis
- Business problem-solving
- Insight communication and data storytelling

---

## 👨‍💻 About the Analyst

**Yash Rana | Aspiring Data Analyst**

Developing practical skills in Python, SQL, Excel, and Power BI to transform raw data into meaningful insights and business recommendations.

This project demonstrates my approach to analytics:

**Understand the business problem → Prepare reliable data → Analyze workforce patterns → Visualize KPIs → Recommend actions → Measure outcomes.**


