# SQL Query Task: Create a View for Employees Hired After 2000

## Objective
The goal of this task is to create a SQL view that displays the first and last names of employees hired after the year 2000. This allows for easier access to this specific dataset without needing to rewrite the query every time.

## SQL Query

```sql
CREATE VIEW `v_employees_hired_after_2000` AS
SELECT first_name, last_name
FROM employees
WHERE YEAR(hire_date) > 2000;
