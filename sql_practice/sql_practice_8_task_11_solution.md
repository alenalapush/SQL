# Решение SQL. Практика 8. Задача 11

```sql
SELECT
    c.name AS company_name,
    STRING_AGG(u.last_name, ', ' ORDER BY u.email) AS list_last_names
FROM company c
JOIN users u ON c.id = u.company_id
WHERE u.last_name IS NOT NULL
GROUP BY c.id, c.name
ORDER BY company_name;
```
