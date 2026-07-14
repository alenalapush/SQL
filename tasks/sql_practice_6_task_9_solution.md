# SQL. Практика 6. Задача 9 — Решение

```sql
select distinct u.username
from users u
join coderun cr on u.id = cr.user_id
left join codesubmit csm on csm.user_id = u.id
where to_char(date_joined, 'YYYY-MM') = '2021-04'
  and csm.user_id is null
order by username;
```
