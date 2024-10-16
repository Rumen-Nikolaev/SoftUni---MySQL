# SQL Query Task: Age Grouping of Wizard Deposits

## Objective
Group the entries in the `wizzard_deposits` table by age ranges and count the number of wizard deposits in each age group.

## SQL Query

```sql
SELECT
    CASE
        WHEN age <= 10 THEN '[0-10]'
        WHEN age <= 20 THEN '[11-20]'
        WHEN age <= 30 THEN '[21-30]'
        WHEN age <= 40 THEN '[31-40]'
        WHEN age <= 50 THEN '[41-50]'
        WHEN age <= 60 THEN '[51-60]'
        ELSE '[61]'
    END AS age_group,
    COUNT(*) AS wizzard_count
FROM wizzard_deposits
GROUP BY age_group
ORDER BY wizzard_count;
