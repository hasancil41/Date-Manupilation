# SQL Query: Job Postings with Formatted Date

## Overview
This SQL query retrieves job titles along with the formatted job posting dates from the `job_postings_fact` table. The job posting date is formatted in the 'DD-Mon-YYYY' format, making it easier to read and understand.

## Purpose
The query is designed to display job titles alongside their posting dates in a more user-friendly format. This is useful for reports or visualizations where the date needs to be presented in a more readable and standardized way.

## Query Breakdown

```sql
SELECT 
    job_title,
    TO_CHAR(job_posted_date, 'DD-Mon-YYYY') AS formatted_date
FROM job_postings_fact;
