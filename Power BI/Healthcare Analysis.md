## Healthcare Performance and Patient Analysis Dashboard
### Project Overview
Healthcare Performance & Patient Analytics Dashboard

This project is an interactive Power BI dashboard designed to evaluate the performance of a healthcare organization operating across multiple Nigerian states. The dashboard provides management with a comprehensive view of financial performance, patient demographics, hospital operations, and patient experience.

The project combines data cleaning and transformation, data modelling, DAX calculations, interactive visualizations, and advanced Power BI features to turn healthcare data into actionable business insights.

The dashboard is designed to answer three key questions:

1. How is the healthcare organization performing?

2. What are patients experiencing?

3. Where are the major areas that require management attention?

The analysis is presented across five interactive dashboard pages:

Executive Overview — Provides a high-level summary of organizational performance.

Patient Analysis — Examines patient demographics, diagnoses, visits, and outcomes.

Hospital Operations — Evaluates departments, branches, waiting times, patient volume, and operational performance.

Financial Performance — Analyzes revenue, costs, profit, margins, targets, and financial performance.

Patient Experience — Evaluates patient satisfaction, waiting times, outcomes, and overall experience.

The dashboard also includes advanced features such as Dynamic RLS, Dynamic Titles, Dynamic Executive Insights, What-if Parameters, Report Tooltips, Drill-through, Navigation, and Mobile Layout.

## Business Problem
Healthcare organizations generate large amounts of patient, operational, and financial data. However, without an integrated analytical solution, management may struggle to identify performance gaps, understand the factors affecting patient experience, and determine where resources and improvement efforts should be prioritized.

This project addresses the need for a centralized healthcare analytics dashboard that transforms raw healthcare data into actionable insights for management and decision-making.

The dashboard is designed to answer key business questions such as:

1. How is the healthcare organization performing overall?
2. What are the major trends in patient visits, revenue, costs, and profitability?
3. Which departments are performing well, and which department has the lowest performance?
4. Which states generate the highest and lowest revenue?
5. Which states generate the highest and lowest profit?
6. Which branches and departments handle the highest patient volumes?
7. Where are patient waiting times highest, and what operational areas may be contributing to delays?
8. Which departments have lower patient satisfaction and require further investigation?
9. What are the most common patient outcomes?
10. What factors may be affecting the overall patient experience?
11. How is revenue performing against the organization's targets?
12. Where is the organization experiencing financial underperformance?
13. Which areas should management focus on to improve operational and financial performance?
14. How can management improve performance in underperforming departments and states?
15. Where should resources, staffing, and operational improvements be prioritized?
16. How can the organization improve patient satisfaction while reducing waiting times?

The ultimate goal of the project is to help management identify underperforming areas, prioritize areas requiring attention, understand the drivers of performance, and make data-driven decisions that improve operational efficiency, financial performance, and patient experience.

## 🛠️ Tools Used

1. Microsoft Excel: Cleaning and Data Preparation.

2. Power BI: Used as the primary business intelligence and visualisation platform to build interactive healthcare performance dashboard. It was used to create the KPI cards, chart, slicers drill through pages, report page tooltips, bookmarks, navigation, dynamic titles and mobile layouts.

3. Power Query:  Used for data cleaning and transformation before the data was loaded into the Power BI data model. Key activities included correcting data types, handling missing or inconsistent values, removing duplicates, transforming columns, and preparing the dataset for analysis.

4. Dax: Used to create calculated measures and analytical logic for the dashboard.

5. Power BI Data Modelling: Used to structure the healthcare data into an analytical model using relationships between tables and a Date Table. The model was designed to support accurate filtering, calculations, and interactive analysis across the dashboard.

6. Row-Level Security (RLS):  Used to implement dynamic state-level access control. Each state manager was assigned a username, email, and state, allowing managers to view only the healthcare data associated with their assigned state.

7. What If Parameters: Used to create a Revenue Target Adjustment parameter that allows management to simulate changes to the revenue target and evaluate the resulting impact on revenue variance and achievement.

8. GitHub: Used to host and document the project, including the project README, cleaned dataset, Power BI report, and supporting project materials.

