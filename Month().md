# Job Postings Analysis: Extracting Month Information

This repository contains an SQL query to extract information about job postings, specifically retrieving the `job_id` and the month when each job was posted.

## Query Details

The SQL query used in this project:

```sql
SELECT job_id,
       EXTRACT(MONTH FROM job_posted_date) AS posted_month
FROM job_postings_fact;
```

### Explanation:
- **job_id**: The unique identifier for each job posting.
- **EXTRACT(MONTH FROM job_posted_date)**: Extracts the month (as an integer, 1-12) from the `job_posted_date` column.
- **job_postings_fact**: The table containing data about job postings.

### Use Case:
This query is useful for analyzing the distribution of job postings by month, identifying seasonal trends, or understanding posting behaviors throughout the year.

## Project Purpose
The purpose of this project is to:
- Analyze job postings data for monthly trends.
- Provide insights into job posting behavior across different months.
- Serve as a foundational step for deeper analysis and visualization.

## Dataset
The dataset (`job_postings_fact`) includes the following columns (example):
- `job_id`: Unique identifier for each job posting.
- `job_posted_date`: The date when the job was posted.
- Additional columns may exist but are not used in this query.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/job-postings-analysis.git
   ```

2. Import the SQL query into your preferred database tool.
3. Run the query against the `job_postings_fact` table.
4. Analyze the results for insights into monthly job posting patterns.

## Requirements
- A database containing the `job_postings_fact` table.
- SQL client to execute the query.


