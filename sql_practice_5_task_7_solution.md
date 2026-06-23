# SQL. Практика 5. Задача 7 — Решение

```sql
select id,
       username,
       email,
       date_joined,
       score
from users
where (date_joined >= '2021-01-01' and date_joined < '2022-01-01')
   or score > 100
order by id;
```
