# Introduction
Dive into the data job market! Focusing on the data analyst roles, this project explores top-paying jobs, in-demand skills, and where high demands meet high salary in data analytics. 

SQL queries? Check them out here: [project_sql folder](/project_sql/)
# Background
Driven by a quest to navigate the data analyst jov market more effeciently, this project was born from a desire to pinpoint top-paid and in-demand skills, streamlining others work to find optimal jobs.

Data hails from (https://lukebarousse.com/sql). It's packed with insights on job titles, salaries, locations, and essential skills. 

### The questions I wanted to answer through my SQL queries were:
1. What are the top-paying data analyst jobs?
2. What skills are requried for these top-paying jobs?
3. What skills are most in demand for data analysts?
4. What skils are associated with higher salaries?
5. What are the most optimal skills to learn? 

# Tools I used
For my deep dive into the data analyst job market, I harnessed the power of a several key tools:

- **SQL:** The backbone of my analysis, allowing me to query the database and unearth critical insights. 
- **PostgreSQL:** The chosen database management system, ideal for handling the job posting data.
- **Visual Studio Code:** My go-to for database management and executing SQL queries.
- **Git and GitHub:** Essential for version control and sharing my SQL scripts and analysis, ensuring collaboration and project tracking

# The Analysis 
Each query for this project aimed at investigating specific aspects of the data analyst job market. Here's how I approached each question:

### 1. Top paying Data Analyst Jobs 
To idenitfy the highest-paying roles, I filtered data analyst positions by average yearly salary and location, focusing on remote jobs. This query highlights the high paying oppurtunities in the field. 

```sql
SELECT
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name AS company_name
FROM   
    job_postings_fact
LEFT JOIN company_dim on job_postings_fact.company_id = company_dim.company_id
WHERE  
    job_title_short = 'Data Analyst' AND
    job_location = 'Anywhere' AND
    salary_year_avg IS NOT NULL
ORDER BY
    salary_year_avg DESC
LIMIT 10
```
# What I Learned 

Throughout this adventure, I've turbocharged my SQL toolkit with some serious firepower:

- **Complex Query Crafting:** Mastered the art of advanced SQL, merging tables like a pro and wielding WITH clauses for ninja-level temp table maneuvers.
- **Data Aggregation:** Got cozy with GROUP BY and turned aggregate functions like COUNT () and AVG () into my data-summarizing sidekicks.
- **Analytical Wizardly:** Leveled up my real-world puzzle solving skills, turning questions into actionable, insightful SQL queries. 

# Conclusions 

### Insights 



### Closing Thoughts 

This project enhanced my SQL skills and provided valuable insights into the data analyst job market. The findings from the analysis serve as a guide to a prioritizing skill development and job search efforts. Aspiring data analysts can better position themselves in a competitive job market by focusing on high-demand. high-salary skills. This exploration highlights the importance of continious learning and adapatation to emerging trends in the field of data analytics. 