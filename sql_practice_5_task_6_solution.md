# SQL. Практика 5. Задача 6 — Решение

```sql
select id,
       username,
       email,
       date_joined
from users
where date_joined >= '2022-01-01'
  and date_joined < '2023-01-01'
  and email like '%bk.ru%'
order by id;
```
