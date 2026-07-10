# SQL. Практика 6. Задача 5 — Решение

```sql
select name
from problem p
left join codesubmit c on p.id = c.problem_id
where c.problem_id is null
order by name;
```
