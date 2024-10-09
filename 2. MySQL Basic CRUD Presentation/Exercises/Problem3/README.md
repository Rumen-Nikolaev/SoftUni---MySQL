# SQL Query Task

## Objective
Retrieve the names and populations of countries located in Europe (`continent_code = 'EU'`), and display the top 30 countries with the largest populations in descending order.

## SQL Query

```sql
SELECT country_name, population 
FROM countries
WHERE continent_code = 'EU'
ORDER BY population DESC, country_name
LIMIT 30;