## 📁 Dataset Description

The dataset contains healthcare and patient-level information from a healthcare organization operating across multiple states and branches in Nigeria. It captures patient visits, demographic information, diagnoses, departments, healthcare outcomes, waiting times, satisfaction levels, and financial performance.

The dataset was used to analyze the organization's overall performance, patient experience, hospital operations, and financial outcomes.

### Key Areas Covered

* **Patient Information:** Patient ID, age, gender, age group, and patient type.
* **Visit Information:** Visit date, number of visits, department, branch, and state.
* **Clinical Information:** Diagnosis, treatment/service information, and patient outcomes.
* **Patient Experience:** Waiting time, satisfaction score, and recovery/outcome status.
* **Financial Information:** Revenue, cost, profit, and revenue targets.
* **Geographical Information:** State and branch locations across Nigeria.

### Key Analytical Questions

The dataset supports analysis of questions such as:

* How many patients and visits does the organization handle?
* Which states and branches have the highest and lowest performance?
* Which departments handle the highest patient volume?
* Which departments have the longest waiting times?
* How satisfied are patients with the services provided?
* What are the most common diagnoses and patient outcomes?
* How are revenue, cost, and profit performing?
* Which states and departments generate the highest and lowest revenue and profit?
* Is the organization meeting its revenue targets?
* Where should management focus to improve operational, financial, and patient-experience performance?

The dataset was cleaned and transformed using Microsoft Excel and Power Query before being used to create the Power BI data model and dashboard.

## Dataset

1. Patient ID
2. Age
3. Gender
4. Visit Date
5. State
6. Branch
7. Department
8. Diagnosis
9. Service
10. Payment Method
11. Outcome
12. Waiting Time
13. Satisfaction Score
14. Revenue
15. Visit Count
16. Insurance Type
17. Cost

## 🧹 Data Cleaning and Transformation 

The raw healthcare dataset was cleaned and transformed using Microsoft Excel and Power Query in Microsoft Power BI to ensure data quality, consistency, and accuracy before analysis.

The following data preparation steps were performed:
* Reviewed the dataset structure to understand the available fields and identify columns required for analysis.
* Corrected data types by assigning appropriate formats to fields such as dates, numerical values, text fields, and financial figures.
* Handled missing and blank values to prevent incomplete records from affecting calculations and visualizations.
* Checked for duplicate records and removed unnecessary duplicates where applicable.
* Standardised categorical values such as states, departments, branches, gender, diagnoses, and patient outcomes to maintain consistency.
* Cleaned text fields by removing unnecessary spaces and correcting inconsistent entries.
* Created and organized analytical fields such as Age Groups and New vs Returning Patient categories where required for analysis.
* Prepared financial fields including Revenue, Cost, Profit, and Revenue Target for accurate financial calculations.
* Created a dedicated Date Table to support monthly analysis and time-intelligence calculations such as MoM and YoY growth %.
* Reviewed the transformed data to ensure that the final dataset was suitable for modelling, DAX calculations, and dashboard visualization.

After the cleaning and transformation process, the prepared data was loaded into Power BI and used to build the analytical data model and interactive dashboard.

## 🗂️ Data Modelling 

A structured data model was created in Power BI to ensure accurate calculations, efficient filtering, and reliable dashboard performance.

The model was organized around the main healthcare data table, supported by a dedicated Date Table and a Managers table used for Row-Level Security (RLS).

### Data Model Structure

* Patient Visit Data – The main fact table containing patient, visit, clinical, operational, geographical, and financial information.
* Date Table – A dedicated calendar table used for date filtering, monthly trends, and time-intelligence calculations such as Month-over-Month and Year-over-Year growth.
* Managers Table – A supporting security table containing manager usernames, email addresses, and assigned states. This table was used to implement dynamic Row-Level Security.

### Relationships
The Date Table was related to the patient_visit data using the relevant date field, allowing date slicers and time based calculations to filter the healthcare records correctly.

The Managers table was connected to the patient_visit data through the State field. This relationship enabled each manager to view only the records associated with their assigned state.

### Data Model Benefits

The model was designed to:

