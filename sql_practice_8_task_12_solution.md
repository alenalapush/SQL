# SQL. Практика 8. Задача 12. Решение

```sql
select u.id,
    u.username,
    coalesce(mode() within group ( order by p.name),'Пользователь ничего не отправлял') as mode_problems
from users u
left join codesubmit c
on u.id=c.user_id
left join problem p
on c.problem_id=p.id
group by u.id,u.username
order by u.id
```
