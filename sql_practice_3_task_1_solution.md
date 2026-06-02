# SQL. Практика 3. Задача 1 — Решение

```sql
select id,
       username,
       first_name,
       last_name,
       lower(first_name)  as lower_first_name,
       upper(last_name)   as upper_last_name,
       length(username)   as length_username
from users
order by length(username) desc, id;
```
