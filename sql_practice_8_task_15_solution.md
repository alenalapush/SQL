# SQL. Практика 8. Задача 15. Решение

```sql
select PERCENTILE_CONT(0.95) within group(order by score) as p95
from users
where date_joined>'2022,01,01'
and score>100
```
