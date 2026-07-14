# SQL. Практика 6. Задача 2 — Решение

```sql
select l.name as language_name,
       p.name as problem_name,
       complexity
from languagetoproblem ltp
join language l on l.id = ltp.lang_id
join problem p on p.id = ltp.pr_id
order by problem_name;
```
