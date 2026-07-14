# SQL. Практика 6. Задача 8 — Решение

```sql
select distinct u.username
from users u
join coderun cr on u.id = cr.user_id
join codesubmit csm on u.id = csm.user_id
where to_char(date_joined, 'YYYY-MM') = '2021-04'
order by username;
```
