# SQL. Практика 6. Задача 1 — Решение

```sql
select u.id,
       username,
       u.date_joined,
       problem_id
from coderun c
join users u on c.user_id = u.id
where c.created_at >= '2021-04-01'
  and c.created_at < '2021-05-01'
order by u.id asc, problem_id;
```
