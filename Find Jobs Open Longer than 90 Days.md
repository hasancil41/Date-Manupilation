# SQL Query: Job Postings Open for More Than 90 Days

## Overview
This SQL query retrieves job postings from the `job_postings_fact` table where the difference between the job posting date (`job_posted_date`) and the job closure date (`job_closed_date`) is greater than 90 days. It provides job titles along with their posting and closure dates for those job postings that remained open for more than 90 days.

## Purpose
The query helps identify job postings that have remained open for an unusually long period, providing insights into potential delays in the recruitment process or challenges in filling specific positions.

## Query Breakdown

```sql
SELECT 
    job_title,
    job_posted_date,
    job_closed_date
FROM job_postings_fact
WHERE DATEDIFF(job_closed_date, job_posted_date) > 90;
