# SQL Query Task: Retrieve Employees Hired Between 1995 and 2005 in Departments 3 and 10

## Objective
The task is to retrieve the first names of employees who were hired between the years 1995 and 2005 and who belong to departments with `department_id` 3 or 10. The results are ordered by employee ID.

## SQL Query

```sql
SELECT first_name
FROM employees
WHERE department_id IN (3, 10)
AND YEAR(hire_date) >= 1995
AND YEAR(hire_date) <= 2005
ORDER BY employee_id;
