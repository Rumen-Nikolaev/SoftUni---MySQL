# SQL Query Task: Retrieve Employees with First Names Starting with "Sa"

## Objective
The task is to retrieve the first and last names of employees whose first names start with the letters "Sa". The results are ordered by employee ID.

## SQL Query

```sql
SELECT first_name, last_name
FROM employees
WHERE first_name REGEXP '^Sa'
ORDER BY employee_id;
