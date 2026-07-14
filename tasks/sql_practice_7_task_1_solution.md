# SQL. Практика 7. Задача 1 — Решение

```sql
select user_id,
       problem_id,
       created_at,
       'run' as attempt_type,
       language_id
from coderun
union all
select user_id,
       problem_id,
       created_at,
       'submit' as attempt_type,
       language_id
from codesubmit;
```
