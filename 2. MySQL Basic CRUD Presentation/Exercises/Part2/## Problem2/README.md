# SQL Query Task

## Objective
Retrieve the first and last names of employees who are not in department 4.

## SQL Query

```sql
SELECT first_name, last_name 
FROM employees 
WHERE department_id != 4;
