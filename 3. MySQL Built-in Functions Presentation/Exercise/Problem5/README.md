# SQL Query Task: Retrieve Employees with Last Names Containing "ei"

## Objective
The task is to retrieve the first and last names of employees whose last names contain the substring "ei". The results are ordered by employee ID.

## SQL Query

```sql
SELECT
     first_name, last_name
FROM
     employees
WHERE
     last_name LIKE '%ei%'
ORDER BY employee_id;
