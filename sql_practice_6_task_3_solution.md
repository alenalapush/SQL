# SQL. Практика 6. Задача 3 — Решение

```sql
select l.name as language_name
from language l
left join languagetoproblem ltp on l.id = ltp.lang_id
where ltp.lang_id is null
order by language_name;
```
