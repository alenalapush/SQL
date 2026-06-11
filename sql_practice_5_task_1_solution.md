# SQL. Практика 5. Задача 1 — Решение

```sql
select id,
       username,
       email,
       date_joined,
       date_trunc('month', date_joined) as registration_month_start
from users
order by date_joined desc, id asc;
```
