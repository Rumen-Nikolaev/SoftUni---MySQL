# SQL Query Task: Retrieve Towns with Names Starting with Specific Letters

## Objective
The task is to retrieve all towns whose names start with the letters 'M', 'm', 'K', 'k', 'B', 'b', 'E', or 'e'. The result is ordered alphabetically by the town names.

## SQL Query

```sql
SELECT * 
FROM towns
WHERE name REGEXP '^[MmKkBbEe]'
ORDER BY name;
