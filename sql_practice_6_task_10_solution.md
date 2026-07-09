# SQL. Практика 6. Задача 10 — Решение

```sql
select u.id
from users u
left join testresult t on u.id = t.user_id
where t.user_id is null
order by id;
```
