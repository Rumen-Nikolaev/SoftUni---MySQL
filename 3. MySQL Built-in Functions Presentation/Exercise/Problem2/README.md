# SQL Query Task: Retrieve Employees Excluding Engineers

## Objective
The goal of this task is to retrieve the first and last names of employees whose job titles do not contain the word "engineer." This allows for filtering out employees in engineering roles.

## SQL Query

```sql
SELECT first_name, last_name
FROM employees
WHERE job_title NOT LIKE '%engineer%'
ORDER BY employee_id;
