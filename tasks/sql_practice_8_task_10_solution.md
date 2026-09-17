# Решение SQL. Практика 8. Задача 10

```sql
SELECT STRING_AGG(email, '; ') AS list_emails
FROM (
    SELECT email
    FROM users
    ORDER BY email
) t;
```
