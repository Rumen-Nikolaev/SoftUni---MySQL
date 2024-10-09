# SQL Query Task

## Objective
Retrieve and display the first names, last names, and job titles of employees from the `employees` table whose salaries are between 20,000 and 30,000.

## SQL Query

```sql
SELECT first_name, last_name, job_title
FROM employees
WHERE salary >= 20000 AND salary <= 30000
ORDER BY employee_id;
