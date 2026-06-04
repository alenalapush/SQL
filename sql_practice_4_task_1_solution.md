# SQL. Практика 4. Задача 1 — Решение

```sql
select id,
       username,
       'Идентификатор пользователя равен' || ' ' || id as text_user_id
from users
order by id;
```
