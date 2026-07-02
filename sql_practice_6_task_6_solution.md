# SQL. Практика 6. Задача 6 — Решение

```sql
select u.id
from users u
left join coderun c on c.user_id = u.id
where c.user_id is null
order by u.id;
```
