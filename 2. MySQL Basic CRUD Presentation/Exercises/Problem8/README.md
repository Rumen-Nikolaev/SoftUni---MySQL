# SQL Query Task

## Objective
Retrieve and display the first and last names of the top 5 employees with the highest salaries from the `employees` table.

## SQL Query

```sql
SELECT first_name, last_name 
FROM employees
ORDER BY salary DESC
LIMIT 5;
