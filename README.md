# Excel_Projects_Data_Analytics
Projects demonstrating my Excel skills 

## Salary Dashboard [check it here](1_Project_GK_Jobs_Around_The_World.xlsx)
## Excel Skills Applied  
- Charts and data visualization  
- Formulas and functions (including array formulas)  
- Data validation for cleaner user interaction


=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*  
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)


=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

---

## Dataset  
The dataset focuses on jobs in data science and related fields. It includes:  
- Job titles  
- Annual salaries  
- Countries and locations  
- Key skills  


<img width="1577" height="857" alt="project 1" src="https://github.com/user-attachments/assets/fbc6fcdd-4e42-4278-8a55-2c1c09897cb0" />

## Salary Analysis [check it here](2_Project_Jobs_Power_Pivot_Query_DAX.xlsx)

To better understand the data science job market, I focused on a few key questions:  

- Do professionals with more skills earn higher salaries?  
- How do salaries compare across different regions?  
- Which skills are most in demand for data professionals?  
- What are the salary levels for the top 10 skills?  

---

## Excel Skills Used  

To answer these questions, I made use of several advanced Excel features:  

- PivotTables  
- PivotCharts  
- DAX (Data Analysis Expressions)  
- Power Query  
- Power Pivot  

---

## PivotTables & DAX  

### PivotTable  
I built a PivotTable using a Data Model created in Power Pivot.  
- `job_title_short` was placed in the rows area.  
- `salary_year_avg` was added into the values area.  

To refine the analysis, I created a new measure that calculates the **median salary for jobs in the United States**:  

dax
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)


<img width="1450" height="836" alt="Project 2 e" src="https://github.com/user-attachments/assets/c7173e90-a042-445b-8917-bc1ec57b2423" />
<img width="1420" height="861" alt="Project 2 d" src="https://github.com/user-attachments/assets/484228e2-38c0-4942-a136-b606341372b0" />
<img width="1214" height="859" alt="project 2 c" src="https://github.com/user-attachments/assets/599c831d-24ab-494c-aee4-5a7e357c69c6" />
<img width="1547" height="865" alt="project 2 b" src="https://github.com/user-attachments/assets/dedc5666-7df1-435a-aaa2-b1c848d752e5" />
<img width="1329" height="854" alt="project 2 a" src="https://github.com/user-attachments/assets/c9e5d729-c891-40c6-890f-b06124337544" />
