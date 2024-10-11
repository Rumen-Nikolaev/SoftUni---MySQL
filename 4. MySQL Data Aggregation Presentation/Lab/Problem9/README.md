# SQL Query Task: Smallest Average Magic Wand Size

## Objective
Retrieve the deposit group that has the smallest average magic wand size from the `wizzard_deposits` table.

## SQL Query

```sql
SELECT deposit_group
FROM wizzard_deposits
GROUP BY deposit_group
ORDER BY AVG(magic_wand_size)
LIMIT 1;
