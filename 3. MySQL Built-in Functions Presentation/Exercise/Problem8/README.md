# SQL Query Task: Retrieve Town Names with 5 to 6 Characters

## Objective
The task is to retrieve all towns where the length of the town's name is between 5 and 6 characters, inclusive. The result is ordered alphabetically by the town names.

## SQL Query

```sql
SELECT name 
FROM towns
WHERE CHAR_LENGTH(name) BETWEEN 5 AND 6
ORDER BY name;