* Maintain a clear separation between transactional healthcare data and supporting dimensions.
* Improve the accuracy of DAX calculations.
* Enable consistent filtering across dashboard pages.
* Support time-intelligence analysis.
* Allow dynamic state-level access through Row-Level Security.
* Provide a reliable foundation for the interactive healthcare dashboard.

## 📊 Key Dax Measures

Some of the key measures created for the dashboard includes: 

Total Patients =
DISTINCTCOUNT('Patients_visit'[Patient_ID])

Total Visits =
COUNTROWS('Healthcare Data')

Total Revenue =
SUM('Healthcare Data'[Revenue])

Total Cost =
SUM('Healthcare Data'[Cost])

Total Profit =
[Total Revenue] - [Total Cost]

Profit Margin % =
DIVIDE([Total Profit], [Total Revenue], 0)

Avg Revenue per Patient =
DIVIDE([Total Revenue], [Total Patients], 0)

Avg Waiting Time =
AVERAGE('Healthcare Data'[Waiting Time])

## Dashboard Pages

The healthcare analytics dashboard consists of five interactive pages, each designed to provide management with a different perspective of organizational performance.

### 1. Executive Overview

Provides a high-level summary of the organization's overall performance.

Key areas analyzed:

* Total patients and visits
* Revenue, cost, and profit
* Average revenue per patient
* Average waiting time
* Patient satisfaction
* Monthly patient trends
* Revenue by state
* Patients by department
* Revenue versus target
* Patient outcomes

Purpose: Give management a quick overview of overall performance and identify areas requiring further investigation.

### 2. Patient Analysis

Focuses on patient demographics, diagnoses, and patient behavior.

Key areas analyzed:

* Age groups
* Gender distribution
* Diagnoses
* Patients by state
* New versus returning patients
* Average visits per patient
* Patient outcomes

Purpose: Understand who the organization's patients are, what conditions they present with, and how patient behavior and outcomes vary.

### 3. Hospital Operations

Analyzes operational efficiency across departments and branches.

Key areas analyzed:

* Visits by department
* Average waiting time
* Waiting time by department
* Patient satisfaction by department
* Patient outcomes
* Branch performance
* Monthly patient volume

Purpose: Identify operational bottlenecks, high-volume departments, long waiting times, and areas where service delivery can be improved.

### 4. Financial Performance

Provides an in-depth view of the organization's financial performance.

Key areas analyzed:

* Revenue
* Cost
* Profit
* Profit margin
* Revenue target
* Revenue variance
* Target achievement
* Revenue by state
* Revenue by department
* Revenue by service
* Profit by department
* Monthly revenue trends

Purpose: Help management understand financial performance, identify profitable areas, investigate underperforming states and departments, and monitor progress toward revenue targets.

### 5. Patient Experience

Focuses on how patients experience the organization's services.

Key areas analyzed:

* Average satisfaction score
* Average waiting time
* Satisfaction by department
* Waiting time by department
* Patient outcomes
* Positive outcome rate
* Department experience performance
* Patient experience insights

Purpose: Identify departments and operational areas affecting patient satisfaction and outcomes and highlight opportunities to improve the overall patient experience.

## 🔍 Key Findings & Insights 

The analysis identified several important findings across patient performance, hospital operations, financial performance, and patient experience.

### Patient Insights

* The dashboard provides a clear view of patient demographics, including age groups and gender distribution.
* Patient volumes vary across departments and states, highlighting differences in healthcare demand.
* The analysis of new and returning patients helps management understand patient retention and service utilization.
* Patient outcomes provide an indication of the effectiveness of healthcare services across different departments and locations.

### Operational Insights
* Some departments experience significantly higher patient volumes than others, creating potential pressure on operational resources.
* Differences in waiting times across departments highlight areas where workflow and staffing may need to be reviewed.
* Department level satisfaction analysis helps identify areas where the patient experience may require improvement.
* Branch performance analysis allows management to identify locations that may require additional operational support.

### Financial Insights
* Revenue and profit performance varies across states and departments.
* Some areas generate strong revenue while others contribute less to overall financial performance.
* Department-level profitability helps management identify the services and departments generating the greatest financial contribution.
* Revenue target analysis highlights whether actual performance is meeting the organization's expected financial goals.
* Revenue variance provides an early indication of areas where corrective financial action may be required.

