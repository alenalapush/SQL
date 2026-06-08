# SQL. Практика 4. Задача 3 — Решение

```sql
select id,
       username,
       score,
       case
           when score > 300 then 'Мастер'
           when score > 150 then 'Эксперт'
           when score > 75  then 'Продвинутый'
           else 'Новичок'
       end as group_user
from users
order by id;
```
