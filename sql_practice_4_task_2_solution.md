# SQL. Практика 4. Задача 2 — Решение

```sql
select id,
       username,
       first_name,
       last_name,
       coalesce(first_name, last_name, 'Дорогой друг') as display_name
from users
order by id;
```
