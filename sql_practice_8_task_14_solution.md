# SQL. Практика 8. Задача 14. Решение

```sql
select
    u.id,
    u.username,
    array_agg(distinct c.problem_id order by c.problem_id) as unique_problem_ids_array
from users u
join codesubmit c on u.id = c.user_id
group by u.id, u.username
order by id
```
