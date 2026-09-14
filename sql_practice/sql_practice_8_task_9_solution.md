# Решение SQL. Практика 8. Задача 9

```sql
SELECT
    c.name AS company_name,
    COALESCE(SUM(CASE WHEN u.is_active = 1 THEN 1 ELSE 0 END), 0) AS cnt_active_users,
    COALESCE(SUM(CASE WHEN u.is_active = 0 THEN 1 ELSE 0 END), 0) AS cnt_not_active_users
FROM company c
LEFT JOIN users u ON u.company_id = c.id
GROUP BY c.id
ORDER BY company_name;
```
