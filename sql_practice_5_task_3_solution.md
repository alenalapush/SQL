# SQL. Практика 5. Задача 3 — Решение

```sql
select id,
       username,
       email,
       date_joined,
       to_char(date_joined, 'YYYY-MM') as formatted_date
from users
order by date_joined desc, id asc;
```
