# Решение SQL. Практика 8. Задача 8

```sql
SELECT
    SUM(CASE WHEN is_active = 1 THEN 1 ELSE 0 END) AS cnt_active_users,
    SUM(CASE WHEN is_active = 0 THEN 1 ELSE 0 END) AS cnt_not_active_users
FROM users;
```
