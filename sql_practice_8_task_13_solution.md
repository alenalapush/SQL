# SQL. Практика 8. Задача 13. Решение

```sql
select array_agg(username) as array_username
from (select username
    from users
order by date_joined desc, username asc) t
```
