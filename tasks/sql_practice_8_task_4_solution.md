# Решение SQL. Практика 8. Задача 4

## Задача

Вывести информацию о пользователях, которые совершали транзакции типа "Пополнение кошелька", с суммой пополнений более 500.

## Столбцы

- `username` — логин пользователя
- `total_score` — общая сумма транзакций

## Решение

```sql
select
    username,
    sum(t.value) as total_value
from users u
join transaction t
    on u.id = t.user_id
join transactiontype tt
    on tt.type = t.type_id
where description = 'Пополнение кошелька'
group by username
having sum(t.value) > 500
order by username;
```
