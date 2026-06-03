# SQL. Практика 3. Задача 2 — Решение

```sql
select id,
       username,
       email,
       right(email, length(email) - position('@' in email)) as domain
from users
order by id;
```
