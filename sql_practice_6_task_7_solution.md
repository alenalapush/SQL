# SQL. Практика 6. Задача 7 — Решение

```sql
select u.id,
       u.username,
       u.date_joined,
       coalesce(c.name, 'Без компании') as company_name
from users u
left join company c on u.company_id = c.id
where to_char(date_joined, 'YYYY') = '2021'
order by id;
```
