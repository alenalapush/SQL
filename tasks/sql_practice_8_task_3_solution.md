# Решение

```sql
select l.name as language_name,
    count(ltp.pr_id) as problem_count
from language l
left join languagetoproblem ltp
    on l.id = ltp.lang_id
group by l.name
order by language_name
```
