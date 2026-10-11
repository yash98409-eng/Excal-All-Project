# NDRI HR Analytics: Attendance & Payroll Analysis

### Workforce Analytics \| Attendance Monitoring \| Shift Analysis \| Overtime & Payroll

**Portfolio Project by Yash Rana**\
**Tools:** Microsoft Excel • Pivot Tables • HR KPI Analysis\
**Dataset:** 5,000 attendance/payroll records\
**Period covered:** 1 January 2025 -- 30 September 2026

------------------------------------------------------------------------

## 1. Project Overview

This project analyzes an attendance and payroll dataset designed around
an NDRI-style workforce environment. It explores employee attendance,
shift patterns, overtime hours, overtime pay, department-level workforce
distribution, and attendance-linked pay.

The Excel workbook contains a 5,000-row `NDRI_Data` table, an
`Employee_Master` table, and analysis sheets for attendance trends,
shift-wise attendance, overtime/pay by department, top overtime
employees, recent attendance/pay summaries, department headcount, and a
summary of key metrics.

The purpose is to turn attendance and payroll records into a clearer
operational view for HR and workforce planning---not simply to display
numbers, but to highlight where managers may need to investigate
attendance patterns, overtime concentration, and payroll distribution.

> **Data transparency:** This is a portfolio analysis of the supplied
> workbook. The figures below describe this dataset and should not be
> interpreted as verified official NDRI workforce statistics. Do not
> publish identifiable employee information or confidential records.

------------------------------------------------------------------------

## 2. Business Problem

When attendance, shifts, overtime, and payroll are tracked across large
spreadsheets, HR teams may find it difficult to answer operational
questions quickly and consistently.

This project focuses on five business challenges:

-   **Attendance visibility:** How many records are marked present,
    absent, on leave, or on holiday?
-   **Shift monitoring:** How do attendance statuses differ across day,
    evening, and night shifts?
-   **Overtime monitoring:** Which departments and periods account for
    the highest recorded overtime?
-   **Payroll visibility:** How much pay is attributed to attendance and
    overtime in the dataset?
-   **Workforce reporting:** How can employee and department information
    be summarized into a repeatable reporting view?

### Main business question

**How can attendance and payroll data help HR monitor workforce
availability, understand overtime patterns, and make better-informed
staffing and payroll decisions?**

------------------------------------------------------------------------

## 3. Dataset at a Glance

The workbook includes the following principal tables and fields.

### `NDRI_Data` --- 5,000 records, 19 columns

  Field                        Purpose
  ---------------------------- ----------------------------------------------
  `Attendance_ID`              Attendance record identifier
  `Employee_ID`                Employee key
  `Employee_Name`              Employee name; treat as personal information
  `Department`                 Department associated with the record
  `Designation`                Employee designation
  `Date`, `Month`, `Weekday`   Time-based analysis
  `Shift`                      Day, Evening, or Night
  `In_Time`, `Out_Time`        Recorded shift times
  `Total_Hours`                Recorded hours for the attendance row
  `OT_Hours`                   Recorded overtime hours
  `Attendance`                 Present, Absent, Leave, or Holiday
  `Basic_Salary`               Salary field in the dataset
  `OT_Rate_Per_Hour`           Overtime rate used in the calculation
  `OT_Pay`                     Overtime pay
  `Attendance_Pay`             Attendance-linked pay amount
  `Total_Pay`                  Attendance pay plus overtime pay

### `Employee_Master`

Contains employee-level reference fields, including employee ID, name,
department, designation, and basic salary.

### Analysis sheets

The workbook includes sheets for attendance trends, shift-wise
attendance, salary/overtime analysis, top overtime employees, recent
attendance/pay summaries, department and employee counts, and a summary
table.

------------------------------------------------------------------------

## 4. Key Findings from the Supplied Dataset

The following figures were calculated directly from `NDRI_Data`.

  Metric                                              Result
  ----------------------------------------- ----------------
  Total attendance records                             5,000
  Unique employee IDs in attendance data                 996
  Departments represented                                 10
  Present records                             4,136 (82.72%)
  Absent records                                 368 (7.36%)
  Leave records                                  347 (6.94%)
  Holiday records                                149 (2.98%)
  Total recorded overtime                        5,613 hours
  Records with overtime greater than zero     2,699 (53.98%)
  Total overtime pay                              ₹32,83,605
  Attendance-linked pay                        ₹32,18,769.23
  Total recorded pay                           ₹65,02,368.90
  Exact duplicate rows                                     0
  Duplicate `Attendance_ID` values                         0

