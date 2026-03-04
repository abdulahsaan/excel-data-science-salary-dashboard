# Excel-Data-Science-Salary-Dashboard
![Data-Science-Salary](https://github.com/user-attachments/assets/5c12c123-536b-47d1-be93-891039275aea)

## Introduction

This Data Science Salary Dashboard was developed to help job seekers explore salary trends across roles, locations, and employment types, enabling informed career decisions and fair compensation insights.

The dataset provides a strong foundation for analytical exploration in Excel, featuring detailed information on job titles, salaries, geographic distribution, and key job attributes presented through an interactive dashboard.

### Dashboard File
 Final interactive Excel dashboard with visualizations and KPI metrics. [Data_Science_Salary_Dashboard.xlsx](Data_Science_Salary_Dashboard.xlsx).   

Raw dataset used for data cleaning, transformation, and analysis. [ds_salaries_raw.xlsx](ds_salaries_raw.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains over 32,000 rows of real-world data science job information from 2023, serving as a practical foundation for performing data analysis in Excel.

It includes structured details such as job titles, salary figures, locations, employment types, and job platforms, enabling comprehensive exploration and visualization.

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/a5a56321-9d3c-47bd-bc86-ce8bedeb2134" />

- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![map](https://github.com/user-attachments/assets/e9e2e928-802b-4d40-ba71-366d650e6e10)

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/c2e77ab9-a950-400d-a38d-7c076c23eb6c" />

📉 Dashboard Implementation

<img width="400" height="500" alt="salry_dashboard_ttle" src="https://github.com/user-attachments/assets/2d69e621-e131-46be-8110-8e6b482c7ec3" />

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

<img width="195" height="119" alt="scheduale_sprted2" src="https://github.com/user-attachments/assets/1d02335a-95b6-45b7-83d1-0dd0c7dc698c" />

📉 Dashboard Implementation:

<img width="400" height="500" alt="last one" src="https://github.com/user-attachments/assets/f7fd3170-757d-4602-8f2a-8f586bb105d2" />

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced
    - 
![super_last](https://github.com/user-attachments/assets/6af2e950-11c4-4eb0-94a7-4c46a1749c30)

## Conclusion

This dashboard was developed to present clear insights into salary trends across various data-related roles. Built using structured job market data, it enables users to explore how factors such as location and employment type influence compensation. The project highlights practical data analysis and dashboard development skills in Excel.
