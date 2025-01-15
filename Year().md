# Job Postings Analysis: Extracting Year Information

This repository contains an SQL query designed to extract the year when each job was posted, along with the unique job identifier (`job_id`).

## Query Details

The SQL query used in this project:

```sql
SELECT job_id,
       EXTRACT(YEAR FROM job_posted_date) AS posted_year
FROM job_postings_fact;
```

### Explanation:
- **job_id**: A unique identifier for each job posting.
- **EXTRACT(YEAR FROM job_posted_date)**: Extracts the year (e.g., 2023) from the `job_posted_date` column.
- **job_postings_fact**: The table containing job postings data.

### Use Case:
This query is particularly useful for:
- Analyzing job postings trends over multiple years.
- Understanding long-term patterns in job posting activity.
- Providing input for further data visualizations or reports.

## Project Purpose
The purpose of this project is to:
- Analyze job postings data for yearly trends.
- Enable insights into job market dynamics over time.
- Serve as a foundational query for further analysis and visualization.

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
4. Analyze the results for insights into yearly trends in job postings.

## Requirements
- A database containing the `job_postings_fact` table.
- SQL client to execute the query.