**How to interpret attendance:** 82.72% is the share of all rows marked
`Present`. It is not necessarily a formal attendance rate against
scheduled employee-days, because the workbook also includes leave and
holiday records and does not establish a complete shift schedule for
every employee-day.

**How to interpret pay:** These amounts are sums of the values recorded
in the supplied dataset. They are not necessarily monthly payroll totals
or the organization's total payroll.

------------------------------------------------------------------------

## 5. Analysis Highlights

### A. Attendance status

Of the 5,000 rows, 4,136 are marked Present, 368 Absent, 347 Leave, and
149 Holiday. This gives HR a first-level breakdown of attendance status.

**Business use:** Review absence patterns by date, department, and shift
before deciding whether staffing or scheduling changes are needed. Leave
and holiday records should not automatically be treated as unplanned
absence.

### B. Shift-wise attendance

The dataset contains:

  Shift       Records   Present   Absent   Leave   Holiday
  --------- --------- --------- -------- ------- ---------
  Day           1,748     1,449      122     122        55
  Evening       1,265     1,058       90      86        31
  Night         1,987     1,629      156     139        63

The Night shift has the highest number of records and the highest raw
counts of absent and leave records. Since it also has the most records
overall, raw counts alone do not establish that it has the worst
attendance rate. Compare rates using scheduled employee-days for a
fairer shift-level comparison.

### C. Department-wise overtime

The departments with the highest total recorded overtime are:

  Department          Overtime hours   Overtime pay
  ----------------- ---------------- --------------
  Maintenance                    631      ₹3,69,135
  Quality Control                629      ₹3,67,965
  Research                       628      ₹3,67,380
  Administration                 611      ₹3,57,435
  Stores                         581      ₹3,39,885

**Business interpretation:** Maintenance, Quality Control, and Research
are useful starting points for investigating overtime demand. These
figures do not, by themselves, prove understaffing or inefficiency. They
should be compared with workload, headcount, shift schedules, and
operational requirements.

### D. Monthly overtime trend

The highest monthly overtime totals in the supplied records are:

  Month            Overtime hours
  -------------- ----------------
  April 2026                  335
  August 2026                 324
  August 2025                 303
  January 2025                300
  March 2025                  287

April 2026 has the highest recorded overtime total at 335 hours. This is
a useful point for further investigation, but the data alone does not
establish why overtime was higher that month.

### E. Overtime and payroll calculations

The dataset records 5,613 overtime hours and ₹32,83,605 in overtime pay.
The overtime pay calculation is internally consistent with
`OT_Hours × OT_Rate_Per_Hour` across the supplied rows.

**Business use:** Monitor overtime costs over time and compare them with
staffing and workload data before recommending changes.

------------------------------------------------------------------------

## 6. HR KPIs and Definitions

  KPI                        Definition
  -------------------------- ---------------------------------------------
  Total Attendance Records   Count of attendance rows
  Unique Employees           Distinct count of `Employee_ID`
  Present Records %          Present rows ÷ all attendance rows × 100
  Absence Records %          Absent rows ÷ all attendance rows × 100
  Total Overtime Hours       Sum of `OT_Hours`
  Overtime Pay               Sum of `OT_Pay`
  Attendance-linked Pay      Sum of `Attendance_Pay`
  Total Recorded Pay         Sum of `Total_Pay`
  Department Overtime        Sum of overtime hours grouped by department
  Shift Attendance           Attendance status counts grouped by shift

For an official attendance-rate KPI, use **present scheduled
employee-days ÷ total scheduled employee-days** and define how approved
leave, holidays, and rest days are handled. Do not use present rows
divided by all rows as a substitute without explaining the limitation.

------------------------------------------------------------------------

## 7. Data Quality Checks and Limitations

A credible analysis also documents what should be validated.

-   **Duplicate check:** No exact duplicate rows and no duplicate
    `Attendance_ID` values were found in the 5,000-row data table.
-   **Missing shift end times:** `Out_Time` is blank for all 864 rows
    marked Absent, Leave, or Holiday. This appears consistent with
    non-present statuses in this dataset, but should still be confirmed
    against the intended business rules.
