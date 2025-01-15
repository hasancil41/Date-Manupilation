# SQL Query: Recent Job Postings
Filtering Jobs Posted in the Last 30 Days
## Overview
This SQL query retrieves job postings that were published in the last 30 days. The query fetches the `job_id`, `job_title`, and `job_posted_date` from the `job_postings_fact` table, filtered by job postings that were published within the last 30 days.

## Purpose
The query is intended to provide a snapshot of the most recent job postings, helping stakeholders quickly assess new job openings and recruitment activities over the past month.

## Query Breakdown

```sql
SELECT 
    job_id,
    job_title,
    job_posted_date
FROM job_postings_fact
WHERE job_posted_date >= CURRENT_DATE - INTERVAL '30 DAYS';
