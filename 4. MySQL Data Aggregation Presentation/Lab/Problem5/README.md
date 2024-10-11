# SQL Query Task: Total Deposit Amounts by Group

## Objective
Retrieve the total deposit amount for each deposit group from the `wizzard_deposits` table and order the results by the total sum.

## SQL Query

```sql
SELECT deposit_group, SUM(deposit_amount) AS total_sum
FROM wizzard_deposits
GROUP BY deposit_group
ORDER BY total_sum;
