# Решение

```sql
select
    id,
    username,
    email,
    date_joined
from users
where (email like '%bk.ru%' or email like '%yandex.ru%') and
    date_joined < '2022-01-01' and date_joined >= '2021-01-01'
order by id;
```
