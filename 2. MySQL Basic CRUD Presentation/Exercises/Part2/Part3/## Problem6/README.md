# SQL Query Task

## Objective
Update the salaries of employees in specified departments by increasing them by 12%, and then retrieve the updated salary information for all employees.

## SQL Queries

```sql
UPDATE employees
SET salary = salary * 1.12
WHERE department_id IN (1, 2, 4, 11);

SELECT salary FROM employees;
