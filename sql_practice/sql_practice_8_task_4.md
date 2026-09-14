# SQL. Практика 8. Задача 4

## Задание

Из таблиц `users`, `transaction` и `transactiontype` требуется вывести информацию только о тех пользователях, которые совершали транзакции типа **Пополнение кошелька**.

**Столбцы в результате:**

| Столбец | Описание |
|---------|----------|
| `username` | Логин |
| `total_score` | Общая сумма транзакций |

**Важно:** Название столбцов должно в точности совпадать с условием.

## Дополнительные условия

- Выведите только тех пользователей, у которых сумма пополнений кошелька превышает 500.
- Результат отсортируйте по возрастанию `username`.

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