-   **Summary completeness:** The workbook's existing Summary sheet
    lists total records, unique employees, present records, and absent
    records, but does not show Leave and Holiday counts. Include all
    four attendance statuses in a complete summary.
-   **Attendance trend aggregation:** The existing `ATTENDENCE TREND`
    sheet labels its measure as a sum of `Attendance_ID`. IDs should not
    be summed to measure attendance. Use a record count or distinct
    count, grouped by date/year and attendance status.
-   **Period coverage:** The data spans 1 January 2025 to 30 September
    2026; comparisons should account for the incomplete 2026 calendar
    year.
-   **Data scope:** The 996 unique employees are IDs present in the
    attendance records. The employee master contains 1,000 rows, so the
    difference should be reconciled before treating either count as the
    official headcount.
-   **Privacy:** Employee names and IDs should be removed, masked, or
    replaced with synthetic values before publishing the raw workbook or
    screenshots publicly.

------------------------------------------------------------------------

## 8. Business Recommendations

Based on the patterns observed, the next steps are:

1.  **Review overtime hotspots:** Start with Maintenance, Quality
    Control, and Research; compare overtime with workload, staffing, and
    shift requirements.
2.  **Investigate April 2026:** Check whether higher overtime was linked
    to workload, staffing availability, maintenance activity, or another
    operational factor.
3.  **Compare shifts fairly:** Calculate absence and presence rates
    using scheduled employee-days instead of comparing raw counts only.
4.  **Improve reporting consistency:** Use correct record-count measures
    for attendance trends and include Present, Absent, Leave, and
    Holiday in summary reporting.
5.  **Validate payroll rules:** Confirm the definitions of attendance
    pay, overtime eligibility, applicable rates, and reporting periods
    with authorized HR/payroll owners.
6.  **Track outcomes:** If a change is introduced, compare overtime
    hours, overtime pay, coverage, and reporting time against a
    documented baseline.

These recommendations identify areas for investigation; the dataset does
not prove that any specific intervention has already improved
attendance, saved money, or increased productivity.

------------------------------------------------------------------------

## 9. Project Workflow

1.  **Inspect:** Review the data schema, date coverage, attendance
    categories, and employee keys.
2.  **Validate:** Check missing values, duplicates, pay calculations,
    and summary-table consistency.
3.  **Analyze:** Aggregate attendance, shift, department, and monthly
    overtime metrics.
4.  **Visualize:** Present the metrics in Excel PivotTables or a Power
    BI dashboard.
5.  **Recommend:** Translate validated patterns into questions and
    actions for HR management.
6.  **Measure:** Track results against a baseline before claiming
    business impact.

------------------------------------------------------------------------

## 10. Project Structure

The supplied artifact is an Excel workbook. A repository can be
organized as follows once the corresponding files are added:

``` text
NDRI-HR-Analytics/
├── data/
│   └── NDRI_Attendance_Payroll_5000_Rows.xlsx
├── analysis/
│   └── hr_analysis_notes.md
├── dashboard/
│   └── hr_dashboard.csv
├── screenshots/
│   └── hr_dashboard_preview.png
└── README.md
```

Only include files that actually exist in the repository. Add the Power
BI file and screenshots only if you have created them. Do not upload
confidential employee-level data to a public repository.

------------------------------------------------------------------------

## 11. Skills Demonstrated

-   Excel data exploration and PivotTable-based reporting
-   HR attendance and payroll analysis
-   KPI definition and metric validation
-   Shift-wise and department-wise comparisons
-   Overtime cost analysis
-   Data quality checking
-   Business interpretation and recommendation writing
-   Responsible handling of employee information

------------------------------------------------------------------------

## 12. About the Analyst

**Yash Rana --- Aspiring Data Analyst**

I am building practical skills in data analytics and business
intelligence, with a focus on using structured data to identify
patterns, validate metrics, and communicate actionable recommendations.

**My approach:** Understand the business question → validate the data →
analyze the pattern → communicate the insight → recommend an action →
measure the result.

------------------------------------------------------------------------

## Final Takeaway

This project shows how workforce attendance and payroll data can be
organized into meaningful HR indicators. The strongest analysis goes
beyond reporting totals: it validates the metrics, distinguishes raw
counts from fair comparisons, identifies overtime patterns worth
investigating, and clearly separates measured findings from
recommendations.
