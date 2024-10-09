# SQL Query Task

## Objective
Retrieve and display a list of projects from the `projects` table, ordered by their start date, name, and project ID, while limiting the results to the first 10 entries.

## SQL Query

```sql
SELECT * 
FROM projects
ORDER BY start_date, name, project_id
LIMIT 10;
