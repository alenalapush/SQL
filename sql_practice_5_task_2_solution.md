# SQL. Практика 5. Задача 2 — Решение

```sql
select id,
       username,
       email,
       date_joined,
       to_char(date_joined, 'DD Mon YYYY') as formatted_date
from users
order by date_joined desc, id asc;
```
