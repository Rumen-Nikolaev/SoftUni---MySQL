# SQL Query Task: Longest Magic Wand Size by Deposit Group

## Objective
Retrieve the maximum size of magic wands from the `wizzard_deposits` table, grouped by deposit group.

## SQL Query

```sql
SELECT deposit_group, MAX(magic_wand_size) AS longest_magic_wand
FROM wizzard_deposits
GROUP BY deposit_group
ORDER BY longest_magic_wand, deposit_group;
