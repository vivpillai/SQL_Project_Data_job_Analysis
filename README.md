**Introduction**
Focusing on data analyst roles,this project explores top - paying jobs, in demand skills and where high deamand meets high salary in data analytics.

**Background**
The questions I wanted to answer through my SQL queries were:

What are the top paying data analyst jobs?
What skills are required for these top-paying jobs?
What skills are most in demand for data analyst?
Which skills are associated with higher salaries?
What are the most optimal skills to learn?
Tools I used
**SQL:** The backbone of my analysis to allowing me to query and unearth critical insights.
**PostgreSQL:** The chosen database management system, ideal for handling the job posting data.
****Visual Studio Code:** My go-to for database management and executing SQL queries.
**Git and Github:** Essential for version control and sharing my SQL scripts and analysis,ensuring collaboration and project tracking.

**The Analysis**
Each query for this project aimed at investigating specific aspects of the data analyst job market. Here is how I approached each question:

**Top-paying Data Analyst Jobs**
To identify the highest-paying roles, I filtered data analyst positions by average yearly salary and location, focusing on remote jobs. 
This query highlights the high paying opportunities in the field.

    SELECT
        job_id,
        job_title,                   
        job_location,
        job_schedule_type,
        salary_year_avg,
        job_posted_date
    FROM
        job_postings_fact
    WHERE
        job_title_short = 'Data Analyst' AND
        job_location = 'Anywhere' AND
        salary_year_avg IS NOT NULL
    ORDER BY
        salary_year_avg DESC
    LIMIT 10;
    ```
