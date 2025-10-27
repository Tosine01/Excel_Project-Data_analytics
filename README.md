# Project 2 Analysis  
## Introduction  
While exploring opportunities in data analytics, I realized there wasn’t much clear data showing which skills lead to better pay or which regions offer the most competitive salaries. This project dives into those questions, using real job data to uncover trends that can help others make informed career decisions.

## Question to Analyze  

Key Questions Explored:  

1. Does possessing more skills correlate with higher pay?  
2. How do data job salaries vary across regions?  
3. What are the top skills for data proffessionals?  
4. What's the pay for the top 10 skills?  

## Excel Skills Used  

The following Excel skills were utilized for this analysis:  


- Pivot Tables  
- Pivot Charts  
- DAX(Data Analysis Expressions)  
- Power Query  
- Power Pivot

  ## Data Jobs Dataset
  This project uses a real-world 2023 dataset on data science jobs, sourced from Luke Barousse’s Excel course. It forms the basis for learning and applying Excel data analysis skills. The dataset includes details on:
  
- Job titles
- Salaries
- location
- Skills
  
## 1. Does possessing more skills correlate with higher pay?   
### Skill: Power Query (ETL)
### Extract

- I Started by using Power Query to extract the original data(data_salary_all_xlsx)and create two queries  
     -First the one with all the data jobs information  
     -Second listing with all the skills with each job ID

### Transform  
  Then i transformed each query by changing column types, removing unneccessary columns, cleaning text to eliminate specific words and trimming excess whitespace  

  data_jobs_all  
  ![Applied_steps](https://github.com/user-attachments/assets/01a51682-b6f5-4038-bd05-4a8d534041c7)  

  data_jobs_Skills  
  ![Applied_st](https://github.com/user-attachments/assets/f8e1ab23-a2e3-40e7-9ad3-789fdb4441cf)  
  
Then, i loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis  

data_jobs_all  
![data_jobs_all](https://github.com/user-attachments/assets/906b08e6-aa4c-4be1-8523-c047aae10e10)

data_jobs_skills
![Data_job_skills](https://github.com/user-attachments/assets/61005b17-ac20-484f-9c45-f7959285ecab)  

### Analysis  
 **Insights**  
 - Analysis reveals a clear positive correlation between the number of skills listed in job postings and the median salary offered. Roles such as Senior Data Engineer and Data Scientist tend to require broader skill sets and command higher compensation.  

 - Positions with fewer required skills—like Business Analyst—typically offer lower salaries. This suggests that deeper specialization and technical breadth significantly enhance market value in the tech industry.
   ![Skill_Analysis](https://github.com/user-attachments/assets/c7badb21-2fce-4ee6-a0eb-df2d16529a94)

## 2. How do data job salaries vary across regions?   
### Skills: PivotTables And DAX  
 **Pivot Table**  
-Used Power Pivot to build a Data Model for job data analysis.  
-Added job_title_short to the Rows area and salary_year_avg to the Values area.  
-Created a custom measure to calculate the median salary specifically for jobs based in the United States.  
```=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)
```

**DAX Measure for Median Salary**  
-Defined a simple DAX measure to compute the **overall median** of yearly salaries:  
```Median Salary := MEDIAN(data_jobs_all[salary_year_avg])```  

### Analysis  
  **Global Salary Insights**  
- High-demand roles like Senior Data Engineer and Data Scientist consistently earn top-tier median salaries, both in the United States and internationally—highlighting the worldwide value placed on advanced data expertise.
  
- Notable salary gaps exist between US and non-US tech roles, especially in high-tech positions. This disparity may reflect the concentration of major tech industries and higher compensation standards within the US market.
  ![Region_salary](https://github.com/user-attachments/assets/86c4553f-d04d-40e7-88c0-c1342e599f8c)

  
## 3. What are the top skills for data proffessionals?   
### Skill: Power Pivot  
**Data Modeling with Power Pivot**  

-Built a unified data model by integrating two cleaned tables: data_jobs_all and data_jobs_skills.  
-Leveraged Power Query for preprocessing, which enabled seamless relationship creation in Power Pivot.  
-Established a relationship between the tables using the job_id column to support cross-table analysis.
![Power_Pivot_Tables](https://github.com/user-attachments/assets/72a64c1b-6a66-48cb-872e-c7cd7b5724cb)  

**Power Pivot Menu**  
Power Pivot Menu was used to refine my data model and makes it easy to create measures.  
![PowerPivot](https://github.com/user-attachments/assets/5eccfe4b-90bb-438f-81b0-04941bfc33df)  

**Bar Chart** 
Top Ten Skills  

![Skills](https://github.com/user-attachments/assets/21cddfd1-4134-46ae-b94b-ea8bffe63a9f)


## 4. What's the pay for the top 10 skills?   

### Skill: Advanced Chart(Pivot Chart)  
Created a PivotChart to compare median salary and skill likelihood (%) using dual axes  
- **Primary Axis**: Median Salary displayed as a Clustered Column.
- **Secondary Axis**: Skill Likelihood shown as a Line with Markers (customized to diamond shapes).
  Enhanced chart clarity by adding axis titles and removing unnecessary lines.

  **Insights**
  High-paying roles are strongly associated with technical skills like Python, Oracle, and SQL, underscoring their market value.
  General productivity tools such as PowerPoint and Word correlate with lower salaries and skill relevance, suggesting limited specialization.
  
  ![Top_ten](https://github.com/user-attachments/assets/53b93af2-9dd8-4ba8-ada1-0aa0324d1949)

  ## Conclusion
  This Excel-driven analysis used real-world job posting data to explore the relationship between job titles, locations, salaries, and required skills. By leveraging tools like Power Query, PivotTables, DAX, and custom charts, the project uncovered clear patterns—most notably, that roles demanding multiple technical skills (especially Python, SQL, and cloud technologies) tend to offer significantly higher salaries.
Overall, this project serves as a practical reference for aspiring data professionals, highlighting the skill sets that align with top-paying opportunities in today’s job market.

















  

