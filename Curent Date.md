# SQL Queries for Retrieving Current Date

This document provides examples of how to retrieve the current date and time from the `job_postings_fact` table using different SQL dialects.

## Queries by SQL Dialect

| **SQL Dialect** | **Query**                                                             | **Description**                                           |
|-----------------|-----------------------------------------------------------------------|-----------------------------------------------------------|
| **PostgreSQL**  | ```sql<br>SELECT CURRENT_TIMESTAMP AS current_date<br>FROM job_postings_fact;``` | Retrieves the current date and time.                       |
|                 | ```sql<br>SELECT now()<br>FROM job_postings_fact;```                  | Alternative way to retrieve current date and time.         |
| **MySQL**       | ```sql<br>SELECT NOW() AS current_date<br>FROM job_postings_fact;```   | Retrieves the current date and time.                       |
| **SQLite**      | ```sql<br>SELECT CURRENT_DATE AS current_date<br>FROM job_postings_fact;``` | Retrieves the current date (without time).                 |

## Explanation:
- `CURRENT_TIMESTAMP` returns the current date and time (including time zone in some databases).
- `NOW()` returns the current date and time in most databases like MySQL and PostgreSQL.
- `CURRENT_DATE` returns the current date (without time) in SQLite.

### Usage:
These queries are helpful when you need to compare the date of the job postings (`job_posted_date`) with the current date or when performing time-based calculations.
