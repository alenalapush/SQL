# SQL. Практика 7. Задача 2 — Решение

```sql
select user_id,
       problem_id
from coderun
union
select user_id,
       problem_id
from codesubmit;
```
