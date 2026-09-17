# SQL. Практика 8. Задача 1 — Решение

```sql
select 
    complexity,
    count(*) as count_of_problems
from problem
group by complexity
order by complexity;
```
