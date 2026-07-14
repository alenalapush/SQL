# SQL. Практика 2. Задача 2 — Решение

```sql
select id,
       username,
       company_id,
       score
from users
where is_active = 1
  and (score > 500
    or company_id = 7)
order by id;
```
