# SQL. Практика 5. Задача 4 — Решение

```sql
select id,
       username,
       date_joined
from users
where date_joined < '2022-02-15'
  and date_joined > '2022-01-01'
order by date_joined desc, id asc;
```
