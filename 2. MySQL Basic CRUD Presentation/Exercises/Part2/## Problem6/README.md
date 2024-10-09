# SQL Query Task

## Objective
Retrieve and display all information from the `employees` table for employees with the job title "Sales Representative," ordered by employee ID.

## SQL Query

```sql
SELECT * FROM employees
WHERE job_title = "Sales Representative"
ORDER BY employee_id;
