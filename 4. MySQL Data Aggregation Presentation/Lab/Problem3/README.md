# SQL Query Task: Total Deposit Amounts by Group for Ollivander Family

## Objective
Retrieve the total deposit amount for each deposit group created by the "Ollivander family" from the `wizzard_deposits` table, filtering groups with a total sum of less than 150,000.

## SQL Query

```sql
SELECT deposit_group, SUM(deposit_amount) AS total_sum
FROM wizzard_deposits
WHERE magic_wand_creator = 'Ollivander family'
GROUP BY deposit_group
HAVING total_sum < 150000
ORDER BY total_sum DESC;