### Patient Experience Insights
* Waiting time and satisfaction are important indicators of patient experience and service quality.
* Departments with weaker satisfaction or longer waiting times should be investigated to identify operational causes.
* Positive outcome analysis provides an additional measure for evaluating the quality of patient care.
* Comparing departments allows management to identify high-performing areas that can serve as benchmarks for improvement.

### Overall Finding

The dashboard demonstrates that organizational performance cannot be evaluated using revenue alone. A complete assessment requires consideration of patient volume, operational efficiency, financial performance, patient satisfaction, and patient outcomes.

These findings provide management with a data-driven basis for identifying priority areas and making targeted improvements.

## 📌 Management Recommendation

Based on the analysis, the following recommendations can help management improve healthcare performance, financial results, operational efficiency, and patient experience:

### 1. Prioritise Low-Performing States and Departments

Management should identify states and departments with low revenue, low profit, high waiting times, or poor patient satisfaction and develop targeted improvement plans. Resources should be directed toward areas with the greatest performance gaps.

### 2. Reduce Patient Waiting Time

Departments with longer waiting times should be investigated to identify bottlenecks in registration, consultation, laboratory services, pharmacy, and other processes. Better staff scheduling, workflow optimization, and resource allocation can help reduce delays.

### 3. Improve Patient Satisfaction

Management should focus on departments with below-average satisfaction scores by collecting patient feedback, improving service delivery, strengthening staff training, and addressing recurring patient complaints.

### 4. Strengthen High-Volume Departments

Departments handling large numbers of patients should receive adequate staffing, equipment, and operational support to prevent overcrowding and maintain service quality as patient volume increases.

### 5. Improve Financial Performance

Low-revenue and low-profit states, departments, and services should be reviewed to identify the causes of underperformance. Management should evaluate service utilization, operating costs, pricing, and resource allocation to improve profitability.

### 6. Monitor Revenue Targets

Management should regularly monitor Revenue Target, Revenue Variance, and Achievement %. Where revenue falls below target, corrective actions should be introduced early rather than waiting until the end of the reporting period.

### 7. Learn From High-Performing Areas

Best practices from high-performing states, departments, branches, and services should be identified and replicated in weaker areas. This can help improve both operational and financial performance across the organization.

### 8. Strengthen Patient Retention

Management should analyse returning patient patterns and identify factors that encourage patients to return. Improving service quality, satisfaction, waiting times, and patient outcomes can support long term patient retention.

### 9. Focus on Patient Outcomes

Positive and negative patient outcomes should be monitored alongside volume and financial KPIs. Departments with weaker outcomes should be investigated to identify opportunities for improving quality of care.

### 10. Establish Regular Performance Reviews

Management should use the dashboard as a recurring decision support tool rather than a one-time reporting solution. Monthly reviews of revenue, profit, patient volume, waiting time, satisfaction, outcomes, and departmental performance can help management identify problems early and track improvement over time.

### Overall Recommendation

Management should prioritize areas where financial performance, operational efficiency, and patient experience are weakest, while using high-performing areas as benchmarks. This will help the organization allocate resources more effectively, improve patient care, increase operational efficiency, and achieve stronger financial performance.

## 📝 Conclusion

The Healthcare Performance & Patient Analytics Dashboard provides a comprehensive view of the organisation's patient activity, operational performance, financial results, and patient experience across states, departments, branches, and services.

The analysis demonstrates that healthcare performance should not be evaluated using financial metrics alone. Patient volume, waiting time, satisfaction, outcomes, revenue, cost, and profitability must be considered together to understand the organization's overall performance.

Overall, this project transforms healthcare data into an interactive decision support solution that helps management understand what is happening, identify why performance differs across the organisation, and determine where action should be taken to improve operational efficiency, financial performance, and patient outcomes.

## 👨🏽‍💻📊 Author

👨🏽‍💻 Sodiq Olamilekan Jimoh
B.Sc. Political Science (Hons.) | IFEXA Certified Data Analyst  


