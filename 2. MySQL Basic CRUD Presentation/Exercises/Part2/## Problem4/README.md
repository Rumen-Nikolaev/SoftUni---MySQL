# SQL Query Task

## Objective
Retrieve the first name, last name, and salary of employees who earn more than 50,000, ordered by salary in descending order.

## SQL Query

```sql
SELECT first_name, last_name, salary 
FROM employees 
WHERE salary > 50000 
ORDER BY salary DESC;
