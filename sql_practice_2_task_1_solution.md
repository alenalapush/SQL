# SQL. Практика 2. Задача 1 — Решение

```sql
select id,
       username,
       score
from users
where score > 100
   or last_name is null
order by id;
```
