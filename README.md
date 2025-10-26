# Excel_Project-Data_analytics
This Data Jobs Salary Dashboard was built to help job seekers explore salary trends across different roles and ensure they are fairly compensated for their skills and experience.  
![Salary_Dashboard](https://github.com/user-attachments/assets/ed7a22d4-708f-4143-8df9-7564ea5dfea4)  
My final dashboard file [Check out my work here](Salary_Dashboard-1)  

## Excel Skill Used  
The following Excel skills were utilized for this analysis:  
-Charts  
-Formulas and Functions  
-Data Validations

## Data Jobs Dataset  
This project uses a real-world 2023 dataset on data science jobs, sourced from Luke Barousse’s Excel course. It forms the basis for learning and applying Excel data analysis skills. The dataset includes details on:  
-Job titles  
-Salaries  
-location  
-Skills  

## Dashboard build  

### Charts 
Data Science Job Salary - Bar Chart  
![Job_Median_Salary](https://github.com/user-attachments/assets/55de709c-b298-4090-83ad-d428762aa209)  
**Excel Features**: Used bar charts with formatted salary values and an optimized layout to enhance clarity.  
**Design Choice**: Horizontal bar chart for visual comparison of median salaries.  
**Data Organizationa**: Sorted job titles by descending salary for improved readability.  
**Insights Gained**: The visualization highlights clear salary trends — senior and engineering roles generally offer higher pay compared to analyst positions.  

**Country Median Salaries - Map Chart**  
![Map](https://github.com/user-attachments/assets/fb6c23fa-8474-4ddf-8c46-7db14e18b3fe)  
**Excel Features**: Leveraged Excel’s map chart to visualize median salaries across countries.  
**Design Choice**: Applied color-coding to distinguish salary variations between different regions.  
**Data Representation**: Displayed median salary values for each country with available data.  
**Visual Enhancement**: Improved readability and supported quick understanding of global salary distribution patterns.  
**Insights Gained**: Offered an at-a-glance view of worldwide salary disparities, highlighting regions with notably higher or lower pay levels.  

## Formulas and Functions  

**Median Salary By Job Title**  

```=MEDIAN(
IF(jobs[job_title_short]=A2)*
  (jobs[job_country]=country)*
  (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
  (jobs[salary_year_avg]<>0).
  (jobs[salary_year_avg])
)
)
```
**Multi-Criteria Filtering** : Applies filters across job title, country, and schedule type, while excluding blank salary entries.
**Array Formula**: Employs the MEDIAN() function combined with nested IF() logic to calculate results dynamically within an array.
**Tailored Insights**: Delivers precise salary metrics segmented by job title, location, and work schedule type.
**Formula Purpose**: Automatically populates the summary table, returning the median salary for each combination of job title, country, and schedule type.



