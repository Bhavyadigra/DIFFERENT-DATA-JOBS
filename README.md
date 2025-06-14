ABOUT MY PROJECT
The main aim of this project was to analyze real-world salary data for roles like Data Scientist, Machine Learning Engineer, and Data Analyst across various countries, job types, and platforms — to better understand what’s driving salaries in the tech world and help the job seekers to analyse the salaries of different data jobs.The dataset used for this project contains real-world data science job information from 2023
Excel Skills Used
The following Excel skills were utilized for analysis:

📉 Charts
🧮 Formulas and Functions
❎ Data Validation
DASHBOARD BUILD:

CHARTS

🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
📉 Data Organization: Sorted job titles by descending salary for improved readability.
💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

MAP

🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
📊 Data Representation: Plotted median salary for each country with available data.
👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

 
 Formulas and Functions 
 
💰 Median Salary by Job Titles
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)

🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.

📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.

🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types

🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.


Count of Job Schedule Type


=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.

🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.



 Data Validation

🔍 Filtered List
🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
🎯 User input is restricted to predefined, validated schedule types
🚫 Incorrect or inconsistent entries are prevented
👥 Overall usability of the dashboard is enhanced
