# SQL Query Task: Retrieve Towns with Names Starting with Specific Letters

## Objective
The task is to retrieve all towns whose names do **not** start with the letters 'R', 'r', 'B', 'b', 'D', or 'd'. The result is ordered alphabetically by the town names.

## SQL Query

```sql
SELECT * 
FROM towns
WHERE name REGEXP '^[^RrBbDd]'
ORDER BY name;
