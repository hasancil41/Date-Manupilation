# SQL Query: Job Postings by Year and Month

## Overview
This SQL query calculates the total number of job postings (`job_count`) by year and month. It extracts the year and month from the `job_posted_date` and groups the results by year and month to show a breakdown of job postings over time.

## Purpose
The query provides insights into job posting trends, helping stakeholders analyze the frequency of job postings on a monthly and yearly basis. This can be useful for tracking recruitment activity, identifying seasonal hiring trends, and planning future recruitment efforts.

## Query Breakdown

```sql
SELECT 
    EXTRACT(YEAR FROM job_posted_date) AS year,
    EXTRACT(MONTH FROM job_posted_date) AS month,
    COUNT(*) AS job_count
FROM job_postings_fact
GROUP BY year, month
ORDER BY year DESC, month DESC;
