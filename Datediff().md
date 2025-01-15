# Job Postings Analysis
Calculate Difference Between Two Dates
## Overview

This project analyzes job postings data to calculate the duration that each job posting remained open. The query extracts job titles and the number of days each job posting was open before being closed.

## SQL Query

```sql
SELECT 
    job_title,
    DATEDIFF(job_closed_date, job_posted_date) AS days_open
FROM job_postings_fact
WHERE job_closed_date IS NOT NULL;
