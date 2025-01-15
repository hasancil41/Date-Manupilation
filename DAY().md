# Job Postings Analysis

This repository contains an SQL query to extract information about job postings from a dataset. The goal is to retrieve the `job_id` and the day of the month when each job was posted.

## Query Details

The SQL query used in this project:

```sql
SELECT job_id,
       EXTRACT(DAY FROM job_posted_date) AS posted_day
FROM job_postings_fact;
```

### Explanation:
- **job_id**: The unique identifier for each job posting.
- **EXTRACT(DAY FROM job_posted_date)**: Extracts the day (as an integer) from the `job_posted_date` column.
- **job_postings_fact**: The table containing job postings data.

### Use Case:
This query is useful for analyzing the distribution of job postings by day of the month or identifying patterns in job posting behavior.

## Project Purpose
The purpose of this project is to:
- Analyze job postings data for trends.
- Provide insights into the timing of job postings.
- Serve as a foundational step for further data analysis or visualization.

## Dataset
The dataset (`job_postings_fact`) includes the following columns (example):
- `job_id`: Unique identifier for each job.
- `job_posted_date`: The date when the job was posted.
- Additional columns may exist but are not used in this query.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/job-postings-analysis.git
   ```

2. Import the SQL query into your preferred database tool.
3. Run the query against the `job_postings_fact` table.
4. Analyze the results for insights.

## Requirements
- A database containing the `job_postings_fact` table.
- SQL client to execute the query.

