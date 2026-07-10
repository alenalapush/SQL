# SQL. Практика 6. Задача 4 — Решение

```sql
select tq.id as question_id,
       tq.value as question_value,
       tq.tag as question_tag,
       ta.value as correct_answer_value
from testquestion tq
join testanswer ta on tq.id = ta.question_id
where ta.is_correct is true
order by question_id;
```
