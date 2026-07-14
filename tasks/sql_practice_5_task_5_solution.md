# SQL. Практика 5. Задача 5 — Решение

```sql
select id,
       username,
       date_joined
from users
where date_joined >= '2021-01-01'
  and date_joined < '2022-01-01'
order by id;
```
