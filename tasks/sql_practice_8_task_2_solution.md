# Решение

```sql
select username,
    sum(t.value) as total_value
from users u
join transaction  t
on u.id=t.user_id
join transactiontype  tt
on tt.type=t.type_id
where description='Пополнение кошелька'
group by username
order by username
```
