# Job Postings Analysis

This repository contains SQL queries and scripts to analyze job postings from a dataset. The queries focus on extracting insights like days since job postings were listed, job title statistics, and other key metrics.

## Query: Days Since Job Posting

The main query calculates the number of days since each job posting was listed and sorts the results in ascending order, providing a quick way to analyze the most recent job postings.

### SQL Query
```sql
SELECT job_title,
       EXTRACT(DAY FROM (current_timestamp - job_posted_date)) AS days_since_posted
FROM job_postings_fact
ORDER BY days_since_posted ASC;
